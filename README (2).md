# Air Quality Analysis of Indian Cities (2015–2020)

An Exploratory Data Analysis project analyzing air pollution patterns across 26 Indian cities.

## Description

This project analyzes 5 years (2015–2020) of daily air quality data across 26 major Indian cities, sourced from the Central Pollution Control Board (CPCB) via Kaggle. Using Python (Pandas, Matplotlib, Seaborn), the project performs end-to-end exploratory data analysis — data cleaning, handling missing values, skewness and outlier detection, and visualization — to uncover which cities are most polluted, how pollution varies by season and month, and which pollutants are most strongly linked to overall Air Quality Index (AQI). The cleaned dataset is also used to build two interactive Power BI dashboards: one comparing pollution across cities, and one focused on pollutant trends and seasonal patterns. The goal is to turn raw government pollution data into clear, actionable insights that could support pollution-control decision-making.

## Getting Started

### Dependencies

* Python 3.x
* Google Colab or Jupyter Notebook
* Libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scipy`
* Power BI Desktop (for the dashboard files)
* Windows 10 / macOS / Linux (any OS that runs Python and/or Power BI Desktop)

### Installing

* Clone or download this repository, or download the individual files (notebook, dataset CSV, dashboard `.pbix` files, report `.docx`)
* If running locally (not Colab), install the required libraries:
```
pip install pandas numpy matplotlib seaborn scipy
```
* No modifications to file paths are needed if the dataset CSV (`air_quality_cleaned.csv` or `city_day.csv`) is kept in the same folder as the notebook — otherwise, update the file path in the `pd.read_csv()` line to match where the CSV is stored

### Executing program

* Open the notebook (`air_quality_analysis.ipynb`) in Google Colab or Jupyter Notebook
* Upload the dataset CSV into the same session/folder as the notebook
* Run all cells from top to bottom in order:
```
Stage 1: Initial EDA (load data, shape, data types, statistical summary)
Stage 2: Data Cleaning & Pre-processing (missing values, duplicates, skewness, outliers, derived columns)
Stage 3: EDA & Visualizations (8 charts covering univariate, bivariate, and multivariate analysis)
Stage 4: Documentation, Insights & Presentation
```
* To view the dashboards, open the `.pbix` file(s) in Power BI Desktop
* To view the full write-up, open the project report (`Air_Quality_Analysis_Project_Report.docx`)

## Help

* If a cell throws a `FileNotFoundError`, check that the CSV filename in `pd.read_csv()` matches the actual uploaded file name exactly (case-sensitive)
* If Power BI shows `Column1`, `Column2` instead of real column names after importing the CSV, open **Transform Data** → **Use First Row as Headers**, then **Close & Apply**
* If a DAX measure shows an "unexpected parameter" error, check for curly/smart quotes (`"`) instead of straight quotes (`"`) around text values, and rewrite them manually
```
Example fix: use 'TableName'[AQI_Bucket] = "Poor" with straight quotes, not curly quotes
```

## Authors

* Monika

## Version History

* 0.2
    * Added skewness and outlier detection (Section 2.6–2.8)
    * Added 3 additional visualizations (8 charts total)
    * Added two Power BI dashboards and full project report
* 0.1
    * Initial data cleaning, EDA, and 5 core visualizations

## License

This project is licensed under the MIT License - see the LICENSE.md file for details

## Acknowledgments

* Dataset: [Air Quality Data in India — Kaggle](https://www.kaggle.com/datasets/rohanrao/air-quality-data-in-india), compiled from CPCB (Central Pollution Control Board), Government of India
* [awesome-readme](https://github.com/matiassingers/awesome-readme)
