# Mini-Project 11 for Data Engineering Systems

The purpose of this project is to work with the Databricks platform, which is designed for massive-scale data engineering and collaborative data science.

To do this, I created a data pipeline using the Databricks platform. 

I connected my github repository with my databricks workspace and pushed my three notebooks (ingest, prepare, and analyze songs) to this repository.

Ingest: 
* Provides filepaths for input and output datasets
* creates a spark SQL schema which maps the dataset to sql columns with datatypes
* reads the data in

Prepare:
* Using SQL code, the program formally creates the sql database

Analyze: 
* Again using a SQL query, this program answers the question: "Which artists released the most songs each year?"

Below is a screenshot of my workflow in databricks (ingest -> prepare -> analyze)
![Workflow](/Workflow.png)
