# Starbuck-Capstone-Project

This repository has all the code and report for my Udacity Data Scientist Nanodegree Capstone project.

## Starbucks Capstone Challenge: Using Starbucks app user data to predict effective offers

## Table of Contents
1. [Installation](#installation)
2. [Introducing a Dataset](#dataset-introduction)
3. [Project Motivation](#project-motivation)
4. [File Descriptions](#files)
5. [Results](#results)
6. [Licensing, Authors, Acknowledgements](#license)

### Installation <a name="installation"></a>
For running this project, the most important library is Python version of Anaconda Distribution. It installs all necessary packages for analysis and building models. 

### Introducing a Dataset <a name="dataset-introduction"></a>
Once every few days, Starbucks sends out an offer to users of the mobile app. An offer can be merely an advertisement for a drink or an actual offer such as a discount or BOGO (buy one get one free). Some users might not receive any offer during certain weeks. Not all users receive the same offer, and that is the challenge to solve with this data set.

### Project Motivation <a name="project-motivation"></a>
I chose this project to understand the success rate of offers being sent and analysis is done through addressing the following questions.
1. What are the most recommended offer that should send to customers?
2. What are the main features influencing the effectiveness of an offer on the Starbucks app?

### Data Preparation <a name="data-preparation"></a>
The data sets contain simulated data that mimics customer behavior on the Starbucks rewards mobile app. It is a simplified version of the real Starbucks app because the underlying simulator only has one product whereas Starbucks actually sells dozens of products.

Three datasets are provided by Starbucks for this project:
1. Portfolio - contains users' age, gender, income, membership start date.
2. Profile -  contains information about the offers, including offer type(Buy one get one free/ discount/informational), offer duration, rewards, minimal transaction amount to use the offer etc.
3. Transcript - contains users' transaction amount, usage of offers, time of transaction etc.

### Results<a name="results"></a>
As a brief summary of my findings:
#### i. Question 1 findings - What are the most recommended offer that should send to customers?:
To predict the offer type recommendation, I created an ML model with multiple outputs to predict the best offer(s) by predicted probability in descending order. Finally, each customer will receive the future offer type that matches their behavior and favor.

#### ii. Question 2 findings - What are the main features influencing the effectiveness of an offer on the Starbucks app?:
According to the feature importances of the model, I found that for BOGO offers top 3 variables are total_rewards_received, avg_reward and avg_reans_amt. For Discount offers are avg_reward, avg_trans_amt and comp_view_ratio. We can infer that based on the price of the products, amount and reward of the offers could classfy the effective and ineffective one.

For Infomational offers, 'info_off_received' are the most importance features. Users who tend to receive various of informational offers are likely to complete the transaction. Since this offers does not have 'offer_completed' event, 'avg_reward' feature are not influence user to buy like BOGO and Discount offers.

The main observations of the code are published [here](https://medium.com/@moookeys/intelligent-offers-recommendation-system-enriching-starbucks-customer-experience-4d117614c350).

### Licensing, Authors, Acknowledgements, etc.<a name="license"></a>
I would like to thank [Udacity](https://eu.udacity.com/) for this amazing project, and [Starbuck](https://www.starbucks.com/) for providing the data.
