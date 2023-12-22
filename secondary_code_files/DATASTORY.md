## Introduction
This is us.
How does actor fame influence movie rating?
- fame in terms of awards, online popularity and connections between actors

## Popularity analysis
Famous is better.

## Network analysis
Networks are nice to have.

## Financial analysis
Our focus is typically on ratings as the primary metric, but isn't the financial aspect of the movie industry just as fascinating? Is there a direct connection between movie ratings and their financial success? And do you think the fame of an actor could sway a movie's revenue potential? Let's dive in and find out!

### Inital Exploration

We started by merging the ADA movies dataset with our budget data, resulting in a curated collection of films where each entry is equipped with both revenue and budget data. These figures were then adjusted for inflation using our CPI data, ensuring that the temporal factors within the dataset are accounted for.

Upon examining the distribution of our data over the years, which movies surprise you the most when looking at their rating or revenue?

{% include fin_first_viz.html %}

### Correlation & Regression Analysis
Diving into the analysis, a Pearson correlation coefficient of 0.23622 indicates a slight positive correlation between higher ratings and increased revenues. Moreover, employing linear regression to model the relationship between ratings (as the independent variable) and revenues (as the dependent variable) yields a coefficient of 7e07. This suggests that, on average, each additional rating point could mean an approximate $70,000,000 increase in movie revenue.

Incorporating the budget as an independent variable confirms that ratings are the dominant predictor, maintaining the established relationship with revenue.

{% include fin_lin_reg.html %}

### Quartiles Analysis
When we segment the data into rating quartiles—specifically, 5.9 (25th percentile), 6.5 (50th percentile), and 7.1 (75th percentile)—the trend persists: movies with higher ratings tend to generate higher revenues.

{% include fin_quartiles_box.html %}

### Checking causation
To distinguish causation from mere correlation between ratings and revenues, we calculated the propensity score for each movie, considering budget and year as potential confounders. We set the threshold for a high rating at the 50th percentile, classifying ratings above 6.5 as 'high'. This categorization yielded two groups for comparison: the treated (high rating) and the control (low rating). After pair matching based on the propensity score, the average revenues of the treatment group and the control group stood at $219,224,169.79 and $106,129,755.70. This underscores that movies with higher ratings typically garner higher revenues.

In the next graphic we visualize the average revenue of both groups, alongside their respective 95% confidence intervals.

{% include fin_revenue_paired.html %}

Afterwards, to see if there is a meaningful difference betwenn the two, a paired T-test is conducted to ascertain the statistical significance of the revenue differences between the treatment and control groups. The results confirm the significance of the disparity. Additionally, when observing the difference between the treatment and control groups over the years, we found that movies in the treatment group outperformed those in the control group revenue-wise in 93% of the years. 

Have a look below to see how treatment and control group revenues change over the years!

{% include fin_revenue_paired_years.html %}

### Results of financial analysis

Finalizing our financial analysis, the data presents compelling evidence that creating a movie with favorable ratings is not only artistically gratifying but is also highly likely to succeed financially, providing great rewards for the cast and directors involved.




