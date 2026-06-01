## Purpose
This project demonstrates a practical relational-to-FHIR transformation workflow aligned to health data interoperability, SQL, Databricks, JSON, Postman, Agile delivery, and Azure DevOps traceability.

## Kaggle dataset
**Healthcare Dataset** by prasad22  
Kaggle handle: `prasad22/healthcare-dataset`

The notebook downloads the Kaggle dataset when Kaggle access is configured. A small synthetic fallback CSV is included so the notebook can still run locally for demonstration purposes.

## Files
- `OPS_FHIR_Interoperability_Portfolio_Notebook.ipynb` — main implementation notebook
- `healthcare_dataset_demo.csv` — offline fallback sample
- `source_to_target_mapping.csv` — relational-to-FHIR mapping document
- `azure_devops_backlog.csv` — import-friendly Agile backlog and acceptance criteria
- `postman_fhir_r4_validation_collection.json` — Postman collection for FHIR API testing
- `requirements.txt` — local dependencies

## Run locally
```bash
python -m venv .venv
# Windows
.venv\Scripts\activate
# macOS/Linux
source .venv/bin/activate

pip install -r requirements.txt
jupyter notebook OPS_FHIR_Interoperability_Portfolio_Notebook.ipynb
```

## Databricks use
Upload the notebook and CSV files into a Databricks workspace. The notebook contains Spark and `%sql` examples for temp views, quality checks, and JSON export.

## Postman use
Import `postman_fhir_r4_validation_collection.json` into Postman. The default environment variable points to a public FHIR R4 test server. Use only synthetic data. Review requests before sending them.

