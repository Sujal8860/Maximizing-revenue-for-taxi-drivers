# Maximizing Revenue for Taxi Cab Drivers through Payment Type Analysis

## Overview

This project leverages NYC taxi trip data to understand how payment methods impact fare amounts and, ultimately, driver revenue. By conducting an in-depth exploratory data analysis (EDA), hypothesis testing, and regression modeling, the study extracts actionable insights that can help taxi companies optimize their operations.

## Problem Statement

In the fast-paced taxi booking sector, maximizing revenue is essential for driver satisfaction and long-term success. Our research aims to determine whether the method of payment (card vs. cash) has a significant effect on fare pricing.

## Objectives

- **Analyze** the relationship between payment type and fare amount.
- **Test** if there is a statistically significant difference in fares between card and cash transactions.
- **Model** fare amounts based on trip duration and payment type to quantify their impact.
- **Recommend** strategies for promoting payment methods that generate higher revenue.

## Data & Methodology

- **Dataset Source:** NYC TLC Trip Record Data (Yellow Taxi)
- **Key Variables:**
  - **Passenger Count**
  - **Trip Distance**
  - **Payment Type** (filtered to include only cash and card)
  - **Fare Amount**
  - **Duration** (computed from pickup and dropoff times)

## Data Cleaning

- Handled missing values and removed duplicates.
- Filtered records to include only rides with passenger counts between 1 and 5 and payment types of cash or card.
- Removed extreme outliers using the IQR method.

## Exploratory Data Analysis (EDA)

- **Univariate Analysis:**  
  Visualized the distribution of each key variable using count plots, histograms, and boxplots.
  
- **Bivariate Analysis:**  
  Compared fare amounts and trip distances by payment type using stacked bar charts and other visualizations to identify trends and patterns.

## Hypothesis Testing

- **Test Conducted:** Mann–Whitney U test  
- **Purpose:** To compare fare amounts between card and cash rides due to the skewed (non-normal) distribution.
- **Finding:** The test indicated a statistically significant difference between the two groups.

## Regression Analysis

- **Model:** Ordinary Least Squares (OLS) Regression  
- **Predictors:** Duration and Payment Type (with Payment Type as a categorical variable)  
- **Key Findings:**
  - **Trip Duration Impact:** Each additional minute increases fare by approximately **\$0.86**.
  - **Payment Type Impact:** Controlling for duration, cash rides are about **\$0.25 cheaper** than card rides.
  - **Model Fit:** The model explains **78.3%** of the variance in fare amounts (R-squared = 0.783).

## Limitations & Future Work

- **Residual Non-Normality:**  
  The Q-Q plot shows that the residuals are not normally distributed. Future analyses might benefit from a **log-transformation** of fare amounts or **robust regression** techniques.

- **Additional Predictors:**  
  Incorporating further predictors—such as **trip_distance**, **time-of-day**, or **passenger_count**—could refine the model and offer deeper insights.

## Key Findings

- **Payment Type Impact:**  
  Card payments dominate the dataset and are associated with higher fare amounts compared to cash, even after controlling for trip duration.

- **Actionable Insight:**  
  Promoting cashless transactions (e.g., via loyalty programs and digital promotions) could potentially boost overall revenue for taxi drivers.

## Recommendation

- **Promote Card Payments:**  
  Incentivize digital transactions through loyalty programs, targeted promotions, or small discounts on digital payments to capture higher revenue per ride.

- **Enhance Digital Infrastructure:**  
  Improve digital transaction systems to support cashless payments, thereby increasing operational efficiency and customer satisfaction.

- **Further Analyze Ride Characteristics:**  
  Investigate additional factors like trip distance, time-of-day, and passenger count to better understand the dynamics behind fare differences and optimize pricing strategies.

## Conclusion

Our analysis confirms that card transactions yield higher fares on average, even when controlling for trip duration. This insight provides a strong basis for taxi companies to consider promoting cashless payments as a means to maximize revenue. The combination of hypothesis testing and regression analysis supports a targeted strategy, while also highlighting the need for further exploration with additional predictors.

