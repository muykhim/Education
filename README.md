# Project Title (This is a template README.md file that you can adapt to your project)

>This project analyzes educational data to explore patterns in school performance and equity across different regions.

---

## Project Overview

Provide a short and concise overview of the project. Mention the problem it solves, the data used, and the key outcomes or findings.

- **Objective:** Clearly state the main goal of the project.
- **Domain:** (e.g., Healthcare, Finance, E-commerce, etc.)
- **Key Techniques:** (e.g., Regression, Classification, Clustering, NLP, Time Series)

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
- **Description:** Brief overview of the dataset features, size, and format
- **License:** (if applicable)

---

## Data Preparation
The raw education datasets were processed to create a clean dataset ready for analysis. The main steps included:
1. Load raw dataset: [EdGap_data.xlsx]  and  [school_information.csv]
2. Explore and inspect: Check data structure, column types, and missing values.
3. Select and rename columns: Keep only relevant information (year, school ID, location, type) and rename columns for clarity and consistency.
4. Join datasets: Merge EdGap data with school information using a left join to retain all primary records.
5. Quality control: Remove invalid values, filter for relevant schools, and remove duplicates.
6. Handle missing values: Drop rows with missing ACT scores and impute missing socioeconomic predictors using iterative regression-based imputation.
7. Export cleaned dataset: Saved as education_clean.csv for further analysis.
8. Notebook performing data preparation: code/education.ipynb
9. Cleaned dataset: data/education_clean.csv

--- 

## Analysis

Describe the notebooks and/or scripts used to perform the analysis. Specify the order in which the code should be run to reproduce the results.

---

## Results

Include a short discussion of the findings and what they imply.

---

## Authors

- Muykhim Ing - [@yourhandle](https://github.com/yourhandle)

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## Acknowledgements

- Tools/libraries used
- Tutorials or papers referenced
- Inspiration or collaborators
