# spark-scala
## Spark Scala big data analysis of movie lens data set


# Installing Apache Spark and Scala Windows!

Spark Scala big data analysis of movie lens data set

- Install a JDK (Java Development Kit) from[link to java!](http://www.oracle.com/technetwork/java/javase/downloads/index.html). Keep track of where you installed the JDK; you’ll need that later. DO NOT INSTALL JAVA 9, 10, or 11 – INSTALL JAVA 8. Spark is not compatible with Java 9 or greater. And BE SURE TO INSTALL JAVA TO A PATH WITH NO SPACES IN IT. Don’t accept the default path that goes into “Program Files” on Windows, as that has a space.
- Download a pre-built version of Apache Spark 2.3 (do not use Spark 2.4; it has a bug and only works with Linux) from [link to spark !](https://spark.apache.org/downloads.html)
- If necessary, download and install WinRAR so you can extract the .tgz file you downloaded. http://www.rarlab.com/download.htm
- Extract the Spark archive, and copy its contents into C:\spark after creating that directory. You should end up with directories like c:\spark\bin, c:\spark\conf, etc.
- Download winutils.exe from[link to winuitls!](https://github.com/nishantvaidya/spark-scala/blob/master/winutils.exe) and move it into a C:\winutils\bin folder that you’ve created. (note, this is a 64-bit application. If you are on a 32-bit version of Windows, you’ll need to search for a 32-bit build of winutils.exe for Hadoop.)
- Create a c:\tmp\hive directory, and cd into c:\winutils\bin, and run winutils.exe chmod 777 c:\tmp\hive
- Open the the c:\spark\conf folder, and make sure “File Name Extensions” is checked in the “view” tab of Windows Explorer. Rename the log4j.properties.template file to log4j.properties. Edit this file (using Wordpad or something similar) and change the error level from INFO to ERROR for log4j.rootCategory
- Right-click your Windows menu, select Control Panel, System and Security, and then System. Click on “Advanced System Settings” and then the “Environment Variables” button.
- Add the following new USER variables:
SPARK_HOME c:\spark
JAVA_HOME (the path you installed the JDK to in step 1, for example C:\ProgramFiles\Java\jdk1.8.0_101)
HADOOP HOME c:\winutils
- Add the following paths to your PATH user variable:
%SPARK_HOME%\bin
%JAVA_HOME%\bin

- Close the environment variable screen and the control panels.
- Install the latest Scala IDE from [link to Scala IDE!](http://scala-ide.org/download/sdk.html)
- Test it out!
Open up a Windows command prompt in administrator mode.
Enter cd c:\spark and then dir to get a directory listing.
Look for a text file we can play with, like README.md or CHANGES.txt
Enter spark-shell
At this point you should have a scala> prompt. If not, double check the steps above.
Enter val rdd = sc.textFile(“README.md”) (or whatever text file you’ve found) Enter rdd.count()
You should get a count of the number of lines in that file! Congratulations, you just ran your first Spark program!
Hit control-D to exit the spark shell, and close the console window.

# Importing and running this project in Downloaded Eclipse IDE.
 - Open up IDE
 - Create a Scala project using New option in Eclipse.
 - Create a package com.test.spark in project.
 - Click on Import button and choose file system option and select scala source code folder project.
 - Import RatingsCounter.sc file
 - Right click on project -> properties-> Java build path -> libraries -> Add external Jar -> Import all jars from downloades scala/Jar folders.
 - Right click again on project -> properties-> Scala compiler -> check use project setting box-> select 2.11 in scala installation dropdown.
 - Dowload ml-100k from [link to DataSet!](http://files.grouplens.org/datasets/movielens/ml-100k.zip) link.
 - unzip in work-space folder.
 - Run the program. you should see below result. Congratulations.!!
   - (1,6110)
   - (2,11370)
   - (3,27145)
   - (4,34174)
   - (5,21201)
## *Scala Basic Example*
- Create a seperate project for LearningScala1 to 4 files in source code folder
- LearningScala1.sc will provide basis idea for variable declaration, variable type , operations, print formatting etc.
  *val is immutable variable and scala recommend to use it highly comarpe to var in functional programming.
- LearningScala2.sc will provide basic programme on flow execution.
- LearningScala3.sc will provide basic programmes on function declartion, functional literal(lambada expression).
- LearningScala4.sc will provide basic programme on scala collections.
  - *Tuple is immutable list in scala similar to pytho var tuple = ("1","2","3");*
  - *List is mutalbe collection var list = List("string", 1, "3");It is singley link list and tail method gives all element except first*
  - *Map is another collection in scala var map = Map("a"->"b", "key2"->"value2")*
