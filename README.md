# 📊 COVID-19 Data Analytics & Automation Suite

An end-to-end **COVID-19 data analytics and reporting system** built using **Excel, Power BI, Python, and n8n automation**.

This repository demonstrates how raw public health datasets can be transformed into **interactive analytical dashboards, statistical insights, and automated AI-generated situation reports**.

The project combines:

* 📊 **Advanced Excel Analytics Dashboard**
* 📈 **Power BI Interactive Data Model**
* 🤖 **AI-Powered Automated Situation Reporting**

Together, these components create a **complete data pipeline from raw data → analytics → automated communication**.

---

# 🎯 Project Objectives

The primary goal of this project is to transform large-scale COVID-19 datasets into **actionable insights and automated reporting systems**.

Key objectives include:

* Monitor pandemic trends using **time-series analysis**
* Track **healthcare performance indicators**
* Evaluate **testing efficiency and vaccination progress**
* Perform **state-level outbreak analysis**
* Forecast future case patterns
* Build **interactive dashboards for decision support**
* Automate **AI-generated public health briefings**

---

# 📊 Dataset Overview

The project integrates multiple structured datasets covering national and state-level COVID-19 statistics.

### Primary Data Sources

* **SummaryData**

  * Daily confirmed cases
  * Recoveries
  * Deaths
  * Positive cases

* **TestingData**

  * State-wise daily testing samples
  * Total tests conducted

* **VaccineData**

  * Total doses administered
  * First and second dose distribution
  * Vaccination coverage

### Key Data Attributes

* Date
* State / Union Territory
* Confirmed Cases
* Deaths
* Recovered Cases
* Active Cases
* Positive Cases
* Total Samples Tested
* Vaccination Data
* Population
* Age Group

Datasets were **cleaned, validated, merged, and structured using composite keys** to support advanced analytical modeling.

---

# 📊 Excel Analytical Dashboard

The Excel dashboard was developed to perform **advanced statistical analysis and forecasting** directly within Excel.

## Key Features

* National Case Trend Analysis
* Monthly Pandemic Wave Detection
* Positive Rate & Testing Efficiency Tracking
* Vaccination vs Recovery Rate Comparison
* State-wise Contribution Analysis
* Dynamic State Drill-Down Selection
* Risk Classification (High / Medium / Low)
* Weekday Seasonality Detection
* CFR Threshold Filtering
* **30-Day Case Forecast using ETS (Exponential Smoothing)**

## Analytical Capabilities

The dashboard integrates multiple analytical techniques:

* Time-series analysis
* Forecast modeling
* KPI engineering
* Conditional risk scoring
* Dynamic dashboard controls

---

# 📈 Power BI Interactive Dashboard

The Power BI dashboard provides **interactive visualization and multi-dimensional analysis** of pandemic data across Indian states.

The dashboard focuses on:

* Trend analysis
* Healthcare performance metrics
* Testing efficiency
* Vaccination progress

---

## 🗂️ Data Model

The Power BI model integrates structured datasets and uses **DAX (Data Analysis Expressions)** for dynamic calculations.

Example measure:

```DAX
Latest Date =
MAX('CovidData'[Date])
```

This ensures that KPI cards always reflect the **most recent available data**.

---

# 📊 COVID-19 Case Summary

| Metric                | Value       |
| --------------------- | ----------- |
| Total Confirmed Cases | ~32 Million |
| Total Deaths          | ~429K       |
| Total Recovered       | ~31 Million |
| Active Cases          | ~386K       |
| Daily New Cases       | ~38K        |
| Recovery Rate         | ~97.45%     |

### Key Observations

* High recovery rate indicates improved healthcare capacity.
* Active cases significantly lower than total confirmed cases.
* Multiple pandemic waves identified during analysis.

---

# 🧪 Testing Analysis

### National Testing Summary

* **Total Tests Conducted:** 524+ Million
* **National Positivity Rate:** ~1.19%

Low positivity rate generally indicates **adequate testing coverage**.

---

## 📊 State Positivity Rate Comparison

### High Positivity States

* Madhya Pradesh
* Tripura
* Haryana
* Maharashtra
* Kerala

### Low Positivity States

* Mizoram
* Lakshadweep
* Uttar Pradesh

### Interpretation

| Scenario                       | Meaning                 |
| ------------------------------ | ----------------------- |
| High Testing + Low Positivity  | Effective surveillance  |
| Low Testing + High Positivity  | Potential hidden spread |
| High Testing + High Positivity | Severe outbreak phase   |

---

# 📊 Case Fatality Rate (CFR) Analysis

```
CFR = Deaths ÷ Confirmed Cases
```

### High CFR States

* Punjab
* Uttarakhand
* Maharashtra

### Low CFR States

* Mizoram
* Kerala
* Telangana

Higher CFR may indicate **healthcare system strain or vulnerable populations**.

---

# 💉 Vaccination Analysis

| Metric                   | Value        |
| ------------------------ | ------------ |
| Total Doses Administered | ~513 Million |
| Vaccination Coverage     | ~48.84%      |
| First Dose               | ~400 Million |
| Second Dose              | ~113 Million |
| Individuals Vaccinated   | ~251 Million |

### Age Group Distribution

* **18–44 years** – Largest vaccinated population
* **45–60 years**
* **60+ years** – Prioritized early due to vulnerability

Vaccination rollout began **16 January 2021**, enabling comparison between:

* Pre-Vaccination Phase
* Post-Vaccination Phase

---

# 📈 Trend Analysis

The dashboards include:

* Confirmed vs Recovered vs Deaths trend
* Daily case growth analysis
* Weekly & monthly aggregation
* Vaccination growth curve
* Pre vs Post vaccination comparison

### Key Insights

* COVID-19 spread followed **distinct wave patterns**
* Reporting delays created **weekday seasonality**
* Vaccination contributed to **long-term stabilization**

---

# 🤖 AI-Powered COVID Situation Report Automation

To complement the dashboards, an **automated reporting pipeline** was built using **Python, n8n, and OpenAI**.

This system generates **daily AI-written COVID situation reports** and distributes them via email.

---

## Automation Architecture

```
Raw Excel Data
        ↓
Python Data Aggregation
        ↓
Structured CSV Output
        ↓
n8n Workflow Automation
        ↓
OpenAI Prompt Generation
        ↓
Automated Gmail Report
```

---

## n8n Workflow

1. Daily scheduled trigger
2. Load national COVID dataset
3. Load state summary dataset
4. Process daily statistics
5. Identify top affected states
6. Merge datasets
7. Generate AI summary
8. Send automated email report

---

## AI Report Inputs

The AI model receives:

* National new cases
* Recoveries and deaths
* Test positivity rate
* Vaccination progress
* Top affected states

The system converts technical metrics into **clear, non-technical public health briefings**.

---

## Example AI Output

> On 12 May, India reported 72,341 new COVID-19 cases. The situation shows a moderate level of spread with a national positivity rate of 5.3%. Recoveries continue to outpace new infections while vaccination efforts remain steady. Maharashtra and Kerala reported the highest number of new cases today.

---

# 📊 Dashboard Preview



---

# 💼 Business & Policy Impact

This project demonstrates how analytical dashboards can support **public health decision-making**.

Key impacts include:

* Hospital capacity forecasting
* Targeted healthcare resource allocation
* Identification of high-risk regions
* Monitoring vaccination progress
* Automated pandemic reporting

---

# 🛠️ Tools & Technologies

| Category       | Tools                      |
| -------------- | -------------------------- |
| Data Analysis  | Excel, Power BI            |
| Programming    | Python                     |
| Automation     | n8n                        |
| AI Integration | OpenAI                     |
| Visualization  | Power BI, Excel Dashboards |
| Data Modeling  | DAX                        |

---

# 📊 Dashboard Preview

<img width="602" height="304" alt="Dashboard Preview" src="https://github.com/user-attachments/assets/7ddcff0c-fbd1-4fcc-8ccb-89db6c0c960d" />

---

# 🏁 Conclusion

This project demonstrates how modern analytics tools can convert **large-scale healthcare datasets into meaningful insights and automated reporting systems**.

By combining **data analytics, visualization, statistical modeling, and AI automation**, the project provides a comprehensive framework for **data-driven pandemic monitoring and communication**.

