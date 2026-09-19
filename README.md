# Statistics-Project
# Overview
This project performs a statistical analysis of a Customer Behavior Dataset using Python. The dataset contains customer information such as gender, region, purchase amount, product category, churn status, and campaign group.
The analysis focuses on descriptive statistics, outlier detection, distribution analysis, hypothesis testing, ANOVA, chi-square testing, the Central Limit Theorem, and confidence intervals.
# Dataset
- Rows: 5,000
- Columns: 7

# Columns
- CustomerID – Unique customer identifier
- Gender – Customer gender
- Region – Customer region
- PurchaseAmount – Amount spent by the customer
- ProductCategory – Product category
- Churn – Whether the customer churned
- CampaignGroup – Email campaign group (A or B)
# Missing Values
The dataset contains missing values in several columns:
| Column | Missing Values|
|--- |---:|
| CustomerID | 0 |
| Gender | 97 |
| Region | 175 |
| PurchaseAmount | 150 |
| ProductCategory | 526 |
| Churn | 265 |
| CampaignGroup | 185 |

# Statistical Analysis
# - 1. Average, Median, and Mode of PurchaseAmount
- Mean: 1003.95
- Median: 998.08
- Mode: 0.00
The mean and median are relatively close, while the mode is 0.00.
# - 2. Outlier Detection
The IQR method was used to identify outliers.
- Q1: 673.64
- Q3: 1327.08
- IQR: 653.44
- Lower limit: -306.51
- Upper limit: 2307.23
- Number of outliers: 15
The detected outliers are purchase amounts above the upper limit.
# - 3. Skewness and Kurtosis
- Skewness: 0.1061
- Kurtosis: -0.2615
The skewness is close to zero, indicating that the distribution is only slightly positively skewed. The negative kurtosis indicates a flatter distribution compared with a normal distribution.
# - 4. Male vs Female Spending
An independent two-sample t-test was used to compare purchase amounts between male and female customers.
- Male average: 1019.18
- Female average: 987.87
- T-statistic: 2.2348
- P-value: 0.0255
At the 5% significance level, the test result indicates a statistically significant difference in average spending between the two groups.
# - 5. Product Category and Customer Churn
A chi-square test of independence was used to examine the relationship between ProductCategory and Churn.
- Chi-square statistic: 0.3960
- Degrees of freedom: 2
- P-value: 0.8204
The result does not provide evidence of a statistically significant relationship between product category and customer churn.
# - 6. Purchase Amount Across Regions
One-way ANOVA was used to compare purchase amounts across South, West, North, and East regions.
Average purchase amounts:
- South: 997.60
- West: 995.25
- North: 1013.02
- East: 1009.95
- Test results:
- F-statistic: 0.3897
- P-value: 0.7605
The result does not provide evidence of a statistically significant difference in purchase amounts across the four regions.
# - 7. Campaign A vs Campaign B
An independent two-sample t-test was used to compare the average purchase amount between Campaign A and Campaign B.
- Campaign A average: 1011.95
- Campaign B average: 994.34
- T-statistic: 1.2431
- P-value: 0.2139
Although Campaign A has a higher observed average purchase amount.
# - 8. Normality of PurchaseAmount
The D'Agostino-Pearson normality test was applied to PurchaseAmount.
- Test statistic: 27.2516
- P-value: 1.2089 × 10⁻⁶
The test result indicates that the PurchaseAmount data do not follow a normal distribution according to this test.
# - 9. Central Limit Theorem
To demonstrate the Central Limit Theorem, 1,000 samples of size 30 were randomly selected with replacement and their means were calculated.
- Original mean: 1003.95
- Mean of sample means: 1004.10
- Standard deviation of sample means: 91.12
The mean of the sample means is very close to the original population mean. The notebook also includes a histogram showing the distribution of the sample means.
# - 10. 95% Confidence Interval
A 95% confidence interval was calculated for the average PurchaseAmount using the t-distribution.
- Sample mean: 1003.95
- Standard error: 6.92
- Margin of error: 13.57
- Lower bound: 990.38
- Upper bound: 1017.52
Therefore, the calculated 95% confidence interval for the mean purchase amount is approximately 990.38 to 1017.52.
# Key Insights
- The average purchase amount is approximately 1003.95.
- There are 15 detected outliers using the IQR method.
- PurchaseAmount shows only slight positive skewness.
- The male and female groups show a statistically significant difference in purchase amount in the t-test used.
- Product category and churn do not show a statistically significant relationship in the chi-square test.
- Purchase amounts do not show a statistically significant difference across regions in the ANOVA test.
- Campaign A has a higher observed average than Campaign B, but the difference is not statistically significant.
- The normality test indicates that PurchaseAmount is not normally distributed.
- The Central Limit Theorem demonstration shows that the mean of repeated sample means is close to the original mean.
- The estimated 95% confidence interval for the population mean purchase amount is approximately 990.38–1017.52.
# Technologies and Libraries
- Python
- Pandas
- NumPy
- SciPy
- Matplotlib
- Seaborn
# Statistical Methods Used
- Mean, Median, Mode
- Interquartile Range (IQR)
- Skewness and Kurtosis
- Independent Two-Sample t-test
- Chi-Square Test of Independence
- One-Way ANOVA
- D'Agostino-Pearson Normality Test
- Central Limit Theorem
- 95% Confidence Interval
# Conclusion
This project provides a statistical overview of customer purchase behavior and examines whether purchase amounts differ across customer groups, regions, and campaign groups. It also investigates the distribution of purchase amounts and demonstrates sampling concepts such as the Central Limit Theorem and confidence intervals
