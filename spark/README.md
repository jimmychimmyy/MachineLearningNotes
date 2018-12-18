# Spark
*Apache Spark is a unified analytics engine for large-scale data processing.*
What exactly does this mean? Put another way, spark is a high performance general-purpose cluster computing system. This means spark can be used to synchronize many computers together to perform some task much faster than a single computer could. Plus, its open source, what more could you ask for?

In my implementations I will be using PySpark, which is an API for spark programming using Python.

#### Why should I learn spark?

As datasets get larger (in the terabytes/petabytes), it becomes more and more important that we are able to manipulate and analyze data in some finite time.

Spark is capable of speeding up machine learning workloads because of its real-time processing and its in-memory data processing. What is in-memory data processing? Data is kept in RAM and can be processed in parallel. Spark is preferred over Hadoop's MapReduce because it is 100x faster and is much easier to implement.

According to Apache,
* spark runs workloads 100x faster (speed).
* spark apps can be written in many languages
* many libraries in its ecosystem which can be combined
* runs practically everywhere

#### How do I use spark?


#### What is RDD?
Resilient Distributed Datasets (RDD) is an abstract data type that supports structured and semi-structured data. Each dataset in RDD is divided into logical partitions and can be computed on different nodes of the cluster.

Two ways to create RDDs:
1. parallelizing an existing collection in your driver program
2. referencing a dataset in external storage system (such as HDFS or any data source offering a Hadoop Input Format)

Spark makes use of the concept of RDD to achieve faster and efficient MapReduce operations.

#### Spark Dataframe:
* **Immutable**
* **Lazy Evaluations** task is not executed until an action is performed
* **Distributed**

These characteristics are common to both Spark Dataframes and RDDs.

#### Setting Up:

You must always create a Spark Context which is required to execute operations in a cluster.

```
from pyspark import SparkContext
sc = SparkContext()
```

In order to use Spark Dataframe, you must do the same with SQLContext.

```
sqlContext = SQLContext(sc)
```


#### Sources
* http://spark.apache.org/
* https://www.quora.com/Why-is-Apache-Spark-used
* https://data-flair.training/blogs/6-important-reasons-to-learn-apache-spark/
* https://www.tutorialspoint.com/apache_spark/apache_spark_introduction.htm
