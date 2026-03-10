# Solar Power Prediction Application

This project builds an **end-to-end machine learning pipeline** that predicts solar power generation using weather data and real-time weather forecasts.

The system processes historical weather data, trains a regression model, fetches live weather forecasts using a public API, and predicts future solar power output.

Location used for prediction: **Pune, Maharashtra, India**

---

# Project Overview

The project demonstrates:

- Data ingestion and preprocessing
- Feature engineering for time-series data
- Machine learning regression model training
- Real-time weather API integration
- Future solar power prediction
- Visualization of historical and predicted solar output

---

# Project Structure

SolarPowerPrediction
│
├── data
│ ├── solar_weather_dataset.csv
│ └── processed_solar_data.csv
│
├── notebooks
│ ├── dataset_generator.ipynb
│ ├── data_processing.ipynb
│ ├── model_training.ipynb
│ ├── weather_api.ipynb
│ └── final_prediction.ipynb
│
├── models
│ └── solar_model.pkl
│
├── outputs
│ ├── weather_forecast.csv
│ ├── solar_predictions.csv
│ └── solar_prediction_plot.png
│
├── requirements.txt
└── README.md


pip install -r requirements.txt


---

# Steps to Run the Project

### 1 Generate Dataset

Run:


dataset_generator.ipynb


This creates:


data/solar_weather_dataset.csv


---

### 2 Data Processing

Run:


data_processing.ipynb


This performs:

- timestamp parsing
- feature engineering
- cyclical time features
- rolling and lag features

Output:


data/processed_solar_data.csv


---

### 3 Train Machine Learning Model

Run:


model_training.ipynb


Model used:


RandomForestRegressor


Evaluation metrics:


MAE = (example value)
RMSE = (example value)
R² = (example value)


Trained model saved as:


models/solar_model.pkl


---

### 4 Weather API Integration

Weather forecast is fetched using:


OpenWeatherMap API


Location:


Pune, India
Latitude: 18.52
Longitude: 73.86


To run this step:

Add your API key inside:


weather_api.ipynb


Example:


API_KEY = "YOUR_API_KEY"


---

### 5 Solar Power Prediction

Run:


final_prediction.ipynb


This step:

- loads trained model
- processes weather forecast
- predicts solar output for next 24–48 hours

Output files:


outputs/solar_predictions.csv
outputs/solar_prediction_plot.png


---

# Visualization

The final output includes a time-series chart showing:

- historical solar output
- predicted solar output

Example output:

![Solar Prediction](outputs/solar_prediction_plot.png)

---

# Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Requests
- OpenWeatherMap API

---

# Author

Sheya Wagh