# Electric Vehicle Population Data Analysis

This project explores an **Electric Vehicle (EV) Population dataset**, performing cleaning, exploratory data analysis (EDA), visualization, and initial modeling steps. The goal is to understand EV adoption patterns, price vs. performance tradeoffs, and geographic distribution.

---

## 📦 Libraries Used

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
from sklearn.preprocessing import StandardScaler
from sklearn.decomposition import PCA
import plotly.express as px
import json
```

---

## 📂 Dataset

* **Source:** Electric Vehicle Population Data (Kaggle)
* **Key Columns:**

  * `VIN (1-10)`, `County`, `City`, `Postal Code`, `Model Year`, `Make`, `Model`, `Electric Vehicle Type`, `CAFV Eligibility`, `Electric Range`, `Base MSRP`, `Legislative District`, `DOL Vehicle ID`, `Electric Utility`, `Census Tract`

---

## 🔹 Data Cleaning

1. Checked for missing values and data types:

   ```python
   ```

df.isnull().sum()
df.dtypes

````
2. Removed duplicate rows based on **`DOL Vehicle ID`**.
3. Segmented dataset into:
   - **Full EVs** (`Clean Alternative Fuel Vehicle Eligible`)
   - **Gas/Hybrid with low range** (`Not eligible due to low battery range`)

---

## 🔹 Exploratory Data Analysis (EDA)
### Value Counts & Filtering
- Distribution of **CAFV eligibility**.
- Subset created for **full electric vehicles**.

### Boxplots & Histograms
- **MSRP distribution** of full EVs:
```python
sns.boxplot(x=full_electric_df['Base MSRP'])
````

* **Make distribution in Renton**:

```python
sns.histplot(x=full_electric_df[full_electric_df["City"]=="Renton"]['Make'])
```

### Market Share

* Count of EVs by **Make**.
* Pie chart showing market share distribution.

### Electric Range

* Boxplot showing distribution of EV ranges.
* Table of `Model`, `Make`, and `Electric Range` for inspection.

---

## 🌍 Geographic Analysis

* Grouped EV counts by **County**.
* Built **choropleth maps** using Plotly:

```python
fig = px.choropleth(df, geojson=geojson_data, locations='Postal Code',
                    color_continuous_scale="Viridis", 
                    title="Choropleth Map by Postal Code")
fig.show()
```

---

## 📊 Visualizations

1. **Adoption Over Time:** Countplot of EVs by `Model Year`.
2. **Price vs Range:** Scatterplot with `Base MSRP` on x-axis, `Electric Range` on y-axis, hue by `Electric Vehicle Type`.

---

## 🤖 Predictive Modeling (Planned)

* Initial exploration of filtered EV dataset (`full_electric_df`).
* Next steps:

  * Regression: Predict `Electric Range` from `Base MSRP` and `Model Year`.
  * Classification: Predict EV type (BEV vs PHEV).
  * Clustering: Group counties by adoption patterns.

---

## ✅ Next Steps

* Refine geographic analysis with Census Tract demographic data.
* Expand predictive modeling.
* Build an **interactive dashboard** for real-time exploration (using Plotly Dash or Tableau).

---

📌 **Author:** Bob Yan
📌 **Goal:** Explore EV adoption trends, price vs. range relationships, and geographic distribution to extract policy and business insights.
