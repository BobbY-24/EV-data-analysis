# Electric Vehicle Population Data Analysis

## Overview
I analyzed electric vehicle population data to explore adoption patterns, geographic distribution, and vehicle characteristics. I treat the project as mainly an exploratory data analysis notebook with cleaning, visualization, and early modeling preparation.

## Motivation
I chose this dataset because EV adoption connects technology, infrastructure, policy, and consumer behavior. I wanted to practice cleaning a real public dataset and turning it into interpretable summaries.

## Dataset
- **Source:** Electric Vehicle Population dataset.
- **File:** `data/Electric_Vehicle_Population_Data.csv.zip`
- **Target variable:** I did not define a supervised target for this version.
- **Important features:** vehicle make/model, model year, EV type, electric range, location fields, and policy/geographic identifiers.
- **Known limitations:** The data reflects reporting practices and regional policy differences, so I treat the analysis as descriptive.

## Methods
- I loaded and cleaned the EV population dataset.
- I explored vehicle attributes and adoption patterns.
- I created visual summaries of the data.
- I prepared some modeling-oriented transformations, but I do not make predictive claims from them.

## Results
I use this notebook for exploratory findings rather than a single headline metric. The main output is a clearer view of EV adoption patterns and data quality issues.

## Key Insights
- EV adoption analysis depends heavily on geography and reporting coverage.
- Vehicle model year, make, and EV type are useful starting points for understanding the dataset.
- I need a sharper prediction target before treating this as a modeling project.

## Limitations
- I do not make causal claims about EV adoption.
- The zipped dataset needs to be extracted before running the notebook.
- Some geographic analysis depends on optional external map files.

## Future Improvements
- Add a clear research question around EV adoption.
- Add geographic visualizations if location files are available.
- Define a meaningful predictive target before adding modeling claims.
- Save cleaned summary tables in `results/`.

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
