# Predicting School Performance from Socioeconomic Factors

> This project investigates how socioeconomic characteristics and school-level factors relate to high school students’ average ACT scores across different regions.

---

## Project Overview

This project explores relationships between community and school-level socioeconomic factors and high school ACT performance.

- **Objective:** Identify how community-level socioeconomic factors influence school performance, focusing on variables such as unemployment rate, adult educational attainment, median household income, family structure, and percent of students receiving free or reduced-price lunch.
- **Domain:** Education
- **Key Techniques:** Data Cleaning, Data Preparation, Data Merging, Data Visualization, Exploratory Data Analysis (EDA), Heatmaps, Simple Linear Regression Modeling, Model Evaluation (Residuals, MAE, R²)

---

## Project Structure

```
├── data/                 # Raw and processed data
├── code/                 # Jupyter notebooks and Python scripts
├── reports/              # Generated reports and visualizations
├── requirements.txt      # Dependencies
└── README.md             # Project documentation
```

---

## Data

- **Source:** 
**[EdGap_data.xlsx]** (https://github.com/brian-fischer/DATA-5100/blob/main/EdGap_data.xlsx)

**[school_information.csv]**(https://www.dropbox.com/scl/fi/fkafjk8902sq8ptxh94r2/ccd_sch_029_1617_w_1a_11212017.csv?rlkey=gucrdz5f6e38bezz2y3yalxbw&e=1&dl=0)
- **Description:** Datasets include school-level ACT scores, community demographics, and school characteristics.
- **License:** Census Bureau’s American Community Survey; National Center for Education Statistics (NCES)

---

## Data Preparation
The raw education datasets were processed to create a clean dataset ready for analysis. The main steps included:
1. Load libraries and datasets – import pandas, numpy, seaborn, matplotlib, and statsmodels.
- Loaded raw dataset: [EdGap_data.xlsx]  and  [school_information.csv]
2. Inspect and clean data – examined dataset structure, converted data types for merging, removed unnecessary columns, filtered for high schools, and replaced invalid values.
3. Rename columns – ensure consistent, descriptive names using lowercase snake_case.
4. Merge datasets – combine EdGap and school information using left join.
5. Handle missing values – drop missing ACT scores and impute missing socioeconomic predictors using iterative regression-based imputation.
6. Export cleaned dataset – saved as education_clean.csv for further analysis.
- Cleaned dataset: data/education_clean.csv
--- 

## Analysis
- **Notebook:** "Education.ipynb"
- **Steps Taken:**
(1) Load cleaned dataset.
(2) Conduct exploratory data analysis using a heatmap to explore correlations between ACT scores and socioeconomic factors.
(3) Build a simple linear regression model using percent_lunch (percentage of students receiving free or reduced-price lunch) as the predictor for ACT scores.
(4) Evaluate model performance using residual plots, MAE, and R-squared metrics.
(5) Interpret findings in clear, non-technical language.

---

## Results
1. The heatmap shows strong negative correlation between average ACT scores and the percentage of students receiving free or reduced-price lunch. Positive correlations exist with median income, percent of adults with college degrees, and percent married.
2. Regression analysis using percent_lunch as the sole predictor explains about 61% of the variation in ACT scores between schools.
3. Schools with higher proportions of low-income students tend to have lower ACT scores.
4. While percent_lunch is a strong predictor, other factors like household income, adult education, and community characteristics also influence ACT performance.

- Conclusion: Addressing socioeconomic disparities, especially supporting low-income students, could meaningfully improve ACT outcomes.

---

## Authors

- Muykhim Ing - [@muykhim](https://github.com/muykhim)

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## Acknowledgements

- Python libraries: pandas, numpy, matplotlib, seaborn, statsmodels, scikit-learn
- NCES and Census Bureau for datasets
- DATA-5100 course materials by Dr. Brian Fischer
