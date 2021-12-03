# mnist-classifier-apachespark

PROBLEM STATEMENT
    • Form an apache cluster on spark connecting 2 or more systems
    • Run wordcount program on cluster
    • Run a classification algorithm on cluster



REQUIREMENTS
 Three computer systems whose internet connections (either Ethernet or Wi-Fi) are
under same DNS server
 Java version 1.8 installed
 Anaconda version 5.3.0 installed
 Hadoop winutils-2.6.0 installed
 Apache spark installed (spark-2.3.1-bin-hadoop2.7.taz)
 scala-SDK-4.7.0 installed
 A text file as input to the wordcount program
 A large data whose memory as high as 500MB


CLUSTER FORMATION

Java is the building block for spark and scala. Hence for the spark and scala to work on java
anywhere the paths in the system has to be set right in all the three systems.
The environment variables,

HADOOP_HOME = where the winutils is installed
JAVA_HOME = where is the jdk file is present
SPARK_HOME = where spark is installed



MASTER NODE CREATION
 Open anaconda prompt in the system which you want to become as a master and
change the directory spark bin folder
 Type spark-class org.apache.spark.deploy.master.Master and hit enter
 The machine is set as master
 Open localhost:8080 in the master system , and note down the ip address of the master
system
 Now add workers under the master



SLAVE NODE CREATION
 Open anaconda prompt in the systems which you want to become as workers and
change the directory spark bin folder
 Type org.apache.spark.deploy.worker.Worker spark://ip-address-of-master
 This system is added as a worker under the previously formed master

