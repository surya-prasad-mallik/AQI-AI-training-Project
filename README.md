# Air Quality Index (AQI) Prediction

A Python machine-learning project for exploring air-quality data and predicting AQI using regression models. The repository includes a Jupyter notebook for analysis and a Streamlit app for interactive experiments.

## Features

- Load and inspect city-level air-quality data
- Clean rows with missing values for the selected model features
- Choose a city or use all available cities
- Select pollutant features and a train/test split
- Train and compare Linear Regression, K-Nearest Neighbors, Decision Tree, and Random Forest regressors
- Review evaluation metrics including MAE, MSE, and R²
- Explore the data through a Streamlit dashboard

## Tech stack

- Python
- Pandas and NumPy
- Matplotlib
- scikit-learn
- Streamlit
- Jupyter Notebook

## Project files

- `app.py` — interactive Streamlit dashboard
- `AIR_QUALITY_PREDECTION.ipynb` — notebook for the analysis and modelling workflow
- `1772272102861_city_day.csv` — dataset used by the app (if included in this repository)
- `requirements.txt` — Python dependencies

## Run locally

### 1. Clone the repository

```bash
git clone https://github.com/surya-prasad-mallik/AQI-AI-training-Project.git
cd AQI-AI-training-Project
```

### 2. Create and activate a virtual environment

Windows PowerShell:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

macOS/Linux:

```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 3. Install dependencies

```bash
python -m pip install --upgrade pip
pip install -r requirements.txt
```

### 4. Start the dashboard

```bash
streamlit run app.py
```

Open the local URL printed by Streamlit (usually http://localhost:8501).

The app expects the dataset file named `1772272102861_city_day.csv` in the project root. If it is missing, the app offers a CSV upload option. Use a compatible dataset containing an `AQI` target column and the pollutant columns you want to select.

## Modelling workflow

1. Load the dataset and choose a city.
2. Select pollutant columns as input features.
3. Drop rows missing the selected features or the AQI target.
4. Choose a regression algorithm and its available hyperparameters.
5. Train and review the evaluation metrics.

## Evaluation

The app displays Mean Absolute Error (MAE), Mean Squared Error (MSE), and R² for the selected train/test split. Results depend on the dataset, chosen features, model settings, and split; run the app to obtain the metrics rather than assuming a model is best in advance.

## Notes

- This is an educational project, not a source of official health or emergency guidance.
- Predictions depend on the quality and coverage of the input data.
- Dataset attribution and usage terms should be retained alongside the dataset if you redistribute it.

## Author

**Surya Prasad Mallik**
