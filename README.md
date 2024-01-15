
Cryptocurrency Clustering - UW FinTech Bootcamp Challenge, Module 10
This project employs K-Means clustering, an unsupervised learning method, to categorize cryptocurrencies based on their performance. The aim is to generate recommendations for profitable portfolios.

Data Sources
crypto_market_data.csv - This file contains market data for various cryptocurrencies over different time frames.

Overview
Initially, I utilize the elbow curve technique with normalized data to determine the most suitable k value for the K-Means algorithm, which incorporates all features from the dataset.

![Elbow curve line plot showing a value of 1 for k to be optimal for the dataset with all features](/Resources/Images/Elbow_Curve.png)


Next, I apply the identified optimal k value to train and forecast the K-Means model, resulting in four distinct cryptocurrency clusters. The clusters displayed substantial inertia, prompting a review of the number of features.

![A scatter plot showing 4 clusters with heavy inertia](/Resources/Images/Scatter_Plot_OG.png)

The PCA data is then used to re-calculate the ideal k value for the K-Means model.
![Elbow curve line plot from the PCA data that shows 4 to be the optimal k value](/Resources/Images/Elbow_Curve_PCA.png)

In the final step, using the PCA-determined optimal k value, I plot the newly formed clusters.

![Scatter plot showing 4 low inertia clusters generated using the PCA dataframe](/Resources/Images/Scatter_Plot_PCA.png)

Technical Tools
This project is developed in Python 3.7 and run through JupyterLab within a conda development environment.

Key dependencies include:

Jupyter - For code execution
Conda (4.13.0) - Development environment management
Pandas (1.3.5) - Data analysis
Matplotlib (3.5.1) - Data visualization
Numpy (1.21.5) - Numerical computations and support for Pandas
hvPlot (0.8.1) - Interactive data visualizations
[scikit-learn](https://scikit-learn.org/stable
/) (1.0.2) - Implementing KMeans clustering, data normalization, and PCA

Installation Instructions
To run this project in JupyterLab, first install the Anaconda package. Then, activate a conda development environment and execute jupyter lab.

For a seamless experience, use the requirements.txt file to replicate the conda development environment from the project. You can create this environment with conda create --name myenv --file requirements.txt, followed by conda install --name myenv --file requirements.txt to install the necessary requirements.

How to Use
For a comprehensive guide through data gathering, preparation, and analysis, refer to the Jupyter notebook crypto_investments.ipynb. It includes in-line data visualizations and corresponding analytical observations.

Licensing
This project is under the GNU General Public License.