# Hadoop

Browsing LinkedIn or Glassdoor for machine learning jobs, you start to notice that most, if not all listings, ask that potential candidates know how to use Hadoop. So what exactly is Hadoop?

Hadoop is a framework for storing and running analysis on large datasets on many machines simultaneously.
According to Apache: The Apache Hadoop software library is a framework that allows for distributed processing of large datasets across clusters of computers using simple programming models ([1](https://readwrite.com/2013/05/23/hadoop-what-it-is-and-how-it-works/)).

Hadoop consist of two main parts: **data processing framework (MapReduce)** and **distributed file system (HDFS)**.

###### Imagine if you had a file that was larger than the storage capacity of your machine, Hadoop would allow you to store this file across multiple machines?

#### What is Hadoop used for?

* Merging large datasets of various types from different sources
* ###### Projects that require clusters of servers where specialized data management and programming skills are limited, implementations are costly?
* **Hadoop should be used only when the datasets are in petabytes or terabytes other wise it would be better to use Postgres or Excel**

#### Why use Hadoop
* Huge cost savings compared to legacy systems
* Robust community for support and advancement

#### How does Hadoop Work?
* HDFS writes data once to server then reads and reuses it many times


#### What is Hadoop MapReduce?

MapReduce is the tool that processes your data.

Hadoop is not a database, it stores data and allows you to access that data but you cannot query Hadoop. Instead, you must rely on MapReduce to process the data.

Job scheduling and processing across the cluster.

#### What is Hadoop Distributed File System (HDFS)?

File system management across the cluster.

#### What is Hadoop Common?

Provided common utilities that can be used across all modules.

#### What is Hadoop YARN?

Improved version of MapReduce.

#### What is Amazon's S3 filesystem?

#### Sources
1. https://readwrite.com/2013/05/23/hadoop-what-it-is-and-how-it-works/
2. https://www.ibm.com/analytics/hadoop/mapreduce
3. https://www.dezyre.com/article/hadoop-explained-how-does-hadoop-work-and-how-to-use-it-/237
