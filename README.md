# Exploratory Data Analysis of Hospital Patient Records for Healthcare Insights

Final year project submitted to the Department of Computer Science, School of Information and Communication Technology, Federal University of Technology, Minna, Nigeria, in partial fulfilment of the requirements for the award of the Bachelor of Technology (B.Tech) degree in Computer Science.

**Author:** Daniel Felix Zamwa
**Supervisor:** Mr. A.M. Salihu
**Academic session:** 2025/2026

## Overview

This project applies Exploratory Data Analysis (EDA) to a hospital patient dataset in order to identify patterns and trends in diagnoses, patient demographics, test results and admission timing. The analysis is written in Python and carried out in a Google Colab notebook, using descriptive statistics, frequency analysis, cross tabulation and graphical visualisation.

## Objectives

1. Determine the most common diagnoses in the hospital patient dataset.
2. Analyse the age distribution across diagnoses.
3. Analyse the distribution of test results among admitted patients.
4. Examine seasonal trends in disease occurrence based on admission dates.
5. Investigate the relationship between patient gender and diagnosis frequency.

## Dataset

The study uses the [Healthcare Dataset](https://www.kaggle.com/datasets/prasad22/healthcare-dataset) by Prasad22, available on Kaggle. It is a synthetic, anonymised dataset in CSV format and contains no identifiable patient information.

| Property | Value |
| --- | --- |
| Original records | 55,500 |
| Variables | 15 |
| Missing values | None |
| Duplicate records removed | 534 |
| Records used for analysis | 54,966 |

The dataset is not included in this repository. The notebook downloads it automatically from Kaggle using the `kagglehub` library.

## Repository Structure

| File | Description |
| --- | --- |
| `FinalYearProject.ipynb` | Google Colab notebook containing the full workflow, from data loading and preprocessing to the analysis and visualisation for each objective |
| `README.md` | Project description and instructions for replicating the analysis |

## Methodology

1. **Data loading:** the dataset CSV file is imported into a Pandas DataFrame.
2. **Preprocessing:** checking for missing values, removing duplicate records, standardising column names to lower case with underscores, converting date columns to datetime format and standardising categorical entries.
3. **Exploratory analysis:** descriptive statistics, frequency and percentage distributions, grouped summaries and cross tabulations aligned with each objective.
4. **Visualisation:** bar charts, pie charts, histograms, box plots, line charts, grouped and stacked bar charts and heatmaps.
5. **Statistical testing:** a chi-square test of independence between gender and diagnosis.

## Summary of Findings

- Arthritis was the most frequently recorded diagnosis (9,218 records, 16.77%), although the six diagnoses were almost evenly distributed.
- Age showed no meaningful variation across diagnoses, with an overall mean of 51.54 years and a range of 13 to 89 years.
- Hospital admissions peaked in August (4,785) and in Summer (14,200), with only modest seasonal variation across the year.
- The chi-square test (p = 0.9565) showed no statistically significant association between gender and diagnosis.
- The near-uniform distributions across variables are consistent with the synthetic nature of the dataset.

## How to Run

1. Open `FinalYearProject.ipynb` in Google Colab (select **Open in Colab** from GitHub, or upload the notebook to Colab).
2. Run the cells in order from the top of the notebook.
3. Allow access to Google Drive when prompted. The notebook mounts Google Drive to save the cleaned dataset (`healthcare_dataset_cleaned.csv`) and the generated charts.
4. The dataset is downloaded automatically from Kaggle by the notebook, so no manual download is needed.

## Requirements

- Python 3
- Pandas
- NumPy
- Matplotlib
- Seaborn
- SciPy (used for the chi-square test of independence)
- kagglehub (used to download the dataset)

Google Colab provides most of these libraries by default, so no local installation is required. If `kagglehub` is not available in the Colab session, install it by running `pip install kagglehub` in a cell.

## Ethical Considerations

The study uses a publicly available, anonymised and synthetic dataset. No identifiable patient information was accessed or analysed, and the data was used strictly for academic purposes.

## Reference

Patil, P. (n.d.). *Healthcare dataset* [Data set]. Kaggle. https://www.kaggle.com/datasets/prasad22/healthcare-dataset
