# House_Price_Prediction
# 🏠 House Price Prediction

A **Machine Learning-based House Price Prediction System** that predicts the estimated price of a property in **Indian Lakhs (₹)** based on property details such as location, size, BHK, property type, furnishing status, nearby facilities, and other features.

The project includes data preprocessing, exploratory data analysis, categorical encoding, regression model training, model evaluation, and a **Streamlit web application** for making predictions.

## 🚀 Project Overview

The objective of this project is to develop a regression model that can predict house prices using property-related features.

Two regression models were explored during the experiment:

* Linear Regression
* Decision Tree Regressor

The final application uses a **Decision Tree Regressor** with a maximum depth of 10.

## ✨ Features

* 🏠 House price prediction
* 📍 State and city-based property information
* 🏢 Property type selection
* 🛏️ BHK and property size inputs
* 💰 Price per square foot
* 📅 Year built and property age
* 🛋️ Furnished / semi-furnished / unfurnished options
* 🏫 Nearby schools and hospitals
* 🚌 Public transport accessibility
* 🚗 Parking availability
* 🛡️ Security information
* 🌿 Amenities and property facing
* 👤 Owner type
* 📋 Availability status
* 📊 Interactive Streamlit interface
* 💵 Estimated price displayed in ₹ Lakhs

The Streamlit application accepts these property details and displays the predicted house price.

## 🧠 Machine Learning Workflow

```text
Dataset
   ↓
Exploratory Data Analysis
   ↓
Data Cleaning
   ↓
Feature Selection
   ↓
Ordinal Encoding
   ↓
Categorical Encoding
   ↓
Train-Test Split
   ↓
Model Training
   ↓
Model Evaluation
   ↓
Decision Tree Model
   ↓
Model Serialization
   ↓
Streamlit Web Application
   ↓
House Price Prediction
```

## 📊 Dataset Preprocessing

The dataset was preprocessed before training the models.

### Data Cleaning

* `ID` column was removed because it was not relevant to prediction.
* `Locality` column was removed because it did not provide meaningful address information.
* Categorical text values were converted to lowercase for consistency.

### Ordinal Encoding

The following categorical features were encoded using `OrdinalEncoder`:

* Property Type
* Furnished Status
* Public Transport Accessibility
* Facing
* Security

### Categorical Encoding

Remaining categorical variables were transformed using **DictVectorizer**.

To reduce training time on limited computing resources, a sample of **40% of the dataset** was used for model training and testing.

## 🤖 Models Used

### 1. Linear Regression

Linear Regression was implemented as a baseline regression model.

### 2. Decision Tree Regressor

A Decision Tree Regressor was used to capture non-linear relationships between property features and house prices.

The final application uses:

```text
DecisionTreeRegressor
random_state = 42
max_depth = 10
```

## 📈 Model Evaluation

The models were evaluated using:

* **MAE** — Mean Absolute Error
* **MSE** — Mean Squared Error
* **RMSE** — Root Mean Squared Error
* **R² Score** — Coefficient of Determination

These metrics were used to compare the performance of the regression models.

## 🖥️ Streamlit Application

The application provides an interactive interface where users enter property details and click **"Predict House Price"**.

The predicted value is displayed as:

```text
Estimated House Price
₹ XX.XX Lakhs
```

The application also provides an expandable section to view the entered input data.

## 🛠️ Technologies Used

* **Python**
* **Pandas**
* **NumPy**
* **Scikit-learn**
* **Streamlit**
* **Matplotlib**
* **Seaborn**
* **Pickle**

## 📁 Project Structure

```text
House-Price-Prediction/
│
├── app.py
├── E06_House Price Prediction.ipynb
├── E06_house price data less.csv
│
├── house_price_model.pkl
├── vectorizer.pkl
├── encoder.pkl
├── features.pkl
│
└── README.md
```

The Streamlit app loads the trained model, vectorizer, ordinal encoder, and feature information from pickle files.

## ⚙️ Installation

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/house-price-prediction.git
```

### 2. Open the Project

```bash
cd house-price-prediction
```

### 3. Install Required Libraries

```bash
pip install pandas numpy scikit-learn streamlit matplotlib seaborn
```

## ▶️ Run the Application

Start the Streamlit application using:

```bash
streamlit run app.py
```

The application will open in your browser.

## 📝 How to Use

1. Open the Streamlit application.
2. Select the **State**.
3. Enter the **City**.
4. Select the property type.
5. Enter BHK and property size.
6. Enter price per square foot.
7. Provide year built and property age.
8. Select furnishing status.
9. Enter nearby schools and hospitals.
10. Select transport accessibility.
11. Provide parking and security details.
12. Enter amenities, facing, owner type, and availability.
13. Click **Predict House Price**.
14. View the estimated house price in ₹ Lakhs.

## 🔐 Model Files

The application requires the following trained files:

```text
house_price_model.pkl
vectorizer.pkl
encoder.pkl
features.pkl
```

These files are generated during the model training process and are loaded by the Streamlit application using Python's `pickle` module.

## 📚 Project Notebook

The Jupyter Notebook contains:

* Dataset loading
* Exploratory Data Analysis
* Data preprocessing
* Feature encoding
* Train-test splitting
* Linear Regression
* Decision Tree Regression
* Model evaluation
* Model serialization

## 🎯 Objective

The main objective is to demonstrate how **Machine Learning regression techniques** can be applied to real-world property data to estimate house prices and deploy the trained model as an interactive web application.

## 🔮 Future Improvements

* Add more locations and cities
* Improve feature engineering
* Compare additional regression algorithms
* Perform hyperparameter tuning
* Add visualizations to the Streamlit dashboard
* Add model performance comparison
* Deploy the application online
* Improve prediction accuracy with a larger dataset

## 👩‍💻 Author

**UNDE RUTUJA MOTIRAM**

AI & Data Science Student

