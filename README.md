# Food Delivery Analytics

## 📌 Project Overview

The **Food Delivery Analytics** project focuses on analyzing food-delivery operational data to evaluate delivery performance, identify potential delay patterns, and generate actionable business insights.

The project uses Python-based data preparation and exploratory data analysis, with the final insights intended to support management reporting and Power BI dashboard development.

---

## 🎯 Business Objective

The primary objective of this project is to understand the factors associated with delivery-time variation and provide data-driven recommendations for improving operational efficiency.

### Key Business Objectives

1. Measure overall food-delivery performance using delivery time.
2. Identify cities with higher average delivery times.
3. Analyze delivery performance across different order hours.
4. Examine operational factors such as traffic, weather, distance, preparation time, and multiple deliveries.
5. Improve data quality and consistency before KPI reporting.
6. Develop insights that can support operational and management decisions.
7. Provide a structured foundation for Power BI dashboard reporting.

---

## 📊 Dataset Overview

The initial dataset contains:

| Metric | Value |
|---|---:|
| Total Records | 41,953 |
| Initial Columns | 17 |
| Primary KPI | `Time_Taken_Min` |
| Initial Average Delivery Time | 26.34 minutes |
| Records with Missing Delivery Time | 4,133 |

### Key Business Fields

Important fields used in the analysis include:

- `City`
- `Order_Date`
- `Order_Hour`
- `Delivery_person_Age`
- `Delivery_person_Ratings`
- `Weatherconditions`
- `Road_traffic_density`
- `multiple_deliveries`
- `Festival`
- `Time_Taken_Min`

---

# 🔧 Data Preparation

The dataset is prepared before performing business analysis.

### Data Cleaning Process

1. **Missing-Value Assessment**  
   Missing values are identified across all columns.

2. **Column Removal**  
   Columns containing more than 50% missing values are removed.

3. **Date Formatting**  
   `Order_Date` is converted into datetime format.

4. **Data-Type Validation**  
   Numerical and categorical columns are reviewed and corrected where required.

5. **Numerical Missing Values**  
   Missing numerical values are replaced using the median.

6. **Categorical Missing Values**  
   Missing categorical values are replaced using the mode.

7. **Duplicate Validation**  
   Duplicate records are checked before analysis.

8. **Outlier Detection**  
   The Interquartile Range (IQR) method is applied to `Time_Taken_Min`.

9. **Outlier Treatment**  
   Delivery-time observations outside the calculated IQR limits are filtered.

---

# 📈 Exploratory Data Analysis

The project performs multiple analytical views to understand delivery performance.

## 1. Delivery-Time Distribution

A histogram is used to analyze the distribution of `Time_Taken_Min`.

**Business Purpose:**  
Understand the overall delivery-time pattern and identify the typical range of delivery durations.

---

## 2. City-Level Delivery Performance

Average delivery time is calculated by `City`.

The analysis identifies the **Top 10 cities by average delivery time**.

**Business Purpose:**

- Identify locations with higher delivery times.
- Highlight cities requiring operational investigation.
- Support location-specific performance management.

---

## 3. Delivery Performance by Order Hour

Average delivery time is calculated by `Order_Hour`.

**Business Purpose:**

- Identify periods with higher delivery times.
- Understand time-of-day performance patterns.
- Support rider and operational capacity planning.

---

## 4. Festival vs Non-Festival Analysis

Order volumes are compared between festival and non-festival conditions using the `Festival` field.

**Business Purpose:**

- Understand demand context.
- Identify potential changes in order patterns during festivals.
- Support operational planning during high-demand periods.

---

## 5. Correlation Analysis

A correlation heatmap is created using numerical variables.

**Business Purpose:**

- Explore relationships between numerical variables.
- Identify variables that may be associated with delivery-time performance.
- Support further root-cause investigation.

---

# 💡 Key Business Insights

The analysis provides a framework for answering the following business questions:

1. Which cities experience higher average delivery times?
2. During which order hours does delivery performance change?
3. What is the overall distribution of delivery time?
4. How does festival demand compare with non-festival demand?
5. Which numerical variables show relationships with delivery performance?
6. Which operational areas require further investigation?

---

# 🚀 Recommended Business Actions

Based on the analytical framework, the following actions are recommended:

### 1. Prioritize High-Delay Locations

Use city-level delivery performance to identify locations requiring operational review, capacity planning, or routing attention.

### 2. Optimize Resource Planning

Use hourly delivery-time patterns to align rider availability and operational capacity with periods of higher delivery times.

### 3. Monitor Operational Conditions

Track factors such as:

- Road traffic
- Weather conditions
- Distance
- Preparation time
- Multiple deliveries

alongside delivery-time KPIs.

### 4. Strengthen Data Quality

Maintain standardized processes for:

- Missing-value treatment
- Data-type validation
- Duplicate checking
- Outlier detection
- KPI calculation

### 5. Implement Continuous Dashboard Monitoring

Use Power BI to monitor delivery performance through:

- KPI cards
- City-level performance
- Hourly delivery trends
- Operational-condition analysis
- Management-level summaries

---

# 📦 Project Deliverables

The project produces the following key deliverables:

1. Cleaned analytical dataset.
2. Data-quality and preparation workflow.
3. Delivery-time distribution analysis.
4. Top 10 cities by average delivery time.
5. Festival vs non-festival analysis.
6. Average delivery time by order hour.
7. Correlation analysis.
8. Business problem statement.
9. Business insights.
10. Recommended operational actions.
11. Power BI dashboard framework.
12. Exported analytical dataset.

---

# 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Python | Data analysis |
| Pandas | Data manipulation |
| NumPy | Numerical operations |
| Matplotlib | Data visualization |
| Seaborn | Statistical visualization |
| Jupyter Notebook | Analysis environment |
| Excel | Analytical data export |
| Power BI | Dashboard and business reporting |

---

# 🔄 Project Workflow

```text
Raw Food Delivery Data
          ↓
Data Inspection
          ↓
Missing-Value Analysis
          ↓
Data Cleaning
          ↓
Data-Type Formatting
          ↓
Duplicate Validation
          ↓
Outlier Detection & Treatment
          ↓
Exploratory Data Analysis
          ↓
Business Insights
          ↓
Dashboard Development
          ↓
Recommended Business Actions
