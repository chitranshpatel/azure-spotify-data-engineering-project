# 🎧 **End-to-End Spotify Data Engineering Project on Azure & Databricks**  
*A Production-Grade Medallion Architecture on Azure & Databricks*

<img width="2752" height="1336" alt="spotify" src="https://github.com/user-attachments/assets/f4de7ce5-1c63-4ce2-9330-15b57ed34644" />


---

## 📌 **Project Overview**

This project demonstrates a complete **enterprise-grade data engineering pipeline** built on Azure and Databricks using the Spotify dataset.

It showcases real-world data engineering capabilities such as:

- Cloud orchestration (Azure Data Factory)
- Scalable ingestion (Auto Loader)
- Metadata-driven transformations (Jinja)
- Spark Structured Streaming
- SCD handling
- Delta Live Tables (DLT)
- Unity Catalog governance
- CI/CD (Databricks Asset Bundles)
- Star Schema Modeling

The solution follows the **Medallion Architecture**:  
**Bronze → Silver → Gold → Warehouse**

---

## 🛠️ **Tech Stack**

### **Cloud & Storage**
- Azure SQL Database  
- Azure Data Lake Storage Gen2 (ADLS)  
- Unity Catalog + Unity Metastore  

### **Orchestration**
- Azure Data Factory (ADF)

### **Compute**
- Azure Databricks  
- Spark Structured Streaming  
- Delta Live Tables (DLT)  

### **DevOps & CI/CD**
- GitHub  
- Databricks Asset Bundles  

### **Architecture Patterns**
- Medallion Architecture  
- Star Schema  

---


# 🥉 **Bronze Layer – Raw Data Ingestion**

### 🔄 **ADF Incremental + Backfill Pipeline**

This pipeline loads data from Azure SQL DB into ADLS Bronze using:

- Incremental CDC logic  
- Backfilling  
- Parameterized pipeline design  
- Dynamic tables  
- Alerting hooks

<img width="801" height="337" alt="Screenshot 2025-12-03 at 12 01 57 PM" src="https://github.com/user-attachments/assets/3d755fda-46af-4612-86fc-f05bcbb9db1a" />
<img width="950" height="465" alt="Screenshot 2025-12-03 at 12 02 05 PM" src="https://github.com/user-attachments/assets/b7fed5e6-78f3-4d9f-b73f-5fdf1be8e29a" />



---

# 🥈 **Silver Layer – Clean & Enriched Data**

### 🧩 **Metadata-Driven SQL Generation (Jinja + Databricks)**

All Silver transformations are fully **dynamic** and **metadata-driven**, enabling:

- Automated column selection  
- Automated JOIN creation  
- Schema evolution  
- SCD prep  
- Central metadata control  

####  🧱 Jinja SQL Template Structure

<img width="600" height="678" alt="Screenshot 2025-12-03 at 12 06 41 PM" src="https://github.com/user-attachments/assets/d326162f-32f9-4704-b1eb-96f7fc5a6454" />


#### 🟢 Generated SQL Output (Dynamic JOINs)

<img width="572" height="499" alt="Screenshot 2025-12-03 at 12 06 46 PM" src="https://github.com/user-attachments/assets/67878c9b-a4a2-4e83-a85e-b1f0fa71bedd" />


---

# 🥇 **Gold Layer – Delta Live Tables (DLT)**

### ⭐ **DLT Pipeline Execution**

DLT builds the final star schema:

- Fact table (`factstream`)
- Dimensions (`dimuser`, `dimtrack`, `dimdate`)
- Streaming updates  
- Upsert & SCD logic  

<img width="682" height="584" alt="Screenshot 2025-12-03 at 12 07 38 PM" src="https://github.com/user-attachments/assets/0536941f-3970-4e43-b8dd-cce107afe1b7" />


---

# ⭐ **Star Schema Modeling**

Your Gold layer exposes a clean and analytics-friendly star schema:

- **Fact Table:** `factstream`  
- **Dimension Tables:** User, Track, Date  

Optimized for BI and warehousing.

---

# 🚀 **CI/CD – Databricks Asset Bundles**

The project uses **Databricks Asset Bundles** for:

- Packaging notebooks, DLT pipelines, configs  
- Environment-wise promotion (dev → prod)  
- Automated deployment  
- GitHub workflow integration  

---

# 🎯 **Key Project Requirements Achieved**

| Requirement | Status |
|------------|--------|
| Incremental ingestion | ✅ |
| Backfilling support | ✅ |
| Metadata-driven pipelines | ✅ |
| Spark structured streaming | ✅ |
| Auto Loader ingestion | ✅ |
| Star schema modeling | ✅ |
| SCD logic | ✅ |
| Delta Live Tables | ✅ |
| CI/CD (Asset Bundles) | ✅ |
| Dynamic SQL generation | ✅ |

---


---

# 📊 **End-to-End Data Flow Summary**

1. Azure SQL DB → ADF → ADLS Bronze  
2. Bronze → Silver via Databricks (Auto Loader + Jinja SQL)  
3. Silver → Gold using DLT  
4. Gold → SQL Warehouse / BI Layer  

---

# 📬 **Contact**

If you'd like to discuss this project or learn more:

**Chitransh Patel**  
Melbourne, Australia  

---



