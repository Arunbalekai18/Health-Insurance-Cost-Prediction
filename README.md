# Health Insurance Prediction API

This project is a FastAPI-based web application that predicts medical insurance charges based on user input. The prediction is powered by a machine learning model (`model.pkl`) trained on insurance data.

## Features

- REST API for predicting insurance charges
- Web interface using Jinja2 templates
- CORS enabled for cross-origin requests

## Requirements

- Python 3.8+
- pip

## Setup

1. **Clone the repository** (if applicable) and navigate to the project directory:
    ```
    cd C:\Users\arunb\MEDICAL-INSURANCE-PREDICTION
    ```

2. **(Optional) Create and activate a virtual environment:**
    ```
    python -m venv .venv
    .venv\Scripts\activate
    ```

3. **Install dependencies:**
    ```
    pip install fastapi uvicorn jinja2 pydantic numpy pandas scikit-learn xgboost
    ```

4. **Ensure `model.pkl` is present in the project directory.**  
   If not, train your model and save it as `model.pkl`.

5. **Ensure you have a `templates` folder with `index.html` inside.**

## Running the App

### Using Uvicorn (recommended)
```
uvicorn app:app --reload
```

### Or using Python directly
```
python app.py
```

## API Endpoints

- **GET /**  
  Returns the home page.

- **POST /predict**  
  Accepts JSON input:
  ```json
  {
    "age": 25,
    "sex": "Male",
    "bmi": 28.5,
    "children": 2,
    "smoker": "No",
    "region": "Northeast"
  }
  ```
  Returns:
  ```json
  {
    "predicted_charges": 12345.67
  }
  ```

## Testing

Visit [http://127.0.0.1:8000/docs](http://127.0.0.1:8000/docs) for interactive API documentation.

## Notes

- Make sure the input values for `sex`, `smoker`, and `region` match the expected case and spelling.
- The model expects the same preprocessing as used during training.

---
```# Medical Insurance Prediction API

This project is a FastAPI-based web application that predicts medical insurance charges based on user input. The prediction is powered by a machine learning model (`model.pkl`) trained on insurance data.

## Features

- REST API for predicting insurance charges
- Web interface using Jinja2 templates
- CORS enabled for cross-origin requests

## Requirements

- Python 3.8+
- pip

## Setup

1. **Clone the repository** (if applicable) and navigate to the project directory:
    ```
    cd C:\Users\arunb\MEDICAL-INSURANCE-PREDICTION
    ```

2. **(Optional) Create and activate a virtual environment:**
    ```
    python -m venv .venv
    .venv\Scripts\activate
    ```

3. **Install dependencies:**
    ```
    pip install fastapi uvicorn jinja2 pydantic numpy pandas scikit-learn xgboost
    ```

4. **Ensure `model.pkl` is present in the project directory.**  
   If not, train your model and save it as `model.pkl`.

5. **Ensure you have a `templates` folder with `index.html` inside.**

## Running the App

### Using Uvicorn (recommended)
```
uvicorn app:app --reload
```

### Or using Python directly
```
python app.py
```

## API Endpoints

- **GET /**  
  Returns the home page.

- **POST /predict**  
  Accepts JSON input:
  ```json
  {
    "age": 25,
    "sex": "Male",
    "bmi": 28.5,
    "children": 2,
    "smoker": "No",
    "region": "Northeast"
  }
  ```
  Returns:
  ```json
  {
    "predicted_charges": 12345.67
  }
  ```

## Testing

Visit [http://127.0.0.1:8000/docs](http://127.0.0.1:8000/docs) for interactive API documentation.

## Notes

- Make sure the input values for `sex`, `smoker`, and `region` match the expected case and spelling.
- The model expects the same preprocessing as
