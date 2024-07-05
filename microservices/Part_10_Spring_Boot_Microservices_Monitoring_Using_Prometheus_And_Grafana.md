## [<<PREV](Part_09_Spring_Boot_Microservices_Dockerize_The_Application.md) - MICROSERVICE Monitoring Using Prometheus And Grafana


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
- pom.xml: Main Maven project file that includes all the submodule dependencies.





