## Purpose
This project provides a practical relational-to-FHIR transformation workflow for health data interoperability, SQL validation, Databricks/Spark processing, JSON generation, Postman API testing, Agile delivery, and Azure DevOps traceability.

## Kaggle dataset
**Healthcare Dataset** by prasad22  
Kaggle handle: `prasad22/healthcare-dataset`

The notebook downloads the Kaggle dataset when Kaggle access is configured. A small synthetic fallback CSV is included so the workflow can still run locally without external access.

## Files
- `Healthcare_FHIR_Interoperability_Notebook.ipynb` - main implementation notebook
- `healthcare_dataset_sample.csv` - offline fallback sample
- `source_to_target_mapping.csv` - relational-to-FHIR mapping document
- `azure_devops_backlog.csv` - import-friendly Agile backlog and acceptance criteria
- `postman_fhir_r4_validation_collection.json` - Postman collection for FHIR API testing
- `requirements.txt` - local dependencies

## Run locally
```bash
python -m venv .venv
# Windows
.venv\Scripts\activate
# macOS/Linux
source .venv/bin/activate

pip install -r requirements.txt
jupyter notebook Healthcare_FHIR_Interoperability_Notebook.ipynb
```

## Databricks use
Upload the notebook and CSV files into a Databricks workspace. The notebook contains Spark and `%sql` examples for temp views, quality checks, and JSON export.

## Postman use
Import `postman_fhir_r4_validation_collection.json` into Postman. The default environment variable points to a public FHIR R4 test server. Use only synthetic data. Review requests before sending them.
