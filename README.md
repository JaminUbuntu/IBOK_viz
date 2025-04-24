7153CEM - Big Data Analytics and Data Visualisation

# 🏡 Predicting Property Prices in Perth Using Big Data Analytics

## 🔍 Overview

Accurate property price prediction is essential in today’s real estate-driven economy. This project uses Big Data tools like **PySpark** and **Tableau** to develop and evaluate predictive models for housing prices in **Perth, Australia**, spanning from 1988 to 2020.

Our approach leverages scalable data processing and multiple machine learning models to identify key property features impacting price. The outcomes inform real estate investors, urban planners, and policy makers while providing a reproducible pipeline for educational and professional use.

---

## 🧠 Project Objectives

- Develop a predictive model using Big Data techniques for real estate pricing.
- Compare regression models including **Linear Regression**, **GLR**, **XGBoost**, and **Random Forest**.
- Visualize insights using **Tableau dashboards**.
- Evaluate models using RMSE, R² Score, MAE, and residual analysis.
- Assess applicability in real-world housing and investment strategies.

---

## 🛠️ Technologies Used

- **Data Platform**: Apache Spark (PySpark)
- **Visualization**: Tableau
- **Languages**: Python (Pandas, NumPy), SQL
- **Machine Learning**: MLlib, XGBoost, Random Forest, GLR
- **Data Handling**: Seaborn, Matplotlib
- **Model Interpretability**: Statsmodels (OLS), Residual Plots, Cook’s Distance

---

## 📁 Dataset

The dataset was sourced from [Kaggle: Perth House Prices](https://www.kaggle.com/datasets/syuzai/perth-house-prices) and contains:

- **Rows**: 33,656
- **Columns**: 18 features including `BEDROOMS`, `BATHROOMS`, `FLOOR_AREA`, `CBD_DIST`, `PRICE`
- **Types**: Integer, Float, String
- **Time Range**: 1988–2020

This dataset includes spatial, temporal, structural, and socioeconomic indicators vital to property valuation.

---

## 🔬 Methodology

1. **Exploratory Data Analysis**: Heatmaps, KDEs, Boxplots
2. **Preprocessing**: Null removal, Feature transformations (e.g. `PROPERTY_AGE`)
3. **Feature Engineering**: Lag, Moving Average, Age Categorization
4. **Encoding**: Label and One-Hot Encoding for ML compatibility
5. **Model Training**: Regression models run on scaled numeric data using Spark ML pipelines
6. **Evaluation**: RMSE, MAE, R², Residual Distribution, OLS Summary
7. **Visualization**: Tableau dashboards for suburb-wise price trends and time-series plots

---

## 📈 Key Insights & Results

- **XGBoost** outperformed other models with an R² of **0.807** and lowest RMSE.
- Floor area and proximity to business districts strongly influence price.
- Visual trends reveal significant housing inflation post-2000 and spikes until 2020.
- Model interpretability via OLS and Cook’s Distance highlighted key features and outliers.

---

## 🧩 Real-World Applications

- **Real Estate Agencies**: Pricing models for client advisory and bidding
- **Urban Planners**: Demand forecasting for zoning and development
- **Financial Analysts**: Property valuation for mortgage approval
- **Educational Use**: Demonstrates practical machine learning for regression in a big data context

---

## 🔗 How to Leverage This Repository

1. Clone the repo:
   ```bash
   git clone https://github.com/JaminUbuntu/IBOK_viz.git
   ```
2. Open `PySpark_Code_Benjamin.ipynb` for full code.
3. Explore dashboards in the `tableau/` directory.
4. Use modular code for your own big data regression tasks.

---

## 🧭 Future Directions

- Integrate deep learning models (e.g. LSTM for time series).
- Apply SARIMA for seasonal price modeling.
- Expand to other cities for comparative insights.
- Build a Flask or Streamlit app for interactive predictions.

---

## 📚 Citation

> Ibok, B. (2024). *Predicting Property Prices in Perth Using Big Data Analytics*. Coventry University.

---

## 🎓 Academic Context

This project was submitted as part of the **7153CEM – Big Data Analytics and Data Visualisation** module at Coventry University. It meets the requirements for:
- Applied machine learning in Spark
- Real-world predictive modeling
- Reproducibility and ethical consideration

---

## 📬 Contact

**Author**: Benjamin Ibok  
**Institution**: Coventry University  
📧 Academic Email: [ibokb@coventry.ac.uk](mailto:ibokb@coventry.ac.uk)  
📧 Personal Email: [benjaminsibok@gmail.com](mailto:benjaminsibok@gmail.com)  

---

## ⚙️ Environment Setup

Tested on **Linux with Hadoop & PySpark**. Reproducible in Google Colab (recommended) and local Jupyter with the following setup:

```bash
pip install pyspark findspark statsmodels seaborn matplotlib
```

Ensure `JAVA_HOME` is configured.  
Requires Java 8+, Spark 3.x, and `all_perth_310121.csv` in `/data`.

---

## 📊 Visualizations & Model Evaluation

Visual outputs include:

- **Tableau dashboards** (Top suburbs, pricing trends)
- **Model comparison plots**
- **Residuals and OLS diagnostics**
- **Cook’s Distance for outlier detection**

<p align="center">
  <img src="images/dashboard1.png" width="600"/>
</p>

---

## 🤝 Contribution Guidelines

We welcome PRs and feature suggestions!

1. Fork the repo  
2. Create your branch `feature/amazing-feature`  
3. Commit with meaningful messages  
4. Push & Submit PR

---

## 💾 Model Inference

Use trained models from the pipeline or persist with:

```python
from joblib import dump, load
dump(model, "models/xgboost_model.joblib")
model = load("models/xgboost_model.joblib")
```

For Spark:
```python
model.save("models/spark_model")
```

---

## 🏷️ Project Badges

![Python](https://img.shields.io/badge/python-3.8+-blue.svg)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)
![Platform: Spark](https://img.shields.io/badge/platform-Apache%20Spark-orange.svg)
![Status: Completed](https://img.shields.io/badge/status-complete-brightgreen.svg)

---

## ❓ FAQ / Known Issues

**Q: Where can I find the dataset?**  
A: [Kaggle – Perth House Prices](https://www.kaggle.com/datasets/syuzai/perth-house-prices)

**Q: What is the best model?**  
A: XGBoost performed best with ~81% variance explanation.

**Q: Can this be used outside Perth?**  
A: Yes, the pipeline is generalizable with slight modifications to the feature set.
