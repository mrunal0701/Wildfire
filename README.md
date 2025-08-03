# wildfire-prediction
# 🔥 Wildfire Risk Prediction System

A Machine Learning-powered web application that predicts the risk of wildfire based on environmental factors like DC (Drought Code), temperature, and month indicators. It provides geolocation tagging, interactive visualization, and a real-time map of predicted wildfire risks.

## 🚀 Features

- 🌲 **Home Page with Informative Cards** – Learn about wildfires, their causes, and how our model works.
- 📊 **Prediction System** – Predict fire risk using environmental inputs.
- 🗺️ **Geolocation-Based Tracking** – Get the user's location when predicting.
- 🧠 **ML Model (KNN)** – A trained K-Nearest Neighbors classifier used for risk classification.
- 🗂️ **SQLite Database** – Store user input, prediction, and location.
- 📍 **Map Visualization** – View all predicted wildfire locations on a map.
- 📈 **Data Page** – Displays a table of historical predictions.

## 🧪 Tech Stack

| Layer        | Technology            |
|--------------|------------------------|
| Frontend     | HTML, CSS, JavaScript  |
| Backend      | Flask (Python)         |
| Database     | SQLite                 |
| ML Model     | K-Nearest Neighbors    |
| Visualization| Leaflet.js, Charts.js  |

## 📂 Project Structure

project-root/
│
├── backend/
│ ├── app.py
│ ├── knn_model.pkl
│ ├── knn_scaler.pkl
│ ├── selected_features.pkl
│ └── wildfire_data.db
│
├── frontend/
│ ├── home.html
│ ├── index.html
│ ├── map.html
│ ├── about.html
│ ├── indicators.html
│ ├── model.html
│ ├── data.html
│ └── static/
│ ├── home.css
│ ├── index.css
│ ├── map.css
│ └── scripts/
│ └── script.js
│
└── README.md

markdown
Copy
Edit

## 📌 How It Works

1. **User inputs** values for DC, temperature, and month indicators.
2. **Geolocation** is automatically fetched using browser API.
3. The **Flask backend** processes the input, scales it, and makes a prediction using the trained KNN model.
4. The **result** is displayed on the same page along with a link to view data on a map.
5. The prediction and coordinates are stored in **SQLite**.
6. Users can browse **historical data** and **map** visualizations.

## 🧠 ML Model

- **Model**: K-Nearest Neighbors (KNN)
- **Trained on**: Preprocessed wildfire dataset
- **Features Used**:
  - Drought Code (DC)
  - Temperature
  - Month (December, March as binary indicators)
- **Tools**: `scikit-learn`, `joblib`, `pandas`, `numpy`

## 💾 Setup Instructions

 1. Clone the Repository
git clone https://github.com/your-username/wildfire-predictor.git
cd wildfire-predictor
2. Install Python Dependencies
bash
Copy
Edit
pip install -r requirements.txt
Example requirements.txt:

text
Copy
Edit
Flask==2.3.2
scikit-learn
numpy
pandas
joblib
3. Run the App
bash
Copy
Edit
cd backend
python app.py
Open your browser and go to http://127.0.0.1:5000
