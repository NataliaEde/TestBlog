# Classification Problem of Bank's Telemarketing Campaign

by Natalia Edelson 

![image](https://user-images.githubusercontent.com/44559346/206246271-d6dbdc19-82bc-4bb2-a14b-ce7c7f4eb45b.png)



#### Introduction

Retail banks collect term deposits as part of their core business investment products. Banks generate a profit by lending funds held in deposit accounts for a higher rate than it pays the customer. Therefore, banks emphasize their marketing efforts to attract customers to deposit funds. 

Although most marketing channels are transitioning to a digital form and telemarketing campaigns are fading away, there is still space in advertising to utilize the phone as a tool for remote marketing. While remote marketing is moving gradually into robocalls, prospects still prefer to talk to a human rather than a robot-speaking voice.  

In finance, an individual who buys a term deposit is called a subscriber. Subscription refers to a potential investor signing up for an investment vehicle agreement involving cash flow and money transfer. Different elements, such as a personal financial situation or high-interest rate, which makes the cost of borrowing more appealing, affect the subscription decision of the prospect. As such, banks benefit from data analysis and prediction models to optimize their campaigns by targeting certain segments of individuals. 

#### Purpose

Our goal is to build a model to predict if a prospect will subscribe to a term deposit campaign.

Using historical data,  we build a model to predict future investors in bank term deposit in order to develop a targeted telemarketing strategy for the bank of Portugal. 

#### Data Analysis and Coding Technicalities 

We analyze the data to determine the rate of subscribers per category within each feature. 

We used a loop function to calculate the percentage of subscribers from prospects contacted  We extracted a data set for each feature and the subscribed column. We used the size() method to count the number of instances while  applying a pivot function to create a column for ‘yes’ and ‘no’ to calculate the percentage rate per each category (e.g. university graduates, high school graduates) within a feature (e.g. education, marital). In the second part of the loop function, we plotted the results for each feature. We will touch upon a few graphs we generated. 



#### Age

![image](https://user-images.githubusercontent.com/44559346/206238694-45f84fda-487f-46a0-87c3-75c3a904743f.png)

#### Occupation

![image](https://user-images.githubusercontent.com/44559346/206240767-fe3dfcb6-788e-41bc-ba49-4070988b5267.png)

#### Preparing to Model the Data 

We used a pipeline to streamline several steps that are required to pass through the data before implementing the predictive classified model. The pipeline was also helpful when we split the data into training and testing because we did not want the information from training data to be leaked into the unseen testing data.

We inserted the pipeline as part of a function so that it can loop around when we employed the various classified models. 

![image](https://user-images.githubusercontent.com/44559346/206961932-b77f80bc-4e42-4494-a25c-20e5b1c35ca4.png)

#### Final Model with Hypertuning -  Random Forest  
 
 GridSEarchCV suggested the following criteria, which produced the following results:

 {'model__criterion': 'gini', <br />
'model__max_depth': 200, <br />
 'model__max_features': 14, <br />
 'model__n_estimators': 900} <br />

* Training_Accuracy: 0.99 <br />
* Test_Accuracy: 0.87<br />
* Precision: 0.9876<br />
* Recall: 0.87<br />
* F1_Score: 0.87<br />



### Conclusions:

In this project,we implemented data analysis and predictive classified models to predict term deposit subscriptions at a Portuguese bank institution. With the F1 score of 87% using Random Forest Classifier, the following business recommendations are:

Pay close attention to socioeconomic data:
* 3 Month Euribor rate - The Euribor rate is based on the average interest rates at which Eurozone banks lend funds to other banks. Ramp up the campaign when rates are high. A prospect is more likely to invest in a term deposit knowing that they will receive a high interest rate.
* Consumer Confidence Index - Individuals are more likely to invest if their financial situation is good and if the country’s outlook is optimistic. 

Target telemarketing calls toward select the individuals who belong to a specific age group and occupation. Seniors, and Students, and Retired Individuals are more likely to subscribe to a term deposit. 

Conduct the campaign during specific months. March, September, and October have been shown to have a higher rate of subscriptions.  

#### Repository Structure

Notebook  PDF - PDF Version of the code of Jupyter Notebook <br />
Jupyter Notebook.ipynb the code in ipynb  <br />
Presentation  - Non-technical business presentation <br />


