# House Price Prediction – Machine Learning Project

## Objective

The goal of this project is to build a **machine learning regression model** that predicts house prices based on features such as area, number of bedrooms, bathrooms, stories, parking, and other property attributes.

This project demonstrates the **complete machine learning workflow**, including data preprocessing, feature engineering, model training, evaluation, and prediction.

---

## Dataset

Dataset Source: Kaggle

House Price Prediction Dataset

The dataset contains housing information such as:

* Area
* Bedrooms
* Bathrooms
* Stories
* Parking
* Main road access
* Guest room availability
* Basement availability
* Air conditioning
* Furnishing status
* House price

---

## Tools and Libraries

This project uses the following Python libraries:

* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Seaborn
* Joblib

Notebook environment: Google Colab

---

## Project Workflow

### 1. Data Exploration (EDA)

Exploratory Data Analysis was performed to understand the dataset:

* Dataset structure using `info()` and `describe()`
* Missing value analysis
* Price distribution visualization
* Correlation heatmap between numerical features
* Scatter plots to observe feature relationships

---

### 2. Feature Engineering

Several preprocessing steps were applied:

* Log transformation of house prices to normalize distribution
* Encoding categorical variables using one-hot encoding
* Feature scaling using StandardScaler

---

### 3. Models Implemented

Three regression algorithms were trained and compared:

* Linear Regression
* Random Forest Regressor
* Gradient Boosting Regressor

---

### 4. Model Evaluation

Models were evaluated using regression metrics:

* RMSE (Root Mean Squared Error)
* MAE (Mean Absolute Error)

Residual analysis was also performed to check prediction errors.

---

## Best Model

Random Forest Regressor provided the best performance among the tested models.

The trained model was saved using **joblib** for future predictions.

Saved model file:

house_price_model.pkl

---

## Example Prediction

Example code to load the trained model and make a prediction:

```python
import joblib
import numpy as np

model = joblib.load("house_price_model.pkl")

sample_house = np.array([[3000,3,2,2,1,0]])

prediction = model.predict(sample_house)

print("Predicted Price:", prediction)
```

If log transformation was used:

```python
import numpy as np
print("Predicted Price:", np.exp(prediction))
```

---

## Repository Structure

house-price-prediction
│
├── House_Price_Prediction.ipynb
├── house_price_model.pkl
├── README.md
└── dataset.csv

---

## How to Run the Project

1. Open the notebook in Google Colab
2. Install required libraries
3. Run all notebook cells
4. Load the saved model
5. Provide input features to predict house price

---

## Conclusion

This project demonstrates how machine learning can be used to estimate house prices using property features. The workflow includes data preprocessing, model comparison, evaluation metrics, and model deployment-ready artifacts.
