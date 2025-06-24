# User Behaviour Analysis and A/A/B Experiment Evaluation for a Food Retail App

## Project Overview

This project analyses user behaviour within a food retail mobile application and evaluates the outcome of an A/A/B experiment aimed at testing the impact of a new font on user conversion. The analysis focuses on user interactions captured via event logs and compares behavioral metrics across experimental groups using statistical hypothesis testing.

## Stakeholder

A startup company in the food retail industry, offering delivery services through a mobile application.

## Objectives

1. Analyse user behaviour within the app by building a product funnel and identifying drop-off points.
2. Evaluate the results of an A/A/B test designed to determine whether a new font style affects user engagement.

## A/A/B Experiment Setup

- **Group A_1 (Control 1)** – original font  
- **Group A_2 (Control 2)** – original font  
- **Group B (Experimental)** – new font  

Using two control groups allows for validating the experimental setup by confirming that both control groups behave similarly.

## Dataset

The dataset was provided by the [Yandex Practicum Data Analyst program](https://practicum.yandex.ru/) and contains event logs from **July 25, 2019 to August 7, 2019**. Due to data completeness concerns, only events from **August 1–7, 2019** were included in the analysis.

### Columns:

- `event_name`: Name of the event (e.g., screen opened, purchase made)
- `device_id`: Unique user identifier
- `event_timestamp`: Unix timestamp of the event
- `exp_id`: Experimental group ID (246 = A_1, 247 = A_2, 248 = B)

## Funnel Analysis Results

The typical user flow in the app follows this sequence:

1. Main Screen  
2. Offers Screen  
3. Cart Screen  
4. Payment Screen

- 47.7% of users completed the full funnel.
- The largest drop-off (38.1%) occurred after viewing the main screen.

## Conversion Funnel Visualisation

Each funnel stage was visualized and calculated per group using bar charts and funnel diagrams. This allowed for clear comparisons of conversion behavior across the experiment groups.

## Hypothesis Testing

### A/A Test

- **Null Hypothesis (H₀):** No significant difference in conversion rates between A_1 and A_2.  
- **Result:** Failed to reject H₀ — control groups behave identically.

### A/B Test

- **Null Hypothesis (H₀):** No significant difference in user behaviour between the control and test groups.  
- **Significance level:** 0.05 adjusted via Bonferroni correction to **0.003** (for 16 comparisons).  
- **Result:** No statistically significant differences found in any funnel event.

## Final Conclusion

- The product funnel is functioning effectively, with nearly half of users completing a purchase.
- The updated font had no measurable impact—positive or negative—on user behaviour.
- It is safe to implement the new font across all users if desired for branding or design consistency.

## Tools & Technologies

- Python
- pandas, numpy
- matplotlib, seaborn, plotly
- scipy (Z-test)
- Jupyter Notebook

## How to Use This Project

To run the project locally:

1. Clone the repository:
   ```bash
   git clone https://github.com/Kate-217/food_app_ab_test.git
   cd food_app_ab_test
    ````

2. Install required libraries:

   ```bash
   pip install pandas numpy matplotlib seaborn scipy plotly
   ```

3. Launch the notebook:

   ```bash
   jupyter notebook food_retail_proj.ipynb
   ```

4. (Optional) If using Anaconda, create a virtual environment:

   ```bash
   conda create -n ab_test_env python=3.11
   conda activate ab_test_env
   ```

## Project Structure

* `food_retail_proj.ipynb` — main analysis notebook
* `logs_exp.csv` — dataset (not included in repo for privacy)
* `README.md` — project documentation

## Author

Katerina Lisovenko


