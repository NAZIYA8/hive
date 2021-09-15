# hive

# cpulogdata_task

hive version 3.1.2
pyhive version 2.6.1

# Aim of the program is to put cpulogdata csv file from hdfs into hive database using pyhive library.
Columns to consider user_name,boot_time,keyboard,mouse
1) Display users and their record counts
2) Finding users with highest number of average hours
3) Finding users with lowest number of average hours
4) Finding users with highest numbers of idle hours
5) Finding users with highest numbers of times late comings

Note: 
The difference of every record is with a difference of 5 min.
If x is user logged in at 10:00 then his second entry will be at 10:05
so every entry is with difference of 5min

# Step1:
Open terminal and start hadoop daemons: 
start-all-sh 
Copy the csv file into hdfs directory into a folder load all csv into hdfs using put command into a folder.


# Step2:
Start hiveserver2 on a terminal Import the necessary library and credentials to make a connection.
Hiveserver2


# Step3:
Code:hive.py

1.Import the necessary libraries.

2.Create connection. 

3.Create a database.

4.Create a table and load the csv file from hdfs.

5.Load the hive data into pandas dataframe.


# Step 4:
Code: cpulogdata.ipynb

1.Import the necessary libraries.

2.Create connection with hive.

3.Find users with lowest number of average hours

4.Find users with highest number of average hours

5.Visualisation with matplotlib ie bar chart and pie chart for work hours.

6.Display user and their counts

7.Barplot and pie chart for displaying user and their counts.




