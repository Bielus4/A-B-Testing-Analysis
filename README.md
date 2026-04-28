# E-news Express — A/B Testing Analysis

This project presents an A/B testing analysis for the **E-news Express** platform, aimed at evaluating whether a redesigned landing page improves user engagement and conversion rates.

---

## Project Overview

The analysis compares two versions of a landing page:

- **Old version** (`old`)
- **New version** (`new`)

The main objectives were to determine whether the new landing page:

1. Increases the time users spend on the page  
2. Improves the conversion rate  
3. Affects user behavior based on language preference  

---

## Business Context

E-news Express is a digital news platform seeking to increase its subscriber base. The company observed a decline in new monthly subscriptions and suspects that the current landing page may not effectively engage users or encourage conversions.

A redesigned landing page was introduced to enhance user experience and improve performance.

---

## Dataset

The dataset contains **100 observations** and **6 variables**.

### Data Dictionary

- `user_id` — unique user identifier  
- `group` — experiment group: `control` or `treatment`  
- `landing_page` — page version: `old` or `new`  
- `time_spent_on_the_page` — time spent (in minutes)  
- `converted` — conversion status (`yes` / `no`)  
- `language_preferred` — user language (`English`, `Spanish`, `French`)  

---

## Technologies Used

- Python  
- pandas  
- numpy  
- matplotlib  
- seaborn  
- scipy  
- statsmodels  

---

## Analysis Performed

The following statistical tests were conducted:

### 1. Time Spent on Landing Page
- Test: **One-tailed independent two-sample t-test**  
- Goal: Compare average time between new and old pages  

### 2. Conversion Rate
- Test: **One-tailed two-proportion Z-test**  
- Goal: Compare conversion rates between pages  

### 3. Language vs Conversion
- Test: **Chi-square test of independence**  
- Goal: Check if conversion depends on language  

### 4. Time Spent vs Language (New Page)
- Test: **One-way ANOVA**  
- Assumptions tested:
  - Shapiro-Wilk (normality)  
  - Levene’s test (homogeneity of variance)  

---

## Key Results

### Time Spent
- New page: **6.22 minutes**  
- Old page: **4.53 minutes**  
- Result: **Statistically significant**  

👉 Users spend more time on the new landing page.

---

### Conversion Rate
- New page: **66%**  
- Old page: **42%**  
- Result: **Statistically significant**  

👉 The new landing page leads to higher conversions.

---

### Language vs Conversion
- Result: **Not statistically significant**  

👉 No evidence that language affects conversion.

---

### Language vs Time Spent (New Page)
- Result: **Not statistically significant**  

👉 Time spent does not differ across language groups.

---

## Business Conclusions

The new landing page:

- Increases user engagement  
- Improves conversion rates  
- Performs consistently across different language groups  

### Recommendations

- Deploy the new landing page as the default version  
- Continue optimizing layout and content  
- Conduct user surveys for deeper insights  
- Analyze additional behavioral metrics (e.g., visits, session duration)  

---

## Project Structure

```bash
.
├── abtest.csv
├── analysis.ipynb
└── README.md
