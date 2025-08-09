# Car Clustering Analysis with Hierarchical Clustering

## Problem Statement and Goal of Project
This project aims to perform hierarchical clustering on a dataset of car models to identify patterns and group similar vehicles based on their attributes, such as horsepower, price, and fuel efficiency. The goal is to explore the dataset's structure, preprocess it for clustering, and visualize the resulting clusters to uncover meaningful insights about car characteristics and their market positioning.

## Solution Approach
The approach involves loading and inspecting a dataset of car models, checking for data quality issues, and applying hierarchical clustering using Python. Key steps include:
1. **Data Loading and Inspection**: Loading the `cars_clus.csv` dataset using pandas and examining its structure and data types.
2. **Data Quality Check**: Identifying missing values to ensure the dataset is suitable for analysis.
3. **Clustering and Visualization**: Applying hierarchical clustering (using `AgglomerativeClustering` from scikit-learn) and visualizing the clusters with a scatter plot, where points are colored by cluster and sized by price.

This project demonstrates my ability to preprocess data, apply unsupervised machine learning techniques, and create insightful visualizations for data exploration.

## Technologies & Libraries
- **Python 3.9.21**: Core programming language used in the Jupyter notebook.
- **pandas**: For data manipulation and analysis.
- **NumPy**: For numerical operations.
- **Matplotlib**: For creating scatter plots and visualizations.
- **SciPy**: For hierarchical clustering (`dendrogram`, `linkage`) and distance matrix calculations.
- **scikit-learn**: For agglomerative clustering (`AgglomerativeClustering`), feature scaling (`MinMaxScaler`), and clustering evaluation **metrics** (`silhouette_score`, `calinski_harabasz_score`, `davies_bouldin_score`).
- **adjustText**: For adjusting text labels in scatter plots to avoid overlap.
- **os**: For file handling and path verification.

## Description about Dataset
The dataset (`cars_clus.csv`) contains information about 159 car models across 16 features, including:
- **Manufacturer and Model**: Categorical identifiers for each car (e.g., Acura Integra, Audi A4).
- **Sales, Resale, Price**: Financial metrics (e.g., sales in thousands, resale value, and price in thousands of dollars).
- **Type**: Vehicle type (encoded as 0.0 for cars, with potential for other values like trucks).
- **Engine Size, Horsepower, Wheelbase, Width, Length, Curb Weight, Fuel Capacity, MPG**: Technical specifications.
- **LnSales**: Log-transformed sales data.
- **Partition**: A float64 column, likely used for dataset splitting (all values observed as 0.0 in the sample).

The dataset has some data quality issues, such as missing values in the `manufact` column (2 missing entries) and a `$null$` value in the `price` column for the Acura CL, which may require preprocessing before clustering.

## Installation & Execution Guide
To run this project locally:
1. **Prerequisites**:
   - Python 3.9.21 or compatible version.
   - Jupyter Notebook or JupyterLab installed.
   - Required libraries: `pandas`, `numpy`, `matplotlib`, `scipy`, `scikit-learn`, `adjustText`.
2. **Installation**:
   ```bash
   pip install pandas numpy matplotlib scipy scikit-learn adjustText
   ```
3. **Setup**:
   - Ensure the `cars_clus.csv` dataset is in the same directory as the notebook (`hierarchy_real_data.ipynb`).
   - Open the notebook in Jupyter:
     ```bash
     jupyter notebook hierarchy_real_data.ipynb
     ```
4. **Execution**:
   - Run all cells sequentially to load the dataset, check for missing values, and generate the cluster visualization.
   - The notebook assumes the dataset file exists; if not, it raises a `FileNotFoundError`.

## Key Results / Performance
- **Dataset Insights**: The dataset contains 159 car models with 16 features. Most columns are stored as `object` types, indicating potential data cleaning needs (e.g., converting to numeric types, handling `$null$` values).
- **Missing Values**: Identified 2 missing entries in the `manufact` column, which may need imputation or removal for robust clustering.
- **Visualization**: The final cell generates a scatter plot of car clusters based on horsepower (`horsepow`) and fuel efficiency (`kml`), with points sized by price and colored by cluster labels. Text annotations display the car type and price for each point, providing an intuitive view of the clustering results.

 ```bash
Note: The notebook appears incomplete, as the clustering step (e.g., defining `agg_cars`, `colors`, and `cluster_labels`) is not shown in the provided code. This suggests the project is a work-in-progress, demonstrating my exploration of hierarchical clustering techniques and visualization.
 ```

## Screenshots / Sample Outputs
The notebook produces a scatter plot visualizing car clusters:
- **Axes**: Horsepower (`horsepow`) on the x-axis and fuel efficiency (`kml`) on the y-axis.
- **Point Size**: Proportional to the car's price.
- **Colors**: Indicate different clusters.
- **Annotations**: Each point is labeled with the car type and price (in thousands).

*Note*: The base64-encoded image output in the notebook is a placeholder for the scatter plot. To view the plot, run the notebook locally or use [nbviewer.org](https://nbviewer.org) for full rendering.

## Additional Learnings / Reflections
This project reflects my hands-on experience with hierarchical clustering and data preprocessing in Python. Key learnings include:
- **Data Quality**: Identifying and addressing missing values and inconsistent data types (e.g., `$null$` in the price column) is critical before applying machine learning algorithms.
- **Visualization**: Using Matplotlib and `adjustText` to create clear, annotated scatter plots enhances interpretability of clustering results.
- **Exploration**: The incomplete clustering step indicates my iterative approach to experimenting with unsupervised learning techniques, which is valuable for understanding how car attributes influence market segmentation.


## 👤 Author
**Mehran Asgari**  
**Email**: [imehranasgari@gmail.com](mailto:imehranasgari@gmail.com)  
**GitHub**: [https://github.com/imehranasgari](https://github.com/imehranasgari)

---

## 📄 License
This project is licensed under the MIT License – see the `LICENSE` file for details.

---
