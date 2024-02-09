# Causal Inference

This repository is dedicated to applying causal inference techniques to real-world business challenges and is part of APPM 6900 Independent Study in Causal Inference at the University of Colorado, Boulder.

## Business Case
The project focuses on leveraging causal analysis to optimize discounting strategies for an e-commerce businesses, showcasing how to predict the impact of various actions on business outcomes and key performance indicators (KPIs).

The company wishes to use discounts to boost sales and hence, profits. But while discounting does boost sales, in the long run, it has a direct negative impact on profits: whatever you give as a discount you don’t make as earnings. The e-commerce company states that each customer’s profitability is given as follows:

$$
Profits_i = Sales_i * 0.05 - Discount_i
$$


## Techniques

1. [Bias Adjustment Using Linear Regression.](bias_adjustment.ipynb)
Leveraged linear regression to adjust for bias, improcing the quality and reliablity of the the data analysis.

2. [Regression Discontinuity Design](rdd.ipynb)
Used regression discontinuity design (RDD) as a form of natural experiment as an alternative to A/B testing. RDD measures treatment effects at points of discontinuity to get an idea of the effectiveness of a program without needing to rigorously A/B test it.

The project closely follows the excellent course offered by [Matheus Facure.](https://matheusfacure.github.io)

3. [Difference in Differences]