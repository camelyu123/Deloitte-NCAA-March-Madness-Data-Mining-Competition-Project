## Deloitte NCAA March Madness Data Mining Competition Project

Team name: Orange

Team member: Yichen Pan, Ziyue Zhong, Haojunzhi Yu, Teena George

### Introduction

The National Collegiate Athletic Association (NCAA) Men's Basketball Tournament is informally referred to as "March Madness." With 68 college basketball teams competing in a single-elimination tournament, March Madness is played every spring in the US to determine the national championship of the major college basketball teams. Based on Kaggle’s Machine Learning Mania(https://www.kaggle.com/c/mens-machine-learning-competition-2018#evaluation ), competitors of 2018 Deloitte March Data Crunch Madness predict the probability that a team wins any given game in the 2018 Tournament. Log loss is used as evaluation. Extensive historical data to jump-start the modeling process is given. Competitors are encouraged to incorporate their sources of data.

### Highlights of Our Project

One of the highlights of our project is the new variables, EFG-OEFG, TPP-DTPP, SRS, SOS, Adj_win and the most important one- Coach Influence. Another one is our project's philosophy, let the machine learning algorithm decide variables and models. We try to make all procedures rational and scientific.

### Flow Chart

![flow chart](https://user-images.githubusercontent.com/44653163/49898097-091e6780-fe26-11e8-8bc7-fd232bd8b2e0.jpg)

### Data Preprocessing

We added variables from other sources (https://www.sports-reference.com/cbb/) and normalized data by using  normalize function from sklearn.preprocessing package in python


![addvariables](https://user-images.githubusercontent.com/44653163/49898112-163b5680-fe26-11e8-871f-faa9064c4514.jpg)

We created a new variable named Coach Influence. 

![coach influence](https://user-images.githubusercontent.com/44653163/49898124-20f5eb80-fe26-11e8-9ad1-6adc6a13604b.jpg)

Also, we created an adjusted win formula.

![adjusted win](https://user-images.githubusercontent.com/44653163/49898123-20f5eb80-fe26-11e8-907f-31db7873762c.jpg)

### Feature and Model Selection

We applied three feature selection methods (L1-based feature selection, Tree-based feature selection, and Pearson correlation linear feature selection). We compared the performance of all eight models measured by testing score and testing log loss. According to the result, we selected Logistic Regression, Random Forest, Gradient boosting and Decision Tree to predict the outcome by using Ensemble Model Voting Classifier.

![testing log loss](https://user-images.githubusercontent.com/44653163/49898126-218e8200-fe26-11e8-81d4-a5121fbb1dbf.png)

![testing score](https://user-images.githubusercontent.com/44653163/49898127-218e8200-fe26-11e8-8f89-3fa8fdbfd802.png)


We measured the performance of Ensemble model by using data selected by all three feature selection methods. The testing score and testing log loss indicate that variables chosen by L1-based feature selection have the best performance.

![featureselection](https://user-images.githubusercontent.com/44653163/49898125-20f5eb80-fe26-11e8-8862-b31802d82c41.png)


This chart shows our prediction distribution and correctness. We finally get 74.6% accuracy (successfully predicted 50 of 67 games)and log loss 0.58


![2018 prediction probability distribution and correctness](https://user-images.githubusercontent.com/44653163/49898111-163b5680-fe26-11e8-81e1-2e6774ce8464.jpg)









