# Introduction
This is us.
How does actor fame influence movie rating?
- fame in terms of awards, online popularity and connections between actors

# Popularity analysis
Famous is better.

# Network analysis
Networks are nice to have.

# Financial analysis

The whole time we focussed on ratings as the main metric. But what about money? Is there any link between movie ratings and their financial success? Can we claim that actor fame also influences a movie's revenue potential? Let's have a look!

## Inital Exploration

To start with, we combined the ADA movies dataset (link) with the budget dataset (link) and to get a cleaned dataset where each movie has renvenue and budget data. Afterwards we adjusted them for inflation  with our CPI data (link), to consider the time series aspect of the dataset.

{% include fin_first_viz.html %}

## Correlation & Regression Analysis
There is correlation

{% include fin_lin_reg.html %}

## Quartiles Analysis
Quartiles for everything

{% include fin_quartiles_box.html %}

## Checking causation
Pair matching here

{% include fin_revenue_paired.html %}

Distribution over years

{% include fin_revenue_paired_years.html %}



