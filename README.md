# Threat Model Example Scenario

## Example Scenario
Threat model is being performed for an E-commerce Platform that that allows customers to browse products, add items to their cart, place orders, and process payments. The platform uses a distributed, clustered infrastructure for high availability, scalability, and fault tolerance. It also includes multiple microservices like user management, inventory management, order processing, and payment gateways.

### Simple Architecture design
`+---------------------+
|  Web & Mobile Clients|
+---------------------+
         |
         v
+---------------------+
|   API Gateway       | <---- Load Balancer ---> Auto-Scaling Group (Web Servers)
+---------------------+
         | 
         v
+---------------------+     +---------------------+     +----------------------+
|   User Service      |<--->|   Order Service     |<--->|   Inventory Service  |
+---------------------+     +---------------------+     +----------------------+
         |                        |                       |
         v                        v                       v
+---------------------+     +---------------------+
|   Payment Service   |<--->|   Messaging Queue   |
+---------------------+     +---------------------+
         |
         v
+---------------------+
|   Relational DB         |
|   (Database Cluster) |
+---------------------+ `

## Tool
The tool used for Threat modelling is [Threagile](https://threagile.io/) . 
