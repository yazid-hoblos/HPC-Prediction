# Hepatocellular Carcinoma (HCC) Prediction 

## Overview

This GitHub repository contains a comprehensive set of tools and scripts for predicting hepatocellular carcinoma using various supervised and unsupervised learning approaches in R. 
The repository covers a range of techniques, including logistic regression, penalized logistic regression (L1 regularization - Lasso), linear discriminant analysis (LDA), 
quadratic discriminant analysis (QDA), resampling methods, decision trees, random forest, bagging, support vector machines (SVM), principal component analysis (PCA), hierarchical clustering, and k-means 
clustering.

## Dataset

This dataset is a microarray consisting of non-normalized gene expression for 357 patients, split almost in half normal and HCC cases. 

## Exploratory Analysis and Data Preprocessing

details
normalization (standardization; min-max; robust scaling)
variance - feature selection: Prepare gene expression data by normalizing values and selecting informative features relevant to hepatocellular carcinoma.

![image](https://github.com/yazid-hoblos/Carcinoma-Prediction/assets/125372209/5a74dddc-cab6-4a21-b37b-71e64fbecd34)

```R
model3 = glm(type~X205695_at +X214677_x_at+X209614_at+X206561_s_at+X220491_at,mut_df[-1],family=binomial())
```

## Approaches 

1. **[Supervised Learning Approaches](supervised_learning_approaches)**
    - *[Logistic Regression](supervised_learning_approaches/logistic_regression.R)*: Utilize logistic regression to model the probability of hepatocellular carcinoma based on gene expression data.
    - *[Penalized Logistic Regression - Lasso](supervised_learning_approaches/penalized_logistic_regression.R):* Apply L1 regularization to select relevant genes for predicting hepatocellular carcinoma, potentially improving model interpretability.

      ![image](https://github.com/yazid-hoblos/Carcinoma-Prediction/assets/125372209/99890140-076d-4943-93cd-64af38a6a52f)
      ![image](https://github.com/yazid-hoblos/Carcinoma-Prediction/assets/125372209/5c513008-0752-41c8-a3b7-60828ec5080c)
      
    - *[Linear Discriminant Analysis (LDA)](supervised_learning_approaches/LDA_QDA.R):* Use LDA to reduce the dimensionality of gene expression data and classify samples into normal and cancer categories.
    - *[Quadratic Discriminant Analysis (QDA)](supervised_learning_approaches/LDA_QDA.R):* Explore non-linear relationships in gene expression data for improved hepatocellular carcinoma prediction.
  
        ![image](https://github.com/yazid-hoblos/Carcinoma-Prediction/assets/125372209/f8558fd1-3503-4012-b81f-ba13d1a0f1d4)

    - *[Resampling Methods](supervised_learning_approaches/resampling.R):* Evaluate and validate predictive models using techniques like bootstrapping and cross-validation on GEO data.

2. **[Tree-Based Approaches](tree_based_approaches)**
    - *[Decision Trees](tree_based_approaches/decision_trees.R):* Build decision trees to identify key gene expression patterns indicative of hepatocellular carcinoma.

      ![image](https://github.com/yazid-hoblos/Carcinoma-Prediction/assets/125372209/9a5a0af0-4e22-4fb7-9302-7aabd49be1a9)

    - *[Random Forest](tree_based_approaches/random_forest_bagging.R):* Aggregate decision trees to enhance accuracy in predicting hepatocellular carcinoma from complex gene expression profiles.

      ![image](https://github.com/yazid-hoblos/Carcinoma-Prediction/assets/125372209/d3edbe9b-2626-4161-acfd-b7d4bd1b21c1)
      
    - *[Bagging](tree_based_approaches/random_forest_bagging.R):* Apply bagging techniques to reduce overfitting and improve the robustness of predictive models.

      ![image](https://github.com/yazid-hoblos/Carcinoma-Prediction/assets/125372209/e21e8a4e-8a20-49d5-b69c-b4763fedf75f)

      ![image](https://github.com/yazid-hoblos/Carcinoma-Prediction/assets/125372209/cf717861-68c0-448d-b5b4-5830ef237196)

3. **[Boruta-based Genes Selection](boruta_gene_selection.R):** Use Boruta alongside random forest for effective gene selection, emphasizing relevance to hepatocellular carcinoma prediction.

    ![image](https://github.com/yazid-hoblos/Carcinoma-Prediction/assets/125372209/d34f7cdd-2e97-47bf-960d-eed19eeb4401)
    ![image](https://github.com/yazid-hoblos/Carcinoma-Prediction/assets/125372209/cb6f5997-55b2-4649-9944-6e210a8919b9)


4. **[Unsupervised Learning Approaches](unsupervised_learning_approaches)**
    - *[Support Vector Machines (SVM)](unsupervised_learning_approaches/SVM.R):* Utilize SVM to find optimal hyperplanes for separating normal and cancer samples in GEO data.

      ![image](https://github.com/yazid-hoblos/Carcinoma-Prediction/assets/125372209/ac8974aa-1b42-4bd8-9cd8-83a5e47da091)
      
    - *[Principal Component Analysis (PCA)](unsupervised_learning_approaches/PCA.R):* Reduce dimensionality with PCA to visualize and identify patterns in hepatocellular carcinoma gene expression data.
    - *[Hierarchical Clustering](unsupervised_learning_approaches/hierarchical_clustering.R):* Group samples with similar gene expression profiles, potentially revealing distinct subtypes of hepatocellular carcinoma.

      ![image](https://github.com/yazid-hoblos/Carcinoma-Prediction/assets/125372209/e721075f-4369-4a11-88f3-4ea54e5e2546)
      
    - *[K-Means Clustering](unsupervised_learning_approaches/k-means.R):** Cluster gene expression profiles to identify similarities and differences in hepatocellular carcinoma samples.

## References 
