# hive

Version:
apache-hive-3.1.2

spark-3.1.2

hadoop-3.3.1

# Setup the spark with hive
1. Get into the spark directory and in jar folder, delete the old derby driver.
2. Copy the derby driver from hive lib folder and paste it into the spark jar folder.
3. Make sure the mysql-connector-java-8.0.26 is copied into the hive lib folder.
4. Also make sure the hadoop daemons are running.

# Code
1. read the csv data from hdfs(hdfs://localhost:9000/spark_sql/merged_CpuLogData.csv)
2. Create a dataframe of csv file by selecting 4 columns ie user_name, DateTime, keyboard, mouse.
3. create a temp view.


Now add this dataframe into hive table using spark.
These are the two methods.


Method 1: 
To save the dataframe into a new table in Hive we just need database. The table name can be given anything.

    df2.write.mode("overwrite").saveAsTable("test.test_data")


Method 2: 
Here test is a database name and just give anything for table name, it will create automatically.

    spark.sql("create table test.test_data2 as select * from myview")


Show the hive tables.

    dfs = spark.sql("use test")
    
    dfs1 = spark.sql("show tables")
    
    dfs1.show()
