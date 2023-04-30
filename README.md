Download Link: https://assignmentchef.com/product/solved-mie1624-assignment2-logistics-regression
<br>
For this assignment, you are responsible for answering the below questions based on the dataset provided. You will then need to submit a 3-page report in which you present the results of your analysis. In your report, you should use visual forms to present your results. How you decide to present your results (i.e. with tables/plots/etc.) is up to you but your choice should make the results of your analysis clear and obvious. In your report, you will need to explain what you have used to arrive at the answer to the research question and why it was appropriate for the data/question. You must interpret your final results in the context of the dataset for your problem.

<strong><u>Background:</u> </strong>

In this assignment, we will continue to work on the “<strong>2020 Kaggle Machine Learning &amp; Data Science Survey</strong>” dataset.

The purpose of this challenge was to “<em>tell a data story about a subset of the data science community represented in this survey, through a combination of both narrative text and data exploration.</em>” More information on the competition, data, and prizes can be found on: <u>https://www.kaggle.com/c/kaggle-survey2020/data</u>

The dataset provided (Kaggle_survey_2020_responses.csv) contains the survey results provided by Kaggle<em>. </em>The survey results from 20036 participants are shown in 355 columns, representing survey questions. Not all questions are answered by each participant, and responses contain various data types. In the dataset, column Q24 <em>“What is your current yearly compensation (approximate $USD)?” </em>contains the <strong>ordinary categorical</strong> target variable. The original data (kaggle_survey_2020_responses.csv) has been transformed to <strong>clean_kaggle_data_2020.csv</strong> as per the code given in <strong>KaggleSalary_DataSet.ipynb</strong>. In the dataset to be used for Assignment 2 (<strong>clean_kaggle_data_2020.csv</strong>– File to be read in notebook for this Assignment, <strong>You should work with the clean dataset for this assignment</strong>), rows with the null values of salaries have been dropped. In addition, two columns (‘Q24_Encoded’ and ‘Q24_buckets’) has been added at the end. Column ‘Q24_buckets’ (Target Variable for Assignment 2) have been obtained by combining some salary buckets in the column ‘Q24’. Column ‘Q24_Encoded’ has been obtained by label encoding the column ‘Q24_buckets’.

The purpose of this assignment is to train, validate, and tune multi-class ordinary classification models that can classify, given a set of survey responses by a data scientist, what a survey respondent’s current yearly compensation bucket is.

<strong>Classification</strong> is a supervised machine learning approach used to assign a discrete value of one variable when given the values of others. Many types of machine learning models can be used for training classification problems, such as logistic regression, decision trees, kNN, SVM, random forest, gradientboosted decision trees and neural networks. In this assignment you are <strong>required to use the ordinal logistic regression algorithm</strong>, but feel free to experiment with other algorithms.

For the purposes of this assignment, any subset of data can be used for data exploration and for classification purposes. For example, you may focus only on one country, exclude features, or engineer new features. If a subset of data is chosen, it <strong>must contain at least 5000 training examples</strong>. You must <strong>justify and explain</strong> why you are selecting a subset of the data, and how it may affect the model.

Data is often split into training and testing data. The training data is typically further divided to create validation sets, either by just splitting, if enough data exists, or by using <strong>cross-validation</strong> within the training set. The model can be iteratively improved by tuning the hyperparameters or by feature selection.




<strong><u>Learning objectives:</u> </strong>

<ol>

 <li>Understand how to clean and prepare data for machine learning, including working with multiple data types, incomplete data, and categorical data. Perform data standardization/normalization, if necessary, prior to modeling.</li>

 <li>Understand how to apply machine learning algorithms (logistic regression) to the task of classification.</li>

 <li>Improve on skills and competencies required to compare performance of classification algorithms, including application of performance measurements, and visualization of comparisons.</li>

 <li>Understand how to improve the performance of your model.</li>

 <li>Improve on skill and competencies required to collate and present domain specific, evidence-based insights.</li>

</ol>




<strong><u>Questions:</u> </strong>

The following sections should be included but the order does not need to be followed. The discussion for each section is included in that section’s marks.

<ol>

 <li><strong> Data cleaning: </strong></li>

</ol>

While the data is made ready for analysis, several values are missing, and some features are categorical. Note that some values that appear “null” indicate that a survey respondent did not select that given option from a multiple-choice list. For example – “<em>Which of the following hosted notebook products do you use on a regular basis?  (Select all that apply) – Selected Choice –  Binder / JupyterHub</em>”.

For the data cleaning step, handle missing values however you see fit and <strong><em>justify your approach</em></strong>. Provide some insight on why you think the values are missing and how your approach might impact the overall analysis. Suggestions include filling the missing values with a certain value (e.g. mode for categorical data) and completely removing the features with missing values. Secondly, convert categorical data into numerical data by encoding and explain why you used this particular encoding method.

These tasks can be done interchangeably, e.g., encoding can be done first.

<ol start="2">

 <li><strong> Exploratory data analysis and feature selection: </strong></li>

</ol>

For the exploratory data analysis step, visualize the order of feature importance. Some possible methods include correlation plot, or a similar method. Given the data, which of the original attributes in the data are most related to a survey respondent’s yearly compensation?

Explain how feature engineering is a useful tool in machine learning in the context of the tasks in this assignment. Apply feature engineering and then select the features to be used for analysis either manually or through some feature selection algorithm (e.g. regularized regression).




Not all features need to be used; features can be removed or added as desired. If the resulting number of features is very high, dimensionality reduction can also be used (e.g. PCA). Use at least one feature selection technique – describe the technique and <strong><em>provide justification</em></strong> on why you selected that set of features.




<ol start="3">

 <li><strong>[4pts] Model implementation: </strong></li>

</ol>

Implement <strong>ordinal logistic regression</strong> algorithm on the training data using <strong>10-fold crossvalidation</strong>. How does your model accuracy compare across the folds? What is average and variance of accuracy for folds? Treating each value of hyperparameter(s) as a new model, which model performed best? Give the reason based on bias-variance trade-off. An output of your algorithm should be a probability of belonging to each of the salary buckets. Apply scaling/normalization of features, if necessary, and justify the reason why scaling/normalization is (not) needed.

<ol start="4">

 <li><strong>Model tuning: </strong></li>

</ol>

Identify all hyperparameters in your model. Select two hyperparameters for model tuning and justify your selection. Improve the performance of the models from the previous step with hyperparameter tuning and select a final optimal model using grid search based on a metric (or metrics) that you choose. Choosing an optimal model for a given task (comparing multiple classifiers on a specific domain) requires selecting performance measures, for example accuracy, precision, recall and/or F1-score to compare the model performance. Justify the metric you selected. There is no minimum model accuracy, as long as your methodology is reasonable and well explained.

<ol start="5">

 <li><strong> Testing &amp; Discussion: </strong></li>

</ol>

Use your optimal model to make classifications on the test set. How does your model perform on the test set vs. the training set? The overall fit of the model, how to increase the accuracy (test, training)? Is it overfitting or underfitting? Why? Plot the distribution of true target variable values and their predictions on both the training set and test set. What insight have you gained from the dataset and your trained classification model?

Insufficient discussion will lead to the deduction of marks.

<ul>

 <li></li>

</ul>




<strong><u>Tools:</u> </strong>

<ul>

 <li><strong>Software: </strong>

  <ul>

   <li><strong>Python Version 3.X </strong>is required for this assignment. our code should run on the CognitiveClass Virtual Lab <u>http://labs.cognitiveclass.ai</u> (Kernel 3). All libraries are allowed but here is a list of the major libraries you might consider: Numpy, Scipy, Sklearn, Matplotlib, Pandas.</li>

  </ul></li>

</ul>

○No other tool or software besides Python and its component libraries can be used to touch the data files. For instance, using Microsoft Excel to clean the data is not allowed.

○ Read the required data file from the same directory as your notebook on the CognitiveClass

Virtual Lab – for example, pd.read_csv(“clean_kaggle_data_2020.csv”).




<ul>

 <li><strong>Required data files: </strong>

  <ul>

   <li><strong>csv</strong>: file to be read in notebook for this Assignment</li>

  </ul></li>

</ul>

○ The data file cannot be altered by any means. The notebook will be run using the local version of this data file. Do not save anything to file within the notebook and read it back.

<strong> </strong>

<ul>

 <li>Auxiliary files:

  <ul>

   <li><strong>csv</strong>: original survey responses.</li>

  </ul></li>

</ul>

○ <strong>kaggle_survey_2020_answer_choices.pdf</strong>: the questions and answer choices in the survey.

○ <strong>kaggle_survey_2020_methodology.pdf</strong>: the methodology and survey flow logic of the survey.

○ <strong>KaggleSalary_DataSet.ipynb</strong>: the code used to transform the original survey responses

(<strong>kaggle_survey_2020_responses.csv</strong>) to the clean dataset <strong>clean_kaggle_data_2020.csv </strong>

<strong><u>What to submit:</u> </strong>