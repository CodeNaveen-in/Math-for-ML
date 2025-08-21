# Inferential Statistics

- It is an important tool that allows us to make predictions and conclusions about populations based on sample data.
- We can use inferential statistics in muliple ways : 
  - Conclude whole population
  - Test Claims or Hypotheses
  - Calculate confidence intervals and p-values to measure uncertainty
  - Make predictions with statistical models.

# Techniques in Inferential Statistics

## 1. Confidence Intervals
- It gives a range of values that likely include population parameter.
- it helps us quantify the uncertainty of an estimate.

$$
CI = \bar{x} ± Z_\frac{\alpha}{2} X \frac{\sigma}{\sqrt{n}}
$$

Where 
- $\bar{x}$ - is the sample mean
- $Z\frac{\alpha}{2}$ is the Z-value from the standard normal distribution.
- $\sigma$ is the population standarad deviation
- n is the sample size.

*(if we measure the average height of 100 people, a 95% confidence interval gives us a range where the true population mean height is likely to fall. This helps gauge the precision of our estimate and compare models (like in A/B testing).)*

## 2. Hypothesis Testing
- It is the formal procedure for testing claims or assumptions about data. 
- Steps involved are : 
  - **Null Hypothesis (${H_0}$)** - It is the default assumption *(Such as there is no difference in models)*
  - **Alternative Hypothesis (${H_1}$)** - It is the claim you prove *(Such as Model A performs better than Model B)*
- We use the data to form a test statistic *(Z or T for respective test)*

$$
Z = \frac{ \bar{x} - \mu_0}{\frac {\sigma} {\sqrt{n}}}
$$
 - Where we have 
   - $\bar{x}$ is the sample mean
   - ${\mu_0}$ is the hypothesised population mean
   - ${\sigma}$ is the population standard deviation
   - $n$ is the sample size
 - After obtaining test statistic we compare it with critical value (or p-value) to decide wheither to accept or reject null hypothesis.

$$
p\text{-value} = 2 \cdot P(Z > |Z_{\text{obs}}|)
$$

- where $Z\text{obs}$ is the observed statistic.
- Small p-value suggest evidence against the null hypothesis.

## 3. Central Limit Theorem
- It states that the distribution of sample mean will approximate a normal distribution as sample size increases regardless of original population distribution.
- This theorem allows us to appply normal distribution-based methods to data that is not normally distributed *(such as skewed income or shopping behaviour)*
- It is important as many methods assume that data is normally distributed.

$$
\bar{X} \sim N (\mu , \frac{\sigma}{\sqrt{n}})
$$

Where we have
- $\mu$ is the population mean
- $\sigma$ is the population standard deviation
- $n$ is the sample size

# Errors in Inferential Statistics
- **Type I Error**
  - Occurs when we wrongly reject a true null hypothesis.
  - It is denoted by $\alpha$ (The significance level)
- **Type II Error**
  - Occurs when we fail to reject a false null hypothesis.
  - Probablity of making that error is noted by $\beta$ (power of test is given by $1-\beta$)
- The goal is to minimize them.

# Parametric and Non Parametric Tests
- They help understand if the data support a hypothesis.
- They show how much a data differs from assumption(null hypothesis)

## Parametric test
- They assume that data follows a specific distribution (normal mostly) and has consistent variance.
- Typically used for continous data.
- Examples : 
  - Z-test, T-test, and ANOVA.

## Non parametric test
- They do not assume a specific distribution for the data.
- Ideal for small samples or non normal data including categorical data.
- Examples
  - Chi-Square test, Mann-Whitney test, Kruskal-Wallis test.

# Example
A quick commerce company wants to check if a new delivery algorithm reduces delivery times compared to the current system.

**Experiment Setup:**

- 100 orders split into two groups: 50 with the new algorithm, 50 with the current system.
- Delivery times for both groups are recorded.

## Steps 

### Hypotheses
- **Null (H0):** The New algorithm does not reduce delivery time.
- **Alternative (H1):** New algorithm reduces delivery time.

### Significance Level:
- Set at 0.05 (5% risk of wrongly rejecting H0).
- **Type I error:** Thinking the new system is better when it isn’t.
- **Type II error:** Missing a real improvement.

### Test Statistic
- Compare average delivery times between the two groups

### Analysis:
- Calculate means and differences.
- Check if the data is roughly normal.

### Perform a t-test or z-test.
- If p-value < 0.05, reject H0 and conclude the new algorithm is better. Otherwise, no clear improvement.
- Confidence Interval: For example, a range of -5 to -2 minutes means deliveries are 2 to 5 minutes faster with the new system.