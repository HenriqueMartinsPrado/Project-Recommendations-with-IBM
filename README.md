## PROJECT RECOMMENDATIONS WITH IBM

### Table of Contents

1. [Installations](#installation)
2. [Project Motivation](#motivation)
3. [File Descriptions](#files)
4. [How to Interact with my project / Results](#results)
5. [Licensing, Authors, and Acknowledgements](#licensing)


## 1. Installations <a name="installation"></a>
There some libraries that you should install to run this python code shared in jupyter notebook. They are:

	1. pandas
	2. numpy
	3. matplotlib
	4. project_tests
	5. pickle
	6. sklearn
	7. pandas_profiling
		
<p align="justify">You can install all of them using pip install <librarie_name> or you can add one more cell in jupyer notebook e write !pip install <librarie_name>
All module used in this project can be see below. They were extracted from the libraries mentioned above.</p>

	import pandas as pd
	import numpy as np
	import matplotlib.pyplot as plt
	import project_tests as t
	import pickle
	from sklearn.metrics import accuracy_score, f1_score
	import pandas_profiling

Beisdes, only to complement, I developed the project using python version 3.8.5. You check the python version with this command:

	!python --version	

## 2. Project Motivation<a name="motivation"></a>

<p align="justify">The development of this project aimed to analyze the interactions that users have with articles on the IBM Watson Studio platform, and make recommendations to them about new articles they will like and also shows the articles that are most pertinent to a specific user. In order to determine which articles to show to each user, I performed a study of the data available on the IBM Watson Studio platform.

.</p>

## 3. File Descriptions<a name="files"></a>

This project consists of the files below:

<ul>		
	<li><p align="justify">Recommendations_with_IBM: In this file you will find all code developed in python such as the organization and steps to explore, recommend and factorize the data.</p>
	<li><p align="justify">Data folder: Here, you will find the articles_community.csv used and user-item-interactions.csv in the development of the project.</p>
	<li><p align="justify">EDA - Pandas Profiling - Df DataFrame: In this file you can find the exploratory data analisys of user-item-interactions.csv created using pandas_profiling library and exported to html formart.</p>
	<li>EDA - Pandas Profiling - Df_Content DataFrame: In this file you can find the exploratory data analisys of articles_community.csv created using pandas_profiling library and exported to html formart..
</ul>

## 4. How to Interact with my project / Results<a name="results"></a>

<p align="justify">In the development of the project, the 6 stages of the CRISP-DM methodology were used, precisely because it is a very consolidated methodology in the area of data mining and with a completeness of topics to be developed and explored that allows to create data solutions.</p>

<ol>
	<li><p align="justify">With the loading of the dataset on the jupyter notebook, I started the project with phase 1 - Understanding the business. In this step, the type of problem that will be solved is identified, in this case predict the churn of customers. In addition, it is worth noting that at this stage the company's background is also identified to know how the project will be conducted until its solution, the main objectives that the project aims to achieve and the success criteria that are metrics that will be used to verify if the project reached the objectives established in the delivery of the same. For this project, the background was defined as the development of the case study through the creation of the file in jupyter notebook in pyhon language. The objective of the project was to answer the questions below:
		<ul>
			<li><p align="justify">Is it possible to achieve a hit rate above 80% in the customer's churn forecast?</li>
			<li><p align="justify">What is the level of correlation between the variables age, year and total_pucharse?</li>
			<li><p align="justify">Is the solution developed passive to be applied in a way that the business identified benefits?</li>
		</ul>
	The use of metrics such as confusion matrix, precision, recall, f1-score and ROC curve are examples of metrics used to analyze the project's success criterion.</li>			
	<li><p align="justify">Evolving to the next phase, phase 2 - Understanding the Data, treatment was carried out through the collection, describing data using statistics, performing exploratory analysis and verifying the quality of the data so that the data makes sense in the solution in which the project intends to deliver. It is important to note that data is a decisive factor for the success of the project, since if poor quality data is used, we will be generating a poor quality solution. Therefore, this step is extremely important to help us understand the data that we will supply to our solution. This phase, according to several authors, articles and books, is responsible for more or less 70% of the project due to its importance. So, for this project, I understood the data by studying the entire data set, identifying: variables, values, data types, number of unique values per variable, describing the data set using statistics, checking the data distribution of the variable target, visualization of the correlation between the variables to identify their impact on the forecast of the models and generating an analysis report for easy verification of the information as well as sharing with those involved in a corporate environment.</p>
	<li><p align="justify">In step 3, in which the data is prepared, four sub-steps were used, which were: data selection, data cleaning, data construction and data integration. Starting with data selection, I tried to check outliers and if all rows and columns are candidates for use in the model. Still in this first sub-step, I segregated the variables in which I separated independent variables from the dependent variable. In the sub-step of cleaning the data set, I checked if there were null data which was not the case for this data set and I did the necessary transformations (modeling) of categorical data to prepare the data for the model. Still in this cleaning step, I segregated the data set between training and test data for training, testing and validating the model's performance. For this project, there was no need to build variables and integrate data with different sources, despite having made the steps for learning purposes explicit.
	<li><p align="justify">In phase 4 - Model, as the data set had the target variable characterizing the problem in a supervised learning model, I made use of 4 models to meet the objectives and validate their performance. The models applied here were: logistic regression, naive bayes, random forest and decision tree.</p>	
	<li><p align="justify">In phase 5 of CRISP-DM, I made use of the performance evaluation of the models by discovering the success and error rate of each one of them as well as the generation of the confusion matrix, identification of the most important variables for each model (this step can only be done after the fit of the model, that's why it was present here), generation of metrics such as precision, recall, f1-score and support as well as raw ROC of each model. It can be seen that the Decision Trees model had a higher hit rate than the other models (92%) based on the data used. It is worth mentioning that some techniques could have been used, such as engineering of characteristics, creation of dummy variables and other approaches, making an exploratory analysis of the data, as well as modifying the model parameters for a better fit. On the other hand, it can be observed that the Naive Bayes model presented a higher accuracy rate (0.92 or 92%) of accuracy, although we found a higher rate of accuracy in the confusion matrix of the decision tree model. The ROC curve is another tool widely used with binary classifiers. The dotted line on the generated graph represented the ROC curve. A good classifier is as far away from that line as possible (towards the upper left corner). Thus, it can be seen that the ROC curve found in the Naive Bayes model is what directs us that within the applied models, the Naive Bayes model is the best model used in this approach. Through this phase, it can be concluded that the objectives set were fulfilled, that is, we achieved a performance above 80% and found that the variables year, age and total_pucharse have low correlation and do not generate negative and biased impact on the models used.
	<li><p align="justify">The last phase, phase 6 - Deploy, is where the implementation is made, it can be delivered in several ways, for example, creating an application for data consumption by those involved, making the model available through the persistence of the trained model using the Pickle library python and etc. For this project, only the development of the case study was generated. The availability for consumption of the data will be developed as a point to improve the structure of this project.</p>
</ol>

<p align="justify">Despite the immense value created through the development of python code to handle the data according to the purpose of each stage of the CRISP-DM methodology, the greatest value is to answer the questions defined at the beginning of the project so that they can generate value in decision making. Thus, the questions and respective answers of each one can be checked below:</p>

<ul>
	<li><p align="justify">Is it possible to achieve a hit rate above 80% in the customer's churn forecast?
	Following the steps of the CRISP-DM methodology, it was possible to carry out an organized and evolutionary process for the development of a data solution. Through these steps, it was possible to train and test 4 different models where hit rates between 83% and 92% were found.</p>
	<li><p align="justify">What is the level of correlation between the variables age, year and total_pucharse?
	Through step 2 of the CRISP-DM, a correlation was made between the variables and a heatmp graph was generated through the seaborn library, which presented a map of color and values in relation to the variables used. In the reading done through it was possible to identify a low correlation between the variables used in the model. It is important to note that this pattern is possible and tends to benefit machine learning models since there is no skewed data.</p>            
	<li><p align="justify">Is the solution developed passive to be applied in a way that the business identified benefits?
	The generated data solution can be applied to the real world, since non-biased data were used and high hit rates were found, according to step 5 of the CRISP-DM, where the performance evaluations of each generated model were made. The point of attention is that for this project it was defined as an objective to reach a rate above 80%, that is, specifically for this project to achieve this rate would positively reflect the success criterion of the same. However, care and attention must be paid to each company and business having their respective rates that reflect their success criteria. A rate of 80% can be great for one company, but this same rate can be bad for another, it is always necessary to evaluate the scenario of the company as a whole always.</p>
</ul>

<p align="justify">Finally, for reflective purposes only, applying data to different models is a good practice for evaluating different possibilities and choosing the one with the best accuracy for a forecast. There are several libraries focused on machine learning that can be applied in this context and expand the options for checking forecasts. In this case, the most suitable model due to its performance was the Naive Bayes.</p>

## 5. Licensing, Authors, Acknowledgements, etc.<a name="licensing"></a>

<ul>
	<li><p align="justify">Book: Hands-On Machine Learning with Scikit-Learn and TensorFlow Concepts, Tools, and Techniques to Build Intelligent Systems-O’Reilly Media</p>
	<li><p align="justify">https://www.kaggle.com/hassanamin/customer-churn</p>
</ul>
