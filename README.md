# Claims Analysis Project

## Project Overview
This project analyzes healthcare claims data from Stony Brook University Hospital using three interconnected datasets: HEADER, LINE, and CODE. The goal is to understand billing patterns, payer distribution, diagnosis frequency, procedure utilization, and financial impact. This analysis highlights how relational claims data can be integrated to generate revenue cycle insights and operational planning.

---

## Required Libraries (Listed in requirements.txt)
pandas>=1.3.0
matplotlib>=3.4.0
seaborn>=0.11.0

## Data Source
The data files were provided as part of the course module:

├── STONYBRK_20240531_HEADER.csv
├── STONYBRK_20240531_LINE.csv
└── STONYBRK_20240531_CODE.csv

- **HEADER:** Claim-level details (providers, payer, place of service)
- **LINE:** Service line details (HCPCS, modifiers, charges, units)
- **CODE:** Diagnosis information (ICD-10 codes per claim)

All files must be placed in the `data/` folder of this repository.

## Project Setup 

To set up the project, the repository was downloaded to a local machine, and the three CSV files (HEADER, LINE, and CODE) were placed in the data folder for access during the analysis. The required Python libraries were installed using pip install -r requirements.txt, which ensured that all packages such as pandas, matplotlib, and seaborn were available. Using the Python 3.13.7 Jupyter Kernel, the analysis was carried out in the claims_analysis.ipynb notebook to allow data to load accurately, the merges and calculations ro run without issues, and generate visualizations and results for each portion of the assignment. 

## Key Findings

From our results and analysis, Medicare played the largest role in the highest total billed charges, contributing about 131,000 and serving as the most significant payer in the dataset. This is consistent with patients that need hospital based care, where a large amount of high acuity instances are billed to Medicare. Out of all of the procedure codes, HCPCS 99291 generated the largest total charges at approximately 78,540, which exceeded far from any other billed service, and is often expected in critical care service due to the involvement of urgent situations, multiple related interventions, and extensive provider time. Consequently, it was also found that the diagnosis most frequently associated with critical care services was J96.01, representing acute respiratory failure. Majority of these claims were submitted from inpatient settings, where office visits appeared less frequently and suggests that majority of patients in this dataset need higher levels of care. Claims containing five or more service lines were linked to higher total charges, reflecting more complex encounters, aligning with the idea that more complex cases would naturally have more billable components. Overall, these patterns observed in this analysis indicate a patient population with complex medical needs and demonstrates the financial impacts in providing their care. # claims-analysis
