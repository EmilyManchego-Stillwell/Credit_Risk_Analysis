# Credit_Risk_Analysis
## Overview:
- **Purpose:**
    - The purpose of this analysis was to determine which supervised machine learning models performed the best when determining whether certain loans had a high or low risk of becoming bad or risky loans.
- **Tools Used:**
    - Scikit-learn
        - Imbalanced-learn
    - Pandas
    - Numpy
    - Jupyter Notebooks

## Results:
### Oversampling Techniques
 - Naive Random Oversampling Model:
 ![Naive Random Oversampling](/Images/Naive_Random_Oversampling.png)
    - Balanced Accuracy Score: 65.47%
    - Precision:
        - Low-Risk (1): 1.00
        - High-Risk (0): 0.01
    - Recall/Sensitivity:
        - Low-Risk (1): 0.59
        - High-Risk (0): 0.72<br><br>

- SMOTE Oversampling Model:
![SMOTE Oversampling](/Images/SMOTE_Oversampling.png)
    - Balanced Accuracy Score: 66.2%
    - Precision:
        - Low-Risk (1): 1.00
        - High-Risk (0): 0.01
    - Recall/Sensitivity:
        - Low-Risk (1): 0.69
        - High-Risk (0): 0.63<br><br>

- Cluster Centroids Undersampling Model:
![Cluster Centroids Undersampling](/Images/ClusterCentroids_Undersampling.png)
    - Balanced Accuracy Score: 54.47%
    - Precision:
        - Low-Risk (1): 1.00
        - High-Risk (0): 0.01
    - Recall/Sensitivity:
        - Low-Risk (1): 0.40
        - High-Risk (0): 0.69<br><br>

- SMOTEENN Combination Oversampling/UnderSampling:
![Combined SMOTEENN](/Images/SMOTEENN_Combo_Sampling.png)
    - Balanced Accuracy Score: 64.73%
    - Precision:
        - Low-Risk (1): 1.00
        - High-Risk (0): 0.01
    - Recall/Sensitivity:
        - Low-Risk (1): 0.57
        - High-Risk (0): 0.72<br><br>

 ### Random Forest and Ensemble Learning Classifiers
 - Balanced Random Forest Classifier:
 ![Balanced Random Forest](/Images/Balanced_Random_Forest_Classifier.png)
    - Balanced Accuracy Score: 78.88%
    - Precision:
        - Low-Risk (1): 1.00
        - High-Risk (0): 0.03
    - Recall/Sensitivity:
        - Low-Risk (1): 0.87
        - High-Risk (0): 0.70<br><br> 

- Easy Ensemble Classifier:
![Easy Ensemble](/Images/Easy_Ensember_Classifier.png)
    - Balanced Accuracy Score: 93.16%
    - Precision:
        - Low-Risk (1): 1.00
        - High-Risk (0): 0.09
    - Recall/Sensitivity:
        - Low-Risk (1): 0.94
        - High-Risk (0): 0.92

## Summary:
- In order to figure out if any of these models worked and which one should be recommended for use, we have to first figure out the question we are asking. The question we are asking is which loans will end up being risky? We are looking to correctly determine or predict which loans will end up being high-risk. Once we know what we are looking for, we then have to decide which model performance assessment is most important to reference for our data. I believe the performance assessment that is most meaningful for our data is the recall/sensitivity numbers. We want to make sure those numbers are as high as possible because we don't want to have a high number of false negatives. In this particular case, the false negatives represent loans that are actually high-risk, but have been predicted to be low-risk. If our model passes a lot of high-risk loans off as low-risk loans, this could end up costing the lender a lot of money because that money is being loaned out with a higher possibility of never being paid back. Based on our findings, the model that would be best to use in this scenario is the Easy Ensemble Classifier model because it gives us the best accuracy score and recall. 
