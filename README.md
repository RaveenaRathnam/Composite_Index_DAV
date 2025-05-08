# European Quality of Life Index 2022

This project builds a composite **European Quality of Life Index** for 30 European countries using publicly available socioeconomic indicators. The goal is to analyze and compare well-being across five key dimensions:

## 📊 Subindices
The index is structured around five major subindices:

1. **Economic Well-Being**  
   _GDP per capita, unemployment, income, poverty, inflation_

2. **Health & Wellness**  
   _Life expectancy, health expenditure, obesity, hospital beds, mental health_

3. **Education & Skills**  
   _Tertiary education, student-teacher ratio, early leavers, adult participation, education spending_

4. **Environmental Sustainability**  
   _CO2 emissions, renewable energy, waste, pollution, environmental taxes_

5. **Social Inclusion**  
   _Crime, poverty & exclusion, deprivation, inequality, gender employment gap_

---

## 🧪 Methodology

### 🧹 Data Preprocessing
- Merged 26 Eurostat and related datasets
- Filtered for the year **2022** (or filled with most recent past year)
- Handled missing values with conditional imputation (fallbacks + column means)
- Standardized all variables for comparability
- Normalized data using **Min-Max Scaling**

### 📏 Dimensionality Reduction & Weighting
- **PCA (Principal Component Analysis)** used to:
  - Detect redundancy among indicators
  - Extract PC1 or weights for subindices
- Two composite index versions created:
  - **PC1 Score-based**
  - **PCA Weighted** (via loading scores)
- Clustering using K-means
- Final aggregation using **geometric mean** to avoid full compensability
- Compared PC1 composite index and PCA based weighted index.

---

## 🗺️ Visualizations
- 📌 **Choropleth Map**: Shows composite index across Europe
- 📊 **Bar Chart**: Ranks countries by index score
- 🕸️ **Radar (Spider) Charts**: Visualize subindex strengths per country
- other charts like scatter plots,etc.

---

## 🔍 Findings
- Countries like **Slovenia, Ireland, and Norway** score high on all dimensions
- Outliers (e.g., **Iceland** or **Romania**) show unique strengths/weaknesses
- PCA reveals clear clusters and correlations across indicators
- Both PC1 and weighted methods give consistent results with some countries having variance.

---

## 🧭 Goals & Applications
- Support policy benchmarking across European countries
- Highlight multidimensional aspects of well-being beyond GDP
- Demonstrate good practice in composite index construction (OECD Handbook aligned)

---

## 🛠️ Tools Used
- Python (pandas, sklearn, matplotlib, seaborn, plotly)
- Jupyter Notebooks
- Eurostat datasets

---


## 👤 Author
- Raveena Rathnam Kuppala
- **Dundalk Institute of Technology**

---
