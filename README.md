# Life Expectancy Analysis & Prediction

## Project Overview
Life expectancy is a key metric for assessing the health and well-being of a country's population. This project analyzes data from the **World Health Organization (WHO)** to identify the primary factors affecting life expectancy across different countries and years.

Using **Human-Centered Data Science** principles, the goal was not just to predict a number, but to understand the socio-economic and health factors (such as Schooling, GDP, and Immunization) that have the strongest correlation with longevity.

## Repository Structure
```text
├── Data/
│   └── Life Expectancy Data.csv   # The dataset used for analysis
├── Life_expectancy_project.ipynb  # Main Jupyter Notebook
├── Project_Report.pdf             # Detailed analysis report
└── README.md                      # Project documentation

## Dataset
The dataset contains health and economic data for 193 countries from the year 2000 to 2015.
- **Source:** World Health Organization (WHO)
- **Key Features:**
  - **Health:** Adult Mortality, Infant Deaths, Hepatitis B, Polio, HIV/AIDS, BMI.
  - **Economic:** GDP, Percentage Expenditure, Income Composition of Resources.
  - **Social:** Schooling, Alcohol Consumption.

## Methodology
The analysis followed a rigorous data science pipeline:

### 1. Data Preprocessing & Cleaning
- **Handling Missing Values:** Imputed missing values using the mean/median for relevant columns to maintain data integrity.
- **Outlier Detection:** Identified outliers in variables like `GDP` and `Infant Deaths` and handled them using Winsorization (capping extreme values) to prevent model skewing.
- **Renaming:** Standardized column names for better readability (removing extra spaces).

  <img width="885" height="424" alt="Screenshot 2026-01-18 at 22 49 14" src="https://github.com/user-attachments/assets/3967495a-348c-4617-99f6-4470715470b3" />


### 2. Exploratory Data Analysis (EDA)
- **Univariate Analysis:** visualized the distribution of variables like `Life Expectancy` and `Adult Mortality`.
- **Correlation Analysis:** A heatmap was used to identify strong positive correlations between **Schooling**, **Income Composition**, and **Life Expectancy**, and negative correlations with **Adult Mortality** and **HIV/AIDS**.
<img width="899" height="681" alt="Screenshot 2026-01-18 at 22 51 22" src="https://github.com/user-attachments/assets/491bc0a4-a7cf-4970-adae-9e6b567c2aa4" />


### 3. Machine Learning Model
- **Algorithm:** Linear Regression (OLS).
- **Goal:** Predict the `Life expectancy` variable based on the most significant features.
- **Feature Selection:** Removed highly correlated independent variables (Multicollinearity) to improve model stability.

## Key Findings
- **Education is Vital:** `Schooling` had one of the highest positive correlations with life expectancy.
- **Economic Impact:** `GDP` and `Income composition of resources` are strong predictors of a longer life.
- **Health Challenges:** `HIV/AIDS` and `Adult Mortality` have the strongest negative impact on life expectancy.
<img width="731" height="637" alt="Screenshot 2026-01-18 at 22 52 26" src="https://github.com/user-attachments/assets/a24008d5-29e3-4e54-892d-35e45b06ed0c" />


## How to Run
1. Clone the repository:
   ```bash
   git clone [https://github.com/slchahmed-sly/Life-Expectancy.git](https://github.com/slchahmed-sly/Life-Expectancy.git)
  ```
2. Install dependencies
```bash
  pip install pandas numpy seaborn matplotlib scikit-learn scipy & jupyter notebook
```
<img width="553" height="409" alt="Screenshot 2026-01-18 at 22 53 05" src="https://github.com/user-attachments/assets/0fa8271f-7d54-402a-8e21-eca9cfba7ebc" />

## License
This project is for educational purposes. Data provided by WHO.
Created by Mohamed Souleimane Cheikh Ahmed
