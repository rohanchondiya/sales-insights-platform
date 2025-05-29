# sales-insights-platform
Azure Data Engineering Project with Databricks, ADLS Gen2, and Power BI
# 🚀 Sales Insights Platform

This project is a complete end-to-end Azure Data Engineering pipeline that ingests, processes, and visualizes automobile sales data using Azure services and Power BI.

---

## 🧱 Architecture

1. **Raw Data Storage**: Azure Data Lake Storage Gen2 (`raw` container)
2. **Data Processing**: Azure Databricks using PySpark
3. **Data Output**: Curated data written back to ADLS or Synapse
4. **Visualization**: Power BI dashboards connected to curated layer

![architecture](pipeline_architecture.png)

---

## 🗂️ Project Structure

```
sales-insights-platform/
├── README.md
├── data/
│   └── sales_data_sample.csv
├── notebooks/
│   ├── 01_ingestion_ADLS.ipynb
│   ├── 02_transformation_databricks.ipynb
│   └── 03_data_export_for_powerbi.ipynb
├── powerbi/
│   └── SalesInsightsReport.pbit
├── pipeline_architecture.png
├── templates/
└── configs/
    └── linked_services.json
```

---

## 📦 Dataset

Sample dataset contains:
- `OrderDate`, `Region`, `SalesPerson`, `Model`, `UnitsSold`, `Price`, `Revenue`

---

## 🧪 How to Run

1. Upload `sales_data_sample.csv` to ADLS Gen2 `raw` container.
2. Run `01_ingestion_ADLS.ipynb` in Azure Databricks to load data.
3. Use `02_transformation_databricks.ipynb` for data cleaning and enrichment.
4. Save processed data to curated container or Synapse.
5. Connect Power BI to curated output and load `SalesInsightsReport.pbit`.

---

## 📊 Power BI Report

Sample report includes:
- Sales by Region & Model
- Monthly Revenue Trend
- Top Salespeople Performance

---

## 🔐 Security

- Secrets (SAS tokens or SP credentials) should be managed via Azure Key Vault.

---

## ✅ Tools & Services

- Azure Data Lake Storage Gen2
- Azure Databricks
- Azure Data Factory (optional)
- Power BI
