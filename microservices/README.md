# Spring Boot Microservices

# Contents

- [01 - How to Create GKE Cluster Using TERRAFORM from Scratch?](../lessons/069)
- [02 - EKS Cluster Auto Scaling](../lessons/070)
- [03 - Kubernetes Horizontal Pod Autoscaler](../lessons/071)
- [04 - How to Install Prometheus on Kubernetes Cluster?](../lessons/072)
- [05 - Horizontal Pod Autoscaler CUSTOM METRICS & PROMETHEUS](../lessons/073)
- [06 - Vertical Pod Autoscaling](../lessons/074)
- [07 - AWS Serverless Application Model](../lessons/075)
- [08 - How to Build Slack Bot?](../lessons/076)
- [09 - AWS Lambda Secrets Manager Example](../lessons/077)
- [10 - How to Secure Nginx with Lets Encrypt on Ubuntu 20.04 with Certbot?](../lessons/078)

## How to run the application using Docker

1. Run `mvn clean package -DskipTests` to build the applications and create the docker image locally.
2. Run `docker-compose up -d` to start the applications.

## How to run the application without Docker

1. Run `mvn clean verify -DskipTests` by going inside each folder to build the applications.
2. After that run `mvn spring-boot:run` by going inside each folder to start the applications.
