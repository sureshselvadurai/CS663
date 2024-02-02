# Principal Component Analysis (PCA) in Machine Learning

## PCA Objectives
- **Reduce Model Size:**
  - Applicable in high-dimensional models.
  - Size refers to the number of model features, not inputs.
- **Ensure Feature Independence:**
  - PCA guarantees uncorrelated features.
  - Uses a linear combination of inputs as new features.
  - Each principal component is orthogonal to all others.
- **Side Effects:**
  - Loss of model interpretability.
  - Potential gain in insight through data visualization.

## Basic ML Algorithms
- **Analysis (Unknown Target):**
  - Principal Component Analysis
- **Regression (Known Target - Real Number):**
  - Linear, LASSO, Ridge, Polynomial
  - K-Nearest Neighbours
  - Decision Trees (CART) & Ensembles
  - Deep Neural Networks - regression
- **Clustering (Unknown Target - Class/Category/Grouping):**
  - k-Means
  - DBSCAN, Hierarchical
- **Classification (Known Target - Class/Category/Grouping):**
  - Logistic Regression
  - K-Nearest Neighbours
  - Decision Trees (CART) & Ensembles
  - Deep Neural Networks - classification

## PCA: How, Why, and When
- **How:**
  - Eigendecomposition.
  - Normalize data before applying PCA.
- **Why:**
  - Captures most data variance.
  - Linear transformation of correlated input variables into fewer uncorrelated variables.
- **When to Use PCA:**
  - Collinearity exists.
  - Data is noisy and needs denoising or compression.
  - High-dimensional data that needs reduction.

## Temperature Data
- Example of temperature data for various cities.

## Determine Eigenvector (PCA Steps)
- Scaling features.
- Determining the origin (mean values for each feature).
- Subtracting mean value.
- Calculating principal components using covariance matrix and eigenvalues.

## Number of Components to Choose
- Arbitrary choice or based on:
  - Proportion of variance explained.
  - Elbow method.

## Other Component Analysis
- Mention of other component analysis techniques like KernelPCA and GaussianRandomProjection.

## PCA in scikit-learn
- Explanation of sklearn functions for PCA.

## Practical Considerations
- Sensitivity to outliers, normalize data before using PCA.
- Example using sklearn.decomposition.PCA.

## Summary
- PCA allows describing a dataset in fewer dimensions.
- Lower-dimensional datasets may enhance model speed and accuracy.
- Principal components are orthogonal.
- The first principal component explains the maximum variance.
- Practice considerations: sensitivity to outliers, normalization.

[Source](https://www.cgtrader.com/3d-models/science/other/glucose-molecular)
