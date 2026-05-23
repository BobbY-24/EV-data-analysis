# Electric Vehicle Population Data Analysis

## Overview
This project explores electric vehicle population data with data cleaning, exploratory analysis, visualization, and initial modeling steps. It focuses on EV adoption patterns, geographic distribution, and vehicle characteristics. The project is best framed as an applied data analysis notebook.

## Motivation
Electric vehicle adoption is a meaningful public data topic involving technology, infrastructure, policy, and consumer behavior. This project demonstrates cleaning a real-world dataset, asking practical data questions, and communicating trends visually.

## Dataset
- **Source:** Electric Vehicle Population dataset.
- **File:** `data/Electric_Vehicle_Population_Data.csv.zip`
- **Target variable:** Not applicable for the current EDA-focused version.
- **Important features:** vehicle make/model, model year, EV type, electric range, location fields, and policy/geographic identifiers.
- **Dataset size:** TODO: add dataset size after rerunning notebook.
- **Known limitations:** Data may reflect reporting practices and regional policy differences rather than complete EV adoption behavior.

## Methods
- Loaded and cleaned the EV population dataset.
- Performed exploratory data analysis.
- Visualized adoption trends and vehicle attributes.
- Started feature scaling and modeling-oriented preparation.

## Results
TODO: add metric after rerunning notebook.

## Key Insights
- TODO: add insight after rerunning notebook.
- TODO: add insight after rerunning notebook.
- TODO: add insight after rerunning notebook.

## Limitations
- The project is mostly exploratory and does not make causal claims.
- The dataset is zipped and may need extraction before running the notebook.
- Regional patterns may reflect data availability and policy reporting.
- Modeling steps need clearer target definition before predictive claims are made.

## Future Improvements
- Add a clear research question around EV adoption.
- Add geographic visualizations if location fields are reliable.
- Define a predictive target only if it is meaningful.
- Add cleaned summary tables in `results/`.

## How to Run
```bash
git clone https://github.com/BobbY-24/EV-data-analysis.git
cd EV-data-analysis
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
unzip data/Electric_Vehicle_Population_Data.csv.zip -d data/
jupyter notebook notebooks/ev_population_trends.ipynb
```
