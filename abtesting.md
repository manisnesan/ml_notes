# AB Testing

## Resource
- [Complete Guide to A/B Testing Design, Implementation and Pitfalls](https://towardsdatascience.com/simple-and-complet-guide-to-a-b-testing-c34154d0ce5a)

## Notes

- When : To test new U/X features, new versions of a product
- Why : To decide whether business should move forward with new feature/product or not
- What: variant version of product shown to experimental group of users and current version of product to different sample of users (control group) - product performance is measured b/w these two groups for a test period -- perf diff is determined and used to make a decision about the new variant of the product - what type of diff

- Motivation: test new product variants to improve the perf of existing product.

- Benefits
  * Understand what works & what doesn't quickly 
  * Direct feedback from users/customers
  * Unbiased results 

- Demerits
  * Change Aversion due to presenting different variant of the same product to users in the same geolocation.
  * Significatn resources from Product, Engg, DS
  * Incorrect conclusion if not conducted properly

- Questions to ask before A/B test
  - Sample Population | Customer Segments
  - is historical analysis conducted?
  - single | multiple variants test
  - truly randomized control & exp groups?
  - integrity preserved during the test duration?

- Choice of Primary Metric
  - Metics Validity Question: If chosen metric increased significantly while everything else stays constant, would be achieve our goal and address the problem?
  - Choose Single primary metric to identify if there is a statistically significant difference. 
  - Click Through Rate (CTR) = # of clicks / (# of clicks + # of impressions) * 100
  - Click Through Propability(takes duplicates into account)  = # of people with >= 1 click / # of unique visitors per page * 100   
  - Conversion Rate (CR) = #converted / (#converted + #notconverted)


- Test Hypothesis
  - stating a solution that would fix a problem iin the product leading to an increase in KPI
  - prioritize on the biggest product impact from the list of problems
  - Example: Improve quality of recommendations by adding XGBoost reranker to increase CTR in recommendations


- Design of the test
  * Statistical Hypothesis
  * Power Analysis 
    1. power test (80%) - proba of making a correct decision ( rejecting null hypothesis) - 20% Type II error
    2. significance level of the test - proba of Type I error (5%)
    3. min. detectable effect
  * 

- Calc Sample Size, Test Duration

- Statistical Tests (T-test, Z-test, Chi-squared test)

- Analysing A/B test results in python

- Statistical significance vs Practical Significance 

- Quality of A/B test (reliability, validity, potency)

- Common problems & pitfalls of A/B test
  * Confounding effects : all known possible factors having an impact on dep var is kept constant. To mitigate 1. control confounding var  2. appropriate choice of ind & dep vars 3. generation of random sample
  * Selection bias - every user has an equal chance of being selected as a sample
  * Systemic bias - relates to the way one measures the impact of treatment, affects the accuracy of results
  * Early stopping or P-hacking - stop the experiment early once you observe statistically significant result
  * Spillover or N/W wffects - observed on social media platforms where the users can be connectors & one can influence other. To detect, perform Stratified sampling.
  * Change Aversion & Novelty effects - users trying out new feature due to novelty - users churn since they don't like the new  
   
   
 

- Ethics & privancy
