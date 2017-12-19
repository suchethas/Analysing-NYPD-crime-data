# Big-cleaned-Project

#### cleanedset
Cleaned.csv: https://1drv.ms/u/s!AnUiz0e7FgpJwTLXrv4zANzPHHxK

#### cleaned Exploration:

##### General Instructions :

1. Each of the analysis features we used are included folder wise
2. The Jupyter Notebook inside is self-explanatory. All the pyspark scripts and the graphs are included.
3. All the pyspark scripts were run on cleaned.csv and are called analysis.py

##### Instructions for Dumbo :

1. Login to Dumbo
2. Setup the following alias :
	* alias hfs='/usr/bin/hadoop fs '
	* export HAS=/opt/cloudera/parcels/CDH-5.9.0-1.cdh5.9.0.p0.23/lib
	* export HSJ=hadoop-mapreduce/hadoop-streaming.jar
	* alias hjs='/usr/bin/hadoop jar $HAS/$HSJ'
3. Upload the dataset to Dumbo
	* On MacOS, open Treminal and run :
		scp cleaned.csv your_netid@dumbo.es.its.nyu.edu:/home/your_netid/
	* On Windows, run cmd.exe and run :
		pscp cleaned.csv your_netid@dumbo.es.its.nyu.edu:/home/your_netid/
	* The file cleaned.csv is already available at  /home/nn1024/
4. Upload the file to hadoop from your local using the command:
	* hadoop fs -copyFromLocal cleaned.csv
5. Run command: 	
  * spark-submit analysis.py cleaned.csv
  * hadoop fs -getmerged cleaned.csv cleaned.csv




