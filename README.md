# Optimizing Medication Inventory Management

## Project Overview
This project was completed as our Capstone Project for the Master of Applied Data Science program at the University of Michigan.  Our project aims to optimize medication inventory management by leveraging historical data from the University of Michigan Medicine Pharmacy Administration to predict pharmaceutical demand. Our project’s goal is to reduce medication waste that would help lower costs and ensure that patients have access to the medications they need when they need them.

## Data Source
The primary data source is the “Medication Inventory Management Dataset” shared by the Pharmacy Manager of U-M: Michigan Medicine - Pharmacy Administration. The dataset contains historical medication inventory and transaction data, covering 3 hospitals, 40 outpatient locations, and over 120 clinics from February 2022 to June 2024. It includes detailed information on inventory levels, transactions (picks, restocks, wastes, etc.), medication details, locations and so on. **Due to the proprietary nature of this dataset, it is not included in our GitHub repository.**

## Packages Used
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- SciPy
- Darts

## Data Pipelines
- **01_data_cleaning_and_preprocessing.ipynb** - This notebook reads in the raw, medication-level, time-series data for each item of inventory. Medication IDs are standardized and missing and/or inconsistent inventory min./max. thresholds are estimated. The data is exported for subsequent use in our demand forecasting model. Additionally, a medication-level dataset is created containing aggregate statistics for each Medication ID. This dataset is used for subsequent analysis in 02_anomaly_detection_and_clustering.
- **02_anomaly_detection_and_clustering.ipynb** - This notebook reads in the aggregate, medication-level data and uses an Isolation Forest to identify the features most relevant in the process of detecting anomalies. A second Isolation Forest is then constructed to identify and remove anomalies from the aggregate dataset. The residual data is then run through a KMeans clustering model to group medications with similar demand signals.
- **03_demand_forecasting.ipynb** - 

## Team Information
Contributors
Ejaz Alam (ejazalam@umich.edu)
Vanessa Scalora (vscalora@umich.edu)
Kevin Steidler (ksteid@umich.edu)

Project Link: https://github.com/nblakkanesser/MADS_Capstone.git
