IBM Data Analyst Capstone Project

Disclaimer:
  This project is for pedagogical purposes to apply the skills learned in the IBM Data Analyst course to a business problem.


Business Task:
  You are a Data Analyst at a Tech company and tasked to identify trends for this year's report on emerging technical skills. This task will assist business stakeholders in making data-driven recruitment, training, and     retention decisions.

Guiding questions:
	What are the top programming languages in demand?
	What are the top database skills in demand?
	What are the popular IDEs?

Problem Statement:
	Identify trends for in-demand skills, such as programming languages, databases, and popular IDEs.

Data Sources:
  Job postings.xlsx webscraped from the Job Postings API
  popular-languages.csv, which has Annual Salary data from webscraping an HTML table
  cleaned_m5_survey_data_demographics, which is 2019 Stack Overflow Survey data

Deliverables:
  Executive Summary of key findings and insights
  IBM Cognos Analytics Dashboard
  
Description of Project Workflow:

Data collection:
  Used Python to access an API, Webscrape, and access a database.

Data Wrangling:
  Used Python and Excel to manipulate, clean, and transform my data.

API data:
  Used Python to connect to the API and pull Job posting data per city, and per programming language. I, then, formatted that data into an Excel file and wrangled it in Excel.

Microsoft Excel:
  I formmated the data into a table, created a pivot table and then pivot charts for Job postings per city, In-demand skills per city, and in-demand skills by annual salary. These charts are in the presentation appendix.

Web Scraped data:
  The web scraped data was a table that had in-demand skills by annual salaries. I scraped the data in python and then exported it to excel to make a pivot table and pivot chart.

Stack Overflow Survey:
  The stack overflow survey data's raw file has 115502 lines

Removed duplicates:
  In python I found and removed all duplicate rows, bringing it down to 11398.

Missing values:
  After that I then found all missing values, and imputed them with either the most frequent/mode (for cartegorical) or the mean (for numerical).

Normalization:
  After that, I decided that Salary was a dependent or target variable to explore. I normalized the compensation frequency, which was weekly, monthly, yearly to just yearly. This NormalizedCompensation became my target 
  variable for Salary exploration. The median Salary is $90,000.

Exploratory Data Analysis (EDA):
  From there I began to analyze the data distribution
  I created a histogram using Seaborn library in python to visualize the distribution of the annual salary. From there I found that the data was skewed left and that there were strong outliers.
  From there I plotted the annual salary as a box plot to view these outliers more clearly.
  At this point, I felt that it was important to remove the outliers to better view the interquartile distribution of the data set.
  I used python to do so, once the outliers were removed, I  replotted the boxplot and could better see the distrubtion.
  The median annual salaray is 47496 with Q1 17574 and Q3 81125 and the record count was 10408 due to the removed outliers. 

  Next, I used SQL to query the same survey as database tables. From my queries I further explored the dataset
  According to the Stack Overflow Survey
  The top 5 most desired programming language skills from respondents are:
	JavaScript
	HTML/CSS
	Python
	SQL
	TypeScript

  Top 5 Database skills
	Postgre
	MongoDB
	Redis
	MySQL
	ElasticSearch

  Top 5 Development Environments
	Visual Studio Code
	Visual Studio
	Notepad ++
	Intellij
	Vim

  Combined list of Programming Languages and Databases that are on each list:
  5 in-demand skills mentioned across each data source:
       Python
       JavaScript
       SQL
       PostgreSQL
       MongoDB
