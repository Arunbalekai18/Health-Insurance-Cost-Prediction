# Health Insurance Charges Prediction

This project predicts medical insurance charges using machine learning models trained on the [insurance.csv](insurance.csv) dataset. The workflow includes data preprocessing, exploratory data analysis, feature engineering, model training, hyperparameter tuning, and deployment using FastAPI.

---

## Table of Contents

- [Project Structure](#project-structure)
- [Setup & Installation](#setup--installation)
- [Data Preprocessing](#data-preprocessing)
- [Modeling](#modeling)
- [API Usage](#api-usage)
- [Example Request](#example-request)
- [Notes](#notes)

---

## Project Structure

```
MEDICAL-INSURANCE-PREDICTION/
│
├── insurance.csv
├── medical.ipynb
├── app.py
├── model.pkl
├── templates/
│   └── index.html
└── README.md
```

---

## Setup & Installation

1. **Clone the repository** (if applicable) and navigate to the project directory:
    ```sh
    cd MEDICAL-INSURANCE-PREDICTION
    ```

2. **(Optional) Create and activate a virtual environment:**
    ```sh
    python -m venv .venv
    .venv\Scripts\activate
    ```

3. **Install dependencies:**
    ```sh
    pip install -r requirements.txt
    ```
    If `requirements.txt` is not present, install manually:
    ```sh
    pip install pandas numpy matplotlib seaborn scikit-learn xgboost feature_engine fastapi uvicorn jinja2
    ```

4. **Ensure `insurance.csv` is present in the project directory.**

---

## Data Preprocessing

- **Column Renaming:** Renames `sex` to `gender` for clarity.
- **Missing Values:** Checks and confirms no missing values.
- **Duplicates:** Removes duplicate rows.
- **Outlier Handling:** Caps outliers in the `bmi` column using the IQR method and `feature_engine`.
- **Encoding:** Encodes categorical variables:
    - `gender`: male=0, female=1
    - `smoker`: yes=1, no=0
    - `region`: northwest=0, northeast=1, southwest=2, southeast=3
- **Feature Selection:** Drops less important features based on model importance.

---

## Modeling

- **Models Used:**
    - Linear Regression
    - Support Vector Regression (SVR)
    - Random Forest Regressor (with GridSearchCV for hyperparameter tuning)
    - Gradient Boosting Regressor (with GridSearchCV)
    - XGBoost Regressor (with GridSearchCV)
- **Evaluation:** Uses R² score and cross-validation for model assessment.
- **Best Model:** The best-performing model is saved as `model.pkl` for deployment.

---

## API Usage

The project includes a FastAPI app (`app.py`) for serving predictions.

### **Run the API**

1. **Start the server:**
    ```sh
    uvicorn app:app --reload
    ```
    or
    ```sh
    python app.py
    ```

2. **Access the web interface:**  
   [http://127.0.0.1:8000/](http://127.0.0.1:8000/)

3. **API documentation:**  
   [http://127.0.0.1:8000/docs](http://127.0.0.1:8000/docs)

---

## Example Request

**POST** `/predict`

```json
{
  "age": 35,
  "sex": "male",
  "bmi": 28.5,
  "children": 2,
  "smoker": "no",
  "region": "northeast"
}
```

**Response:**
```json
{
  "predicted_charges": 12345.67
}
```

---

## Notes

- Ensure the input values for categorical fields (`sex`, `smoker`, `region`) match the expected values and case.
- The model expects the same preprocessing as used during training.
- The notebook (`medical.ipynb`) contains all data exploration, preprocessing, and model training steps for full reproducibility.

---

## License

This project is
