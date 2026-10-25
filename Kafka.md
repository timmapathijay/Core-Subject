Q1. What is Apache Kafka and why did you use it in your projects ?
- Apache Kafka is a distributed event-streaming platform used for asynchronous communication between microservices.
In our project we used kafka to publish & consume business events. Instead of making synchronous REST API calls 
between every services, we could publish events to Kafka topics and interested services could consume them independently.
This helped us to reduce tight coupling between services and improves scalability and reliability.

- REST APIs are generally synchronous request-response interactions, whereas Kafka enables asynchronous, event-driven communication.

Topic - A logical category where kafka records are stored 
Partition - A portion of a topic that stores an ordered sequence of records
Offset	- The position of a record within a partition
Producer - Application that publishes records
Consumer - Application that reads records
Consumer group	- Consumers that share processing of topic partitions

Q2. What is consumer lag in Kafka ?
- Consumer lag indicates how far a consumer group is behind the latest available records in a Kafka partition.

DLQ  - A Dead Letter Topic stores messages that could not be processed successfully after the configured retry attempts.
