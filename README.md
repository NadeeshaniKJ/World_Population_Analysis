# World Population Analysis 

This project provides an in-depth analysis of global demographic trends using the dataset **"Global Demographic Dynamics: Population Trends"**, sourced from the UN DESA Population Division and accessed via Kaggle. The dataset includes historical population estimates (1950–2021) and projections (2022–2050) by gender and age groups.  

## Introduction  

This project examines global population trends to provide insights into historical growth, future projections, and demographic structures. Key analyses include:  
- Population pyramids for specific years (1950, 2021, 2050).  
- Workforce, aging, and child population metrics.  
- Gender-based population distribution.  
- Population growth rates by countries and non-country economies.  
- Linear regression for population prediction.  

---

## Dataset  

**File:** `US_PopAgeStruct_20230713030811.csv`  
- **Source:** [UNCTADstat](https://unctadstat.unctad.org/datacentre/)  
- **Size:** 121 MB  
- **Theme:** Population and Labour Force  

### Dimensions  
- `SERIES`: Population indicators (absolute values in various units).  
- `AGE CLASS`: Age groups (e.g., 0–4, 5–9).  
- `ECONOMY`: Country/region/economy.  
- `YEAR`: Timeframe (1950–2050).  
- `SEX`: Gender classification (Male/Female/Total).  

---

## Setup  

### Installing PySpark  
Install PySpark for data processing and analysis. Use the following command:  
```bash  
pip install pyspark
```

### Initializing Spark Session  

Configure and initialize a Spark session to handle the dataset:  
```python  
from pyspark.sql import SparkSession  
spark = SparkSession.builder.appName("PopulationTrends").getOrCreate()  
```

## Data Exploration  

1. **Schema Inspection:** Display dataset schema and structure.  
2. **Data Cleaning:** Remove null, duplicate, and zero values in key columns (e.g., `Absolute value in thousands`).  
3. **Partitioning:** Evaluate the number of partitions for optimal performance.  
4. **Descriptive Statistics:** Summarize key statistics for numeric fields.  

---

## Analysis  

### Population Trends  
- **Total Population Over the Years:** Analyze trends from 1950 to 2050.  
- **Gender-Based Analysis:** Visualize male and female population trends.  
- **Population Pyramids:** Explore age distribution for 1950, 2021, and 2050.  

### Gender Distribution  
- Variation in male and female populations by age groups and over time.  

### Age Group Analysis  
- **Children:** Population below 20 years.  
- **Workforce:** Population aged 20–60 years.  
- **Aging:** Population above 60 years.  

### Regional and Country-Specific Insights  
- Top 10 countries with highest and lowest populations for 1950, 2021, and 2050.  
- Growth rate analysis for individual countries and non-country economies.  
- Focused analysis of Japan, Qatar, and Sri Lanka.  

---

## Visualizations  

The project includes a variety of visualizations to better understand population trends:  

1. **Population Over Time**  
   - Line graphs showing total population from 1950 to 2050.  
   - Separate graphs for male and female populations over the years.  

2. **Population Pyramids**  
   - Stacked bar charts representing age-group-wise distribution for 1950, 2021, and 2050.  

3. **Country-Specific Trends**  
   - Bar plots showing the top 10 and bottom 10 countries by total population for selected years.  
   - Growth rate comparisons among countries.  

4. **Gender Differences**  
   - Graphs showcasing variations in population between males and females by age group and over time.  

5. **Demographic Focus Areas**  
   - Pie charts representing the proportion of children (below 20 years), workforce (20–60 years), and elderly (above 60 years).  

---

## Machine Learning Model  

- **Linear Regression:** Predict total population trends based on historical data.  
- **Evaluation:** Measure prediction accuracy and visualize forecasted trends.  

---

## Technologies Used  

- **PySpark**: For handling large datasets efficiently.  
- **Pandas**: For smaller-scale data manipulation.  
- **Matplotlib** and **Seaborn**: For creating visualizations.  
- **Jupyter Notebook**: For interactive coding and analysis.  
- **Python Libraries**: NumPy, Scikit-learn (for Linear Regression).  

---

## Features  

- **Data Cleaning:** Removes inconsistencies like missing values and duplicates.  
- **Exploratory Data Analysis (EDA):** Provides insights through descriptive statistics and visualizations.  
- **Predictive Analytics:** Uses Linear Regression to forecast future population trends.  
- **Custom Queries:** Allows filtering by specific countries, age groups, or genders.  
- **Interactive Graphs:** Easily interpretable visualizations to explore trends over time.  

---

## Future Work  

- Incorporate additional datasets for a more comprehensive analysis (e.g., economic indicators or migration data).  
- Explore machine learning models beyond Linear Regression for better prediction accuracy.  
- Develop a web-based dashboard for interactive visualizations and real-time insights.  

---

## Conclusion  

This project provides actionable insights into global demographic dynamics, emphasizing historical patterns, future projections, and population disparities. Key findings highlight:  
- **Workforce Potential:** Significant opportunities in various regions.  
- **Aging Populations:** Challenges posed by an increasing elderly demographic.  
- **Demographic Shifts:** Transformative changes in population structures over the century.
