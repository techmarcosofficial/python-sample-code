# AWS Lambda ROI Calculator

This Python project is designed to run as an AWS Lambda function. It calculates cost savings and Return on Investment (ROI) for organizations by comparing scenarios with and without data governance across digital, paper, and tape storage systems, as well as eDiscovery costs.

---

## 📦 Features

- Parse and normalize data volumes
- Estimate digital estate growth over 5 years
- Calculate annual eDiscovery fees
- Determine digital and paper storage costs
- Evaluate tape backup management savings
- Compute total ROI across all categories

---

## 🛠 Technologies Used

- **Python 3.x**
- **AWS Lambda**
- **Modular structure with constants**
- **Math utilities for rounding and parsing**
- **Formatted financial reporting**

---

## 📁 Project Structure


---

## ⚙️ Core Functions

| Function                         | Description |
|----------------------------------|-------------|
| `get_estates()`                  | Forecasts estate size growth for 5 years |
| `get_ediscovery_annual_costs()` | Calculates eDiscovery costs over time |
| `get_digital_storages()`        | Estimates annual digital storage savings |
| `get_paper_storage_costs()`     | Projects paper storage growth and cost |
| `get_tape_management_data()`    | Simulates tape backup savings |
| `get_roi_detail()`              | Summarizes total ROI from all categories |

---

## 🚀 Deployment

This project is built to be deployed as an AWS Lambda function.

1. Package your code with dependencies.
2. Upload the ZIP to Lambda or deploy via AWS CLI/CDK.
3. Ensure the `constants.py` is correctly configured for the domain-specific data.

---

## 🧪 Sample Input (Environment / Event Data)

```json
{
  "employee_volume": 1000,
  "litigation_volume": { "Medium": "50% (Medium)" },
  "paper_storage": { "50,000 - 100,000": "75,000" },
  "paper_growth": ["Medium"],
  "tape_backup_utilization": { "Partial": "50%" }
}

```OutPut
{
  "roi": {
    "items": [
      {
        "without_governance": "120,000.00",
        "with_governance": "55,000.00",
        "savings": "65,000.00"
      },
      ...
    ],
    "total": "325,000"
  }
}
