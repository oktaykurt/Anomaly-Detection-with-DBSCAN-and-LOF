
# Anomaly Detection in Hypothyroidism Dataset Using DBSCAN and LOF

This project presents an in-depth analysis of a dataset related to hypothyroidism, focusing on anomaly detection using unsupervised learning techniques. The analysis includes data preprocessing, visualization, and the implementation of DBSCAN, Local Outlier Factor (LOF), and a combined method of both.

## Table of Contents
- [Introduction](#introduction)
- [Dataset](#dataset)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [Methodology](#methodology)
  - [Data Preprocessing](#data-preprocessing)
  - [Visual Exploration](#visual-exploration)
  - [Anomaly Detection](#anomaly-detection)
    - [Gower Distance](#gower-distance)
    - [t-SNE](#t-sne)
    - [DBSCAN](#dbscan)
    - [LOF](#lof)
    - [Combined DBSCAN and LOF](#combined-dbscan-and-lof)
- [Results](#results)
- [Discussion](#discussion)
- [Conclusion](#conclusion)
- [References](#references)
- [License](#license)

## Introduction
Hypothyroidism is a medical condition characterized by an underactive thyroid gland. Detecting anomalies in medical datasets is crucial for identifying unusual patterns that could indicate potential health issues. This study employs unsupervised learning techniques to detect anomalies in a hypothyroidism dataset.

## Dataset
The dataset contains 21 attributes (15 binary and 6 continuous) and 7,200 data objects. The attributes are anonymized and represented as `Dim_0`, `Dim_1`, etc.

## Requirements
- Python 3.6+
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- gower

## Installation
Clone the repository and install the required packages:

```bash
git clone https://github.com/oktaykurt/Anomaly-Detection-with-DBSCAN-and-LOF.git
cd Anomaly-Detection-with-DBSCAN-and-LOF
pip install -r requirements.txt
```

## Usage
1. Ensure the dataset file (`Unsupervised_Learning_23-24_Project_Dataset.csv`) is in the project directory.
2. Run the script to perform the analysis and generate visualizations:

```bash
python anomaly_detection.py
```

## Methodology

### Data Preprocessing
1. **Loading the Dataset:** The dataset is loaded from a CSV file with attributes separated by semicolons and decimals marked by commas.
2. **Dropping Unnecessary Columns:** The last two columns, which are empty due to the way the CSV file is read, are dropped.
3. **Identifying and Converting Column Types:** Binary columns are identified and converted to integer type, while continuous columns are converted to float type. The 'Row' column, serving as an index, is dropped.
4. **Handling Missing Values:** The dataset is checked for missing values. No missing values were found.

### Visual Exploration
- **Histograms of Continuous Features:** Visualize the distribution of continuous features.
- **Box Plots of Continuous Features:** Highlight the spread and potential outliers in continuous data.
- **Bar Plots of Binary Features:** Show the frequency of binary attributes.
- **Correlation Matrix Heatmap:** Visualize the correlation between features.

### Anomaly Detection
- **Gower Distance:** Used for handling mixed data types, combining distances of binary and continuous attributes.
- **t-SNE:** Dimensionality reduction technique for visualizing high-dimensional data.
- **DBSCAN:** Density-based clustering algorithm.
- **LOF:** Local Outlier Factor algorithm for anomaly detection.
- **Combined DBSCAN and LOF:** A method leveraging both DBSCAN and LOF to enhance anomaly detection.

## Results
The analysis includes multiple figures to illustrate the findings:
1. **Histograms of Continuous Features**
2. **Box Plots of Continuous Features**
3. **Bar Plots of Binary Features**
4. **Correlation Matrix Heatmap**
5. **t-SNE of Gower Distance Matrix**
6. **3D Scatter Plot of eps, min\_samples, and Silhouette Score**
7. **DBSCAN Clustering (t-SNE)**
8. **DBSCAN Clustering with Anomalies Highlighted (t-SNE)**
9. **DBSCAN Pair Plot of Continuous Features Highlighting Anomalies**
10. **Histogram of Anomaly Counts (LOF)**
11. **LOF Clustering with Anomalies Highlighted**
12. **LOF Pair Plot of Continuous Features Highlighting Anomalies**
13. **LOF Values**
14. **Comparison of Outliers Detected by DBSCAN and LOF**
15. **Number of Anomalies Detected by Each Technique**
16. **Combined DBSCAN and LOF Clustering with Anomalies Highlighted**
17. **Combined DBSCAN and LOF Pair Plot of Continuous Features Highlighting Anomalies**

## Discussion
The analysis demonstrates the effectiveness of DBSCAN and LOF in detecting anomalies in the hypothyroidism dataset. The combined approach enhances anomaly detection by leveraging the strengths of both methods. However, visual interpretations indicate that LOF performs better in separating anomalies from normal data points.

## Conclusion
This study successfully applies DBSCAN, LOF, and a combined approach for anomaly detection in a hypothyroidism dataset. Visualizations and performance metrics indicate that these methods are effective in identifying unusual patterns. Based on visual interpretation, LOF was selected as the preferred method for anomaly detection. Future work could involve exploring other clustering algorithms and improving parameter optimization techniques.

## References
- F. Pedregosa et al., "Scikit-learn: Machine Learning in Python," Journal of Machine Learning Research, vol. 12, pp. 2825-2830, 2011.
- L. Van der Maaten and G. Hinton, "Visualizing Data using t-SNE," Journal of Machine Learning Research, vol. 9, pp. 2579-2605, 2008.
- J. C. Gower, "A general coefficient of similarity and some of its properties," Biometrics, vol. 27, pp. 857-874, 1971.

## License
This project is licensed under the MIT License - see the LICENSE file for details.
