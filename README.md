
# ✈️ Flight Price Prediction: Exploratory Data Analysis (EDA) & Feature Engineering

This project focuses on preparing flight price data for machine learning modeling. It involves **deep exploratory data analysis**, **data cleaning**, and **feature engineering** on a real-world flight dataset. The final aim is to develop insights and create a refined dataset that can be used to build predictive models for **estimating flight ticket prices**.

---

## 📌 Objective

- Understand the key factors that influence flight ticket prices.
- Clean and preprocess raw data into a machine-readable format.
- Perform EDA to derive meaningful patterns and insights.
- Create new features to enhance model performance.
- Set up a strong foundation for building regression models in future steps.

---

## 📁 File Structure

```bash
📂 flight-price-prediction/
│
├── 2.0-EDA And FE Flight Price.ipynb   # Main Jupyter Notebook
├── README.md                           # Project Documentation
├── data/                               # (Optional) Store original/raw datasets
└── output/                             # (Optional) Store processed/cleaned datasets
```

---

## 📊 Dataset Overview

The dataset contains various features that describe a flight, such as:

- **Date_of_Journey**: When the journey starts
- **Airline**: Airline carrier
- **Source / Destination**: Cities of departure and arrival
- **Route**: The path taken
- **Dep_Time / Arrival_Time**: Departure and arrival time
- **Duration**: Total flight time
- **Total_Stops**: Number of stops
- **Additional_Info**: Miscellaneous info
- **Price**: Target variable

---

## 🔍 Step-by-Step Process

### ✅ 1. Data Loading and Exploration
- Load the dataset using `pandas`.
- Understand the shape, types, and null values.
- Identify inconsistencies and anomalies in the raw data.

### 🧹 2. Data Cleaning
- Convert `Date_of_Journey`, `Dep_Time`, and `Arrival_Time` to datetime objects.
- Remove or impute missing values from `Route` and `Total_Stops`.
- Standardize `Duration` by converting it into total hours and minutes.

### 🏗️ 3. Feature Engineering
New features created for better prediction include:
- **Journey_Day**, **Journey_Month**
- **Dep_Hour**, **Dep_Minute**
- **Arrival_Hour**, **Arrival_Minute**
- **Duration_Hour**, **Duration_Minute**
- **Encoded categorical variables** for `Airline`, `Source`, `Destination`, etc.

Techniques used:
- **Label Encoding** for ordinal features
- **OneHotEncoding** for nominal features using `sklearn.preprocessing`

### 📈 4. Exploratory Data Analysis (EDA)
Insights were derived using:
- **Distribution plots** for Price and Duration
- **Count plots** for Airline, Stops, and Route
- **Boxplots** to identify outliers in price
- **Correlation heatmaps** to identify relationships among numerical variables

### 📌 5. Final Output
A clean, preprocessed dataset ready for use in machine learning models for **regression-based price prediction**.

---

## 🧠 Insights & Observations

- **Airline** plays a significant role in price differences.
- **Flight duration** does not always correlate linearly with price.
- **Midnight or early morning flights** tend to be cheaper in some cases.
- **Number of stops** significantly affects both price and duration.
- Some features like `Additional_Info` have little to no variance.

---

## 🧰 Tools & Libraries Used

| Library        | Purpose                         |
|----------------|----------------------------------|
| `pandas`       | Data manipulation                |
| `numpy`        | Numerical operations             |
| `matplotlib`   | Visualization                    |
| `seaborn`      | Statistical graphics             |
| `sklearn`      | Encoding and preprocessing       |
| `datetime`     | Handling time-based columns      |

---

## 📊 Future Roadmap

- Train Regression Models: Linear Regression, Random Forest, XGBoost
- Evaluate Model Metrics: RMSE, MAE, R² Score
- Use GridSearchCV or RandomizedSearchCV for hyperparameter tuning
- Export the best model using `joblib` or `pickle`
- Deploy using a Flask/Streamlit web interface or via REST API

---

## 📌 Use Case

The insights and models from this project can be used by:
- **Online travel agencies (OTAs)** to optimize pricing
- **Consumers** for price prediction and alerts
- **Airlines** for dynamic pricing strategies

---

## 🙋 Author

**Anuj Agarwal**  
*Data Analyst Intern @ Visao.io*  
📍 Noida, Uttar Pradesh  

---

## 📢 Acknowledgements

- Thanks to Kaggle for providing the original dataset.
- Inspired by various public solutions and notebooks on flight price prediction.
