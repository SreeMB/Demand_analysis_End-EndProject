
# Bike Rental Demand Prediction System

## Overview
This project is a **machine learning-based system** designed to predict the daily count of bikes rented based on various parameters such as weather, temperature, humidity, and seasonality. The system includes data preprocessing, model training, and deployment via APIs and a web interface. It demonstrates end-to-end development skills, including machine learning, API development, and web application deployment.

---

## Features
- **Data Preprocessing**:  
  - Perform feature engineering, including scaling numeric features (`temp`, `humidity`, etc.) and encoding categorical features (`season`, `weather`, etc.).  

- **Machine Learning Models**:  
  - Experimented with multiple models, including **XGBoost**, **Random Forest**, and **CatBoost**, to achieve the best predictive performance.  
  - Built **modular data pipelines** using `scikit-learn` for preprocessing and model training.  

- **API Development**:  
  - Developed a **RESTful API** using **Flask** to serve predictions.  
  - Implemented input validation using `pydantic` for robust error handling.  

- **Web Interface**:  
  - Created an interactive web application using **Streamlit** for users to input parameters and view predictions in real-time.  
  - Integrated the Flask API with the Streamlit app for dynamic results.  

---

## Technologies Used
- **Programming Language**: Python  
- **Libraries**: `pandas`, `scikit-learn`, `Flask`, `Streamlit`, `XGBoost`, `CatBoost` 
- **Machine Learning Models**: XGBoost, Random Forest, CatBoost  

---


## Usage
- **API**: Send a POST request to the Flask API (`/predict`) with input parameters (e.g., `temp`, `humidity`, `weather`) to get the predicted bike rental count.  
- **Web Interface**: Use the Streamlit app to input parameters and view predictions in real-time.  

---

## Example API Request
```bash
curl -X POST "http://127.0.0.1:5000/predict" \
-H "Content-Type: application/json" \
-d '{
  "datetime": "2023-10-01 00:00:00",
  "season": 3,
  "holiday": 0,
  "workingday": 1,
  "weather": 1,
  "temp": 25.0,
  "atemp": 28.0,
  "humidity": 50,
  "windspeed": 10.0
}'
```

---

## Results
- Achieved high accuracy in predicting bike rental counts using different ML models.  
- Delivered a scalable and modular solution for bike rental demand prediction.  

