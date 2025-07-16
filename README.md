# COVID-19 Forecast Platform

A web platform for forecasting COVID-19 cases and deaths, combining Machine Learning (LSTM, CNN-LSTM) models with a Django web backend and a front-end interface using Django templates.

This project simulates a real-world pipeline for ingesting COVID-19 data, training predictive models, and serving forecasts via a web interface.

---

## Features

- COVID-19 time series forecasting (cases, deaths, vaccinations)
- LSTM and CNN-LSTM models for univariate and multivariate prediction
- ETL pipeline to process historical datasets
- Django web backend for interaction and serving results
- Basic front-end interface with Django templates and JavaScript
- Database management and result storage

---

## Technologies Used

- Python 3.x
- Django
- TensorFlow / Keras
- NumPy / Pandas
- SQLite3 (for quick local storage)
- HTML5 / CSS3 / JavaScript (Front-end)

---

## Project Structure

| Folder/File               | Description |
|--------------------------|-------------|
| `covid_plataform/`        | Django backend and settings |
| `be_scripts/`             | Backend scripts (ETL, prediction, database management) |
| `be_scripts/training_models/` | Model training scripts (LSTM, CNN-LSTM) |
| `templates/cp_app/`       | Django HTML templates (front-end) |
| `fe_scripts/code.js`      | Front-end JavaScript logic |
| `db.sqlite3`              | Local SQLite database (for dev only) |
| `manage.py`               | Django management CLI |

---

## Models Implemented

- LSTM Univariate Model
- CNN-LSTM Univariate Model

These models forecast future COVID-19 cases based on historical data.

---

## How to Run

### 1. Clone the repository

```
git clone https://github.com/your-username/covid-forecast-platform.git
cd covid-forecast-platform
```

### 2. Install dependencies

```
pip install -r requirements.txt
```

### 3. Run Django server

```
python manage.py runserver
```

### 4. Run predictions / ETL (optional)

```
python be_scripts/main.py
```

---

## ETL and Data Processing

The ETL scripts:

- Download and process COVID-19 data
- Prepare datasets for model training
- Store predictions and historical data in `db.sqlite3`

---

## Front-end

This project includes a basic front-end implemented using **Django templates** and **JavaScript**.

### Templates

- `index.html` – Main page for interaction
- `history.html` – Display historical data
- `history_selection.html` – Select historical parameters
- `mode.html` – Choose model modes or configurations

### JavaScript

- `fe_scripts/code.js` – Handles front-end logic and interactions with the backend

### Next Steps

The current front-end is functional for basic interactions but can be expanded with:

- Better UI/UX design
- Real-time data visualizations (charts, graphs)
- Integration with Django REST APIs for decoupled front-end (optional)

---

## Code Organization

**Important:**  
This project is fully functional but requires **future code organization and refactoring**.

Currently, scripts are grouped by functionality but not fully modularized.  
Recommended next steps include:

- Splitting scripts into clear layers (API, ETL, ML models, utils)
- Creating services for prediction and data management
- Packaging the models and pipelines for easier maintenance
- Adding Docker and CI/CD pipelines
- Improving the front-end with REST API integration or advanced visualization

---
