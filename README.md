# Breast Cancer PCA Analysis

## Overview
This project performs exploratory analysis and Principal Component Analysis (PCA) on the scikit-learn Breast Cancer dataset. The analysis includes data scaling, 2D PCA projection visualization, and component heatmaps for interpretation of principal components.

## Dataset
- **Source**: scikit-learn Breast Cancer dataset
- **Target Classes**: Malignant (0) and Benign (1)
- **Features**: 30 medical diagnostic features derived from breast mass images
- **Samples**: 569 records

## Analysis Workflow

### 1. Data Loading & Exploration
- Load the breast cancer dataset from scikit-learn
- Create a pandas DataFrame with feature names
- Examine dataset structure and feature descriptions

### 2. Data Preprocessing
- **Standardization**: Apply `StandardScaler` to normalize feature values (mean=0, std=1)
- Ensures all features contribute equally to PCA

### 3. Principal Component Analysis
- Perform PCA with 2 components to reduce dimensionality
- Fit PCA model on scaled data
- Transform data to 2D principal component space

### 4. Visualization
- **2D Scatter Plot**: Visualize the relationship between the first two principal components, colored by target class
  - X-axis: First Principal Component
  - Y-axis: Second Principal Component
  - Clear separation between malignant and benign cases
  
- **Component Heatmap**: Display the contribution of each original feature to PC1 and PC2
  - Identifies which features contribute most to variance in each component
  - Useful for interpreting the principal components

## Key Findings
- The first two principal components capture significant variance in the data
- Clear visual separation between malignant and benign tumors in the 2D projection
- Component heatmap reveals which medical features are most influential in distinguishing between tumor types

## Technologies Used
- **Python 3.x**
- **pandas**: Data manipulation
- **numpy**: Numerical computing
- **scikit-learn**: Machine learning (data loading, scaling, PCA)
- **matplotlib**: Visualization
- **seaborn**: Statistical data visualization

## Files
- `pca-breast-cancer-analysis.ipynb`: Main Jupyter notebook containing the complete analysis
- `README.md`: This file

## How to Run
1. Install required packages: `pip install pandas numpy scikit-learn matplotlib seaborn`
2. Open the Jupyter notebook: `jupyter notebook pca-breast-cancer-analysis.ipynb`
3. Execute cells in order to reproduce the analysis

## Output
The notebook generates:
- Dataset summary and feature descriptions
- Scaled data shape confirmation (569, 30)
- Reduced data shape after PCA (569, 2)
- 2D PCA scatter plot showing class separation
- Heatmap showing feature contributions to principal components
