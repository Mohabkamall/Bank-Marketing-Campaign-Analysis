# Bank Marketing Campaign Analysis

## Overview

This project analyzes the **Bank Marketing** dataset to understand customer characteristics and campaign-related factors associated with subscribing to a term deposit.

The project focuses on **Exploratory Data Analysis (EDA)**, data quality assessment, feature engineering, categorical and numerical analysis, multivariate analysis, and data visualization.

The goal is to extract meaningful patterns from the data and communicate the main findings clearly.

## Dataset

The dataset used in this project is the **Bank Marketing** dataset from the **UCI Machine Learning Repository**.

The dataset contains information about direct marketing campaigns conducted by a Portuguese banking institution through phone calls. The target variable `y` indicates whether the client subscribed to a term deposit (`yes` / `no`).

* **Dataset:** Bank Marketing
* **Source:** [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/222/bank%2Bmarketing)
* **Instances:** 45,211
* **Features:** 16 input features + 1 target variable
* **Target Variable:** `y`
* **File Used:** `bank-full.csv`

The project uses the `bank-full.csv` version of the dataset, which contains 45,211 records and 17 variables in total.


### Target Variable

* `y` — Indicates whether the customer subscribed to a term deposit (`yes` / `no`).

### Main Features

* `age` — Customer age
* `job` — Type of job
* `marital` — Marital status
* `education` — Education level
* `default` — Whether the customer has credit in default
* `balance` — Average yearly balance
* `housing` — Whether the customer has a housing loan
* `loan` — Whether the customer has a personal loan
* `contact` — Contact communication type
* `day` — Day of the month when the customer was contacted
* `month` — Month when the customer was contacted
* `duration` — Duration of the last contact, in seconds
* `campaign` — Number of contacts performed during the current campaign
* `pdays` — Number of days since the customer was last contacted
* `previous` — Number of contacts performed before the current campaign
* `poutcome` — Outcome of the previous marketing campaign

## Project Workflow

### 1. Data Loading & Understanding

* Loaded the dataset using Pandas
* Inspected the dataset structure
* Identified numerical and categorical features
* Examined the target variable distribution

### 2. Data Quality & Cleaning

* Checked for missing values
* Checked for duplicate records
* Investigated unknown values in categorical variables
* Examined potential numerical outliers using the IQR method
* Evaluated whether flagged values represented potential data issues or valid observations

### 3. Feature Engineering

Created grouped features to make the analysis easier to interpret:

* `age_group`

  * Young
  * Adult
  * Old

* `duration_group`

  * `< 1 min`
  * `1–3 min`
  * `3–5 min`
  * `> 5 min`

### 4. Exploratory Data Analysis

Analyzed the relationship between customer/campaign characteristics and subscription outcome.

The analysis included:

* Job vs. subscription
* Age group vs. subscription
* Housing loan vs. subscription
* Personal loan vs. subscription
* Previous campaign outcome vs. subscription
* Previous campaign contacts vs. subscription
* Call duration vs. subscription

### 5. Multivariate Analysis

Explored combinations of multiple variables to identify whether relationships observed in individual analyses changed when considering additional customer characteristics.

Examples include:

* Age group + job vs. subscription
* Housing loan + personal loan + credit default vs. subscription

Sample size was considered when interpreting subgroup rates, especially for small combinations.

### 6. Data Visualization

Created focused visualizations for the strongest findings:

* Subscription Rate by Age Group
* Subscription Rate by Job
* Subscription Rate by Call Duration
* Subscription Rate by Previous Campaign Outcome

The visualizations were selected to communicate the most meaningful patterns rather than creating a chart for every variable.

## Key Findings

* The **Old** age group had the highest subscription rate at approximately **42.26%**, while the **Adult** group had the lowest at approximately **9.85%**.

* Subscription rates varied across job categories. **Students** had the highest subscription rate at approximately **28.68%**, followed by **retired** customers at approximately **22.79%**.

* Subscription rates increased substantially across call-duration groups. Customers with calls longer than **5 minutes** had a subscription rate of approximately **28.17%**, compared with approximately **0.19%** for calls shorter than one minute.

* Customers with a **successful previous campaign outcome** had a substantially higher subscription rate, approximately **64.73%**.

* Customers who had been contacted in previous campaigns showed a higher subscription rate than customers with no previous contacts.

## Important Interpretation Notes

The findings in this project describe **relationships and patterns in the dataset**. They should not be interpreted as proof of causation.

Subgroup sample size was also considered when interpreting rates. A high percentage from a very small group may be less reliable than a similar percentage based on a larger number of observations.

## Tools & Libraries

* Python
* Pandas
* NumPy
* Matplotlib
* Jupyter Notebook

## Project Structure

```text
bank-marketing-campaign-analysis/
│
├── Bank_Marketing_Professional.ipynb
├── README.md
└── Dataset/
```

## Conclusion

This project demonstrates an end-to-end **Exploratory Data Analysis workflow** on a real-world bank marketing dataset.

The analysis focuses on understanding the data, identifying meaningful patterns, validating findings through multiple perspectives, and communicating insights through clear visualizations.

This project intentionally focuses on **EDA and analysis rather than predictive machine learning**.

