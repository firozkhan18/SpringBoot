## SPTINGBOOT MICROSERVICE INTER SERVICE COMMUNICATION

- [01 - Introduction](#introduction)
- [02 - Solution Architecture of Microservices](#solution-architecture-of-microservices)
- [03 - Logical Architecture of Services](#logical-architecture-of-services)
- [04 - Create A Microservice](#create-a-microservice)
- [05 - Implement Product Service](#implement-product-service)
- [06 - Manual Testing through Postman](#manual-testing-through-postman)
- [07 - Implement Automated Tests](#implement-automated-tests)
- [08 - Test Containers](#test-containers)
- [09 - Write Integration Tests](#write-wntegration-tests)
- [10 - Generate Order Service](#generate-order-service)
- [11 - Implement Order Service](#implement-order-service)
- [12 - Test Order Service](#test-order-service)
- [13 - Generate Inventory Service](#generate-inventory-service)
- [14 - Implement Inventory Service](#implement-inventory-service)
- [15 - Migrate to Maven Multi-Module Project](#migrate-to-maven-multi-module-project)
- [16 - Bugfix in Inventory Service](#bugfix-in-inventory-service)
- 
![Desktop Screenshot](images/services-commu.PNG)

- registry-server Module

![Desktop Screenshot](images/registry-server.PNG)

The Service Implementation module implements the service. It depends on Repository Module and Service API Module.
```
registry-server
├── src
│   ├── main
│   │   ├── java
│   │   │   └── com
|   |   |       └── springboot
|   |   |           └── microservice
|   |   |               └── registry
|   |   |                   ├── RegistryServiceApplication.java
|   |   |                   ├── controller
|   |   |                   |   └── RegistryController.java
│   │   │                   ├── model
│   │   │                   │   └── Registry.java
|   |   |                   ├── service
|   |   |                   |   └── RegistryService.java
|   |   |                   └── repository
|   |   |                       └── RegistryRepository.java
|   |   └── resources
|   |       ├── application.properties
|   |       ├── static
|   |       ├── templates
|   |       └── META-INF
|   |           └── MANIFEST.MF
|   └── src
|       ├── test
|       │   ├── java
|       │   │   └── com
|       │   │       └── springboot
|       │   │           └── microservice
|       │   │               └── registry
|       │   │                   └── RegistryServiceApplicationTest.java
|       └── resources
|           └── application.properties
└── pom.xml
```
In this structure:

RegistryServiceApplication.java is the main class that contains the main method to run the Spring Boot application.

controller package contains the controller classes with mapping endpoints.

service package contains the service classes which contain business logic.

repository package contains the repository classes that interact with the database.

application.properties contains application-specific properties.

static directory contains static resources like Javascript, CSS, etc.

templates directory contains HTML templates for the application.

META-INF directory contains the manifest file.


```pom
<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
  xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 https://maven.apache.org/xsd/maven-4.0.0.xsd">
  <modelVersion>4.0.0</modelVersion>
  <parent>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-parent</artifactId>
    <version>3.3.1</version>
    <relativePath/> <!-- lookup parent from repository -->
  </parent>
  <groupId>com.springboot.microservice</groupId>
  <artifactId>product-service</artifactId>
  <version>0.0.1-SNAPSHOT</version>
  <name>product-service</name>
  <description>product-service</description>
  <url/>  
  <properties>
    <java.version>17</java.version>
  </properties>
  <dependencies>
    <dependency>
      <groupId>org.springframework.boot</groupId>
      <artifactId>spring-boot-starter-data-mongodb</artifactId>
    </dependency>
    <dependency>
      <groupId>org.springframework.boot</groupId>
      <artifactId>spring-boot-starter-web</artifactId>
    </dependency>
    <dependency>
      <groupId>org.projectlombok</groupId>
      <artifactId>lombok</artifactId>
      <optional>true</optional>
    </dependency>
    <dependency>
      <groupId>org.springframework.boot</groupId>
      <artifactId>spring-boot-starter-test</artifactId>
      <scope>test</scope>
    </dependency>
  </dependencies>
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
- application.properties
```properties
#MongoDB database congfiguration
spring.data.mongodb.uri=mongodb://localhost:27017/product-service
```
- api-gateway Module

![Desktop Screenshot](images/api-gateway.PNG)

The Service Implementation module implements the service. It depends on Repository Module and Service API Module.
```
api-gateway
├── src
│   ├── main
│   │   ├── java
│   │   │   └── com
|   |   |       └── springboot
|   |   |           └── microservice
|   |   |               └── apigateway
|   |   |                   ├── ApiGatewayApplication.java
|   |   |                   ├── controller
|   |   |                   |   └── ApiGatewayController.java
│   │   │                   ├── model
│   │   │                   │   └── ApiGateway.java
|   |   |                   ├── service
|   |   |                   |   └── ApiGatewayService.java
|   |   |                   └── repository
|   |   |                       └── ApiGatewayRepository.java
|   |   └── resources
|   |       ├── application.properties
|   |       ├── static
|   |       ├── templates
|   |       └── META-INF
|   |           └── MANIFEST.MF
|   └── src
|       ├── test
|       │   ├── java
|       │   │   └── com
|       │   │       └── springboot
|       │   │           └── microservice
|       │   │               └── apigateway
|       │   │                   └── ApiGatewayApplicationTest.java
|       └── resources
|           └── application.properties
└── pom.xml
```
In this structure:

ApiGatewayApplication.java is the main class that contains the main method to run the Spring Boot application.

controller package contains the controller classes with mapping endpoints.

service package contains the service classes which contain business logic.

repository package contains the repository classes that interact with the database.

application.properties contains application-specific properties.

static directory contains static resources like Javascript, CSS, etc.

templates directory contains HTML templates for the application.

META-INF directory contains the manifest file.


```pom
<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
  xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 https://maven.apache.org/xsd/maven-4.0.0.xsd">
  <modelVersion>4.0.0</modelVersion>
  <parent>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-parent</artifactId>
    <version>3.3.1</version>
    <relativePath/> <!-- lookup parent from repository -->
  </parent>
  <groupId>com.springboot.microservice</groupId>
  <artifactId>product-service</artifactId>
  <version>0.0.1-SNAPSHOT</version>
  <name>product-service</name>
  <description>product-service</description>
  <url/>  
  <properties>
    <java.version>17</java.version>
  </properties>
  <dependencies>
    <dependency>
      <groupId>org.springframework.boot</groupId>
      <artifactId>spring-boot-starter-data-mongodb</artifactId>
    </dependency>
    <dependency>
      <groupId>org.springframework.boot</groupId>
      <artifactId>spring-boot-starter-web</artifactId>
    </dependency>
    <dependency>
      <groupId>org.projectlombok</groupId>
      <artifactId>lombok</artifactId>
      <optional>true</optional>
    </dependency>
    <dependency>
      <groupId>org.springframework.boot</groupId>
      <artifactId>spring-boot-starter-test</artifactId>
      <scope>test</scope>
    </dependency>
  </dependencies>
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
- application.properties
```properties
#MongoDB database congfiguration
spring.data.mongodb.uri=mongodb://localhost:27017/product-service
```
- notification-service Module

![Desktop Screenshot](images/notification-service.PNG)

The Service Implementation module implements the service. It depends on Repository Module and Service API Module.
```
notification-service
├── src
│   ├── main
│   │   ├── java
│   │   │   └── com
|   |   |       └── springboot
|   |   |           └── microservice
|   |   |               └── notification
|   |   |                   ├── NotificationApplication.java
|   |   |                   ├── controller
|   |   |                   |   └── NotificationController.java
│   │   │                   ├── model
│   │   │                   │   └── Notification.java
|   |   |                   ├── service
|   |   |                   |   └── NotificationService.java
|   |   |                   └── repository
|   |   |                       └── NotificationRepository.java
|   |   └── resources
|   |       ├── application.properties
|   |       ├── static
|   |       ├── templates
|   |       └── META-INF
|   |           └── MANIFEST.MF
|   └── src
|       ├── test
|       │   ├── java
|       │   │   └── com
|       │   │       └── springboot
|       │   │           └── microservice
|       │   │               └── notification
|       │   │                   └── ProductApplicationTest.java
|       └── resources
|           └── application.properties
└── pom.xml
```
In this structure:

NotificationApplication.java is the main class that contains the main method to run the Spring Boot application.

controller package contains the controller classes with mapping endpoints.

service package contains the service classes which contain business logic.

repository package contains the repository classes that interact with the database.

application.properties contains application-specific properties.

static directory contains static resources like Javascript, CSS, etc.

templates directory contains HTML templates for the application.

META-INF directory contains the manifest file.


```pom
<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
  xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 https://maven.apache.org/xsd/maven-4.0.0.xsd">
  <modelVersion>4.0.0</modelVersion>
  <parent>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-parent</artifactId>
    <version>3.3.1</version>
    <relativePath/> <!-- lookup parent from repository -->
  </parent>
  <groupId>com.springboot.microservice</groupId>
  <artifactId>product-service</artifactId>
  <version>0.0.1-SNAPSHOT</version>
  <name>product-service</name>
  <description>product-service</description>
  <url/>  
  <properties>
    <java.version>17</java.version>
  </properties>
  <dependencies>
    <dependency>
      <groupId>org.springframework.boot</groupId>
      <artifactId>spring-boot-starter-data-mongodb</artifactId>
    </dependency>
    <dependency>
      <groupId>org.springframework.boot</groupId>
      <artifactId>spring-boot-starter-web</artifactId>
    </dependency>
    <dependency>
      <groupId>org.projectlombok</groupId>
      <artifactId>lombok</artifactId>
      <optional>true</optional>
    </dependency>
    <dependency>
      <groupId>org.springframework.boot</groupId>
      <artifactId>spring-boot-starter-test</artifactId>
      <scope>test</scope>
    </dependency>
  </dependencies>
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
- application.properties
```properties
#MongoDB database congfiguration
spring.data.mongodb.uri=mongodb://localhost:27017/product-service
```
- POM Aggregator (Parent POM)

The parent pom contains all the application modules. It also includes all the common dependencies and properties that are needed by more than one module. Dependencies are defined without version because the project has defined the Spring IO Platform as a parent.

Let's understand the structure of the multi-module application that we have created.

Spring-boot-microservices  
├── pom.xml  
│   └── REDME.adoc  
├── application  
│   ├── pom.xml  
│   └── src  
│       └── main  
│           ├── java  
│           │   └── sample  
│           │       └── multimodule  
│           │           ├── SampleWebJspApplication.java  
│           │           └── web  
│           │               └── WelcomeController.java  
│           └── resources  
│               ├── application.properties  
│               └── templates  
│                   └── welcome  
│                       └── show.html  
├── model  
│   ├── pom.xml  
│   └── src  
│       └── main  
│           └── java  
│               └── sample  
│                   └── multimodule  
│                       └── domain  
│                           └── entity  
│                               └── Account.java  
|  
├── repository  
│   ├── pom.xml  
│   └── src  
│       └── main  
│           └── java  
│               └── sample  
│                   └── multimodule  
│                       └── repository  
│                           └── AccountRepository.java  
├── service-api  
│   ├── pom.xml  
│   └── src  
│       └── main  
│           └── java  
│               └── sample  
│                   └── multimodule  
│                       └── service  
│                           └── api  
│                               ├── AccountNotFoundException.java  
│                               └── AccountService.java  
└── service-impl  
    ├── pom.xml  
    └── src  
        └── main  
            └── java  
                └── sample  
                    └── multimodule  
                        └── service  
                            └── impl  
                                └── AccountServiceImpl.java  
                                
Step 1: Create a Maven Project with the name spring-boot-microservices.

Step 2: Open the pom.xml (parent pom) file and change the packaging type jar to pom.

pom.xml (parent pom)
```pom
<?xml version="1.0" encoding="UTF-8" standalone="no"?>  
<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">  
<modelVersion>4.0.0</modelVersion>  
<!-- Spring IO Platform is the parent of the generated application to  
be able to use Spring Boot and all its default configuration -->  
<parent>  
<groupId>io.spring.platform</groupId>  
<artifactId>platform-bom</artifactId>  
<version>2.0.1.RELEASE</version>  
</parent>  
<groupId>com.springboot.microservices</groupId>  
<artifactId>spring-boot-microservices</artifactId>  
<version>0.0.1-SNAPSHOT</version>  
<packaging>pom</packaging>  
<name>Parent - Pom Aggregator</name>  
<properties>  
<java.version>1.8</java.version>  
</properties>  
<dependencies>  
<!-- Spring Boot dependencies -->  
<dependency>  
<groupId>org.springframework.boot</groupId>  
<artifactId>spring-boot-starter</artifactId>  
</dependency>  
<dependency>  
<groupId>org.springframework.boot</groupId>  
<artifactId>spring-boot-starter-data-jpa</artifactId>  
</dependency>  
<dependency>  
<groupId>org.springframework.boot</groupId>  
<artifactId>spring-boot-starter-test</artifactId>  
<scope>test</scope>  
</dependency>  
</dependencies>  
</project>  
```
One thing to be noticed in the above pom file is that there is no maven module configured because we have not created yet. Now we will create Maven Modules one by one that we have specified above.

Step 3: Create a Maven Module with the name application.

Step 4: Open the pom.xml file of application module and ensure that the packaging type is jar.

pom.xml
```pom
<?xml version="1.0" encoding="UTF-8" standalone="no"?>  
<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">  
    <modelVersion>4.0.0</modelVersion>  
    <parent>  
        <groupId>sample.multimodule</groupId>  
        <artifactId>sample.multimodule</artifactId>  
        <version>0.0.1-SNAPSHOT</version>  
    </parent>  
    <artifactId>sample.multimodule.application</artifactId>  
    <packaging>jar</packaging>  
    <name>Project Module - Application</name>  
    <dependencies>  
      <!-- Project modules -->  
      <dependency>  
        <groupId>sample.multimodule</groupId>  
        <artifactId>sample.multimodule.service.impl</artifactId>  
        <version>${project.version}</version>  
      </dependency>  
  
      <!-- Spring Boot dependencies -->  
          <dependency>  
              <groupId>org.apache.tomcat.embed</groupId>  
              <artifactId>tomcat-embed-jasper</artifactId>  
              <scope>provided</scope>  
          </dependency>  
      <dependency>  
        <groupId>org.springframework.boot</groupId>  
        <artifactId>spring-boot-starter-web</artifactId>  
      </dependency>  
      <dependency>  
        <groupId>org.springframework.boot</groupId>  
        <artifactId>spring-boot-starter-thymeleaf</artifactId>  
      </dependency>  
      
    </dependencies>  
      
    <build>  
        <plugins>  
            <!-- Spring Boot plugins -->  
            <plugin>  
                <groupId>org.springframework.boot</groupId>  
                <artifactId>spring-boot-maven-plugin</artifactId>  
            </plugin>  
        </plugins>  
    </build>  
  
</project>
```
Step 5: Create the main class. It is the class that is to be run.
```java
SampleWebJspApplication.java

package sample.multimodule;  
import org.springframework.boot.autoconfigure.SpringBootApplication;  
import org.springframework.boot.SpringApplication;  
import org.springframework.boot.orm.jpa.EntityScan;  
@SpringBootApplication  
public class SampleWebJspApplication   
{  
public static void main(String[] args) throws Exception   
{  
SpringApplication.run(SampleWebJspApplication.class, args);  
}  
}
```
Step 6: Create a Controller class with the name WelocameController under the package smaple.multimodule.web.

WelcomeController.java
```java
package sample.multimodule.web;  
import java.util.Date;  
import java.util.Map;  
import org.springframework.beans.factory.annotation.Autowired;  
import org.springframework.beans.factory.annotation.Value;  
import org.springframework.stereotype.Controller;  
import org.springframework.web.bind.annotation.RequestMapping;  
import sample.multimodule.domain.entity.Account;  
import sample.multimodule.service.api.AccountService;  
@Controller  
public class WelcomeController   
{  
@Value("${application.message:Hello World}")  
private String message = "Hello World";  
@Autowired  
protected AccountService accountService;  
@RequestMapping("/")  
public String welcome(Map<String, Object> model)   
{  
// Trying to obtain 23 account  
Account account = accountService.findOne("23");  
if(account == null){  
// If there's some problem creating account, return show view with error status  
model.put("message", "Error getting account!");  
model.put("account", "");  
return "welcome/show";  
}    
// Return show view with 23 account info  
String accountInfo = "Your account number is ".concat(account.getNumber());  
model.put("message", this.message);  
model.put("account", accountInfo);  
return "welcome/show";  
}  
@RequestMapping("foo")  
public String foo(Map<String, Object> model) {  
throw new RuntimeException("Foo");  
}  
}
```
Step 7: Open theapplication.properties file, configure the application message and thymeleaf cache to false.

application.properties
```
# Application messages  
application.message = Hello User!  
dummy.type = type-inside-the-war  
# Spring Thymeleaf config  
spring.thymeleaf.cache = false
```
After creating all the above files, the application module directory looks like the following:

### Spring Boot Multi-Module Project

Create a multimodule project where parent module named as **spring-boot-microservice**.

Add below dependencies for parent module **spring-boot-microservice** pom.xml.

```pom
<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0"
         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
    <modelVersion>4.0.0</modelVersion>

    <parent>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-parent</artifactId>
        <version>3.2.1</version>
        <relativePath/> <!-- lookup parent from repository -->
    </parent>

    <groupId>com.spring.boot.microservice</groupId>
    <artifactId>spring-boot-microservice</artifactId>
    <packaging>pom</packaging>
    <version>1.0-SNAPSHOT</version>
    <modules>
        <module>product-service</module>
        <module>order-service</module>
        <module>inventory-service</module>
        <module>discovery-server</module>
        <module>api-gateway</module>
        <module>notification-service</module>
    </modules>

    <properties>
        <maven.compiler.source>17</maven.compiler.source>
        <maven.compiler.target>17</maven.compiler.target>
        **<spring-cloud.version>2023.0.0</spring-cloud.version>**
    </properties>

    **<dependencyManagement>
        <dependencies>
            <dependency>
                <groupId>org.springframework.cloud</groupId>
                <artifactId>spring-cloud-dependencies</artifactId>
                <version>${spring-cloud.version}</version>
                <type>pom</type>
                <scope>import</scope>
            </dependency>
        </dependencies>
    </dependencyManagement>**

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
            <plugin>
                <groupId>com.google.cloud.tools</groupId>
                <artifactId>jib-maven-plugin</artifactId>
                <version>3.2.1</version>
                <configuration>
                    <from>
                        <image>eclipse-temurin:17.0.4.1_1-jre</image>
                    </from>
                    <to>
                        <image>microservices-tutorial/${project.artifactId}</image>
                    </to>
                </configuration>
                <executions>
                    <execution>
                        <phase>package</phase>
                        <goals>
                            <goal>dockerBuild</goal>
                        </goals>
                    </execution>
                </executions>
            </plugin>
        </plugins>
    </build>
</project>
```
Inside parent module create the child modules named as **product-service**, **order-service**, **inventory-service**, **notification-service**, **dicovery-server** and **api-gateway**.

Add below dependencies for child modules **product-service**, **order-service**, **inventory-service**, **notification-service** and **api-gateway** pom.xml file.

Child module product-service pom.xml:

```pom
<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0"
         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
    <parent>
        <groupId>com.spring.boot.microservice</groupId>
        <artifactId>spring-boot-microservice</artifactId>
        <version>1.0-SNAPSHOT</version>
    </parent>
    <modelVersion>4.0.0</modelVersion>

    <artifactId>product-service</artifactId>

    <properties>
        <maven.compiler.source>17</maven.compiler.source>
        <maven.compiler.target>17</maven.compiler.target>
    </properties>

    <dependencies>
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-data-mongodb</artifactId>
        </dependency>
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-web</artifactId>
        </dependency>
       **<dependency>
            <groupId>org.springframework.cloud</groupId>
            <artifactId>spring-cloud-starter-netflix-eureka-client</artifactId>
        </dependency>**
        <dependency>
            <groupId>org.projectlombok</groupId>
            <artifactId>lombok</artifactId>
            <optional>true</optional>
        </dependency>
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-test</artifactId>
            <scope>test</scope>
        </dependency>
        <dependency>
            <groupId>org.testcontainers</groupId>
            <artifactId>mongodb</artifactId>
            <scope>test</scope>
        </dependency>
        <dependency>
            <groupId>org.testcontainers</groupId>
            <artifactId>junit-jupiter</artifactId>
            <scope>test</scope>
        </dependency>
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-testcontainers</artifactId>
            <scope>test</scope>
        </dependency>
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-actuator</artifactId>
        </dependency>
        <dependency>
            <groupId>io.micrometer</groupId>
            <artifactId>micrometer-tracing-bridge-brave</artifactId>
        </dependency>
        <dependency>
            <groupId>io.zipkin.reporter2</groupId>
            <artifactId>zipkin-reporter-brave</artifactId>
        </dependency>
        <dependency>
            <groupId>io.micrometer</groupId>
            <artifactId>micrometer-registry-prometheus</artifactId>
            <scope>runtime</scope>
        </dependency>
    </dependencies>
</project>
```
Child module order-service pom.xml:
```pom
<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0"
         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
    <parent>
        <groupId>com.spring.boot.microservice</groupId>
        <artifactId>spring-boot-microservice</artifactId>
        <version>1.0-SNAPSHOT</version>
    </parent>
    <modelVersion>4.0.0</modelVersion>

    <artifactId>order-service</artifactId>

    <properties>
        <maven.compiler.source>17</maven.compiler.source>
        <maven.compiler.target>17</maven.compiler.target>
    </properties>

    <dependencies>
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-data-jpa</artifactId>
        </dependency>
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-web</artifactId>
        </dependency>
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-webflux</artifactId>
        </dependency>
       **<dependency>
            <groupId>org.springframework.cloud</groupId>
            <artifactId>spring-cloud-starter-netflix-eureka-client</artifactId>
        </dependency>**
        <dependency>
            <groupId>org.springframework.cloud</groupId>
            <artifactId>spring-cloud-starter-circuitbreaker-resilience4j</artifactId>
        </dependency>
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-actuator</artifactId>
        </dependency>
        <dependency>
            <groupId>com.mysql</groupId>
            <artifactId>mysql-connector-j</artifactId>
            <scope>runtime</scope>
        </dependency>
        <dependency>
            <groupId>org.postgresql</groupId>
            <artifactId>postgresql</artifactId>
            <scope>runtime</scope>
        </dependency>
        <dependency>
            <groupId>org.projectlombok</groupId>
            <artifactId>lombok</artifactId>
            <optional>true</optional>
        </dependency>
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-test</artifactId>
            <scope>test</scope>
        </dependency>

        <dependency>
            <groupId>org.springframework.kafka</groupId>
            <artifactId>spring-kafka</artifactId>
        </dependency>
        <dependency>
            <groupId>org.springframework.kafka</groupId>
            <artifactId>spring-kafka-test</artifactId>
            <scope>test</scope>
        </dependency>
        <dependency>
            <groupId>io.micrometer</groupId>
            <artifactId>micrometer-tracing-bridge-brave</artifactId>
        </dependency>
        <dependency>
            <groupId>io.zipkin.reporter2</groupId>
            <artifactId>zipkin-reporter-brave</artifactId>
        </dependency>
        <dependency>
            <groupId>io.micrometer</groupId>
            <artifactId>micrometer-registry-prometheus</artifactId>
            <scope>runtime</scope>
        </dependency>
    </dependencies>
</project>
```
Child module inventory-service pom.xml:
```pom
<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0"
         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
    <parent>
        <groupId>com.spring.boot.microservice</groupId>
        <artifactId>spring-boot-microservice</artifactId>
        <version>1.0-SNAPSHOT</version>
    </parent>
    <modelVersion>4.0.0</modelVersion>

    <artifactId>inventory-service</artifactId>

    <properties>
        <maven.compiler.source>17</maven.compiler.source>
        <maven.compiler.target>17</maven.compiler.target>
    </properties>

    <dependencies>
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-data-jpa</artifactId>
        </dependency>
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-web</artifactId>
        </dependency>
        **<dependency>
            <groupId>org.springframework.cloud</groupId>
            <artifactId>spring-cloud-starter-netflix-eureka-client</artifactId>
        </dependency>**
        <dependency>
            <groupId>com.mysql</groupId>
            <artifactId>mysql-connector-j</artifactId>
            <scope>runtime</scope>
        </dependency>
        <dependency>
            <groupId>org.projectlombok</groupId>
            <artifactId>lombok</artifactId>
            <optional>true</optional>
        </dependency>
        <dependency>
            <groupId>org.postgresql</groupId>
            <artifactId>postgresql</artifactId>
            <scope>runtime</scope>
        </dependency>
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-test</artifactId>
            <scope>test</scope>
        </dependency>

        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-actuator</artifactId>
        </dependency>
        <dependency>
            <groupId>io.micrometer</groupId>
            <artifactId>micrometer-tracing-bridge-brave</artifactId>
        </dependency>
        <dependency>
            <groupId>io.zipkin.reporter2</groupId>
            <artifactId>zipkin-reporter-brave</artifactId>
        </dependency>
        <dependency>
            <groupId>io.micrometer</groupId>
            <artifactId>micrometer-registry-prometheus</artifactId>
            <scope>runtime</scope>
        </dependency>
    </dependencies>
</project>
```
Child module discovery-server pom.xml:
```pom
<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0"
         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
    <parent>
        <groupId>com.spring.boot.microservice</groupId>
        <artifactId>spring-boot-microservice</artifactId>
        <version>1.0-SNAPSHOT</version>
    </parent>
    <modelVersion>4.0.0</modelVersion>

    <artifactId>discovery-server</artifactId>

    <properties>
        <maven.compiler.source>17</maven.compiler.source>
        <maven.compiler.target>17</maven.compiler.target>
    </properties>

    <dependencies>
        **<dependency>
            <groupId>org.springframework.cloud</groupId>
            <artifactId>spring-cloud-starter-netflix-eureka-server</artifactId>
        </dependency>**
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-security</artifactId>
        </dependency>
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-actuator</artifactId>
        </dependency>
        <dependency>
            <groupId>io.micrometer</groupId>
            <artifactId>micrometer-tracing-bridge-brave</artifactId>
        </dependency>
        <dependency>
            <groupId>io.zipkin.reporter2</groupId>
            <artifactId>zipkin-reporter-brave</artifactId>
        </dependency>
        <dependency>
            <groupId>io.micrometer</groupId>
            <artifactId>micrometer-registry-prometheus</artifactId>
            <scope>runtime</scope>
        </dependency>
    </dependencies>
</project>
```
Child module api-gateway pom.xml:
```pom
<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0"
         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
    <parent>
        <groupId>com.spring.boot.microservice</groupId>
        <artifactId>spring-boot-microservice</artifactId>
        <version>1.0-SNAPSHOT</version>
    </parent>
    <modelVersion>4.0.0</modelVersion>

    <artifactId>api-gateway</artifactId>

    <properties>
        <maven.compiler.source>17</maven.compiler.source>
        <maven.compiler.target>17</maven.compiler.target>
    </properties>

    <dependencies>
        <dependency>
            <groupId>org.springframework.cloud</groupId>
            <artifactId>spring-cloud-starter-gateway</artifactId>
        </dependency>
        **<dependency>
            <groupId>org.springframework.cloud</groupId>
            <artifactId>spring-cloud-starter-netflix-eureka-client</artifactId>
        </dependency>**
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-oauth2-resource-server</artifactId>
        </dependency>
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-security</artifactId>
        </dependency>
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-actuator</artifactId>
        </dependency>
        <dependency>
            <groupId>io.micrometer</groupId>
            <artifactId>micrometer-tracing-bridge-brave</artifactId>
        </dependency>
        <dependency>
          <groupId>io.zipkin.reporter2</groupId>
          <artifactId>zipkin-reporter-brave</artifactId>
        </dependency>

        <dependency>
            <groupId>io.micrometer</groupId>
            <artifactId>micrometer-registry-prometheus</artifactId>
        </dependency>
    </dependencies>
</project>
```
Child module notification-service pom.xml:
```pom
<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0"
         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
    <parent>
        <groupId>com.spring.boot.microservice</groupId>
        <artifactId>spring-boot-microservice</artifactId>
        <version>1.0-SNAPSHOT</version>
    </parent>
    <modelVersion>4.0.0</modelVersion>

    <artifactId>notification-service</artifactId>

    <properties>
        <maven.compiler.source>17</maven.compiler.source>
        <maven.compiler.target>17</maven.compiler.target>
        <java.version>17</java.version>
    </properties>

    <dependencies>
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-web</artifactId>
        </dependency>
        <dependency>
            <groupId>org.springframework.kafka</groupId>
            <artifactId>spring-kafka</artifactId>
        </dependency>
        **<dependency>
            <groupId>org.springframework.cloud</groupId>
            <artifactId>spring-cloud-starter-netflix-eureka-client</artifactId>
        </dependency>**
        <dependency>
            <groupId>org.projectlombok</groupId>
            <artifactId>lombok</artifactId>
            <optional>true</optional>
        </dependency>
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-test</artifactId>
            <scope>test</scope>
        </dependency>
        <dependency>
            <groupId>org.springframework.kafka</groupId>
            <artifactId>spring-kafka-test</artifactId>
            <scope>test</scope>
        </dependency>
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-actuator</artifactId>
        </dependency>
        <dependency>
            <groupId>io.micrometer</groupId>
            <artifactId>micrometer-tracing-bridge-brave</artifactId>
        </dependency>
        <dependency>
            <groupId>io.zipkin.reporter2</groupId>
            <artifactId>zipkin-reporter-brave</artifactId>
        </dependency>
        <dependency>
            <groupId>io.micrometer</groupId>
            <artifactId>micrometer-registry-prometheus</artifactId>
            <scope>runtime</scope>
        </dependency>
    </dependencies>
</project>
```

### Register the microservices to Eureka Server by adding the **@EnableDiscoveryClient** annotation service main class and EurekaClient properties in **application.properties** file.

- **product-service**

```java
import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;

@SpringBootApplication
public class ProductServiceApplication {

    public static void main(String[] args) {
        SpringApplication.run(ProductServiceApplication.class, args);
    }
}
```
**application.properties**

```
spring.data.mongodb.host=localhost
spring.data.mongodb.port=27017
spring.data.mongodb.database=product-service
eureka.client.serviceUrl.defaultZone=http://eureka:password@localhost:8761/eureka
spring.application.name=product-service
server.port=0
```

- **order-service**

```java
import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;

@SpringBootApplication
public class OrderServiceApplication {

    public static void main(String[] args) {
        SpringApplication.run(OrderServiceApplication.class, args);
    }

}
```
**application.properties**

```
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
spring.datasource.url=jdbc:mysql://localhost:3306/order_service
spring.datasource.username=root
spring.datasource.password=mysql
spring.jpa.hibernate.ddl-auto=update

server.port=8081
eureka.client.serviceUrl.defaultZone=http://eureka:password@localhost:8761/eureka
spring.application.name=order-service
```

- **inventory-service**

```java
import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;

@SpringBootApplication
public class InventoryServiceApplication {

    public static void main(String[] args) {
        SpringApplication.run(InventoryServiceApplication.class, args);
    }
}
```

**application.properties**

```
server.port=0
spring.datasource.url=jdbc:mysql://localhost:3306/inventory_service
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
spring.datasource.username=root
spring.datasource.password=mysql
spring.jpa.hibernate.ddl-auto=update
eureka.client.serviceUrl.defaultZone=http://eureka:password@localhost:8761/eureka
spring.application.name=inventory-service
```

- **notification-service**

```java
import io.micrometer.observation.Observation;
import io.micrometer.observation.ObservationRegistry;
import io.micrometer.tracing.Tracer;
import lombok.RequiredArgsConstructor;
import lombok.extern.slf4j.Slf4j;
import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;
import org.springframework.kafka.annotation.KafkaListener;

@SpringBootApplication
@Slf4j
@RequiredArgsConstructor
public class NotificationServiceApplication {

    private final ObservationRegistry observationRegistry;
    private final Tracer tracer;

    public static void main(String[] args) {
        SpringApplication.run(NotificationServiceApplication.class, args);
    }

    @KafkaListener(topics = "notificationTopic")
    public void handleNotification(OrderPlacedEvent orderPlacedEvent) {
        Observation.createNotStarted("on-message", this.observationRegistry).observe(() -> {
            log.info("Got message <{}>", orderPlacedEvent);
            log.info("TraceId- {}, Received Notification for Order - {}", this.tracer.currentSpan().context().traceId(),
                    orderPlacedEvent.getOrderNumber());
        });
        // send out an email notification
    }
}
```

**application.properties** file

```
eureka.client.serviceUrl.defaultZone=http://eureka:password@localhost:8761/eureka
spring.application.name=notification-service
server.port=0
```
- **api-gateway**

```java
import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;
import org.springframework.cloud.client.discovery.EnableDiscoveryClient;

@SpringBootApplication
@EnableDiscoveryClient
public class ApiGatewayApplication {
    public static void main(String[] args) {
        SpringApplication.run(ApiGatewayApplication.class, args);
    }
}
```
**application.properties**
```
spring.application.name=api-gateway
eureka.client.serviceUrl.defaultZone=http://eureka:password@localhost:8761/eureka
app.eureka-server=localhost

## Product Service Route
spring.cloud.gateway.routes[0].id=product-service
spring.cloud.gateway.routes[0].uri=lb://product-service
spring.cloud.gateway.routes[0].predicates[0]=Path=/api/product

## Order Service Route
spring.cloud.gateway.routes[1].id=order-service
spring.cloud.gateway.routes[1].uri=lb://order-service
spring.cloud.gateway.routes[1].predicates[0]=Path=/api/order

## Discover Server Route
spring.cloud.gateway.routes[2].id=discovery-server
spring.cloud.gateway.routes[2].uri=http://eureka:password@${app.eureka-server}:8761
spring.cloud.gateway.routes[2].predicates[0]=Path=/eureka/web
spring.cloud.gateway.routes[2].filters[0]=SetPath=/

## Discover Server Static Resources Route
spring.cloud.gateway.routes[3].id=discovery-server-static
spring.cloud.gateway.routes[3].uri=http://eureka:password@${app.eureka-server}:8761
spring.cloud.gateway.routes[3].predicates[0]=Path=/eureka/**
```

### Register the **discovery-server** to Eureka Server by adding the **@EnableEurekaServer** annotation service main class and in **application.properties** file.

DiscoveryServerApplication.java

```java
import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;
import org.springframework.cloud.netflix.eureka.server.EnableEurekaServer;

@SpringBootApplication
**@EnableEurekaServer**
public class DiscoveryServerApplication {
    public static void main(String[] args) {
        SpringApplication.run(DiscoveryServerApplication.class, args);
    }
}
```
**discovery-server application.properties** file
```
eureka.instance.hostname=localhost
eureka.client.register-with-eureka=false
eureka.client.fetch-registry=false
eureka.client.serviceUrl.defaultZone=http://localhost:8761/eureka/
server.port=8761
```

