# ML Logistic Regression
Machine Learning Algorithm Logistic Regression is a classification algorithm that can be used to predict the probability of a categorical dependent variable. The data that contains 1 (Success) or 0 (Failure) which is also called as binary variable is used logistic regression and this variable should be a dependent variable.  

Main Usage of Logistic Regression is categorization. It can be used in different use cases like for e.g. Predicting if it rains or not, individual gets a loan or not etc.


## Objective:
The purpose of this assignment is to apply Logistic regression to classify a binary value or categorical value 
and also to discuss why we chose that attribute/feature and what we are trying to learn from the classification.

## What is the Dataset all about? 
We used restaurant Dataset to predict the “Restaurant Rating“
Dataset: https://www.kaggle.com/shrutimehta/zomato-restaurants-data 

## What we  Achieved ?
Based on the Different features in the dataset using Logistic Regression, we are able to get if the restaurant rating is "Excellent" or "Average". The reason for choosing this feature is to help the restaurant owners to focus the  areas that can impact a  better rating. 

## What Data Preparation we did :

1) Load the data using the Pandas library.
2) Considered only the  columns in the Dataset , which can impact the rating. 
3) The Dataset has different sets of  target values for Rating like (‘Excellent’, ‘Good’, ‘Average’ , 'Very Good '). 
    Since we would like to implement a binary classification algorithm, we decided to have the rows with 
    target value Excellent and Average
4) Format the column headers as they have spaces. ( why formatting ? To apply functions on the columns headers ) 
5) Rating is in the  text Format , so updated to Binary Values 0 and 1.
6) Convert required  features  like 'Table booking','Has Online delivery to numerical  values
7) Data Analysis - Use Library like  pairplot Which gives fair idea bout how data is 
   distributed or organized

## Accuracy score: 
## 0.95 
![Alt text](/images/Score.png)


##  Sigmoid Function:

Sigmoid function can be used for Classification type problems, where we scale the data in some given range with the threshold, where it adjusts all the data points between 0 and 1. We want to have the output of the Logistic Regression Algorithm to be class variable in our case which is Rating as 0-Average, 1-Excellent.The S-curve below depicts sigmoid function for the Train  data present in our restaurant data set.  
![Alt text](/images/Sigmoid.png)


 ##  Confusion Matrix:
 The confusion matrix  result tells us correct and incorrect predictions.
 ![Alt text](/images/ConfusionMatrix.png)



## Conclusion
 Logistic regression  can be used for both binary and multivariate classification tasks. With the current solution we used  binary classification task, which gives the rating of restaurent which can be "Excellent" or "Average".

## Team

|Name | Detail|SJSU Id | Contributions
|---|---|---|---|
| University | [SJSU UNIVERSITY]( http://www.sjsu.edu/) |
| Team-Name | Code Busters|
|Professor| Mr. Arsanjani|
|Team | [Harini Balakrishnan](https://www.linkedin.com/in/harini-balakrishnan/) | 010830755 | Signoid Function
|Team | [Ravi Katta](https://www.linkedin.com/in/ravi-shanker-katta/)  | 012127011 | Data Cleaning / Data Analysis
|Team | [Anushri Srinath Aithal](https://www.linkedin.com/in/anushri-aithal/) | 012506897 | Logistic Regression
|Team | [Sunder Thyagarajan](https://www.linkedin.com/in/sunderthyagarajan/) | 011528062 | Confusion Matrix/ Data Analysis 
