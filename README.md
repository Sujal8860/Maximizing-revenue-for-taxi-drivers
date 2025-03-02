# Maximizing Revenue for Taxi Cab Drivers through Payment Type Analysis

## Overview

This project leverages NYC taxi trip data to understand how payment methods impact fare amounts and ultimately driver revenue. By conducting an in-depth exploratory data analysis (EDA), hypothesis testing, and regression modeling, the study extracts actionable insights that can help taxi companies optimize their operations.

## Problem Statement

In the fast-paced taxi booking sector, maximizing revenue is essential for driver satisfaction and long-term success. Our research aims to determine whether the method of payment (card vs. cash) has a significant effect on fare pricing.

## Objectives

Analyze the relationship between payment type and fare amount.

Test if there is a statistically significant difference in fares between card and cash transactions.

Model fare amounts based on trip duration and payment type to quantify their impact.

Recommend strategies for promoting payment methods that generate higher revenue.


## Data & Methodology

Dataset Source: NYC TLC Trip Record Data (Yellow Taxi)

## Key Variables:

### Passenger Count

### Trip Distance

### Payment Type (filtered to include only cash and card)

### Fare Amount

### Duration (computed from pickup and dropoff times)


## Data Cleaning:

Handled missing values and removed duplicates.

Filtered records (passenger count between 1 and 5; payment type as cash/card).

Outlier removal was performed using the IQR method.


## Exploratory Data Analysis (EDA):

Univariate and bivariate visualizations (countplots, histograms, boxplots, and 100% stacked bar charts) were used to understand data distributions and relationships.


## Hypothesis Testing:

A Mann–Whitney U test was conducted to compare fare amounts between card and cash rides, given the non-normal (skewed) distribution.


## Regression Analysis:

An OLS regression model was fitted with fare_amount as the dependent variable and Duration and Payment Type as predictors.

The model indicates that each additional minute increases fare by roughly $0.98, and controlling for duration, cash rides are approximately $0.28 cheaper than card rides.


## Limitations & Future Work:

Residuals are non-normally distributed. A log-transformation or robust regression may improve model fit.

Incorporating additional predictors (e.g., trip_distance, time-of-day) could refine the analysis.



## Key Findings

### Payment Type Impact:

Card payments dominate the dataset and are associated with higher fare amounts compared to cash, even after controlling for trip duration.


### Actionable Insight:

Promoting cashless transactions (e.g., via loyalty programs and digital promotions) could potentially boost overall revenue for taxi drivers.



## Recommendation

Promote Card Payments: Incentivize digital transactions to capture higher revenue per ride.

Enhance Digital Infrastructure: Improve the payment system to support seamless cashless transactions.

Further Analysis: Incorporate additional variables and consider alternative modeling techniques (e.g., log-transformation) for a more robust understanding.


Conclusion

Our analysis confirms that card transactions yield higher fares on average. This insight provides a strong basis for taxi companies to consider promoting cashless payments to maximize revenue.
