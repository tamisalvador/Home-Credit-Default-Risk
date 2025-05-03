# Home Credit Default Risk - Project Overview

This project was completed as part of a group assignment, where each team member developed and evaluated their own machine learning model. I contributed to the project individually by performing exploratory data analysis (EDA), preparing the data, and developing a decision tree model. As a group, we compared all of our models and ultimately selected the one with the best performance, a black-box model (XGBoost), to serve as our final solution.

This repository showcases my individual contribution to the project.

## Summary of Business Problem and Objective

Home Credit is working to improve financial inclusion by offering loans to individuals with limited or no credit history. However, accurately assessing the repayment ability of these applicants is challenging. Poor predictions can result in two major issues: denying credit to reliable borrowers and approving loans for high-risk applicants, both of which harm business performance and customer trust.

## Group Solution

Each team member built a different machine learning model using a shared dataset. After evaluating all models using AUC and other metrics, we selected the **XGBoost** algorithm as our final model due to its superior performance.

## My Contribution

I focused on exploratory data analysis (EDA), data preparation, and developing a **decision tree model** using `rpart` in R. This included:

- Performing 70/30 train-test split 
- Further splitting the training data into 80/20 for validation
- Training a decision tree with customized parameters
- Visualizing the tree with `rpart.plot`
- Evaluating the model using AUC (**65%**) on the validation set
- Identifying key predictors: EXT_SOURCE_3, EXT_SOURCE_2, and EXT_SOURCE_1

Although my decision tree model was not selected as the final approach, it was useful for understanding feature importance and model interpretability.

## Business Value of the Solution

Our final model (XGBoost) achieved an AUC and a mean Kaggle score of **76%** on cross-validation. This offers significant improvement over baseline methods and provides a practical decision-making tool. Adjusting the decision threshold allows financial institutions to tune risk tolerance in lending decisions—balancing profitability with default mitigation.

## Challenges Faced

- I encountered issues running the C50 package in R and had to switch to `rpart.plot`, which has less intuitive visualizations
- Managing class imbalance and interpretability across models was also a challenge
- Collaborating on model comparison and selection required good communication and compromise within the group

## What I Learned

- Hands-on experience with model evaluation using AUC and ROC curves
- The importance of selecting not just the most interpretable model, but the one that performs best in context
- How to balance statistical accuracy with real-world business considerations
- Collaborating with teammates to integrate multiple notebooks into a cohesive project
