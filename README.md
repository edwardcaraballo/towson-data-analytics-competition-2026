# U.S. County Health Analysis Project

## Overview:

This project analyzes county-level health insurance coverage, health outcomes, and socioeconomic factors using the 2025 County Health Rankings & Roadmaps dataset. The focus of this analysis is to identify where insurance gaps overlap with poor health outcomes, determine which factors are most strongly associated with those outcomes, and develop data-driven recommendations for targeted public health intervention.

## Project Structure:
- notebooks/ - Jupyter notebooks used for overlap analysis and regression modeling

- data/ - Dataset used for the analysis

- visuals/ - Final charts and visualizations used in the project

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
![Lowest Avg Number of Physically Unhealthy Days](https://github.com/edwardcaraballo/towson-data-analytics-competition-2026/blob/main/visuals%3A/LowestPhysUnhealthyDays2.png)

![Lowest % Fair or Poor Health](https://github.com/edwardcaraballo/towson-data-analytics-competition-2026/blob/main/visuals%3A/LowestPctPoorHealth2.png)

![Highest % Fair or Poor Health](https://github.com/edwardcaraballo/towson-data-analytics-competition-2026/blob/main/visuals%3A/HighestPctPoorHealth.png)

![Highest % Uninsured](https://github.com/edwardcaraballo/towson-data-analytics-competition-2026/blob/main/visuals%3A/HighestPctUninsured.png)

### 2. Overlap Analysis
A heatmap was created using the 10 counties with the highest uninsured rates to determine which counties also ranked poorly across other health outcomes.

![Counties with Highest Uninsured Rates and Overlapping Health Vulnerabilities Heatmap](https://github.com/edwardcaraballo/towson-data-analytics-competition-2026/blob/main/visuals%3A/HeatmapCaraballo.png)


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

![Mental Health Regression](https://github.com/edwardcaraballo/towson-data-analytics-competition-2026/blob/main/visuals%3A/MentallyUnhealthRegression.png)

![Physical Health Regression](https://github.com/edwardcaraballo/towson-data-analytics-competition-2026/blob/main/visuals%3A/PhysRegression.png)

![Fair or Poor Health Regression](https://github.com/edwardcaraballo/towson-data-analytics-competition-2026/blob/main/visuals%3A/FairPoorHealthRegression.png)

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

## How to run:
- Download the entire repository to your local machine
- Open a terminal and navigate to the project root folder
```bash
cd /path/to/county-health-analysis
- Install required packages (if not already installed)
pip install pandas matplotlib scikit-learn jupyter
- Launch Jupyter Notebook from the project root folder
jupyter notebook
- In the Jupyter interface that opens in your browser, open the notebook located in the notebooks/ folder
- Run the notebook cells in order
<sub>Note:
This project uses relative file paths, so it will run as long as the folder structure remains the same. Do not move the notebook, data, or visuals out of their respective folders. Always launch Jupyter Notebook from the project root folder so the relative paths work correctly.</sub>
