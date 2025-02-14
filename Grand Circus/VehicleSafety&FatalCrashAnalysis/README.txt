# Vehicle Safety & Fatal Crash Data Pipeline

## Project Overview
This project analyzes vehicle safety ratings and their correlation with fatal crash data to provide insights for insurers on risk assessment and premium pricing.

## Data Pipeline Overview
The pipeline extracts, transforms, and loads (ETL) vehicle crash data from an API, integrates it with vehicle safety ratings, and performs exploratory data analysis (EDA) to uncover trends.

## Data Sources
- **Crash Data API:** National Highway Traffic Safety Administration (NHTSA) - Provides fatal crash records by vehicle make, model, and year.
- **Safety Ratings Dataset:** Insurance Institute for Highway Safety (IIHS) - Contains vehicle crash test ratings.
- **Insurance Premium Trends (Optional):** Public insurance datasets for comparative analysis.

## Setup Instructions

### 1 Install Dependencies
Ensure you have Python 3.8+ and install required libraries:
```bash
pip install pandas numpy requests tqdm aiohttp matplotlib seaborn
```

### 2 Clone the Repository
```bash
git clone https://github.com/your-repository/vehicle-safety-analysis.git
cd vehicle-safety-analysis
```

### 3 Data Pipeline Execution

#### **Step 1: Extract Data**
- The script `data_extraction.py` retrieves crash data from the NHTSA API and vehicle safety ratings.
- The API calls are optimized for performance using **async requests**.

#### **Step 2: Transform Data**
- Data is cleaned, formatted, and merged into a structured DataFrame.
- String values are converted to lowercase for consistency.
- Data is grouped by year, make, and model to compute fatality trends.

#### **Step 3: Load Data into Database**
- The cleaned dataset is stored in a local PostgreSQL/MySQL database.
- Alternatively, it can be saved as a **CSV/Parquet file** for easy access.

```python
import pandas as pd
df.to_csv("cleaned_crash_data.csv", index=False)
```

### 4 Running Exploratory Data Analysis (EDA)
- Open `analysis.ipynb` in Jupyter Notebook.
- Run each cell to generate insights and visualizations.

```bash
jupyter notebook analysis.ipynb
```

### 5 Running the Data Pipeline End-to-End
- Execute the main script to pull and analyze crash data.
```bash
python main.py
```

### 6 Power BI Dashboard (Optional)
- Open the Power BI file (`dashboard.pbix`).
- Load `cleaned_crash_data.csv` and refresh visuals.

## Key Features
**Automated API data extraction**  
**Data transformation & cleaning**  
**Exploratory Data Analysis (EDA)**  
**Power BI dashboard for visualization**  
**GitHub-hosted repository for code versioning**  

## Contributors
- **Your Name**
- **Team Members**

## Future Enhancements
- Automate API updates to keep crash data live.
- Add machine learning models for risk prediction.

---
*By leveraging real crash data, insurers can improve risk assessment and offer fairer premiums.* 
