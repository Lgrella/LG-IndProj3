# Individual Project 3 for Data Engineering Systems

The purpose of this project is to work with the Databricks platform, which is designed for massive-scale data engineering and collaborative data science.

Project Requirements:
* A well-documented Databricks notebook that performs ETL (Extract, Transform, Load) operations, checked into the repository.
* Usage of Delta Lake for data storage (show you understand the benefits).
* Usage of Spark SQL for data transformations.
* Proper error handling and data validation.
* Visualization of the transformed data.
* An automated trigger to initiate the pipeline.


To do this, I created a data pipeline using the Databricks platform. 

I connected my github repository with my databricks workspace and pushed my three notebooks (ingest, prepare, and analyze songs) to this repository.

Steps to Build ETL Pipeline in Databricks: 
1. Create a cluster. Using the compute tab in the Databricks menu bar,I first created a new cluster with a unique name.
2. Ingest the data. After creating a new notebook (by selecting new->notebook), I use AutoLoader, which works to automatically detect and process new files as they arrive in cloud object storage, to ingest the data into a delta lake.
3. Prepare the data. In this step, we first install the data into databases that are filtered to the columns we need. In this step, I also perform data validation to confirm the year variable is acting as expected. We learn in this step that year is 0, essentially missing, for many records. This is important to keep in mind when analyzing the visualization.
4. Query the data. I first want to answer the question of who have the most hit songs in a single year. After querying, and reviewing the results in the form of a table, I use databricks visualization software to make a graphical version of this query (see screenshot below).
5. Lastly, I make a job that runs this pipeline automatically on any push, see the workflow below. 

Below is a screenshot of my visualization made with Databricks Visualization software: Songs Over Time
![newplot](/newplot.png)

Below is a screenshot of my workflow in databricks (ingest -> prepare -> analyze)
![Workflow](/Workflow.png)

In conclusion, if this analysis/visualization were to go to management, the two important facts that shine are 1) expect 4 songs or less 2)fewer songs become hit songs. 

I would also argue that this is historical data and we are in a new environment now with social media like TikTok. It is not smart to assume we are following historical trends.

# Youtube Demo: 
[Demo for Individual Project 3](https://youtu.be/kmbNlLlhOMU)
