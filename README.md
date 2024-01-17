# spark-hadoop-install
Installation process of spark and hadoop on local computers.

## 1. Install JDK
Install long term support jdk compatible with spark:
```
https://download.oracle.com/java/17/latest/jdk-17_windows-x64_bin.zip
```
after downloading the archive unpack it to c:\jdk

## 2. Install spark
Install spark with hadoop, use version 3.5.0 and pre-built Apache Hadoop 3.3 and later
```
https://spark.apache.org/downloads.html
```
unpack it to c:\spark
find log4j.properties.template (spark\conf folder) and rename it to log4j.properties
open it up and change:
```
rootLogger.level = info -> rootLogger.level = error
```
save the file after
## 3. Install winutils
download winutils version for hadoop downloaded with spark
```
https://github.com/cdarlint/winutils
```
click the green *Code* button and choose the option do download zip archive
uzip the archive and place it in c:\hadoop folder

## 4. Add user variables

SPARK_HOME 
JAVA_HOME
HADOOP_HOME
PYSPARK_PYTHON
path for user variables:
%SPARK_HOME%\bin
%JAVA_HOME%\bin



