# Week 3: Multi-Source Data Integration Pipeline

## Project Overview
This repository contains a multi-source data engineering pipeline built in Python. The pipeline integrates operational sensor readings, live weather API metrics, and database metadata into a unified Master DataFrame to perform correlation analysis and deliver actionable business recommendations.

## Repository Deliverables & Links
- **GitHub Repository:** [https://github.com/Sigei200/week3_multi_source_pipeline](https://github.com/Sigei200/week3_multi_source_pipeline)
- **Primary Data Pipeline Notebook:** `week3_multi_source_pipeline.ipynb`
- **Internal CSV Dataset:** `cleaned_sensor_readings.csv`
- **Presentation Slides (PDF):** `presentation_slides.pdf` *(Replace/Upload your 3-slide PDF here)*
- **Recorded Video Presentation:** [Insert Loom / YouTube / Google Drive Link Here]

## Data Architecture
1. **Source 1 (Internal Operational Data):** `cleaned_sensor_readings.csv` containing sensor logs aggregated at the daily zone level (`Pressure_PSI`, `Temperature_C`, `Flow_Rate_LPM`).
2. **Source 2 (External API Data):** Live ambient weather metrics fetched via the `requests` library with `try-except` exception handling.
3. **Source 3 (Relational Database):** SQLite database (`operations_metadata.db`) storing plant capacity ratings and staffing shifts, queried using `JOIN` and `GROUP BY` via SQL.
4. **Data Integration & Cleaning:** Merged across `date` and `Zone` alignment keys with missing value handling.
5. **Correlation Analysis:** Evaluates operational relationships (e.g., impact of rainfall and pressure on total fluid throughput).

## How to Run Locally
1. Clone the repository:
git clone https://github.com/Sigei200/week3_multi_source_pipeline.git
  
  