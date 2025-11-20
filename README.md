DFIR Metadata Dashboard – AI/ML + DFIR Internship Task
A Digital Forensics Metadata Extraction & Analysis Toolkit

Overview

This project is part of the Kriyavan Cyber Forensic Service Pvt Ltd – AI/ML + DFIR Internship selection task.
The goal of this project is to build a complete metadata extraction pipeline and an interactive Streamlit dashboard for analyzing file metadata, grouping by attributes, and performing forensic insights.

Features:

1. Metadata Extraction Pipeline
    Recursively scans any folder
    Extracts:
       File size, timestamps
       MD5, SHA1 (SHA256 optional)
       Image EXIF metadata
       PDF metadata
        DOCX core properties
Normalizes all extracted metadata into a single Parquet file

 2. Streamlit Dashboard

     Interactive filters (filetype, hash, metadata fields, etc.)
     Charts and top-group visualizations
     Drill-down for individual files
     Metadata table view + CSV export

3.  Installation

 Clone the repository
           git clone <your_repo_url>
             cd <repo_folder>

4.  Install dependencies
        pip install -r requirements.txt

5.Running the Pipeline

   To run metadata extraction:
      python src/pipeline/pipeline.py --input <folder_path> --output data/output/metadata.parquet

Example:
python src/pipeline/pipeline.py --input sample_data --output data/output/metadata.parquet

6 .Running the Dashboard

Start Streamlit:
streamlit run streamlit_app.py


Then open browser:

http://localhost:8501

 Output:
  Your pipeline will generate:
     data/output/metadata.parquet
     This contains the fully normalized metadata table.


