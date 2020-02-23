# Skytrax Airline Review
This Project is about analyzing the skytrax airline review dataset where the review of the airline was given by the passengers with the respective airline. The features selected in the model comprises of numerical data. So linear Regression in Mlib Of Apache Spark is used to predict the overall rating and whether the airline is recommendable or not. The model is implemented in spark dataframe which takes Less computational storage and execution time.

## Getting Started
As the model is implememted using PySpark spark has to installed and configured in environmental Variables. Download the spark from the apache spark and configure enivornment as follows:
 SPARK_HOME- C:\Spark\spark-2.4.4-bin-hadoop2.7
 Here we have to specify the path of downloaded spark extract and name it as Spark_Home.
To install spark in anaconda prompt type the command 

conda install -c conda-forge pyspark

Then in environment variables of the system add
PYSPARK_DRIVER_PYTHON -jupyter


PYSPARK_DRIVER_PYTHON_OPTS -notebook

By adding this varibales Pyspark when called from the anaconda prompt will open in jupyter notebook.


## Data cleaning
 The missing data and messy data is cleaned up by using Openrefine.
 
 The dataset contains a blank row after every row that contain data. Select text facet for airline column and remove null feilds which elimates all the empty rows.
 
 The data in columns like Overall, Seat_comfort, Entertainment, Recommendable, food_bev etc which are actually numeric feilds are stored in string format. So they are changed into numeric data and Missing feilds are filled by using fill down transfrom. An openRefine Export is uploaded which Involve the process of data cleaning.
 
 
 ## Model Implementaion using PySpark
 
 The data is load into dataframe by using spark Session.
 
 
 Intially the aircraft feild which is feature of the model is in string format. Convert the aircraft row into numeric type by using String indexer and add it as new row as aircraft_cat.
 
 Check the schema and change the schema with appropriate data type.
 
 The Machine learning Library Support only vectors. So transform the data into Vectors Using vector assembler and then Features and label is selected and applied with the linear regression model.
 
 
 Then split the data ranomly using randomsplit as train and test data then trained and fitted with the training data and model is evaluated with Regression metrics.
 
 
The model is given with the Unlabeled data or unseen data and the labels are predicted from the given Features.


## Visualization
Visualization is done in tableau and export is uploaded as Visualization.twbx
