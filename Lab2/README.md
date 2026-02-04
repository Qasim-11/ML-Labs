# MNIST Unsupervised: Digit Discovery with Clustering

This notebook explores the **MNIST dataset** without using any ground-truth labels. The goal is to see if a machine can naturally group handwritten digits together based purely on pixel patterns using a Gaussian Mixture Model (GMM) pipeline.

## 🚀 The Pipeline

The project follows a standard unsupervised learning workflow to handle the high dimensionality of image data:

1. **Data Scaling**: Normalizing pixel intensities to ensure the model isn't biased by high-variance features.
2. **PCA (Dimensionality Reduction)**: Compressing the 784-pixel space down to the most significant components to speed up training and remove noise.
3. **Gaussian Mixture Model (GMM)**: An advanced clustering algorithm that uses probability distributions to identify the underlying "shapes" of different digits.

## 🛠️ Key Features

* **Interactive 3D Visualization**: Uses PCA to project the high-dimensional data into a 3D space you can rotate and explore.
* **Cluster Inspection**: Logic to visualize the "mean image" of each cluster to see what the model thinks a typical '0' or '8' looks like.
* **Performance Analysis**: Comparison between different dimensionality settings to see how much "information" is needed to distinguish a 4 from a 9.

## 📦 Requirements

```bash
pip install pandas numpy matplotlib scikit-learn plotly

```

## 📊 Results

By reducing the data to 196 principal components and applying GMM, the model successfully separates distinct digits into 10 clusters. While unsupervised models occasionally mix up similar digits (like 7s and 9s), the resulting "cluster templates" clearly represent the structure of the MNIST dataset.
