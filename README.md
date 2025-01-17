# Flight Price Prediction

This project implements a **Machine Learning-based Flight Price Prediction model**. The goal of the project is to predict flight prices based on various input features such as airline, journey date, source, and destination. The model is trained using different algorithms, including **RandomForestRegressor**, **LinearRegression**, and **XGBoost**, and saved for deployment.

[Flight Price Prediction App - Live](https://flight-predictor-model.onrender.com/)

## Features

- **Flight Price Prediction**: Predict flight prices based on user input.
- **Machine Learning Models**: Built using algorithms like **RandomForestRegressor**, **SVR**, **LinearRegression**, and **XGBoost**.
- **Data Preprocessing**: Handles missing values, scales numerical features, encodes categorical variables, and extracts datetime features.
- **Model Training and Evaluation**: The model is trained, evaluated, and saved for deployment.

## Technologies Used

- **Python**: Programming language for model building and backend logic.
- **Scikit-learn**: For data preprocessing, model building, and evaluation.
- **XGBoost**: For gradient boosting.
- **Joblib**: For serializing the trained model.
- **Matplotlib**: For visualizing learning curves.
- **Flask**: For serving the model as an API.

## Data Preprocessing

The data undergoes various preprocessing steps:

- **Numerical Features**: Imputation for missing values and scaling using **StandardScaler**.
- **Categorical Features**: Imputation for missing values and encoding with **OneHotEncoder**.
- **Datetime Features**: Extracting components like day, month, and time of day, and scaling them.

## Model Training

The following models are trained:

1. **Linear Regression**: A simple linear model.
2. **Support Vector Regressor (SVR)**: A model based on support vector machines.
3. **Random Forest Regressor**: An ensemble learning method using random forests.
4. **XGBoost**: A gradient-boosting method for better performance.

The model training code is located in the `model_training.ipynb` notebook. Once trained, the model is serialized using **joblib**.


## Web Application

The web application is built using **Flask** to interact with the trained model. Users can input their flight details (such as airline, source, and destination), and the model predicts the flight price.

### How to Run the Web App

1. Clone this repository to your local machine:

```bash
git clone https://github.com/yourusername/flight-price-prediction.git
cd flight-price-prediction
```

2. Install the required dependencies:

```bash
pip install -r requirements.txt
```

3. Start the Flask web server:

```bash
python app.py
```

4. Navigate to `http://127.0.0.1:5000/` in your browser to use the flight price prediction web app.

## Model Deployment

The trained model (`model.joblib`) is loaded in the Flask app to make predictions. The `app.py` file serves as the API that accepts user input, loads the model, and returns the predicted flight price.

## Contributing

Feel free to fork this repository, submit issues, and contribute via pull requests. Contributions to improve the project are welcome!



