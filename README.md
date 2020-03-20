# kafkaWriteStrategy
A simple MongoDB Kafka connector custom write strategy to get you started.


## Prerequisites
Get the Kafka connector demo environment up and running:
http://docs.mongodb.com/kafka-connector/master/kafka-docker-example/

## Build Custom Write Strategy JAR File
Clone Repo:
https://github.com/felixreichenbach/kafkaWriteStrategy

Cd into the directory and run:

```mvn clean install```

## Deploy Custom Write Strategy JAR File
Copy the jar file into the "connect" container:

```docker cp ./target/kafka-write-strategy-1.0-SNAPSHOT.jar connect:/usr/share/confluent-hub-components/kafka-connect-mongodb/lib/kafka-write-strategy-1.0-SNAPSHOT.jar```


Restart the container “connect”:

```docker restart connect


