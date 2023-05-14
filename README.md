A small example of event driven microservices using spring boot and kafka.

Event Driven Architecture also called asynchronous communication, applications communicate with each other by sending/receiving events/messages.


Configured Kafka producer in aplication.properties of order-service project 

Configured Kafka topic KafkaTopicConfig in order-service project


Create Kafka Producer OrderProducer in OrderService Microservice

Create REST API OrderController to Send Order and Test Kafka Producer in OrderService Microservice.


Configure Kafka Consumer in application.properties of StockService Microservice



Create Kafka Consumer OrderConsumer in StockService Microservice.


Configure Kafka Consumer in application.properties of EmailService Microservice.

Create Kafka Consumer OrderConsumer in EmailService Microservice.


So now we have one kafka producer and two consumers. 


Start zookeeper and kafka :: 
sudo systemctl start zookeeper
sudo systemctl start kafka 

Run the microservices : order-service, stock-service, email-service
Test with postman by sending a request to the controller. 
