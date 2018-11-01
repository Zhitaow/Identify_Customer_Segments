# Udacity Data Science Nanodegree
## Creating Customer Segments
### Comments Received from Udacity Reviewer
 [https://review.udacity.com/#!/reviews/1411362](https://review.udacity.com/#!/reviews/1411362)

### Table of Contents

1. [Introduction](#introduction)
2. [Project Overview](#overview)
3. [Objective](#objective)
4. [File Description](#file)
5. [General Steps of Analysis](#step)

### Introduction <a name="introduction"></a>
The data and design for this project was provided by Arvato Financial Services. You will apply unsupervised learning techniques on demographic and spending data for a sample of German households. You will preprocess the data, apply dimensionality reduction techniques, and implement clustering algorithms to segment customers with the goal of optimizing customer outreach for a mail order company.

### Project Overview <a name="overview"></a>
In this project, you will work with real-life data provided to us by our Bertelsmann partners AZ Direct and Arvato Finance Solution. The data here concerns a company that performs mail-order sales in Germany. Their main question of interest is to identify facets of the population that are most likely to be purchasers of their products for a mailout campaign. Your job as a data scientist will be to use unsupervised learning techniques to organize the general population into clusters, then use those clusters to see which of them comprise the main user base for the company. Prior to applying the machine learning methods, you will also need to assess and clean the data in order to convert the data into a usable form.

### Objective <a name="objective"></a>
The unsupervised learning branch of machine learning is key in the organization of large and complex datasets. While unsupervised learning lies in contrast to supervised learning in the fact that unsupervised learning lacks objective output classes or values, it can still be important in converting the data into a form that can be used in a supervised learning task. Dimensionality reduction techniques can help surface the main signals and associations in your data, providing supervised learning techniques a more focused set of features upon which to apply their work. Clustering techniques are useful for understanding how the data points themselves are organized. These clusters might themselves be a useful feature in a directed supervised learning task. This project will give you hands-on experience with a real-life task that makes use of these techniques, focusing on the unsupervised work that goes into understanding a dataset.

In addition, the dataset presented in this project requires a number of assessment and cleaning steps before you can apply your machine learning methods. In workplace contexts, you will frequently need to work with data that is untidy or needs preprocessing before standard algorithms and models can be applied. The ability to perform data wrangling and the ability to make decisions on data that you work with are both valuable skills that you will practice in this project.

### File Descriptions <a name="file"></a>

####Udacity_AZDIAS_Subset.csv 
Demographic data for the general population of Germany; 891211 persons (rows) x 85 features (columns).
####Udacity_CUSTOMERS_Subset.csv
Demographic data for customers of a mail-order company; 191652 persons (rows) x 85 features (columns).
####Data_Dictionary.md
Information file about the features in the provided datasets.
####AZDIAS_Feature_Summary.csv
Summary of feature attributes for demographic data.
####Identify_Customer_Segments.ipynb
Jupyter Notebook divided into sections and guidelines for completing the project. The notebook provides more details and tips than the outline given here.

### General Steps of Analysis <a name="step"></a>
**Step 1: Preprocessing** 
When you start an analysis, you must first explore and understand the data that you are working with. In this (and the next) step of the project, you’ll be working with the general demographics data. As part of your investigation of dataset properties, you must attend to a few key points:

How are missing or unknown values encoded in the data? Are there certain features (columns) that should be removed from the analysis because of missing data? Are there certain data points (rows) that should be treated separately from the rest?
Consider the level of measurement for each feature in the dataset (e.g. categorical, ordinal, numeric). What assumptions must be made in order to use each feature in the final analysis? Are there features that need to be re-encoded before they can be used? Are there additional features that can be dropped at this stage?
You will create a cleaning procedure that you will apply first to the general demographic data, then later to the customers data.

**Step 2: Feature Transformation**
Now that your data is clean, you will use dimensionality reduction techniques to identify relationships between variables in the dataset, resulting in the creation of a new set of variables that account for those correlations. In this stage of the project, you will attend to the following points:

The first technique that you should perform on your data is feature scaling. What might happen if we don’t perform feature scaling before applying later techniques you’ll be using?
Once you’ve scaled your features, you can then apply principal component analysis (PCA) to find the vectors of maximal variability. How much variability in the data does each principal component capture? Can you interpret associations between original features in your dataset based on the weights given on the strongest components? How many components will you keep as part of the dimensionality reduction process?
You will use the sklearn library to create objects that implement your feature scaling and PCA dimensionality reduction decisions.

**Step 3: Clustering**
Finally, on your transformed data, you will apply clustering techniques to identify groups in the general demographic data. You will then apply the same clustering model to the customers dataset to see how market segments differ between the general population and the mail-order sales company. You will tackle the following points in this stage:

Use the k-means method to cluster the demographic data into groups. How should you make a decision on how many clusters to use?
Apply the techniques and models that you fit on the demographic data to the customers data: data cleaning, feature scaling, PCA, and k-means clustering. Compare the distribution of people by cluster for the customer data to that of the general population. Can you say anything about which types of people are likely consumers for the mail-order sales company?
sklearn will continue to be used in this part of the project, to perform your k-means clustering. In the end, you will export the completed notebook with your work as an HTML file, which will serve as a report documenting your approach and findings.


