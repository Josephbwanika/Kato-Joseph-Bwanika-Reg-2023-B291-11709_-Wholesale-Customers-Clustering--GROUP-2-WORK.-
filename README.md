# Wholesale Customers Clustering (Group Two)

## Overview
Our project applies **K-Means** and **DBSCAN** clustering algorithms on the **UCI Wholesale Customers Dataset** to segment customers based on their annual spending across different product categories.
The main goal is to identify meaningful customer groups and provide actionable insights for business strategy and marketing.

## Team Members
* Kato Joseph Bwanika — Reg: 2023-B291-11709
* Mambo Emmanuel — Reg: 2022-B291-11357
* Ssenkaayi Vihan — Reg: 2023-B291-11360
* Kutosi Mark — Reg: 2023-B291-11708
* Lubangakene Jonathan — Reg: 2023-B291-13195

## Objectives
* Segment wholesale customers based on spending behavior.
* Compare **K-Means** and **DBSCAN** clustering performance.
* Visualize and interpret cluster patterns.
* Provide business recommendations based on identified segments.

## Dataset Description
* File used: UCI Wholesale Customers.csv (stored locally)
* Features included: Fresh, Milk, Grocery, Frozen, Detergents_Paper, Delicassen, Channel, and Region.

## Workflow Summary
### 1. Data Loading and Preprocessing
* Loaded dataset and checked data types and dimensions.
* Handled missing values and removed duplicates.
* Scaled features using **RobustScaler** to reduce the influence of outliers.

### 2. Exploratory Data Analysis (EDA)
* Generated descriptive statistics and visualized distributions using boxplots and histograms.
* Applied log transformation to correct skewed distributions.
* Created a correlation heatmap to explore relationships between spending categories.

### 3. Feature Engineering
* Created new features:
  * **TotalSpend:** sum of all spending categories.
  * **ProportionFresh:** Fresh divided by TotalSpend.
  * **LogTotalSpend:** logarithm of TotalSpend to reduce skewness.

### 4. Clustering Modelling
* **K-Means:** Tested cluster numbers from 2 to 8 and evaluated using Silhouette and Davies–Bouldin indices.
* **DBSCAN:** Tuned parameters `epsilon (ε)` and `min_samples` using k-distance plots and tested various combinations.

### 5. Model Evaluation
* Compared the performance of both algorithms based on:
  * Number and size of clusters.
  * Number of noise points (for DBSCAN).
  * Visual and statistical differences between clusters.

### 6. Statistical Tests
* Used **Kruskal–Wallis test** to check for significant differences in TotalSpend across clusters.
* Applied **Chi-square test** to determine associations between clusters and categorical features (Region and Channel).

### 7. Visualization
* Applied **Principal Component Analysis (PCA)** for 2D visualization of clusters.
* Highlighted DBSCAN noise points to distinguish outlier customers.

### 8. Reflection and Recommendations
* **K-Means:** Works well for equally sized, spherical clusters.
* **DBSCAN:** Handles arbitrary shapes but sensitive to parameter selection.
* **Recommendations:** Use findings to create targeted marketing campaigns, loyalty programs, and regional sales strategies.

## Tools and Libraries
* Programming Language: Python (Jupyter Notebook)
* Libraries Used:
  * pandas
  * numpy
  * matplotlib
  * seaborn
  * scikit-learn
  * scipy

## Key Insights
* Grocery, Milk, and Detergents_Paper are strongly correlated, likely representing Horeca (Hotel/Restaurant/Café) customers.
* Clusters revealed clear differences between high-value and low-value customers.
* DBSCAN identified several noise points representing unique spending patterns.
* These findings can support better marketing and inventory management decisions.
  
## Conclusion
Both clustering techniques successfully uncovered meaningful customer groups.
K-Means produced interpretable and compact clusters, while DBSCAN effectively identified outliers and irregular spending behaviors.
Overall, this analysis provides a data-driven foundation for targeted business strategies.

## Future Work
* Include hierarchical clustering for deeper comparison.
* Automate parameter tuning for DBSCAN.
* Integrate customer demographic data for more detailed segmentation.
his project?

