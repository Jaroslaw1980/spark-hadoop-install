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
click the green *Code* button and choose the option do download zip-archive  
uzip the archive and place it in c:\hadoop folder  
choose version 3.3.5  
!!! HINT if you set variables for Hadoop type in command prompt:
```
%HADOOP_HOME%/bin/wintuils.exe
```
if error pop up  
paste in bin folder missing .dll from the repo

## 4. Add user variables
Open Environmet Variables on your computer and add new User Variables for you:

* for Spark
click *New...* button and in *Variable name:* field type:
```
SPARK_HOME
```
on *Variable value:* field click *Browse Directory...* button and find folder where you unpack your spark+hadoop  
for example: c:\spark,  
in this folder there should be spark folders like bin, conf, data etc.

* for Java set Variable name to:
```
JAVA_HOME
```
and for Variable value use the path to jdk for example c:\jdk

* for Hadoop set variable name to:
```
HADOOP_HOME
```
and variable value as path to hadoop for example c:\hadoop

* for pyspark:
```
PYSPARK_PYTHON
```
and path to your python install on your computer, for that,  
open command prompt on windows and type:
```
where python
```
copy paste this path into PYSPARK_PYTHON variable value

* for path variables:  
use *Edit...* button on your User variables *Path* variable, and then use *New* button and add those variables:
```
%SPARK_HOME%\bin
```
click *Enter* after adding variable
```
%JAVA_HOME%\bin
```
hit *OK* button after adding variables.




