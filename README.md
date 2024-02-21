# Causal Inference

This repository is dedicated to applying causal inference techniques to real-world business challenges and is part of APPM 6900 Independent Study in Causal Inference at the University of Colorado, Boulder.

## Business Case
The project focuses on leveraging causal analysis to optimize discounting strategies for an e-commerce businesses, showcasing how to predict the impact of various actions on business outcomes and key performance indicators (KPIs).

The company wishes to use discounts to boost sales and hence, profits. But while discounting does boost sales, in the long run, it has a direct negative impact on profits: whatever you give as a discount you don’t make as earnings. The e-commerce company states that each customer’s profitability is given as follows:

$$
Profits_i = Sales_i * 0.05 - Discount_i
$$


## Techniques

1. [Bias Adjustment Using Linear Regression](bias_adjustment.ipynb):
Leveraged linear regression to adjust for bias, improcing the quality and reliablity of the the data analysis.

Before debiasing and denoising
![2](images/pre_debiasing.jpg)

After debiasing and denoising
![](images/post_debiasing.jpg)

We see that the customers with high residualized discounts no longer have high sales_prediction_bins. The regression adjustment has made the residual discount seem as good as randomly assigned.


2. [Regression Discontinuity Design](rdd.ipynb):
Used regression discontinuity design (RDD) as a form of natural experiment as an alternative to A/B testing. RDD measures treatment effects at points of discontinuity to get an idea of the effectiveness of a program without needing to rigorously A/B test it.

![rdd_kernel](images/rdd_kernel.png)

3. [Difference in Differences](difference_in_differences.ipynb):
Employed Difference-in-Differences (DiD) methodology to evaluate the impact of policy changes or interventions over time by comparing the differences in outcomes before and after the treatment across treated and control groups.

![](images/did.png)

4. [Synthetic Control](difference_in_differences.ipynb)
Utilized the Synthetic Control Method to construct a counterfactual scenario using a weighted combination of control units that closely resemble the treated unit(s) before the intervention.

![](images/synthetic_control.png)

We see the profits for MG decreasing after the intervention which suggests that the effect of discounts on profit is negative.

The project closely follows the excellent course offered by [Matheus Facure.](https://matheusfacure.github.io)