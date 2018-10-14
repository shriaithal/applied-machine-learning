# Decision Tree

In general, a tree has many analogies in the real life and helps Machine Learning with both Classification and Regression. Decision Tree visually represents with the root at the top followed by the branches/edges. The data that contains 1 (Success) or 0 (Failure) which is called as binary variable is used in the decision tree. It helps to classify one of the binary value to provide clear understanding of the data set.

All the internal nodes are based on the binary conditions based on the list of categories/features that helps to make the final decision. The final split is known as the decision/leaf node which provides the successful data retrieved. Decision Tree algorithms is referred to as CART (Classification and Regression Trees).


### Advantages of CART

- Simple to understand, visualize and interpret.
- Decision trees implicitly perform feature selection and variable screening.
- It can handle numerical and categorical data.
- It requires relatively less effort for data preparation.
- It can also resolve multi-output problems.
- Nonlinear relationships between parameters do not affect tree performance.


## Decision Tree Classification

The main target of the classification tree is to classify the data with certain decisions based on the features in the dataset. Classification is the task of predicting a discrete class label. A classification algorithm may predict a continuous value, but the continuous value is in the form of a probability for a class label. This is also known as greedy algorithm as it recursively does binary splitting thus makes the root node the best predictor/classifier.

**Classification : G = sum(pk * (1 — pk))**

Maximum depth refers to the length of the longest path from the root to a leaf. It is important to know when to stop the splitting.


## Decision Tree Regression

Regression tree are in general used to get the prediction continuous value for a certain use case.
Regression is the task of predicting a continuous quantity. A regression algorithm may predict a discrete value, but the discrete value in the form of an integer quantity.

**Regression : sum(y — prediction)²**

**Note:**
*Classification predictions can be evaluated using accuracy, whereas regression predictions cannot*


## Objective:
The purpose of this assignment is to apply Decision Tree to classify a binary value or categorical value and also to discuss why we chose that attribute/feature and what we are trying to learn from the classification.

## What is the Dataset all about?
We used restaurant Dataset to predict the “Restaurant Rating“
Dataset: https://www.kaggle.com/shrutimehta/zomato-restaurants-data


## What Data Analysis we did:

Data collected can be seen as a raw .json file in the zip folder
- Zomato.csv has 90% Indian restaurants in which 30-40% are restaurants at Delhi.
- The collected data has been stored in the Comma Separated Value file Zomato.csv. Each restaurant in the dataset is uniquely identified by its Restaurant Id.
- Consist of 9550 restaurants data collected in 2018
- 20% Data doesn't have rated values
- Rating score distribution looked like Normal
- 90% comes from India. 30-40% of the data set includes restaurants in New Delhi

Every Restaurant contains the following features :

[![Features and Data Types](https://i.imgur.com/7EiLFsU.png)](https://i.imgur.com/7EiLFsU.png)

- Use Library like pair plot Which gives fair idea bout how data is distributed or organized

[![Pair Plot](https://i.imgur.com/9RHPHon.png)](https://i.imgur.com/9RHPHon.png)

## What Data Preparation we did :

1) Load the data using the Pandas library.
2) Considered only the  columns in the Dataset , which can impact the rating.
3) The Dataset has different sets of  target values for Rating like (‘Excellent’, ‘Good’, ‘Average’ , 'Very Good ').
    Since we would like to implement a binary classification algorithm, we decided to have the rows with target value Excellent, Average and not rated
4) Rating is in the text Format , so updated to Binary Values 0 and 1. Similarly converted all 'yes' to 1 and 'no' data to 0.

[![Data preparations](https://i.imgur.com/tBU2t90.png)](https://i.imgur.com/tBU2t90.png)


## What we  Achieved ?
Using the 11 different features in the dataset we used Decision Tree to get the essential features leading a restaurant to be rated either as "Excellent" or "Average". The reason for choosing this feature is to help the restaurant owners to focus the  areas that can impact a  better rating.

**Entropy:** *A common measure of target class impurity*

**Entropy=Σi–pilog2pi**

**Gini:** *Gini Impurity is another measure of impurity*

**Gini=1–Σip2i**

## Decision Tree Classifier Accuracy score:
### Score is 0.982  or 98%

[![Accuracy Score](https://i.imgur.com/irEcmbq.png)](https://i.imgur.com/irEcmbq.png)

**Note:** *Defining some of the attributes like max_depth, max_leaf_nodes, min_impurity_split, and min_samples_leaf can help prevent over-fitting the model to the training data.*

## Confusion Matrix:


[![Confusion Matrix](https://i.imgur.com/buSool3.png)](https://i.imgur.com/buSool3.png)


## Classification Report:


- TP = True Positive
- FP = False Positive
- FN = False Negative
- TN = True Negative

**Formulas:**
- Accuracy = TP+TN/TP+FP+FN+TN
- Precision = TP/TP+FP
- Recall = TP/TP+FN
- F1 Score = 2 x (Recall x Precision) / (Recall + Precision)


[![Confusion Matrix](https://i.imgur.com/GI8pC6k.png)](https://i.imgur.com/GI8pC6k.png)


## ROC-AUC curve:
### Score is 0.944  or 94%

The confusion matrix  result tells us correct and incorrect predictions. When we make a binary prediction, there can be 4 types of outcomes:
True Positive, False Positive, True Negative and False Negative.

**FPR** : *False Positive rate*
**TPR** : *True Positive rate*

[![AUC](https://i.imgur.com/wcWpNfU.png)](https://i.imgur.com/wcWpNfU.png)

## Visualize Decision Tree


[![Decision Tree](https://i.imgur.com/vWYqGON.png)](https://i.imgur.com/vWYqGON.png)

## Conclusion
 Decision Tree Classifier is used for both binary and multivariate classification tasks. With the current solution we used  binary classification task, which gives the rating of restaurant which can be "Excellent" or "Average" based on the 12 features.


## Team

|Name | Detail|SJSU Id | Contributions
|---|---|---|---|
| University | [SJSU UNIVERSITY]( http://www.sjsu.edu/) |
| Team-Name | Code Busters|
|Professor| Mr. Arsanjani|
|Team | [Harini Balakrishnan](https://www.linkedin.com/in/harini-balakrishnan/) | 010830755 | Decision Tree Classification & AUC-ROC
|Team | [Ravi Katta](https://www.linkedin.com/in/ravi-shanker-katta/)  | 012127011 | Visualize Decision Tree & Classification Report
|Team | [Anushri Srinath Aithal](https://www.linkedin.com/in/anushri-aithal/) | 012506897 | Data Cleaning & Data Fabrication
|Team | [Sunder Thyagarajan](https://www.linkedin.com/in/sunderthyagarajan/) | 011528062 | Confusion Matrix & Data Analysis
