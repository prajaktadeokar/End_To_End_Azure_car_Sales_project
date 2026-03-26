# End-to-End Data Engineering Pipeline on Azure 
 
## Overview 
This project demonstrates a scalable end-to-end data pipeline built using Azure services. 
 
The pipeline ingests raw data using Azure Data Factory, stores it in Azure Data Lake Storage Gen2, and performs transformations using Azure Databricks following the Medallion Architecture (Bronze, Silver, Gold). 
 
## Tech Stack 
- Azure Data Factory 
- Azure Databricks 
- Azure Data Lake Storage Gen2 
- Python 
- PySpark 
 
## Architecture 
![Architecture](architecture/pipeline_architecture.png) 
 
## Pipeline Workflow 
1. Data is ingested using Azure Data Factory 
2. Raw data is stored in Bronze layer in ADLS 
3. Databricks cleans and transforms data into Silver layer 
4. Business-ready data stored in Gold layer in the Star Schema format.
 
## Medallion Architecture 
Bronze → Raw Data   
Silver → Cleaned Data   
Gold → Business Aggregations 


 
## Project Structure 
zure-data-pipeline-project/ 
│ 
├── README.md 
├── architecture/ 
│     └── pipeline_architecture.png 
│ 
├── data/ 
│     └── sample_data.csv 
│ 
├── adf_pipeline/ 
│     ├── pipeline.json 
│     └── linked_services.json 
│ 
├── databricks_notebooks/ 
│     ├── bronze_layer_ingestion.py 
│     ├── silver_layer_transformation.py 
│     └── gold_layer_aggregation.py 
│ 
├── configs/ 
│     └── config.yaml 
│ 
├── scripts/ 
│     └── create_adls_containers.py 
│ 
├── docs/ 
│     ├── pipeline_steps.md 
│     └── setup_guide.md 
│ 
└── requirements.txt 