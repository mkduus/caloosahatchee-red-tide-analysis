# Predicting Harmful Algal Blooms (HABs) in Southwest Florida

This project uses environmental data and machine learning to explore the potential for predicting harmful algal blooms (HABs) along the Southwest Florida coast, with a focus on the Caloosahatchee River and Gulf of Mexico region.

## 📊 Data Sources

- **Nutrient data (TN, TP)** – Florida STORET / Water Atlas  
- **River discharge** – USGS site 02292900 (Caloosahatchee at S.R. 79)  
- **Sea Surface Temperature (SST)** – Copernicus Marine Service (NetCDF)  
- **Wind speed & direction, precipitation** – NOAA climate station near Fort Myers  
- **HAB observations** – NOAA HABSOS dataset (Karenia brevis concentrations)  

## 🛠️ Methods

- Time series cleaning and interpolation  
- Seasonal and geographic visualization using Cartopy  
- Outlier detection for TN/TP using IQR method  
- Feature engineering for monthly averages  

## 🧠 Machine Learning

- Binary classification (bloom vs. non-bloom)  
- Random Forest and Logistic Regression models  
- Model evaluation with confusion matrix, ROC-AUC, and precision-recall curves  
- Data leakage checks and retesting with corrected feature sets  

## 🔍 Findings

- Models performed well initially but were found to have data leakage via `HAB_Cells`  
- After correction, Random Forest achieved 73% accuracy but struggled to detect blooms  
- Logistic Regression performed better on bloom detection but had lower overall accuracy  
- ROC/PR curves confirmed modest predictive power from environmental features alone  

## 📁 Contents

- `REMApp_Data_ML.ipynb` – Main data processing and machine learning notebook  
- `REMApp_Visualization.ipynb` – Cartopy visualizations and site maps  
- `data/` – Cleaned and raw data sources (if included)  
- `README.md` – This file  

## 👥 Team

This project was completed as part of a course at [Your School/Department Name]  
Team members: [Add names here]
