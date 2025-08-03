# 🏥 Health Insurance Cost Prediction Using Machine Learning

This project predicts **medical insurance costs** based on user-provided features such as age, gender, BMI, smoking habits, number of children, and region. It uses a **Random Forest Regressor** model to provide accurate cost estimations. The goal is to help insurance companies price policies efficiently and assist users in understanding the impact of their lifestyle choices on insurance charges.

---

## 📌 Features

- 🚀 Predict insurance costs in real-time via a web interface
- 📊 Machine Learning model trained using Random Forest Regressor
- ⚡ FastAPI backend for quick and scalable APIs
- 🌐 Simple and responsive web UI with HTML and CSS
- 💾 Model serialized with Pickle for efficient reuse

---

## 🛠️ Tools and Technologies Used

| Category         | Tools/Frameworks                     |
|------------------|--------------------------------------|
| Programming      | Python                               |
| Web Framework    | FastAPI, HTML, CSS, Jinja2           |
| Machine Learning | scikit-learn (RandomForestRegressor) |
| Data Handling    | Pandas, NumPy                        |
| Deployment       | Uvicorn (local server)               |
| Serialization    | Pickle                               |
| Version Control  | Git, GitHub                          |

---

## 🔍 How It Works

1. **User Input**: User provides inputs like age, sex, BMI, children, smoker status, and region via a web form.
2. **Model Prediction**: These values are passed to the trained RandomForest model.
3. **Output**: Predicted insurance cost is displayed on the webpage.

---

## 🧠 Machine Learning Workflow

- **Dataset**: `insurance.csv` containing real-world health insurance data.
- **Preprocessing**: Label encoding of categorical features.
- **Model**: RandomForestRegressor
- **Evaluation**: Trained model was evaluated using metrics like MAE, MSE, RMSE.
- **Serialization**: Final model was saved using `pickle` for API use.

---

## 🚀 Running the Project Locally

### 1. Clone the repo
```bash
git clone https://github.com/Arunbalekai18/Health-Insurance-Cost-Prediction.git
cd Health-Insurance-Cost-Prediction
 Create and activate virtual environment
bash
Copy
Edit
python -m venv .venv
# Windows
.venv\Scripts\activate
# Linux/macOS
source .venv/bin/activate
3. Install dependencies
bash
Copy
Edit
pip install -r requirements.txt
4. Run the app
bash
Copy
Edit
uvicorn app:app --reload
5. Open in browser
Visit http://127.0.0.1:8000 to use the app.

📷 Screenshots
Add screenshots of your UI here to make the README more visual and attractive.

📝 Future Improvements
Add feature importance visualization

Add user authentication

Deploy on platforms like Heroku or Render

