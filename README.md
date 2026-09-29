# Databricks E-Commerce Medallion Pipeline

End-to-end Data Engineering project implementing Medallion Architecture (Bronze-Silver-Gold) with automated daily orchestration.

### 🏗️ Architecture

**Bronze Layer:** Ingested raw e-commerce data (4 products) from API with nested JSON (title, price, rating)
**Silver Layer:** Flattened nested `rating` column using `pandas.json_normalize` into `rating_rate` and `rating_count`
**Gold Layer:** Converted clean data into Spark DataFrame for analytics-ready layer

### ⚙️ Tech Stack
- Databricks Notebooks
- PySpark & Pandas
- Databricks Workflows / Jobs
- Serverless Compute
- Delta Lake

### ⏰ Orchestration
- **Job Name:** `remya_ecommerce_daily_2am`
- **Schedule:** Daily at 2:00 AM IST (Asia/Calcutta)
- **Trigger:** Scheduled
- **Compute:** Serverless (auto-start)
- **Status:** Succeeded ✅ (6.22s)

This job runs automatically every night even when local machine is off.

### 📸 Proof of Execution
- Job runs showing green Succeeded status
- Scheduled trigger configured for daily 2 AM IST

### 📂 File Structure


### 🚀 Future Improvements
- Load real-time data from API
- Write Gold layer to Delta Table
- Add data quality checks

### 👩‍💻 Author
Remya - Aspiring Data Engineer
