# Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu

## AIM

To implement Pseudo Node configuration for Hadoop on ubuntu

## Pre-requisites

a) jdk

Single-Node Configuration

1.	Create a dedicated user account for hadoop

![image](https://github.com/Catty12384/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/120629225/47927dbb-ce7c-48b9-8e86-91f466cd8019)


2.	Install java1.8 in folder /usr/local

![image](https://github.com/Catty12384/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/120629225/5009c1f1-d738-4337-acf2-f379022496cd)

3.	Install Hadoop

![image](https://github.com/Catty12384/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/120629225/ee3817ae-e3a0-4bbb-b234-adf541584fa8)

4.	Set the hadoop environment variables: Include the following lines in the
$HOME/.bashrc file

![image](https://github.com/Catty12384/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/120629225/f1ea63a5-0e90-43a2-bb42-fb242436b2cd)

 
5.	Set hadoop environment variables: Include the following lines /etc/profile file

![image](https://github.com/Catty12384/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/120629225/a24a72b0-a1e8-4c8a-b853-023fddc0fae1)


6.	Run the.bashrc & profile files from the $ prompt for updating the changes

![image](https://github.com/Catty12384/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/120629225/4154d3bd-f36e-4778-8e57-2c4dcccb0bf6)

![image](https://github.com/Catty12384/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/120629225/7f1c12b6-d4eb-492b-8227-15e91b0978bb)


$ bin/hadoop version	

7.	Configuration of the hadoop files: hadoop-env.sh, core-site.xml, mapred-site.xml, hdfs- site.xml and yarn-site.xml

path ::	/usr/local/hadoop-2.5.1/etc/hadoop

a)	hadoop-env.sh
Include the following lines in hadoop-env.sh file

![image](https://github.com/Catty12384/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/120629225/844cff7e-3f1e-414e-a81e-ff3aa4f010ea)


b)	core-site.xml
Configure the directory for Hadoop to store its data files, the network ports it listens to, etc. Setup will use Hadoop’s Distributed File System (HDFS-single local machine)

![image](https://github.com/Catty12384/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/120629225/51b54485-92ea-4a57-b6eb-17076292f706)

 
Include the following lines in core-site.xml file between <configuration> and
</configuration> tags

![image](https://github.com/Catty12384/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/120629225/b432be8a-f769-42ee-996d-13233b2bd359)


c)	mapred-site.xml

```
$sudo cp mapred-site.xml.template mapred-site.xml

```

Include the following lines in mapred-site.xml file

```
<property>
<name>mapreduce.framework.name</name>
<value>yarn</value>
</property>

```
 

d)	hdfs-site.xml
Include the following lines in hdfs-site.xml file


![image](https://github.com/Catty12384/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/120629225/b1cf4c00-4d65-4c35-9c66-7f85e15f3dde)

e)	yarn-site.xml

Include the following lines in yarn-site.xml file


![image](https://github.com/Catty12384/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/120629225/7895e318-a301-4016-8b8c-76aa7a5df4dc)


8.	Format the Hadoop File system implemented on top of the local file system using


![image](https://github.com/Catty12384/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/120629225/2ca45305-78bb-4068-aff2-d1044aec5dc9)

9.	Start Hadoop using


![image](https://github.com/Catty12384/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/120629225/98da0ed2-f524-4652-b7f8-25270b410a7c)


Explore Hadoop using http://localhost:50070/ from the browser	
 
10.	The commonly used HDFS Commands are as follows:


![image](https://github.com/Catty12384/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/120629225/8fa903ec-51a5-4fb7-b756-4484b63ebbdb)


11.	Create a directory ‘/input’ in HDFS


![image](https://github.com/Catty12384/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/120629225/952e1067-a734-4730-bbdf-7419eb16edf5)

12.	Copy the input files into the distributed file system


![image](https://github.com/Catty12384/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/120629225/647ce7f2-4381-4229-a829-c63737d8575d)


13.	Run some of the examples provided


![image](https://github.com/Catty12384/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/120629225/1be95c70-727e-4a90-a0fe-e3b02fd1eb15)


14.	Examine the output files
Copy the output files from the distributed file system to the local file system and examine them:


 ![image](https://github.com/Catty12384/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/120629225/2372a3e2-975e-46b6-9e4b-b5a0bc3fe930)

or

View the output files on the distributed file system

```
$ bin/hdfs dfs -cat /output/*

```


## Result:
Thus, the implementation of Pseudo Node configuration for Hadoop on ubuntu is successfully executed.
# Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu

## AIM

To implement Pseudo Node configuration for Hadoop on ubuntu

## Pre-requisites

a) jdk

Single-Node Configuration

1.	Create a dedicated user account for hadoop

2.	Install java1.8 in folder /usr/local
3.	Install Hadoop

4.	Set the hadoop environment variables: Include the following lines in the
$HOME/.bashrc file

 
5.	Set hadoop environment variables: Include the following lines /etc/profile file


6.	Run the.bashrc & profile files from the $ prompt for updating the changes




$ bin/hadoop version	

7.	Configuration of the hadoop files: hadoop-env.sh, core-site.xml, mapred-site.xml, hdfs- site.xml and yarn-site.xml

path ::	/usr/local/hadoop-2.5.1/etc/hadoop

a)	hadoop-env.sh
Include the following lines in hadoop-env.sh file


b)	core-site.xml
Configure the directory for Hadoop to store its data files, the network ports it listens to, etc. Setup will use Hadoop’s Distributed File System (HDFS-single local machine)


 
Include the following lines in core-site.xml file between <configuration> and
</configuration> tags


c)	mapred-site.xml
 

Include the following lines in mapred-site.xml file
 

d)	hdfs-site.xml
Include the following lines in hdfs-site.xml file


e)	yarn-site.xml
Include the following lines in yarn-site.xml file
8.	Format the Hadoop File system implemented on top of the local file system using

9.	Start Hadoop using


Explore Hadoop using http://localhost:50070/ from the browser	
 
10.	The commonly used HDFS Commands are as follows:


11.	Create a directory ‘/input’ in HDFS


12.	Copy the input files into the distributed file system

13.	Run some of the examples provided


14.	Examine the output files
Copy the output files from the distributed file system to the local file system and examine them:
 
or
View the output files on the distributed file system

## Result:
Thus, the implementation of Pseudo Node configuration for Hadoop on ubuntu is successfully executed.
