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

<p align="justify">In the development of the project, I divided into the following tasks:</p>

<ol>
	<li><p align="justify">Exploratory Data Analysis: Before making recommendations of any kind, you will need to explore the data you are working with for the project. Dive in to see what you can find. There are some basic, required questions to be answered about the data you are working with throughout the rest of the notebook. Use this space to explore, before you dive into the details of your recommendation system in the later sections.</li>			
	<li><p align="justify">Rank Based Recommendations: To get started in building recommendations, you will first find the most popular articles simply based on the most interactions. Since there are no ratings for any of the articles, it is easy to assume the articles with the most interactions are the most popular. These are then the articles we might recommend to new users (or anyone depending on what we know about them).</p>
	<li><p align="justify">User-User Based Collaborative Filtering: In order to build better recommendations for the users of IBM's platform, we could look at users that are similar in terms of the items they have interacted with. These items could then be recommended to the similar users. This would be a step in the right direction towards more personal recommendations for the users. You will implement this next.
	<li><p align="justify">Matrix Factorization: Finally, you will complete a machine learning approach to building recommendations. Using the user-item interactions, you will build out a matrix decomposition. Using your decomposition, you will get an idea of how well you can predict new articles an individual might interact with (spoiler alert - it isn't great). You will finally discuss which methods you might use moving forward, and how you might test how well your recommendations are working for engaging users.</p>
</ol>

## 5. Licensing, Authors, Acknowledgements, etc.<a name="licensing"></a>

<ul>
	<li><p align="justify">Book: Hands-On Machine Learning with Scikit-Learn and TensorFlow Concepts, Tools, and Techniques to Build Intelligent Systems-O’Reilly Media</p>
</ul>
