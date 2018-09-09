# Hadoop

Browsing LinkedIn or Glassdoor for machine learning jobs, you start to notice that most, if not all listings, ask that potential candidates know how to use Hadoop. So what exactly is Hadoop?

Hadoop is a framework for storing and running analysis on large datasets on many machines simultaneously.
According to Apache: The Apache Hadoop software library is a framework that allows for distributed processing of large datasets across clusters of computers using simple programming models ([1](https://readwrite.com/2013/05/23/hadoop-what-it-is-and-how-it-works/)).

###### Imagine if you had a file that was larger than the storage capacity of your machine, Hadoop would allow you to store and process this file across multiple machines?

#### What is Hadoop used for?

* Merging large datasets of various types from different sources
* ###### Projects that require clusters of servers where specialized data management and programming skills are limited, implementations are costly?
* **Hadoop should be used only when the datasets are in petabytes or terabytes other wise it would be better to use Postgres or Excel**

###### Note that Big Data is considered to be any data that cannot reside in Hard Disk or single System (its size is more than 1000s of GBs)

#### What does Hadoop actually do?

Hadoop can be used to solve many problems including:
* recommendation systems
* identifying classes
* fraud detection
* building indexes
* sentiment analysis
* etc

Basically, Hadoop distributes the same job across the cluster and gets it done within very limited time on a cluster of commodity hardware.

#### Why use Hadoop
* Huge cost savings compared to legacy systems
* Robust community for support and advancement

#### How does Hadoop Work?
* HDFS writes data once to server then reads and reuses it many times
* Job Tracker is the master node which manages all Task Tracker slave nodes and executes the jobs
* Whenever some data is required, request is sent to **NameNode** (master node) of HDFS and manages all the **DataNode** (slave nodes). The request is passed on all the slave nodes which serve the required data.
* **Heartbeat** is a ping sent by all slaves to their master to indicate that the slave is still alive
* MapReduce/YARN are used for scheduling and processing. MapReduce executes a sequence of jobs where each job is a Java application that runs on the data. Alternative querying tools (**Pig Hadoop**, **Hive Hadoop**, etc) provide more power and flexibility to the user.

#### What are the main components of Hadoop?
* **Hadoop Common**
  * Provided common utilities that can be used across all modules.
  * contains libraries and utilities needed by other Hadoop modules
* **Hadoop Distributed File System (HDFS)**
  * File system management across the cluster.
* **Hadoop MapReduce**
  * Job scheduling and processing across the cluster.
  * Hadoop is not a database, it stores data and allows you to access that data but you cannot query Hadoop. Instead, you must rely on MapReduce to process the data.
* **Hadoop YARN**
  * Improved version of MapReduce

#### How to use Hadoop?

Read [this[4]](https://www.dezyre.com/article/cloudera-vs-hortonworks-vs-mapr-hadoop-distribution-comparison-/190).

#### Choosing the right Hadoop Distribution for your needs
* Cloudera (CDH)
* Hortonworks
* MapR

All three distributions use the **Core Distribution** of Hadoop.

#### What is Amazon's S3 filesystem?

#### Sources
1. https://readwrite.com/2013/05/23/hadoop-what-it-is-and-how-it-works/
2. https://www.ibm.com/analytics/hadoop/mapreduce
3. https://www.dezyre.com/article/hadoop-explained-how-does-hadoop-work-and-how-to-use-it-/237
4. https://www.dezyre.com/article/cloudera-vs-hortonworks-vs-mapr-hadoop-distribution-comparison-/190
5. https://www.quora.com/How-should-I-start-learning-Hadoop
