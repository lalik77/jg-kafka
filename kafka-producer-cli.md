# Kafka Producer And Consumer CLI

For Mac or Linux we use `kafka-console-producer.sh` script

We must have our three servers up and running and topics created.

Let's look at the example where we don't have this topic `payment-canceled-events-topic`

![terminal-list-topic.png](img/4/terminal-list-topic.png)

Let's write this command 

![terminal-produce-message-topic-does-not-exist.png](img/4/terminal-produce-message-topic-does-not-exist.png)

We have error , after exit with `ctrl +c` 

![terminal-produce-0.png](img/4/terminal-produce-0.png)

It's not good practice because first we have an error after automatically a topic is created
with default parameters , let's see :

![terminal-topic-describe.png](img/4/terminal-topic-describe.png)

#### 1 - Send message (Publish, Produce)

`bin/kafka-console-producer.sh --topic payment-creation-events-topic --bootstrap-server localhost:9092,localhost:9094 --property "parse.key=true" --property "key.separator=:"`

![terminal-produce-1.png](img/4/terminal-produce-1.png)

![terminal-produce-2.png](img/4/terminal-produce-2.png)

#### 2 - Receive message (Consume)

For Mac or Linux we use `kafka-console-consumer.sh` script

In new tab let's write this command

`bin/kafka-console-consumer.sh --topic payment-creation-events-topic --bootstrap-server localhost:9092,localhost:9094 --from-beginning`

![terminal-consumer-1.png](img/4/terminal-consumer-1.png)

Look at those videos , we can add some options in command `--property "print.key=true"`

Consume without printing keys
https://youtu.be/Tg7Yrw8XzG4

Consume with printing keys
https://youtu.be/WOvoYe_zOR4






We can also remove `--from-beginning` flag 

