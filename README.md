# Big Data Analysis with PySpark – World Bank Indicators

This repository contains the full submission for my Big Data Analysis coursework project at UCL. The project uses PySpark and Spark MLlib to analyze the World Bank’s World Development Indicators dataset (1960–2022), exploring development tiers, short-term forecasting, and the drivers of income inequality.

---

## 📂 Repository Structure

## Project Structure

```
big_data_pyspark/
├── notebook/
│ └── BDA.ipynb # PySpark notebook (Component 2)
├── report/
│ └── big-data.pdf # Combined topic proposal + summary (Components 1 & 3)
├── README.md # Project overview
├── requirements.txt # Python dependencies
└── .gitignore
```

## Project Overview

### Goal

To demonstrate an end-to-end distributed data pipeline using PySpark and HDFS-compatible workflows, while exploring global development patterns across countries and time.

### Analyses Included

- **Clustering (K-Means):** Segment countries by 2020 indicators into development tiers  
- **Forecasting (Linear Regression):** Predict GDP and life expectancy using lag-1 models  
- **Inequality Modeling (ElasticNet):** Identify key predictors of the Gini index

## Dataset

- **Source:** World Bank World Development Indicators  
- **Accessed via:** [Kaggle Dataset](https://www.kaggle.com/datasets/nicolasgonzalezmunoz/world-bank-world-development-indicators)  
- The dataset includes 268 countries, 63 years, and 48 indicators covering economy, health, governance, infrastructure, and inequality.

## Submission Components 

***Component 1:*** Topic Proposal and planned analysis -- see 'report/big-data.pdf'
***Component 2:*** Full PySpark notebook -- see 'notebook/BDA.ipynb'
***Component 3:*** Summary and conclusions -- included in 'big-data.pdf'

## Dataset 
- Source: World Bank World Development Indicators via Kaggle
- Years: 1960-2022
- Countries: 268
- Format: CSV
- Size: ~2MB (raw)

The dataset includes 48 numerical indicators across economic, social, infrastructure, and governance domains 

## ✅ Summary of Results

### 📊 Clustering
- **Optimal number of clusters:** K = 2  
- **Silhouette score:** 0.7363  
- **Cluster 0 (high development):** GDP ≈ 10¹³, life expectancy ≈ 76.8 years  
- **Cluster 1 (lower development):** GDP ≈ 2.85×10¹⁰, life expectancy ≈ 66.1 years  

### 📈 Forecasting

**GDP (Lag-1) model**  
- RMSE ≈ 12.2 billion  
- R² = 0.998  

**Life Expectancy (Lag-1) model**  
- RMSE ≈ 1.33 years  
- R² = 0.951  

### 🧮 Inequality Modeling

**ElasticNet Regression (5 predictors)**  
- RMSE ≈ 6.52 Gini points  
- R² = 0.154  

**Top features:** internet usage, rule of law, corruption control, education, and health spending  

---

## 📚 References

- World Bank Data Catalog – World Development Indicators  
- Nicolás A. González Muñoz (Kaggle Dataset Publisher)  
- Apache Spark & PySpark MLlib Documentation  
- Pedregosa et al. (2011). *Scikit-learn: Machine Learning in Python*. JMLR  
- Zaharia et al. (2016). *Apache Spark: A Unified Engine for Big Data Processing*. CACM  
- Tibshirani, R. (1996). *Regression Shrinkage and Selection via the Lasso*

---

## 🙏 Acknowledgements

- UCL Big Data Analysis course team  
- Apache Spark open-source contributors  
- Nicolás A. González Muñoz for packaging the World Bank dataset on Kaggle

---

## 📎 License

This project is for academic purposes only.


