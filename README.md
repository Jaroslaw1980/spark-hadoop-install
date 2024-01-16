# spark-hadoop-install
Installation process of spark and hadoop on local computers.

## 1. Install JDK
Install long term support jdk compatible with spark:
```
https://download.oracle.com/java/17/latest/jdk-17_windows-x64_bin.zip
```
after downloading the archive unpack it to c:\jdk

## 2. Install spark
Isntall spark with hadoop, use version 3.5.0 and pre-built Apache Hadoop 3.3 and later
```
https://spark.apache.org/downloads.html
```
unpack it to c:\spark
find log4j.properties.template and rename it to log4j.properties
open it up and change:
```
log4j.rootCategory=INFO -> log4j.rootCategory=ERROR
```
## 3. Install winutils
download winutils version for hadoop downloaded with spark
```
https://github.com/cdarlint/winutils/tree/master
```
place it in hadoop folder

## 4. Add user variables

SPARK_HOME 
JAVA_HOME
HADOOP_HOME
PYSPARK_PYTHON
path for user variables:
%SPARK_HOME%\bin
%JAVA_HOME%\bin



