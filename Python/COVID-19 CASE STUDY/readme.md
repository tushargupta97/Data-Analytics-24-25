# 🦠 COVID-19 Global Pandemic Analysis using Python

A complete analytical study of global COVID-19 data including **confirmed cases, recoveries, and deaths** across multiple countries and time periods.  
This project demonstrates the use of Python for data cleaning, transformation, visualization, and comparative pandemic analysis.

---

## 📑 Overview

COVID-19, first identified in late 2019, rapidly evolved into a global pandemic.  
This study focuses on how data analytics enables better monitoring of virus spread, recovery rates, and mortality trends.  
Using structured time-series datasets, this analysis explores country-level patterns and the progression of the pandemic over time.

---

## 📂 Datasets Used

| Dataset | Contains | Duration | Regions |
|--------|----------|----------|---------|
| **Confirmed Cases** | Daily cumulative confirmed COVID-19 cases | Jan 22, 2020 – May 29, 2021 | 276+ |
| **Deaths** | Daily cumulative COVID-19 deaths | Same | Same |
| **Recovered Cases** | Daily cumulative recovered patients | Same | Same |

Each dataset includes:  
`Province/State | Country/Region | Lat | Long | Daily Cumulative Columns`

> 🔗 Datasets were downloaded from the official COVID-19 timeseries repository.

---

## 🎯 Objectives

- Use Python to analyze real-world COVID-19 data
- Handle missing values & clean time-series data
- Visualize country-wise spread trends
- Compare peak infections, recovery rate & death ratios
- Merge multi-dataset information for deeper insights

---

## 🛠 Tech Stack

| Tool | Purpose |
|------|----------|
| **Python** | Primary analysis language |
| **Pandas** | Data manipulation, cleaning, merging |
| **NumPy** | Numerical calculations |
| **Matplotlib/Seaborn** | Data visualization |
| **Jupyter Notebook** | Execution & stepwise exploration |

---

## 🔍 Analysis Workflow

# 1️⃣ Data Loading

```python
confirmed = pd.read_csv("confirmed.csv")
deaths = pd.read_csv("deaths.csv")
recovered = pd.read_csv("recovered.csv")
```

# 🔍 Detailed Project Analysis

---

# 2️⃣ Exploratory Data Analysis

- Checked rows, columns & data types  
- Identified missing values  
- Visualized confirmed cases over time for:
  - **Top affected countries globally**
  - **China** (separate country-focused timeline)

📈 *Time-series graphs were plotted to observe spread intensity, spike periods, and growth curves.*

---

# 3️⃣ Handling Missing Data

Forward-fill method applied to maintain time-series continuity:

```python
df = df.fillna(method="ffill")
```

#  4️⃣ Data Cleaning

During the preprocessing phase, blank entries were found in the **Province/State** column.  
To maintain data consistency and avoid null-label grouping issues during aggregation, these missing values were replaced with a unified label:

```python
df["Province/State"].replace("", "All Provinces", inplace=True)
```
## 🔍 Why This Step Was Important?

- Eliminates empty-text Province fields in grouped analysis  
- Ensures consistent category representation across the dataset  
- Prevents grouping splits caused by blank values  
- Helpful for country-level summaries where province data isn't available  

This step strengthened data uniformity and enabled error-free analytics.

---

#  5️⃣ Independent Dataset Analysis

The COVID-19 dataset was explored at a country-comparative level to derive useful insights regarding infection surges, recovery rates, and fatality distribution.

##  Key Analytical Results

| Analysis Task | Findings |
|--------------|----------|
| Peak daily new cases in **Germany, France & Italy** | Highest infection spike identified for each country along with the exact surge date |
| Recovery rate comparison between **Canada & Australia** (as of 31 Dec 2020) | Determined which nation handled recoveries more efficiently |
| **Canadian provinces** death-rate distribution | Province with highest and lowest fatality ratios highlighted |

---

#  6️⃣ Data Transformation

The *Deaths* dataset originally existed in **wide format** with dates as column headers.  
To enable aggregation, merging, and time-series analysis, the dataset was reshaped into **long format**.

## Transformation Code

```python
deaths_long = deaths.melt(
    id_vars=["Province/State", "Country/Region", "Lat", "Long"],
    var_name="Date",
    value_name="Deaths"
)
deaths_long["Date"] = pd.to_datetime(deaths_long["Date"])
```
## 📊 Derived Metrics After Transformation

After converting the dataset and restructuring the format, several core metrics were computed to understand COVID-19 impact trends:

✔ Total deaths per country  
✔ Top 5 countries with the highest **average daily deaths**  
✔ Full U.S. death trend visualized across pandemic timeline  

These metrics supported comparative analysis and helped highlight regions with most critical spread intensity.

# 7️⃣ Dataset Merging

The cleaned and transformed COVID-19 datasets for Confirmed Cases, Deaths & Recoveries were merged to form a consolidated dataset for unified analysis.

## Merging Code Used:

```python
merged = confirmed_long.merge(deaths_long).merge(recovered_long)
```

## 📊 Insights From the Merged Dataset

After merging the confirmed, deaths, and recovery datasets, comparative analysis was performed to study COVID-19 patterns more holistically.

---

### 📅 Monthly Analysis Conducted For:

- Confirmed Cases  
- Recoveries  
- Deaths  

Breaking the timeline into monthly segments allowed clear observation of rise, fall, and stability phases across the pandemic period.

---

### 🌍 Country-wise Impact Comparison

| Country |
|--------|
| USA |
| Italy |
| Brazil |

These three countries were among the most heavily affected globally. Their comparison enabled insights into:

### 🔎 What the comparison revealed:

- **Infection intensity** across regions  
- **Response efficiency** through recovery patterns  
- **Mortality behavior** over time  

This analysis demonstrated how different nations controlled or struggled during the waves of the pandemic.

--- 

# 8️⃣ Combined Insights

Using the merged dataset, multiple comparative analyses were performed to understand the global COVID-19 outcome trends.

---

### 📌 Key Findings

- **Top 3 countries with the highest average death rate in 2020** were identified  
- **South Africa** recovery count vs death count was compared to evaluate case outcomes  
- **USA (March 2020 → May 2021)** monthly recovery ratio was calculated and analyzed  
  ➤ The month with the *best recovery performance* was highlighted along with reasoning

---

### 📈 Interpretation

These insights reflect:

- Pandemic **severity variations** across countries  
- **Public health response strength** in recovery management  
- How healthcare systems coped during **case surges and decline phases**

Overall, the analysis showcases how data-driven observation helps evaluate the effectiveness of pandemic strategies across different nations.

---
# 📝 Conclusion

This project demonstrates how real-world pandemic data can be cleaned, visualized, merged, and interpreted to generate meaningful insights.  
Understanding infection growth rate, mortality probability, and recovery behavior helps governments, health agencies, and researchers make informed decisions during global crises like COVID-19.

The COVID-19 data analysis strongly reflects how **data science plays a critical role in public health response, prevention strategies, and outbreak management.**

Data-driven insights help us:

- Track pandemic progression  
- Evaluate impact across countries  
- Measure recovery vs mortality outcomes  
- Support future preparedness and planning  

COVID-19 analysis stands as a representation of how analytical thinking and technology can help the world respond to health emergencies more effectively.

