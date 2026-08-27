# Message broker 
- A message broker is software that receives message from one service and delivers them to another service . 
- Producer → Message Broker → Consumer

  Example: In an e-commerce system:

  Order Service → Broker → Email Service
                         → Inventory Service
                         → Payment Service

  When an order is placed, the Order Service publishes an OrderCreated message. The broker stores and
  routes it to the services that need it. 


- Popular message brokers include are :- 
   - RabbitMQ 
   - Apache Kafka 
   - Amazon SQS
   - Google pub/sub 
   - Redis Stream 

