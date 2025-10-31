# Adventure Works ETL Project — Medallion Architecture

## 🚀 Overview
This beginner-friendly project demonstrates how to design and implement an **end-to-end data engineering pipeline** using **Azure Databricks**, **Delta Lake**, and **Unity Catalog**, following the **Medallion Architecture** (Bronze → Silver → Gold).  
The pipeline transforms raw data into business-ready insights, securely governed and visualized using **Power BI** or **Tableau**.

---

## 🧩 Architecture Overview
![Databricks Medallion Architecture](https://github.com/rishigundla/adventureworks-databricks-project/blob/main/assets/Databricks%20Diagram.drawio%20(1).png)

---

## 📂 Project Workflow

1. **Data Ingestion (Bronze Layer)**  
   - Raw CSV files ingested into **Azure Data Lake Storage Gen2 (ADLS)**.  
   - Data stored in the **Bronze layer** using Delta format for immutability and traceability.  

2. **Data Cleaning (Silver Layer)**  
   - Data is cleansed, validated, and standardized.  
   - Duplicate records removed and schema consistency ensured.  

3. **Data Transformation (Gold Layer)**  
   - Business-level aggregations and KPIs generated.  
   - Optimized tables serve as the data source for BI tools.  

4. **Data Visualization**  
   - Cleaned and transformed data visualized in **Power BI** or **Tableau** for insights.  

---

## ⚙️ Setup Steps (Unity Catalog Configuration)

1. **Create Metastore** — Centralized governance layer  
2. **Create Credentials** — Secure access to ADLS Gen2  
3. **Create External Locations** —  
   - Bronze Layer  
   - Silver Layer  
   - Gold Layer  
4. **Create Catalog and Schemas** —  
   - `bronze`: Raw landing zone  
   - `silver`: Cleaned & validated data  
   - `gold`: Aggregated business-level data  

---

## 🧰 Tools & Technologies

| Category | Tool |
|-----------|------|
| Data Lake | Azure Data Lake Storage Gen2 |
| Compute & Processing | Azure Databricks |
| Governance | Unity Catalog |
| Storage Format | Delta Lake |
| Visualization | Power BI / Tableau |

---

## 📒 Notebooks

| Layer | Notebook | Description |
|-------|-----------|-------------|
| 🟤 Bronze | [Data Ingestion](notebooks/1.%20Data%20Ingestion%20in%20Bronze%20Layer.ipynb) | Loads raw data from external CSVs into Bronze Delta tables |
| ⚪ Silver | [Data Cleaning](notebooks/2.%20Data%20Cleaning%20in%20Silver%20Layer.ipynb) | Cleans, deduplicates, and validates data |
| 🟡 Gold | [Data Transformation](notebooks/3.%20Data%20Transformation%20in%20Gold%20Layer.ipynb) | Applies business logic and creates analytical datasets |

---

## 💾 Data Folder

📁 **`/data`**  
Contains all raw CSV files used for ingestion into the Bronze layer.  

| File Name | Description |
|------------|-------------|
| `Product.csv` | Contains product-level details such as product name, category, and price. |
| `Region.csv` | Includes region mapping and hierarchy details for sales distribution. |
| `Reseller.csv` | Holds reseller information including name, type, and contact details. |
| `Sales.csv` | Primary transactional sales data combining customers, products, and resellers. |
| `Salesperson.csv` | Details of sales representatives such as ID, name, and assigned region. |
| `SalespersonRegion.csv` | Mapping between salespersons and regions for performance tracking. |
| `Targets.csv` | Contains quarterly and annual sales target information. |

🧩 These datasets are processed through the Databricks pipeline:
- Loaded into **Bronze Layer** as raw Delta tables.  
- Cleaned and standardized in **Silver Layer**.  
- Aggregated into **Gold Layer** for Power BI reporting.

---

## 🧭 Key Learnings

- Designed an **end-to-end Medallion Architecture** pipeline.  
- Configured **Unity Catalog** for centralized governance, lineage, and security.  
- Implemented **Delta Lake** features for optimized storage and performance.  
- Integrated Databricks with **Power BI** for interactive visualization.  
- Practiced **Azure resource setup** (ADLS, Databricks workspace, and schema design).  

---

## 🪜 Folder Description

| Folder | Description |
|---------|-------------|
| `data/` | Contains raw CSV files used for ingestion |
| `notebooks/` | All Databricks notebooks for Bronze, Silver, and Gold layers |
| `assets/` | Architecture diagram and visuals |
| `README.md` | Documentation for the entire project |

---

## 👨‍💻 Author
**Rishikesh Gundla**  
_Senior Business Intelligence Engineer | Data Engineering & Analytics Enthusiast_  
🔗 [LinkedIn](https://www.linkedin.com/in/rishikeshgundla)
