# EDA Steps

1. **Understand the Data:**
   - Evaluate data quality and relevance.

2. **Cleanse the Data:**
   - Address outliers, missing data, and inconsistencies.

3. **Analyse Relationships:**
   - Explore univariate and multivariate relationships.

4. **Derive Features:**
   - Employ feature engineering techniques.

5. **Test Hypotheses:**
   - Conduct hypothesis testing on data.


# Data Types

1. **Categorical (Cat):**
   - Represents distinct categories.
   - Examples: Gender, Country.

2. **Nominal:**
   - Represents categories without order.
   - Examples: Colors, Types of Fruit.

3. **Ordinal:**
   - Represents ordered categories.
   - Examples: Education Levels, Customer Satisfaction.

4. **Interval:**
   - Represents numeric values with consistent intervals.
   - Examples: Temperature in Celsius, IQ Scores.

5. **Ratio:**
   - Represents numeric values with a true zero point.
   - Examples: Height, Weight.
# Features of Normal Distribution

- **Mean (μ):**
  - Equal to mode and median.

- **Equal Distribution:**
  - Equal number of points on the left and right of the mean.

- **Standard Deviation (σ):**
  - 68% of data falls within one standard deviation.

- **Z-Score:**
  - Measures the distance from the mean in standard deviation units.
  - Provides probability information.

- **Outliers:**
  - Typically considered as values beyond 3 standard deviations from the mean (x > 3σ).


# Z-Score in Normal Distribution

- **Z-Score Definition:**
  - A standardized score that represents the number of standard deviations a data point is from the mean.

- **Formula:**
  - Z = (X - μ) / σ
    - Z: Z-Score
    - X: Individual data point
    - μ: Mean of the distribution
    - σ: Standard deviation of the distribution

- **Interpretation:**
  - A positive Z-Score indicates a data point above the mean.
  - A negative Z-Score indicates a data point below the mean.

- **Z-Score and Probability:**
  - Z-Score is used to find the probability of a data point occurring in a standard normal distribution.

- **Outliers Detection:**
  - Commonly, values beyond 3 standard deviations (|Z| > 3) are considered outliers.


# One-Hot Encoding

- **Encoded Categorical Data:**
  - Initial encoding may create a false sense of relationship (e.g., 1 = Alabama, 2 = Alaska).

- **1-Hot Encoding:**
  - Transformation to multiple unrelated binary columns.
  - Each category becomes a binary feature column.

- **Example:**
  - Original Data:
    - 1. Alabama
    - 2. Alaska

  - After 1-Hot Encoding:
    - Alabama Column: 1 or 0
    - Alaska Column: 1 or 0

- **Purpose:**
  - Eliminates false ordinal relationships in categorical data.
  - Ensures each category is represented independently.

# Discrete Hypothesis Tests using 𝜒2

- **Contingency Table:**
  | Immigration        | Gender  | Job Offer | No Job Offer |
  | ------------------ | ------- | --------- | ------------ |
  | Domestic Female    | 17      | 6         |              |
  | Domestic Male      | 12      | 23        |              |
  | International Female| 35      | 9         |              |
  | International Male  | 14      | 7         |              |
  | **Total**           | 78      | 45        |              |

- **Calculation of 𝜒2:**
  - 𝜒2 = Σ((Expected - Observed)² / Expected)
  - Observed values from the table.
  - Expected values calculated based on independence assumption.

- **Results:**
  | 𝜒2    | Expected | Observed | P-Value   |
  | ----- | -------- | -------- | --------- |
  | 1.74  | 0.6808   | 17.38    | 0.6808    |
  | 13.38 | 0.0039   | 13.38    | 0.0039    |
  | 4.10  | 0.2509   | 4.10     | 0.2509    |
  | 0.16  | 0.9838   | 0.16     | 0.9838    |

- **Interpretation:**
  - P-values are compared to a significance threshold (e.g., 0.05) to determine if the observed pattern is statistically significant.
  - A smaller p-value suggests stronger evidence against the null hypothesis.

# Numeric Hypothesis Tests

- **Objective:**
  - Determine if the relationship between two variables is due to chance.
  - Assess if the mean values of variables are significantly different.

- **Types of Hypotheses:**
  - **H0 (Null Hypothesis):**
    - Assumes one variable is *not* dependent on another (e.g., Survival depends on Pclass).
  - **H1 (Alternative Hypothesis):**
    - Assumes variables are *not* independent.

- **Numeric Test for Significance:**
  - **Steps:**
    1. Establish a significance threshold (e.g., p = 0.05).
    2. If standard deviation is known, use a z-test.
    3. If standard deviation is unknown or N < 30, use a t-test.
    4. For more than two columns, employ an ANOVA test.
    5. Ensure the observed p-value is below the significance threshold.

- **Interpretation:**
  - A smaller p-value indicates stronger evidence against the null hypothesis.
  - If p-value < significance threshold, reject the null hypothesis.
