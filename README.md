# PCA


This repository contains Principal Component Analysis (PCA) Implementation from scratch and using sci-kit learn:

- `Implementation.ipynb` contains implementation of PCA from scratch.

- `PCA step-by-step.ipynb` contains implementation of PCA using `scikit-learn` on Mnist Dataset.

# What is PCA?

**Principal Component Analysis (PCA)** is a dimensionality reduction technique used in data analysis and machine learning. It helps you to reduce the number of features in a dataset while keeping the most important information. It changes your original features into new features these new features don’t overlap with each other and the first few keep most of the important differences found in the original data.

## How PCA Works

1. **Standardize the Data**: Different features may have different units and scales like salary vs. age. To compare them fairly PCA first standardizes the data by subtracting the mean and dividing by the standard deviation. making each feature have:
  A mean of 0 and 
  A standard deviation of 1

2. **Calculate Covariance Matrix**: Next PCA calculates the covariance matrix to see how features relate to each other whether they increase or decrease together. 

3. **Eigenvalues and Eigenvectors**: PCA identifies new axes where the data spreads out the most:

  1st Principal Component (PC1): The direction of maximum variance (most spread).
  2nd Principal Component (PC2): The next best direction, perpendicular to PC1 and so on.
  These directions come from the eigenvectors of the covariance matrix and their importance is measured by eigenvalues.

4. **Pick the Top Directions & Transform Data**: After calculating the eigenvalues and eigenvectors PCA ranks them by the amount of information they capture. We then:

  Select the top k components hat capture most of the variance like 95%.
  Transform the original dataset by projecting it onto these top components.
  This means we reduce the number of features (dimensions) while keeping the important patterns in the data.

## Key Benefits of PCA

- **Dimensionality Reduction**: PCA helps to reduce the number of features in a dataset while preserving the important information, making computations more efficient.
  
- **Visualization**: PCA can reduce data to 2 or 3 dimensions, making it easier to visualize.
  
- **Noise Reduction**: By focusing on components with the highest variance, PCA can reduce the influence of noise and irrelevant features.

## When to Use PCA

- When you have a large number of features and want to reduce complexity without losing significant information.
- When you want to eliminate multicollinearity among features.
- When you need to visualize high-dimensional data in 2D or 3D space.

## Example Use Case

PCA is often used in image processing, such as in the **MNIST digit classification problem**. Here, PCA can reduce the number of pixels (features) in the dataset while retaining the essential information for classifying handwritten digits.




### Requirements
Make sure you have the following libraries installed:

`numpy`

`pandas`

`matplotlib`

`scikit-learn`



### Contributing
Contributions are welcome! Please feel free to submit a Pull Request or open an issue to discuss any changes or improvements.
