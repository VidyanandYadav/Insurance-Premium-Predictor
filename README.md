# 🏥 Insurance Premium Category Predictor

A machine learning web application that predicts an individual's insurance premium category based on personal, financial, lifestyle, and demographic information.

The application uses a trained machine learning model served through a **FastAPI backend** and provides an interactive user interface built with **Streamlit**.

## 🚀 Features

* Predicts insurance premium categories: **Low, Medium, and High**.
* Accepts user information through an interactive web interface.
* Uses BMI and lifestyle-related information as prediction features.
* Provides a REST API for making predictions.
* Separates the backend API from the frontend interface.
* Uses a trained machine learning model for classification.

## 🛠️ Technologies Used

* **Python**
* **FastAPI** — Backend API
* **Streamlit** — Frontend interface
* **Scikit-learn** — Machine learning
* **Pandas** — Data processing
* **NumPy** — Numerical computing
* **Pydantic** — Input validation
* **Requests** — API communication

## 📁 Project Structure

```text
Insurance-Premium-Predictor/
│
├── app.py
├── frontend.py
├── model.pkl
├── requirements.txt
├── README.md
└── .gitignore
```

## ⚙️ Installation and Setup

### 1. Clone the repository

```bash
git clone YOUR_REPOSITORY_URL
cd Insurance-Premium-Predictor
```

Replace `YOUR_REPOSITORY_URL` with your GitHub repository URL.

### 2. Create a virtual environment

```bash
python -m venv venv
```

Activate it on Windows PowerShell:

```powershell
.\venv\Scripts\Activate.ps1
```

### 3. Install dependencies

```bash
python -m pip install -r requirements.txt
```

**Note:** The saved model was created using scikit-learn 1.5.1. Keep this version consistent when loading the model.

## ▶️ Run the Application

The application requires the backend and frontend to run in separate terminals.

### Terminal 1: Start the FastAPI backend

```bash
python -m uvicorn app:app --host 127.0.0.1 --port 8000
```

The API will be available at:

`http://127.0.0.1:8000`

Interactive API documentation:

`http://127.0.0.1:8000/docs`

### Terminal 2: Start the Streamlit frontend

```bash
python -m streamlit run frontend.py
```

Open the local URL displayed in the terminal, usually:

`http://localhost:8501`

## 🔌 API Endpoint

**Endpoint:** `POST /predict`

The endpoint accepts user information, processes the input, and returns a predicted insurance premium category.

Example response:

```json
{
  "predicted_category": "Low"
}
```

The predicted category may be **Low, Medium, or High**, depending on the input and the trained model.

## 🧠 Machine Learning

The application uses a trained scikit-learn classification pipeline saved as `model.pkl`.

The prediction pipeline uses features including:

* BMI
* Age group
* Lifestyle risk
* City tier
* Annual income in lakhs
* Occupation

The backend validates user input, prepares the features required by the model, and returns the predicted category.

## ⚠️ Disclaimer

This project is intended for educational and demonstration purposes. Predictions are model-generated estimates and should not be treated as official insurance quotes or financial advice.

## 👨‍💻 Author

**Vidyanand Yadav**

GitHub: [VidyanandYadav](https://github.com/VidyanandYadav)
