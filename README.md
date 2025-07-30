# IPL scoreprediction
A machine learning-based model to predict IPL cricket scores for the first innings using historical match data and live match features. Built with Python, deployed via Flask.

## 🧠 Project Overview

This project aims to **predict the first-innings score** of an IPL match based on match conditions and historical data. It leverages regression techniques to forecast a score range rather than an exact value, improving robustness.

## 📋 Features

- Historical IPL dataset (2008–present) including:
  - **Venue**, **batting team**, **bowling team**
  - Recent performance: **runs and wickets in previous 5 overs**
  - Match conditions (e.g., overs completed, wickets currently down)
- Preprocessing:
  - Label encoding for categorical variables
  - Feature engineering and scaling
- Model: Trained regression algorithm (e.g. Random Forest or Gradient Boosting)
- Prediction output: Estimated score ± tolerance (e.g., ±10 runs)

## 🛠️ Installation & Setup

1. **Clone the repository**  
   ```bash
   git clone https://github.com/dheerajraqesh/ipl_scoreprediction_dheeraj.git
   cd ipl_scoreprediction_dheeraj
Install dependencies
pip install -r requirements.txt
Place the IPL dataset (e.g. ipl_dataset.csv) in the project folder if not included.
Run the app
python app.py
This will start a Flask app served at http://127.0.0.1:5000/.
🚀 How It Works

Data Preprocessing: handles missing values, encodes categorical features, computes rolling stats (e.g. last 5 overs).
Training & Prediction: loads pre-trained regression model (model.pkl) to predict the score based on user inputs.
Inference: displays a projected score range (e.g. predicted_score ± 10). 
