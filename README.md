# NYC taxi data engineering Azure

## Goal  
The main goal of this project is to develop an end-to-end Data Engineering Pipeline to fetch data from the NYC Taxi public dataset, transform and enrich it, and store it efficiently using Microsoft Azure tools while understanding and implementing Delta table formats.

---

## Project Architecture  
![NYC_DE_Arc](https://github.com/user-attachments/assets/7c159c27-e09f-441e-b251-6b9fba079449)


---

## Pipeline Overview

### 1. Data Ingestion - Azure Data Factory  
Azure Data Factory was used to ingest raw data from the **NYC Taxi Data Government website**, which was then stored in the **Bronze** layer in **Parquet format**.

---

### 2. Data Transformation - Azure Databricks  
Data from the Bronze layer was transformed using **Azure Databricks (PySpark)**.  
- Data was cleaned, deduplicated, and enriched.  
- Intermediate output was saved to the **Silver** layer in Parquet format.  
- Further transformations were applied and the final data was saved in **Delta format** in the **Gold** layer.

---

### 3. Data Consumption  
The final data stored in the **Gold** layer (Delta format) is used for **analytics and visualization**, enabling better insights through dashboards or external BI tools.

---

## Technologies Used  
- **Microsoft Azure**  
  - Azure Data Factory  
  - Azure Data Lake Storage (Bronze, Silver, Gold containers)  
  - Azure Databricks (PySpark)  
- **Delta Lake** – For scalable and ACID-compliant data storage  
- **Parquet Format** – For efficient intermediate data storage  
- **Visualization Tools** (e.g., Power BI, Synapse Studio) – For interactive dashboards  

---

## Learnings  
Through this project, I gained practical experience in building scalable, layered data pipelines using Azure services. I learned how to:
- Design and implement a modern data lake architecture.
- Use **Delta Lake** for reliable and performant data workflows.
- Transform and enrich data using **PySpark** in **Databricks**.
- Separate and manage datasets through the **Bronze-Silver-Gold** architecture for modularity and maintainability.

---
