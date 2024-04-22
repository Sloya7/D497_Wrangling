# SPARKIFY Database Project:

## General Information:
<a id="General-Information"></a>

This project's goal is to establish an easy accessed and readable POSTGRES database that combines elements from the Million Song Database and the user information from Sparkify's internal information. 

## Needed Languages:
<a id="Needed-Languages"></a>

There are two major sections to this project. One is the python script running and dataframe side and the other is the POSTGRES SQL server to upload and store data. 

_Python Notebook_

This project is created using the Jupyter Notesbook suite. Link for installing and support for Jupyter can be found here: 
    *Jupyter Install [https://jupyter.org/install]
    *Jupyter Support [https://docs.jupyter.org/en/latest/]
    
Installing Python 3 can be done here:
    *Lastest Python download [https://www.python.org/downloads/]

The following libraries need to be install and imported for this code to function: 'os', 'glob','psycopg2', and 'pandas'.



_POSTGRES CONNECTION_

Finding your POSTGRES connection:
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;From inside a POSTGRES environment
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; * Stack Overflow thread [https://stackoverflow.com/questions/5598517/find-the-host-name-and-port-using-psql-commands]   
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; From inside a terminal:
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; * Commandprompt POSTGRES  [https://www.commandprompt.com/education/how-to-checkfind-the-hostname-and-port-number-in-postgresql/]

## Data Sources and Importing:

_Data Sources_
This database sources song meta-data from the Million Song Database and imports the JSON data and uses the Sparkify log files for user meta-data. Ensure that you have appropriate credentials to the meta data sources. If you don't have the ability to access the data directly, this project has some data attached with it under 'Data' to ensure the code and server connection and processing is functional.

## Processing the Data
<a id="Process-Data"></a>
Lets get the tables set up to recieve the data and get the data processed! To do so, ensure that you run the project files in this order using you IDE. 
    1. create_tables.py
    2. etl.py
 
Your should see an output showing the processed number of processed files. Once complete, your data should now be imported into the selected POSTGRES Database for further review.
**NOTE**: This script is designed for the initial import only and wipes the SQL tables clean each time. Some slight future modification will allow for a database updating script if desired. 
 

## Troubleshooting:
<a id="Troubleshooting"></a>

If errors occur, make sure the above steps of adjusting information to the new environment are correct. Then review the outline of code below to better locate and adjust coding based on the errors recieved. 

Code Structure:
'create_tables.py' = constructs the defined tables using loops and create table SQL statements located in the 'sql_queries.py'.
etl.py = defines and executes the file gathering and processing loops.
etl.ipynb = notebook environment file for defining and importing small volumes of data to test functionality.
test.ipnb = notebook environment file with code to test sucessful imports of data into SQL server


Other Considerations:
If you are modifying or troubleshooting this coding, ensure you are opening and closing connections to your database appropriately. 
