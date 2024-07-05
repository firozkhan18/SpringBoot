## [<<PREV](Part_03_Spring_Boot_Microservices_Service_Discovery.md) - MICROSERVICE API GATEWAY - [NEXT>>](Part_05_Spring_Boot_Microservices_Security.md)



- Service-Discovery
  - Create a new Spring Boot project for Service-Discovery using Netflix Eureka
  - Add dependencies for Spring Cloud Eureka Server
  - Configure Eureka Server to register and discover microservices
- API-Gateway
  - Create a new Spring Boot project for API-Gateway using Spring Cloud Gateway
  - Add dependencies for Spring Cloud Gateway
  - Configure API Gateway to route requests to appropriate microservices based on the path
- Notification-Service
  - Create a new Spring Boot project for Notification-Service
  - Implement REST endpoints for sending notifications to users
  - Add dependencies for Spring Web and Spring Messaging
  - Implement a messaging service to send notifications
    
By following this structure, you can create a modular and scalable microservice architecture using Spring Boot. Each microservice is responsible for a specific domain (such as products, orders, inventory, notifications) and can be easily extended or updated without affecting other services. Service Discovery and API Gateway help in managing communication between services and routing requests efficiently.

Open the pom.xml (parent pom) file.

pom.xml (parent pom)
```
<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0"
         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
    <modelVersion>4.0.0</modelVersion>

    <parent>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-parent</artifactId>
        <version>3.2.4</version>
        <relativePath/> <!-- lookup parent from repository -->
    </parent>

    <groupId>com.springboot.microservice</groupId>
    <artifactId>spring-boot-microservices</artifactId>
    <packaging>pom</packaging>
    <version>1.0-SNAPSHOT</version>
    <modules>
        <module>product-service</module>
        <module>order-service</module>
        <module>inventory-service</module>
    </modules>

    <properties>
        <maven.compiler.source>21</maven.compiler.source>
        <maven.compiler.target>21</maven.compiler.target>
        <spring-cloud.version>2023.0.1</spring-cloud.version>
    </properties>

    <build>
        <plugins>
            <plugin>
                <groupId>org.springframework.boot</groupId>
                <artifactId>spring-boot-maven-plugin</artifactId>
                <configuration>
                    <excludes>
                        <exclude>
                            <groupId>org.projectlombok</groupId>
                            <artifactId>lombok</artifactId>
                        </exclude>
                    </excludes>
                </configuration>
            </plugin>
        </plugins>
    </build>
</project>
```
```
spring-boot-microservices
├───product-service
|   ├── src
|   │   ├── main
|   │   │   ├── java
|   │   │   │   └── com
|   |   |   |       └── springboot
|   |   |   |           └── microservice
|   |   |   |               └── product
|   |   |   |                   ├── ProductServiceApplication.java
|   |   |   |                   ├── controller
|   |   |   |                   |   └── ProductController.java
|   |   |   |                   ├── dto
|   |   |   |                   |   ├── ProductRequest.java
|   |   |   |                   |   └── ProductResponse.java
│   |   │   │                   ├── model
│   |   │   │                   │   └── Product.java
|   |   |   |                   ├── service
|   |   |   |                   |   └── ProductService.java
|   |   |   |                   └── repository
|   |   |   |                       └── ProductRepository.java
|   |   |   └── resources
|   |   |       ├── application.properties
|   |   |       ├── static
|   |   |       ├── templates
|   |   |       └── META-INF
|   |   |           └── MANIFEST.MF
|   |   └── src
|   |       ├── test
|   |       │   ├── java
|   |       │   │   └── com
|   |       │   │       └── springboot
|   |       │   │           └── microservice
|   |       │   │               └── product
|   |       │   │                   └── ProductServiceApplicationTest.java
|   |       └── resources
|   |           └── application.properties
|   └── pom.xml
├───order-service
|   ├── src
|   │   ├── main
|   │   │   ├── java
|   │   │   │   └── com
|   |   |   |       └── springboot
|   |   |   |           └── microservice
|   |   |   |               └── order
|   |   |   |                   ├── OrderServiceApplication.java
|   |   |   |                   ├── controller
|   |   |   |                   |   └── OrderController.java
|   |   |   |                   ├── dto
|   |   |   |                   |   ├── OrdertRequest.java
|   |   |   |                   |   └── OrderResponse.java
│   |   │   │                   ├── model
│   |   │   │                   │   └── Order.java
|   |   |   |                   ├── service
|   |   |   |                   |   └── OrderService.java
|   |   |   |                   └── repository
|   |   |   |                       └── OrderRepository.java
|   |   |   └── resources
|   |   |       ├── application.properties
|   |   |       ├── static
|   |   |       ├── templates
|   |   |       └── META-INF
|   |   |           └── MANIFEST.MF
|   |   └── src
|   |       ├── test
|   |       │   ├── java
|   |       │   │   └── com
|   |       │   │       └── springboot
|   |       │   │           └── microservice
|   |       │   │               └── order
|   |       │   │                   └── OrderServiceApplicationTest.java
|   |       └── resources
|   |           └── application.properties
|   └── pom.xml
├───inventory-service
|   ├── src
|   │   ├── main
|   │   │   ├── java
|   │   │   │   └── com
|   |   |   |       └── springboot
|   |   |   |           └── microservice
|   |   |   |               └── inventory
|   |   |   |                   ├── InventoryServiceApplication.java
|   |   |   |                   ├── controller
|   |   |   |                   |   └── InventoryController.java
|   |   |   |                   ├── dto
|   |   |   |                   |   ├── InventoryRequest.java
|   |   |   |                   |   └── InventoryResponse.java
│   |   │   │                   ├── model
│   |   │   │                   │   └── Inventory.java
|   |   |   |                   ├── service
|   |   |   |                   |   └── InventoryService.java
|   |   |   |                   └── repository
|   |   |   |                       └── InventoryRepository.java
|   |   |   └── resources
|   |   |       ├── application.properties
|   |   |       ├── static
|   |   |       ├── templates
|   |   |       └── META-INF
|   |   |           └── MANIFEST.MF
|   |   └── src
|   |       ├── test
|   |       │   ├── java
|   |       │   │   └── com
|   |       │   │       └── springboot
|   |       │   │           └── microservice
|   |       │   │               └── inventory
|   |       │   │                   └── InventoryServiceApplicationTest.java
|   |       └── resources
|   |           └── application.properties
|   └── pom.xml
├───notification-service
|   ├── src
|   │   ├── main
|   │   │   ├── java
|   │   │   │   └── com
|   |   |   |       └── springboot
|   |   |   |           └── microservice
|   |   |   |               └── notification
|   |   |   |                   ├── NotificationServiceApplication.java
|   |   |   |                   ├── controller
|   |   |   |                   |   └── NotificationController.java
|   |   |   |                   ├── dto
|   |   |   |                   |   ├── NotificationRequest.java
|   |   |   |                   |   └── NotificationResponse.java
│   |   │   │                   ├── model
│   |   │   │                   │   └── Notification.java
|   |   |   |                   ├── service
|   |   |   |                   |   └── NotificationService.java
|   |   |   |                   └── repository
|   |   |   |                       └── NotificationRepository.java
|   |   |   └── resources
|   |   |       ├── application.properties
|   |   |       ├── static
|   |   |       ├── templates
|   |   |       └── META-INF
|   |   |           └── MANIFEST.MF
|   |   └── src
|   |       ├── test
|   |       │   ├── java
|   |       │   │   └── com
|   |       │   │       └── springboot
|   |       │   │           └── microservice
|   |       │   │               └── notification
|   |       │   │                   └── NotificationServiceApplicationTest.java
|   |       └── resources
|   |           └── application.properties
|   └── pom.xml
├───service-discovery
|   ├── src
|   │   ├── main
|   │   │   ├── java
|   │   │   │   └── com
|   |   |   |       └── springboot
|   |   |   |           └── microservice
|   |   |   |               └── product
|   |   |   |                   ├── ProductServiceApplication.java
|   |   |   |                   ├── controller
|   |   |   |                   |   └── ProductController.java
|   |   |   |                   ├── dto
|   |   |   |                   |   ├── ProductRequest.java
|   |   |   |                   |   └── ProductResponse.java
│   |   │   │                   ├── model
│   |   │   │                   │   └── Product.java
|   |   |   |                   ├── service
|   |   |   |                   |   └── ProductService.java
|   |   |   |                   └── repository
|   |   |   |                       └── ProductRepository.java
|   |   |   └── resources
|   |   |       ├── application.properties
|   |   |       ├── static
|   |   |       ├── templates
|   |   |       └── META-INF
|   |   |           └── MANIFEST.MF
|   |   └── src
|   |       ├── test
|   |       │   ├── java
|   |       │   │   └── com
|   |       │   │       └── springboot
|   |       │   │           └── microservice
|   |       │   │               └── product
|   |       │   │                   └── ProductServiceApplicationTest.java
|   |       └── resources
|   |           └── application.properties
|   └── pom.xml
└───api-gateway
|   ├── src
|   │   ├── main
|   │   │   ├── java
|   │   │   │   └── com
|   |   |   |       └── springboot
|   |   |   |           └── microservice
|   |   |   |               └── gateway
|   |   |   |                   ├── ApiGatewayApplication.java
|   |   |   |                   ├── controller
|   |   |   |                   |   └── ProductController.java
|   |   |   |                   ├── dto
|   |   |   |                   |   ├── ProductRequest.java
|   |   |   |                   |   └── ProductResponse.java
│   |   │   │                   ├── model
│   |   │   │                   │   └── Product.java
|   |   |   |                   ├── service
|   |   |   |                   |   └── ProductService.java
|   |   |   |                   └── repository
|   |   |   |                       └── ProductRepository.java
|   |   |   └── resources
|   |   |       ├── application.properties
|   |   |       ├── static
|   |   |       ├── templates
|   |   |       └── META-INF
|   |   |           └── MANIFEST.MF
|   |   └── src
|   |       ├── test
|   |       │   ├── java
|   |       │   │   └── com
|   |       │   │       └── springboot
|   |       │   │           └── microservice
|   |       │   │               └── gateway
|   |       │   │                   └── ApiGatewayApplicationTest.java
|   |       └── resources
|   |           └── application.properties
|   └── pom.xml
└── pom.xml
```
- product-service: This module contains the code for managing products.
- order-service: This module contains the code for managing orders.
- inventory-service: This module contains the code for managing inventory.
- notification-service: This module contains the code for sending notifications.
- service-discovery: This module contains the code for service discovery using Eureka or Consul.
- api-gateway: This module contains the code for API gateway using Zuul or Spring Cloud Gateway.
- pom.xml: Main Maven project file that includes all the submodule dependencies
