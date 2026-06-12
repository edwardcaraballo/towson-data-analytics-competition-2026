# U.S. County Health Analysis Project

## Overview:

This project analyzes county-level health insurance coverage, health outcomes, and socioeconomic factors using the 2025 County Health Rankings & Roadmaps dataset. The focus of this analysis is to identify where insurance gaps overlap with poor health outcomes, determine which factors are most strongly associated with those outcomes, and develop data-driven recommendations for targeted public health intervention.

## Project Structure:
- notebooks/ - Jupyter notebooks used for overlap analysis and regression modeling
- data/ - Dataset used for the analysis
- visualizations/ - Final charts and visualizations used in the project
- presentation/ - Final PowerPoint presentation
- report/ - One-page competition summary report

## Data Preparation Steps:
- Selected relevant variables related to uninsured rate, health outcomes, and social determinants
- Removed rows with missing county names and incomplete records where necessary
- Cleaned and filtered the dataset for overlap and regression analysis
- Ranked counties across major health outcome variables
- Standardized predictor variables before regression so coefficient strength could be compared fairly

## Analytical Approach:

### 1. Descriptive Ranking
Counties were ranked to identify the best and worst performers in:
- % Uninsured
- % Fair or Poor Health
- Average Number of Physically Unhealthy Days
- Average Number of Mentally Unhealthy Days

![Lowest Avg Number of Physically Unhealthy Days](https://github.com/edwardcaraballo/towson-data-analytics-competition-2026/blob/main/visualizations%3A/LowestPhysUnhealthyDays2.png)

![Lowest % Fair or Poor Health](https://github.com/edwardcaraballo/towson-data-analytics-competition-2026/blob/main/visualizations%3A/LowestPctPoorHealth2.png)

![Highest % Fair or Poor Health](https://github.com/edwardcaraballo/towson-data-analytics-competition-2026/blob/main/visualizations%3A/HighestPctPoorHealth.png)

![Highest % Uninsured](https://github.com/edwardcaraballo/towson-data-analytics-competition-2026/blob/main/visualizations%3A/HighestPctUninsured.png)

### 2. Overlap Analysis
A heatmap was created using the 10 counties with the highest uninsured rates to determine which counties also ranked poorly across other health outcomes.

![Counties with Highest Uninsured Rates and Overlapping Health Vulnerabilities Heatmap](https://github.com/edwardcaraballo/towson-data-analytics-competition-2026/blob/main/visualizations%3A/HeatmapCaraballo.png)

### 3. Multiple Linear Regression
Separate regression models were run for:
- Average Number of Physically Unhealthy Days
- Average Number of Mentally Unhealthy Days
- % Fair or Poor Health

The predictors tested were:
- % Some College
- % Completed High School
- 80th Percentile Income
- % Unemployed
- % Severe Housing Problems
- Food Environment Index

![Mental Health Regression](https://github.com/edwardcaraballo/towson-data-analytics-competition-2026/blob/main/visualizations%3A/MentallyUnhealthRegression.png)

![Physical Health Regression](https://github.com/edwardcaraballo/towson-data-analytics-competition-2026/blob/main/visualizations%3A/PhysRegression.png)

![Fair or Poor Health Regression](https://github.com/edwardcaraballo/towson-data-analytics-competition-2026/blob/main/visualizations%3A/FairPoorHealthRegression.png)

## Key Findings:

**Priority Counties for Intervention:**
- Kenedy County, Texas
- Presidio County, Texas
- Hidalgo County, Texas

These counties showed the strongest overlap between high uninsured rates and poor health outcomes.

**Strongest Predictors:**
- Education-related variables were the strongest predictors across all three regression models
- % Some College was the strongest predictor in the physical and mental health models
- % Completed High School was strongest in the % Fair or Poor Health model

**Benchmark Patterns:**
- Texas counties dominated the worst uninsured and poor health rankings
- West Virginia counties stood out in mentally unhealthy days
- Strong performers such as Lincoln County, South Dakota and Falls Church City, Virginia consistently ranked well across multiple measures

## Key Takeaways:
- Not every county with high uninsured rates faces the same level of burden
- Kenedy, Presidio, and Hidalgo stood out because insurance gaps and poor health outcomes were stacking on top of each other
- Education-related variables were the most consistent predictors of poor health outcomes across all three models
- Short-term recommendations should focus on reducing the health consequences of unemployment, especially loss of insurance and reduced access to care
- Long-term improvement likely requires stronger educational opportunity in the most vulnerable counties

## Public Health Recommendations:
- Expand insurance enrollment outreach in high-priority counties to help eligible residents enroll in Medicaid or Marketplace coverage
- Increase access to care through mobile clinics in harder-to-reach areas
- Invest in community health workers who can help residents navigate coverage and connect to care
- Support partnerships with school districts, workforce development programs, and community colleges to strengthen long-term educational opportunity

## Data Source:
2025 County Health Rankings & Roadmaps (CHR&R)

## Tools Used:
- Python (pandas, scikit-learn, matplotlib, Jupyter Notebook)
- Microsoft Excel
- PowerPoint

## How to Run

### 1. Download the Project

Click the green **Code** button on this GitHub page, then click **Download ZIP**.

After the ZIP file downloads, unzip the folder.

---

### 2. Open a Terminal in the Project Folder

Open the main project folder. This is the folder that contains:

```txt
README.md
data/
notebooks/
presentation/
report/
visualizations/
```

On Mac, right-click the project folder and choose **New Terminal at Folder**.

On Windows, right-click the project folder and choose **Open in Terminal**.

---

### 3. Install Required Packages

Copy and paste this into the terminal:

```bash
python -m pip install pandas matplotlib scikit-learn jupyter openpyxl
```

If you are on Mac and `python` does not work, use this instead:

```bash
python3 -m pip install pandas matplotlib scikit-learn jupyter openpyxl
```

---

### 4. Launch Jupyter Notebook

Copy and paste this into the terminal:

```bash
jupyter notebook
```

---

### 5. Open and Run the Notebook

When Jupyter opens in your browser, click the `notebooks` folder.

Open the `.ipynb` notebook file and run the cells in order.

The project should run correctly as long as the original folder structure stays the same.
