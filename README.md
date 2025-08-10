# Happiness Predictor Web Application
A lightweight, interactive web application built using Flask and scikit-learn that predicts an individual's happiness score based on their income. This app uses a simple Linear Regression model and is fully deployable on Render.

✨ Features
🔍 Predict happiness based on income

🧠 Machine Learning model built with scikit-learn

🌐 Frontend using HTML and CSS

⚙️ Backend powered by Flask

☁️ Cloud deployment ready (Render-compatible)

📁 Project Structure
php
Copy code
happiness-predictor/
│
├── app.py                 # Main Flask application  
├── model.pkl              # Pre-trained Linear Regression model  
├── requirements.txt       # Python dependencies  
├── render.yaml            # Deployment config for Render  
│
├── templates/  
│   └── index.html         # Frontend HTML  
│
└── static/  
    └── style.css          # CSS styling  
⚙️ Getting Started
Follow these steps to run the project locally:

Clone the Repository

bash
Copy code
git clone https://github.com/yourusername/happiness-predictor.git
cd happiness-predictor
Set Up Virtual Environment

bash
Copy code
python -m venv venv
# Windows
venv\Scripts\activate
# macOS/Linux
source venv/bin/activate
Install Dependencies

bash
Copy code
pip install -r requirements.txt
Run the Application

bash
Copy code
python app.py
Open your browser and go to http://127.0.0.1:5000 to use the app.

🧠 Model Overview
This app uses a simple Linear Regression model trained on synthetic data to predict happiness scores from income.

☁️ Deployment on Render
Create a render.yaml file with the following content:

yaml
Copy code
services:
  - type: web
    name: happiness-predictor
    env: python
    buildCommand: ""
    startCommand: gunicorn app:app
    plan: free
    region: oregon
Push your project to GitHub.

Go to Render, create a new web service, and connect your GitHub repo.

Set the Start Command as:

nginx
Copy code
gunicorn app:app
Render will automatically build and deploy your app.

✅ Requirements
Your requirements.txt should include:

ini
Copy code
Flask==2.3.3
gunicorn==21.2.0
scikit-learn==1.4.2
numpy==1.26.4

