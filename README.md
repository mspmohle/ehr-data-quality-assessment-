Overview

This project demonstrates how to evaluate the quality and completeness of Electronic Health Record (EHR) data using synthetic datasets and open-source data validation frameworks.
It follows a clinical data engineering perspective aligned with healthcare data governance principles.

Objectives

Validate core data quality dimensions (completeness, consistency, accuracy).

Visualize missingness and outliers within EHR-style data.

Automate rule-based validation using Great Expectations.

Produce reproducible metrics and charts suitable for clinical data teams.

Repository Structure
```text
ehr-data-quality-assessment-/
│
├── data/
│   ├── raw/               # Raw synthetic EHR dataset
│   └── processed/         # Cleaned datasets, summaries
│
├── figures/               # Visualizations of data quality metrics
│
├── notebooks/
│   └── 01_ehr_quality_assessment.ipynb  # Main analysis notebook
│
├── requirements.txt       # Python dependencies
├── README.md              # Project overview (this file)
└── .gitignore             # Git tracking exclusions

Environment Setup
# Clone repository
git clone https://github.com/mspmohle/ehr-data-quality-assessment-.git
cd ehr-data-quality-assessment-

# Create and activate environment
conda create -n ehr-quality python=3.11 -y
conda activate ehr-quality

# Install dependencies
pip install -r requirements.txt

# Launch Jupyter
jupyter lab

Notebook Summary

01_ehr_quality_assessment.ipynb

Synthetic EHR Dataset Generation – creates a mock clinical dataset with demographics, vitals, and lab results.

Data Validation (Great Expectations) – applies expectation suites to check for missingness and logical ranges.

Visual Analysis – produces heatmaps, histograms, and anomaly plots for completeness and accuracy.

Summary Output – exports metrics and flagged records to /data/processed for downstream analysis.

Example Insights

Missing lab results concentrated among older patient cohorts.

Implausible values identified for systolic blood pressure and BMI.

Validation success rate >95% after cleaning pipeline execution.

Tools & Libraries

Python 3.11

Pandas / NumPy

Matplotlib / Seaborn

Great Expectations

JupyterLab

Next Steps

Integrate real EHR export schemas for field alignment testing.

Add FHIR (Fast Healthcare Interoperability Resources) mapping validation.

Deploy validation reports via web-based dashboards (Streamlit or Power BI).

MIT License

Copyright (c) 2025 Michael S. Mohle

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
