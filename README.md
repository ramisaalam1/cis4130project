# CIS 4130 Project

## Project Description 

CIS 4130 Big Data Technologies – Semester Project
For this semester-long project, students will build a complete machine learning pipeline that incorporates big data technologies using a cloud infrastructure.  The project is split into 6 milestones that will be due throughout the semester.  The project must be original (e.g., not copied from a previous semester, competition or other source). However, code examples can be referenced (proper citations required).
To begin, create a Project Document in MS Word, Google Docs, etc. Create a cover page with CIS 4130, your name and e-mail address on it.  For each milestone, continue adding pages to this document throughout the semester.  For example, when turning in Milestone 3, include everything you wrote about in Milestones 1 and 2.
.

Milestone 1 Due 2/9/2024 (10 points)
Proposal: Research and find a data set larger than 10 GB (should be free, open source etc.)  OR  describe a plan to collect at least 10 GB of data (e.g., from Twitter or other API).    Some suggestions for data sets include Kaggle, DataHub.io, Data.gov, Open Data on AWS, UCI Machine Learning Repository, NYC OpenData, and Google Public Datasets. Try and pick a data set that aligns with your personal interests. Do not pick data sets that are mostly images, videos or audio (unless you have prior experience working with these types of data).  You may not use the Amazon Customer Reviews Data set.
Write up a brief 1 page proposal that includes a description of the data set, URL/Location for downloading the data, the data set attributes (columns), and a description of what you intend to predict, forecast, etc. using the data set.  Be clear about what column or variable you will predict and whether you will use linear regression, logistic regression or another ML model.
Submission by e-mail with Subject: CIS 4130 Project Milestone 1  attach file name: cis_4130_project_milestone_1_LastName_FirstName.pdf
.

Milestone 2 Due 3/1/2024 (15 points)
Data Acquisition: Download or collect the data into a bucket on Google Cloud Storage (or in BigQuery if that is more appropriate). Create a bucket in GCS such as my-bigdata-project-XX (where XX are your initials). Within the bucket, create folders for landing, cleaned, trusted, code and models.  Your data files should end up in the landing folder for this milestone.
Document the code, commands and steps you used to extract and collect the data.  If you are collecting data from an API, show the code used. If you are downloading the data from a site, document the commands used to download the data. The downloading process should be able to be automated (scripted) in code and repeatable. The data should not be downloaded to your own computer. Add a new section to your project document with all of the above details. You can show a screen shot (picture) of your GCS bucket and landing folder to demonstrate that you have the data downloaded. If you have extensive code examples, place these in Appendix A and just give a summary of your main steps in the body of the project report.
Submission by e-mail with Subject: CIS 4130 Project Milestone 2  attach file name: cis_4130_project_milestone_2_LastName_FirstName.pdf
.

Milestone 3 Due 3/29/2024     NEW DUE DATE: 4/5/2024 (20 points)
Exploratory Data Analysis and Data Cleaning: Write the Python, PySpark or SparkSQL codes to load the data set from GCS and produce descriptive statistics about the data.  Use a Compute Engine instance and the google-cloud-storage Python module or a Dataproc cluster. At a minimum, EDA should include the number of observations (records, images, reviews, documents, etc.), list of variables (fields or columns), number of missing (null or N/A) fields in the observations, and the min/max/avg/stdev for all numeric variables. For date variables, include min and max dates. For image data include the number of images in each category and the min/max/average height and width of the images. For reviews, tweets, comments and other text data, include the number of each document and statistics about the number of words in the documents.  Create graphs / charts to show the distribution of data (e.g., histograms for categorical variables). Copy your EDA source code into Appendix B and provide the highlights and conclusions of your work in the main part of your project report.
Create a separate Notebook that will clean your data by removing records with missing data, filling in missing values where appropriate, dropping unneeded columns and applying appropriate data types to all columns. Be sure to rename columns and remove spaces from column names. The Data Cleaning code will read data from /landing folder, apply the schema to the data, fill in nulls or remove records with nulls, remove unnecessary columns and then write the data to the /cleaned folder as a Parquet file.  Copy your data cleaning code to Appendix C.
Complete this section with a brief paragraph summarizing the data and any challenges you believe you will have in feature engineering. In your code examples, obscure any private keys (such as for kaggle.json and any GCS access key and secret key).  
Submission by e-mail with Subject: CIS 4130 Project Milestone 3  attach file name: cis_4130_project_milestone_3_LastName_FirstName.pdf
.

Milestone 4 Due 4/19/2024 (30 points)
Feature Engineering and Modeling:  Write the PySpark code to read and process this data using a Dataproc cluster. This will include code to read the source data, normalize the data, feature engineering, training/testing, validation and evaluation of the predictive models and output. 
In your project report, make a table showing the column name, data type, and feature engineering treatment (indexer, modeler, scaler etc.) you will need to complete for each column (variable) you will use in your model. (see example spreadsheet: example_features_treatment.xlsx)
Your code will read the cleaned data from the /cleaned folder, perform feature engineering, train/test split, modeling, validation and evaluation. Data with features should be saved to the /trusted folder and models should be saved to the /models folder. Copy your feature engineering and modeling code into Appendix D.
Results of the analysis should be written to a file (or a series of files). Include all source code and proper references to each of the libraries/modules you are using. The resulting code should be able to be automated (scripted). Complete this section with a brief paragraph summarizing the main steps your program takes and any challenges you may have encountered while feature engineering and modeling the data. Provide a summary of the outputs in the main part of the report.
Submission by e-mail with Subject: CIS 4130 Project Milestone 4  attach file name: cis_4130_project_milestone_4_LastName_FirstName.pdf
.

Milestone 5  Due 5/3/2024 (15 points)
Data Visualizing:  Create visualizations for the data and prediction results. Create at least four interesting visualizations that help you tell a data story and present the results.  These can be done in Python (e.g., Matplotlib, Seaborn etc.) or using a Visualization tool such as Tableau.  If possible, automate the visualizations portion of the pipeline.  Copy and paste screen shots of these visualizations into your project report document and include a few sentences of description for each of the visualizations. Include any Python codes for your visualization in an Appendix.
Submission by e-mail with Subject: CIS 4130 Project Milestone 5  attach file name: cis_4130_project_milestone_5_LastName_FirstName.pdf
.

Milestone 6 Due 5/17/2024 (10 points)  
Summary and Conclusions:  Document the completed data processing pipeline and complete the project report with a summary of the project and the main conclusions you were able to draw from the data. Be sure to include citations for any code examples or other resources used. Include the GitHub URL for the shared project (see next milestone). 
Share the Project:  Post the project description and code on GitHub.  Include the URL  of your GitHub Project in the final report. Be sure to hide any security keys, passwords, credentials, etc. that may appear in your code. When you create your GitHub account, be sure to use your real name (or as close to it as possible) so that prospective employers can find you.
Submission by e-mail with Subject: CIS 4130 Project Milestone 6  attach file name: cis_4130_project_milestone_6_LastName_FirstName.pdf
.
Project Grading
Full points will be awarded at each milestone if the materials are complete and submitted on time. Points will be deducted for late submissions, incomplete and incorrect work.  The professor reserves the right to veto the project idea if it does not meet the guidelines.
