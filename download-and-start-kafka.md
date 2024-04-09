
1 - Download Apache Kafka 
From official site
![apche-kafka-download.png](img/1/apche-kafka-download.png)

2 - Start Kafka
There is 2 ways to start Kafka :
- Zookeper
- KRaft
In this tutorial we will start it with Kraft
  
3 - After downloading Apache Kafka 
 We have the KRaft config files here \config\kraft
that we have to point before run the server.
We  will use the server.properties

![kraft-configs.png](img%2Fkraft-configs.png)


3 - Launch the server
How we can start the server, we have `bin` folder and `bin\windows` 
where we will use scripts.

 3.1 - Generate a Cluster UUID
![kafka-storage-random-uuid.png](img/1/kafka-storage-random-uuid.png)

 3.2 - Format Log Directories
 ![format-log-directories.png](img/1/format-log-directories.png)

3.2 - Start the Kafka Server with default properties

![kafka-started-1.png](img/1/kafka-started-1.png)

![kafka-started-2.png](img/1/kafka-started-2.png)

