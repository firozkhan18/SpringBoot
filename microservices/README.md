# Spring Boot Microservices

# Contents

- [01 - Building_Services](../lessons/069)
- [02 - EKS Cluster Auto Scaling](../lessons/070)
- [03 - Kubernetes Horizontal Pod Autoscaler](../lessons/071)
- [04 - How to Install Prometheus on Kubernetes Cluster?](../lessons/072)
- [05 - Horizontal Pod Autoscaler CUSTOM METRICS & PROMETHEUS](../lessons/073)
- [06 - Vertical Pod Autoscaling](../lessons/074)
- [07 - AWS Serverless Application Model](../lessons/075)
- [08 - How to Build Slack Bot?](../lessons/076)
- [09 - AWS Lambda Secrets Manager Example](../lessons/077)
- [10 - How to Secure Nginx with Lets Encrypt on Ubuntu 20.04 with Certbot?](../lessons/078)

Part_01_Spring_Boot_Microservices_Building_Services.md
Part_02_Spring_Boot_Microservices_Inter_Service_Communication.md
Part_03_Spring_Boot_Microservices_Service_Discovery.md
Part_04_Spring_Boot_Microservices_API_Gateway.md
Part_05_Spring_Boot_Microservices_Security.md
Part_06_Spring_Boot_Microservices_Resilience4J_Circuit_Breaker.md
Part_07_Spring_Boot_Microservices_Distributed_Tracing.md
Part_08_Spring_Boot_Microservices_Event_Driven_Architecture_Using_Kafka.md
Part_09_Spring_Boot_Microservices_Dockerize_The_Application.md
Part_10_Spring_Boot_Microservices_Monitoring_Using_Prometheus_And_Grafana.md


## How to run the application using Docker

1. Run `mvn clean package -DskipTests` to build the applications and create the docker image locally.
2. Run `docker-compose up -d` to start the applications.

## How to run the application without Docker

1. Run `mvn clean verify -DskipTests` by going inside each folder to build the applications.
2. After that run `mvn spring-boot:run` by going inside each folder to start the applications.
