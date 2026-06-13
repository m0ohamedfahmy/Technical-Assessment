# Tech Sales Analytics — ETL, Data Model & Power BI Dashboard
> 💡 **Architectural Note:** The structural creation of the data warehouse schema, relational tables, constraints mapping, and the eventual data loading phase are completely programmatically orchestrated as native components of the ETL pipeline scripts. The database interaction and SQL execution layers are powered natively by **SQLAlchemy** inside the Python environment to ensure high performance and strict schema governance.

## 📁 Project Structure

```
│
├── 📂 Dashboard/
│   └── Dashboard.pbix              # The interactive Power BI dashboard and visualization layout            
│
├── 📂 Data/
│   ├── 📂 Celan_data /            # Production-ready data after passing transformation and type cleaning
│   │            
│   └── 📂 Raw_data /              # Immutable raw source logs (Sales transactions and Forecast sheets)
│
├── 📂 DataModel/
│   └── datamodel.png              # Visual Entity-Relationship Diagram (ERD) of the Star Schema       
│
├── 📂 Documentation/  
│   └── Documentation.pdf          # Comprehensive technical documentation            
│                                                 
│
├── 📂 Scripts/
│   ├── 00_Data_Exploration(EDA).ipynb              # Jupyter notebook for EDA
│   ├── 01_Sales_ETL_Pipeline.ipynb                 # Transactional ETL: Cleans Sales Data, handles dates, Create Database Tables and Data Modeling ,and models SQL tables via SQLAlchemy
│   └── 02_Forecast_ETL_Pipeline.ipynb              # Forecast ETL: Cleans Data, Create Database Tables and Data Modeling ,and models SQL tables via SQLAlchemy, Handles granularity mismatch, aggregates targets, and maps schemas
└── 
```

---