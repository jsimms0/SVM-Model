# SSDS Data Analysis and SVM Fit
This project analyzes the Sloan Digital Sky Survey (SDSS) dataset, which is over 10,000 data points spread across 18 columns.  
It creates visuals to understand the data distribution, and then creates a SVM algorithm to classify objects into three celestial bodies: Galaxies, Stars, and Quasars.

## Skills Used:
Data Preparation: Data Import and Handling, Data Visualization, Data Cleaning and Processing.
SVM Classification: Data Scaling and Transformation, Model Building and Implementation, Hyperparameter Tuning, Performance Evaluation.
Data Interpretation and Conclusions: Analyzing Results.


## Project Summary:

**Goal:**
Classify objects from the Sloan Digital Sky Survey (SDSS) dataset into three celestial bodies: Galaxies, Stars, and Quasars using Support Vector Machine (SVM) kernels.

**Dataset Overview:**
Over 10,000 data points spread across 18 columns.

## Part One: Data Preparation
**Data Handling:**
* Imported from a CSV using pandas.
* Checked data types, null values, and unique categories.
* Defined celestial terms: Quasar, Galaxy, Star.

**Visualization:**
* Displayed distribution of celestial classes via a bar plot.
* Showcased data distribution against features using density distribution plots.
* Used a 3D scatter plot for the 'Right Ascension', 'Declination', and 'Redshift', colour-coded by class.

**Data Cleaning and Processing:**
* Grouped and melted data for summed density distributions based on spectrum values.
* Removed non-numeric columns and converted 'class' to a categorical datatype.
* Split the dataset for training and testing.

## Part Two: SVM Classification

**Linear Kernel:**
* Scaled data using StandardScaler.
* Achieved 0.96 accuracy using LinearSVC.

**Polynomial Kernel:**
* Used with an accuracy of 0.799.

**RBF Kernel:**
* Used with an accuracy of 0.799.

**Hyperparameter Tuning:**
* Used GridSearchCV for RBF kernel.
* Found best parameters: C=8 and gamma=0.01 with a score of 0.8276.

**Extended Hyperparameter Tuning:**
* Scaled and tuned for various hyperparameters.
* Best parameters: C=100, gamma=1, kernel='linear' yielding an accuracy of 0.9893 on the test set.

## Conclusions:
* SVM kernels have varied performance with this dataset.
* The linear kernel performed best with an accuracy of 0.96, while the polynomial and RBF kernels reached 0.799.
* Hyperparameter tuning improved performance, especially for the linear kernel which reached nearly 0.99 accuracy.
* The SVM linear kernel, post-tuning, proved optimal for this dataset.
