# SPRINGBOOT

## INTROSUCTION

Spring Boot, a powerful extension of the Spring framework, is designed to simplify developing new Spring applications through convention over configuration. This innovative framework focuses on streamlining deployment and development processes, making it a preferred choice for building microservices and enterprise applications. With its robust auto-configuration features, Spring Boot allows developers to focus more on business features and less on boilerplate code.

### 1. What is Spring Boot and what are its Benefits?
   
Spring Boot represents a fusion of the lightweight Spring application framework, configuration annotations, and embedded HTTP server.

Made available with an auto-configuration feature, and support for Spring Initializer, Groovy, and Java, Spring Boot reduces Integration Test, Development, and Unit Test time.

It aids the development of fast, responsive, and secure web applications, providing users with a complete configuration and programming model for Java enterprise applications.

Spring Boot, utilizing the core features of the Spring application framework, offers a faster development technique for RESTful or REST architecture-based web services. 

### 2. What makes Spring Boot superior to JAX-RS?

By leveraging Spring Boot features, users can experience significant advantages over JAX-RS, including:

- Fast deployment
- High scalability
- Container compatibility
- Minimal configuration
- Lower production time
- Increased productivity 
- Reduced development time
- Easy monitoring and management of applications

### 3. What Spring Boot features help develop Microservices Applications?

Primarily used for developing microservices-based applications, Spring Boot offers the following key features for configuring, developing, and deploying microservices architecture.

- Integrates a tool called the Actuator, which enables users to manage and monitor applications
- Provides support for embedded servers, such as Jetty and Tomcat
- Users can simply run war files, without deploying it
- Includes an Auto-Configuration functionality, allowing users to configure Spring applications automatically
- Supports HTTP client Feign

### 4. Why Spring Boot is preferred over any other framework?

The Spring cloud that comes with Spring Boot, includes vast libraries, which is one of the major reasons why most developers prefer the Java-based Spring Boot. 
In addition, Spring Boot offers superior compatibility with Spring frameworks, and it also provides excellent support for docker containerization, heightening performance, and useability. 

Some of the most compelling reasons for using Spring Boot include: 

- Provides the best means to configure Java beans
- Offers robust batch processing 
- Helps users effectively manage Representational State Transfer (REST) endpoints
- Integrates an auto-configuration tool, eliminating the need for manual configuration 
- Enables  annotation-based configurations
- Ease of dependency management
- Includes embedded servlet containers

### 5. What are the key dependencies of Spring Boot?

Mentioned below are important Spring Boot dependencies that need to be added to a Gradle-based or Maven-based application, to ensure application compatibility with Spring Boot features.

- spring-boot-starter-parent
- spring-boot-maven-plugin
- spring-boot-starter-test
- spring-boot-starter-security
- spring-boot-starter-actuator
- Spring-boot-starter-web

### 6. What are the advantages of Spring Boot?

The advantages of Spring Boot are as follows:

- It is very simple to create Spring-based apps in Java or Groovy.
- It cuts down on development time and also increases the output.
- It eliminates the requirement to write repetitive code, annotations, and XML configuration.
- It is very simple to combine Spring Boot Application with its Spring Ecosystem, which includes Spring JDBC, Spring ORM, Spring Data, and Spring Security, among other things.
- To minimize developer effort, it employs the **"Opinionated Defaults Configuration"** approach.
- It provides Embedded HTTP servers such as Tomcat, Jetty, and others to help us build and test our web applications quickly.

### 7. What are the features of Spring Boot?

Features of Spring Boot:

- It is an excellent Spring module for developing online applications.
- Spring Application class offers an easy way to bootstrap a Spring application that can be started from the main method.
- Spring Boot utilizes application events and listeners to handle a variety of tasks. It enables us to build factory files for adding listeners.
- Spring Boot allows you to activate admin-related features for your application.   

### 8. How do you create a Spring Boot application using Maven?

Let us learn how to create a Spring Boot application with Maven. 

Consider Maven is already installed and configured on your machine.

Firstly create a Spring Boot application and to make it simpler create an application with a single main class.

### 9. How do you create a Spring Boot project using Spring Initializer?

Step-by-step instructions for making a spring boot project.

Step 1: Go to https://start.spring.io and launch Spring Initializr.

Step 2: Specify Project Details - Once all of the details are entered, select the Generate Project button to generate and download a Spring Boot project. Following that, unzip the downloaded zip file and transfer it into your preferred IDE.

Step 3: Next open Eclipse and import the file.

Select File -> Import -> Existing Maven Project in Eclipse. On the next page, navigate to or type in the path to the folder where you extracted the zip file. Maven will take some time to download all the dependencies and initialize the project after you select Finish.

### 10. How do you create a Spring Boot project using boot CLI?

- Setting up the CLI: By using SDKMAN, the Spring Boot CLI (Command-Line Interface) can be directly installed!

- Employing the CLI: Once the CLI has been installed, you can launch it by typing spring and hitting Enter.

- Launch a New project: By using start.spring.io and the init command, you can initiate a new project without leaving the shell.

- Using the Embedded Shell: For the BASH and zsh shells, Spring Boot provides command-line completion routines.

### 11. How do you create a simple Spring Boot application?

Check out the simplest method possible used to create a basic "Hello World!" example. Of course, there are many ways to accomplish that, but we'll choose the simplest one. We'll make use of Spring Initializr. With the selected language, version, and dependencies, that tool will automatically build the base project for us. 

### 12. What are the Spring Boot Annotations?

- **@SpringBootApplication**: A configuration class that defines one or more **@Bean** methods and initiates auto-configuration and component scanning is indicated by the annotation.
- **@EnableAutoConfiguration**: Using the jar dependencies you have provided, the **@EnableAutoConfiguration** annotation instructs Spring Boot to "guess" how you want to configure Spring.
- **@ConditionalOnMissingClass**: The Class conditions are these comments' home. Depending on the existence or absence of particular classes, a configuration can be included using the **@ConditionalOnClass** and **@ConditionalOnMissingClass** annotations.
- **@Conditional**: A class evaluating the specific condition can be made for circumstances that are even more complicated.

### 13. What are the Spring Boot properties?

Spring Boot Properties files are used to configure its auto-configuration and application properties. Spring Boot has many properties that can be used to configure the behavior of the application. Some of the commonly used properties in Spring Boot include **server.port**, t**spring.profiles.active**, t**spring.datasource.url**, t**spring.jpa.show-sql**, and many more.

### 14. What are the Spring Boot Starters?

Spring Boot Starters are a set of pre-configured dependencies that can be easily included in your project to quickly get started with common features or technologies. By including a starter in your project, you can quickly get up and running with minimal configuration.

### 15. What is Spring Boot Actuator?

Spring Boot Actuator is a set of features that provide monitoring and management capabilities for your Spring Boot application. Actuator endpoints expose information about your application, such as health status, metrics, and environment variables, that can be used to monitor and manage your application.

Get access and complete hands-on experience on a plethora of software development skills in our unique Job Guarantee bootcamp. Get job-ready with HackerEarth and HIRIST by enrolling in our comprehensive Full Stack Java Developer Masters program today!

### 16. What is thyme leaf?

Thyme leaf is a popular templating engine used in Spring Boot applications for building dynamic web pages. Moreover, it is humanly readable and developers can use it to create templates that can be rendered in HTML

### 17. How to use thyme leaf?

​​To use Thymeleaf in a Spring Boot application you should include the **thymeleaf-spring-boot-starter** dependency in your project. 

### 18. How do you connect Spring Boot to the database using JPA?

To connect Spring Boot to a database using JPA, configure the JPA properties in the **application.properties** or **application.yml** file. 

### 19. How to connect the Spring Boot application to a database using JDBC?

To connect the Spring Boot to a database using JDBC, configure the JDBC properties in the **application.properties** or **application.yml** file.

### 20. What is @RestController annotation in Spring Boot?

**@RestController** is a Spring Boot annotation used to create RESTful web services.

### 21. What is @RequestMapping annotation in Spring Boot?

**@RequestMapping** is a Spring Boot annotation used to map a URL request to a controller method.

### 22. How do you create a Spring Boot application using Spring Starter Project Wizard?

Follow the steps mentioned below to create a Spring Boot application using the Spring Starter Project Wizard, you need to follow these steps:

- Open your preferred IDE and select the "New Project" option.
- Next choose the "Spring Initializr" or "Spring Starter Project" option.
- Fill in the required project information, such as project name, description, and dependencies.
- Click on "Generate" to create the project structure and download the necessary dependencies.
- Start coding your application logic.

### 23. Spring Vs Spring Boot?

Spring is a framework that provides various modules for building enterprise-level applications.

Spring Boot is a framework that simplifies Spring development by providing a pre-configured environment that enables developers to focus on building the application logic.

Difference between Spring and Spring Boot

|Spring|Spring Boot|
|----------------------------------------------------|----------------------------------------------------|
|Spring is an open-source lightweight framework widely used to develop enterprise applications.|Spring Boot is built on top of the conventional spring framework, widely used to develop REST APIs.|
|The most important feature of the Spring Framework is dependency injection.|The most important feature of the Spring Boot is Autoconfiguration.|
|It helps to create a loosely coupled application.|It helps to create a stand-alone application.|
|To run the Spring application, we need to set the server explicitly.|Spring Boot provides embedded servers such as Tomcat and Jetty etc.|
|To run the Spring application, a deployment descriptor is required.|There is no requirement for a deployment descriptor.|
|To create a Spring application, the developers write lots of code.|It reduces the lines of code.|
|It doesn’t provide support for the in-memory database.|It provides support for the in-memory database such as H2.|
|Developers need to write boilerplate code for smaller tasks.|In Spring Boot, there is reduction in boilerplate code.|
|Developers have to define dependencies manually in the pom.xml file.|pom.xml file internally handles the required dependencies.|

### 24. What annotations are used to create an Interceptor?

A prominent functionality of Spring Boot, Interceptor uses the annotated class @Component, and it implements the interface HandlerInterceptor.

The interface contains 3 main methods, which are:

**The preHandle() Method** − preHandle() is used for intercepting the request prior to the implementation of the handler. If preHandle() returns a “true” boolean value, developers can continue with handler execution. If preHandle() returns a “false” boolean value, developers should stop the handler execution. 

preHandle() implementation looks like:

```java
 @Override
    public boolean preHandle(HttpServletRequest httpServletRequest, HttpServletResponse httpServletResponse, Object o)
            throws Exception {
        logger.info(" Pre handle ");
        if(httpServletRequest.getMethod().equals("GET"))
            return true;
        else
            return false;
    }
```
**The postHandle() Method** − postHandle() is used for intercepting a request following the implementation of the handler. It allows the manipulation of the ModelAndView Object before users render it.

postHandle() implementation looks like:

```java
@Override
    public void postHandle(HttpServletRequest httpServletRequest, HttpServletResponse httpServletResponse,
                           Object o, ModelAndView modelAndView) throws Exception {
        logger.info(" Post handle ");
        if(modelAndView.getModelMap().containsKey("status")){
            String status = (String) modelAndView.getModelMap().get("status");
            if(status.equals("SUCCESS!")){
                status = "Authentication " + status;
                modelAndView.getModelMap().put("status",status);
            }
        }
    }
```
**The afterCompletion() Method** − A HandlerInterceptor callback approach, the afterCompletion() method is used when the entire request gets completed.

afterCompletion() looks like:

```java
@Override
    public void afterCompletion(HttpServletRequest httpServletRequest, HttpServletResponse httpServletResponse,
                                Object o, Exception e) throws Exception {
        logger.info(" After Completion ");
    }
}
```

### 25. What is a Swagger in Spring Boot?

Swagger is used for clearly detailing and documenting RESTful APIs in a machine-readable and human-readable format, which is easily comprehensible for testers and developers, as well as individuals having little knowledge of source code.

Enabling hassle-free application discovery, development, and integration, Swagger allows API consumers to interact with remote services with minimum implementation logic.

### 26. What are Profiles in Spring Boot?

Profiles in the Spring framework enables users to map components and beans to specific profiles, such as the Development (dev) profile, Production (prod) profile, or the Test profile. 

In Spring Boot, the annotation @Profile is used to map components and beans to a certain profile. 

Developers can also set up profiles using the SpringApplication, for instance, SpringApplication.setAdditionalProfiles("dev");

### 27. What differentiates Spring Data JPA and Hibernate?

A Java Persistence API (JPA) implementation, Hibernate facilitates Object-Relational Mapping (ORM), allowing users to store, retrieve, map, and update application data to and from Java objects and relational databases. Hibernate maps the data types in Java to SQL (Structured Query Language) data types, and the classes in java to the database tables, relieving developers from scripting data persistence SQL programs. 

A Spring Data sub-project, Spring Data JPA, on the other hand, gives abstraction over the DAL (Data Access Layer) applying JPA and Object–Relational Mapping implementations, such as Hibernate. Spring Data JPA facilitates the smooth implementation of JPA repositories, and it intends to improve the overall implementation of DAL to a great extent. 

### 28. How are the @RestController and @Controller Annotation different?
The traditional Spring @Controller annotation specifies that an annotated class represents a controller. 

It’s basically a @Component specialization, and it is autodetected via the classpath scanning. 

The @Controller annotation is used along with the annotated handler methodologies based on @RequestMapping annotations.

Developers use the @RestController annotation to develop RESTful web services, utilizing the Spring Model–View–Controller (MVC). 

The Spring @RestController maps the request data to specified request handler methods. 

Once the handler method generates the response body, the @RestController modifies it to XML or JSON response.

### 29. In springboot application.properties or application.yml file which one is loading automatically or which one is default property?

In a Spring Boot application, the default property file that gets loaded automatically is the application.properties file. If both application.properties and application.yml files are present in the classpath, the properties defined in the application.properties file will take precedence over the properties defined in the application.yml file.

### 1. What is Spring Boot?

Spring Boot is built on the top of Spring framework to create stand-alone RESTful web application with very minimal configuration and there is no need of external servers to run the application, because it has embedded servers like Tomcat and Jetty etc.

Spring Boot framework is independent.
It creates executable spring applications that are production-grade.

### 2. What are the Features of Spring Boot?

There are many useful features of Spring Boot. Some of them are mentioned below:

- **Auto-configuration** – Spring Boot automatically configures dependencies by using **@EnableAutoconfiguration** annotation and reduces boilerplate code.
- **Spring Boot Starter POM** – These Starter POMs are pre-configured dependencies for functions like database, security, maven configuration etc.
- **Spring Boot CLI (Command Line Interface)** – This command line tool is generally for managing dependencies, creating projects and running the applications.
- **Actuator** – Spring Boot Actuator provides health check, metrics and monitors the endpoints of the application. It also simplifies the troubleshooting management.
- **Embedded Servers** – Spring Boot contains embedded servers like Tomcat and Jetty for quick application run. No need of external servers.

### 3. What are the advantages of using Spring Boot?

Spring Boot is a framework that creates stand-alone, production grade Spring based applications. So, this framework has so many advantages.

- **Easy to use**:  The majority of the boilerplate code required to create a Spring application is reduced by Spring Boot.
- **Rapid Development**: Spring Boot’s opinionated approach and auto-configuration enable developers to quickly develop apps without the need for time-consuming setup, cutting down on development time.
- **Scalable**: Spring Boot apps are intended to be scalable. This implies they may be simply scaled up or down to match your application’s needs.
- **Production-ready**: Metrics, health checks, and externalized configuration are just a few of the features that Spring Boot includes and are designed for use in production environments.

### 4. Define the Key Components of Spring Boot.

The key components of Spring Boot are listed below:

- Spring Boot starters
- Auto-configuration
- Spring Boot Actuator
- Spring Boot CLI
- Embedded Servers

### 5. Why do we prefer Spring Boot over Spring?

Here is a table that summarizes why we use Spring Boot over Spring framework.

Feature
||Spring|Spring Boot|
|-----------------------|--------------------------------------------|--------------------------------------------|
|Ease of use|More complex| Easier|
|Production readiness| Less production-ready|More production-ready|
|Scalability|Less scalable|More scalable|
|Speed|Slower|Faster|
|Customization	|Less Customizable|	More Customizable|

### 6. Explain the internal working of Spring Boot.

Here are the main steps involved in how Spring Boot works:

- Start by creating a new Spring Boot project.
- Add the necessary dependencies to your project.
- Annotate the application with the appropriate annotations.
- Run the application.

### 7. What are the Spring Boot Starter Dependencies?

Spring Boot provides many starter dependencies. Some of them which are used the most in the Spring Boot application are listed below:

- Data JPA starter
- Web starter
- Security starter
- Test Starter
- Thymeleaf starter

### 8. How does a spring application get started?

A Spring application gets started by calling the main() method with **@SpringBootApplication** annotation in the SpringApplication class. 

This method takes a SpringApplicationBuilder object as a parameter, which is used to configure the application.

Once the SpringApplication object is created, the run() method is called.

Once the application context is initialized, the run() method starts the application’s embedded web server.
Example:
```java
import org.springframework.boot.SpringApplication; 
import org.springframework.boot.autoconfigure.SpringBootApplication;
@SpringBootApplication
public class MyApplication 
{ 
  public static void main(String[] args) {
    SpringApplication.run(MyApplication.class, args);
  }
}
```
### 9. What does the @SpringBootApplication annotation do internally?

The @SpringBootApplication annotation combines three annotations. 

Those three annotations are: **@Configuration**, **@EnableAutoConfiguration**, and **@ComponentScan**.

- **@AutoConfiguration**: This annotation automatically configuring beans in the class path and automatically scans the dependencies according to the application need.
- **@ComponentScan**: This annotation scans the components (@Component, @Service, etc.) in the package of annotated class and its sub-packages.
- **@Configuration**: This annotation configures the beans and packages in the class path.

**@SpringBootApplication** automatically configures the application based on the dependencies added during project creation and bootstraps the application by using run() method inside the main class of an application.

**@SpringBootApplication** = **@Configuration** + **@EnableAutoConfiguration** + **@ComponentScan**

### 10. What is Spring Initializr?

Spring Initializer is a tool that helps us to create skeleton of spring boot project or project structure by providing a maven or gradle file to build the application. 
It set up the framework from scratch.

### 11. What are Spring Boot CLI and the most used CLI commands?

Spring Boot CLI is a command-line tool that can be used to create, run, and manage Spring Boot applications. It is a powerful tool that can help us to get started with Spring Boot quickly and easily. It is built on top of the Groovy programming language.

Most used CLI commands are:

-run
-test
-jar
-war
–init
-help


### 12. What are the basic Spring Boot Annotations?

- **@SpringBootApplication**: This is the main annotation used to bootstrap a Spring Boot application. It combines three annotations: **@Configuration**, **@EnableAutoConfiguration**, and **@ComponentScan**. It is typically placed on the main class of the application.
- **@Configuration**: This annotation is used to indicate that a class contains configuration methods for the application context. It is typically used in combination with **@Bean** annotations to define beans and their dependencies.
- **@Component**: This annotation is the most generic annotation for any Spring-managed component. It is used to mark a class as a Spring bean that will be managed by the Spring container.
- **@RestController**: This annotation is used to define a RESTful web service controller. It is a specialized version of the **@Controller** annotation that includes the **@ResponseBody** annotation by default.
- **@RequestMapping**: This annotation is used to map HTTP requests to a specific method in a controller. It can be applied at the class level to define a base URL for all methods in the class, or at the method level to specify a specific URL mapping.

### 13. What is Spring Boot dependency management?

Spring Boot dependency management makes it easier to manage dependencies in a Spring Boot project. It makes sure that all necessary dependencies are appropriate for the current Spring Boot version and are compatible with it.

To create a web application, we can add the Spring Boot starter web dependency to our application.

### 14. Is it possible to change the port of the embedded Tomcat server in Spring Boot?

Yes, it is possible to change the port of the embedded Tomcat server in a Spring Boot application.

The simple way is to set the server. port property in your application’s **application.properties** file. For example, to set the port to **8081**, add the following property to the **application.properties** file:
```
server.port=8081
```
### 15. What is the starter dependency of the Spring boot module?

Spring Boot Starters are a collection of pre-configured maven dependencies that makes it easier to develop particular types of applications. These starters include,

Dependencies
Version control
Configuration needed to make certain features.
To use a Spring Boot starter dependency, we simply need to add it to our project’s **pom.xml** file. For example, to add the Spring Boot starter web dependency, add the following dependency to the **pom.xml** file:
```pom
<dependency>
      <groupId>org.springframework.boot</groupId> 
      <artifactId>spring-boot-starter-web</artifactId> 
</dependency>
```
### 16. What is the default port of Tomcat in spring boot?

The default port of the embedded Tomcat server in Spring Boot is **8080**. We can change the default port by setting the **server.port** property in your application’s **application.properties** file.

### 17. Can we disable the default web server in the Spring Boot application?

Yes, we can disable the default web server in the Spring Boot application. To do this, we need to set the **server.port** property to **“-1”** in the application’s **application.properties** file.

### 18. How to disable a specific auto-configuration class?

To disable a specific auto-configuration class in a Spring Boot application, we can use the **@EnableAutoConfiguration** annotation with the **“exclude”** attribute.
```java
@EnableAutoConfiguration(exclude = {//classname})**
```
### 19. Can we create a non-web application in Spring Boot?

Yes, we can create a non-web application in Spring Boot. Spring Boot is not just for web applications. Using Spring Boot, we can create applications like Microservices, Console applications, and batch applications.

### 20. Describe the flow of HTTPS requests through the Spring Boot application.
The flow of HTTPS requests through a Spring Boot application is as follows:

Spring Boot HTTP Request Flow

- First client makes an HTTP request (GET, POST, PUT, DELETE) to the browser.
- After that the request will go to the controller, where all the requests will be mapped and handled.
- After this in Service layer, all the business logic will be performed. It performs the business logic on the data that is mapped to JPA (Java Persistence API) using model classes.
- In repository layer, all the CRUD operations are being done for the REST APIs.
- A JSP page is returned to the end users if no errors are there.

### 21. Explain @RestController annotation in Spring Boot.

@RestController annotation is like a shortcut to building RESTful services. It combines two annotations:

@Controller: Marks the class as a request handler in the Spring MVC framework.
@ResponseBody: Tells Spring to convert method return values (objects, data) directly into HTTP responses instead of rendering views.
It enables us to Define endpoints for different HTTP methods (GET, POST, PUT, DELETE), return data in various formats (JSON, XML, etc.) and map the request parameters to method arguments.

### 22. Difference between @Controller and @RestController

Features	
@Controller

@RestController

Usage

It marks a class as a controller class.

It combines two annotations i.e. @Controller and @ResponseBody.

Application

Used for Web applications.

Used for RESTful APIs.

Request handling and Mapping

Used with @RequestMapping annotation to map HTTP requests with methods.

Used to handle requests like GET, PUT, POST, and DELETE.

Note: Both annotations handle requests, but @RestController prioritizes data responses for building API.

### 23. What is the difference between RequestMapping and GetMapping?

Features

@RequestMapping

@GetMapping

Annotations

@RequestMapping

@GetMapping

Purpose

Handles various types of HTTP requests (GET, POST, etc.)

Specifically handles HTTP GET requests.

Example

@RequestMapping(value = “/example”, method = RequestMethod.GET)

@GetMapping(“/example”)

### 24. What are the differences between @SpringBootApplication and @EnableAutoConfiguration annotation?

Features

@SpringBootApplication

@EnableAutoConfiguration

When to use

When we want to use auto-configuration

When we want to customize auto-configuration

Entry point

Typically used on the main class of a Spring Boot application, serving as the entry point.

Can be used on any configuration class or in conjunction with @SpringBootApplication.

Component Scanning

Includes @ComponentScan annotation to enable component scanning.

Does not perform component scanning by itself.

Example

@SpringBootApplication public class MyApplication { public static void main(String[] args) { SpringApplication.run(MyApplication.class, args); } }

@Configuration @EnableAutoConfiguration public class MyConfiguration { }

### 25. What are Profiles in Spring?

Spring Profiles are like different scenarios for the application depending on the environment.

You define sets of configurations (like database URLs) for different situations (development, testing, production).
Use the @Profile annotation to clarify which config belongs to where.
Activate profiles with environment variables or command-line options.
To use Spring Profiles, we simply need to define the spring.profiles.active property to specify which profile we want to use.

### 26. Mention the differences between WAR and embedded containers.

Feature

WAR

Embedded containers

Packaging

Contains all of the files needed to deploy a web application to a web server.

It is a web application server included in the same JAR file as the application code.

Configuration

Requires external configuration files (e.g., web.xml, context.xml) to define the web application.

Uses configuration properties or annotations within the application code.

Security

Can be deployed to a web server that is configured with security features.

Can be made more secure by using security features that are provided by JRE.

### 27. What is Spring Boot Actuator?

Spring Boot Actuator is a component of the Spring Boot framework that provides production-ready operational monitoring and management capabilities. We can manage and monitor your Spring Boot application while it is running.

Note: To use Spring Boot Actuator, we simply need to add the spring-boot-starter-actuator dependency to our project.

To know more about Actuator, refer to this article – Spring Boot Actuator

### 28. How to enable Actuator in the Spring boot application?

Below are the steps to enable actuator in Spring Boot Application:

Add Actuator dependency.
Enable endpoints in application.properties.
Run your Spring Boot app.
Now we can access Actuator endpoints at URLs on the management port.

### 29. What is the purpose of using @ComponentScan in the class files?

@ComponentScan annotation is used to tell Spring to scan a package and automatically detect Spring components, configurations, and services to configure. The @ComponentScan annotation can be used in the following ways:

Without arguments
With basePackageClasses
With basePackages
To know more about @ComponentScan annotation, refer to this article –Spring @ComponentScan Annotation with Example

### 30. What are the @RequestMapping and @RestController annotations in Spring Boot used for?

@RequestMapping: @RequestMapping is used to map HTTP requests to handler methods in your controller classes. It can be used at the class level and method level. It supports mapping by:

HTTP method – GET, POST, PUT, DELETE
URL path
URL parameters
Request headers
@RestController: @RestController is a convenience annotation that combines @Controller and @ResponseBody. It indicates a controller where every method returns a domain object instead of a view.

@RestController = @Controller + @ResponseBody

### 31. How to get the list of all the beans in your Spring boot application?

Using the ApplicationContext object in Spring Boot, we can retrieve a list of all the beans in our application.
The ApplicationContext is responsible for managing the beans and their dependencies.

### 32. Can we check the environment properties in your Spring boot application explain how?

Yes, we can check the environment properties in our Spring Boot Application. The Environment object in a Spring Boot application can be used to check the environment’s properties.

Configuration settings for the application, includes:

property files
command-line arguments
environment variables
We can get the Environment instance by calling the getEnvironment() method.

### 33. How to enable debugging log in the spring boot application?

To enable debugging log in Spring Boot Application, follow the below steps:

Add the logging level property to application.properties.
Configure the log pattern to include useful information.
Run the Spring Boot application.
Using the actuator endpoint, the log level can also be changed at runtime.

Curl -X POST \http://localhost:8080/actuator/loggers/<logger-name> 
\ -H 'content-type: application/json' \-d '{"configuredLevel": "DEBUG"}'

### 34. What is dependency Injection and its types?

Dependency Injection (DI) is a design pattern that enables us to produce loosely coupled components. In DI, an object’s ability to complete a task depends on another object. There three types of dependency Injections.

Constructor injection: This is the most common type of DI in Spring Boot. In constructor injection, the dependency object is injected into the dependent object’s constructor.
Setter injection: In setter injection, the dependency object is injected into the dependent object’s setter method.
Field injection: In field injection, the dependency object is injected into the dependent object’s field.
To know more about Dependency Injection, refer to the article – Spring Dependency Injection with Example – GeeksforGeeks

### 35. What is an IOC container?

An IoC (Inversion of Control) Container in Spring Boot is essentially a central manager for the application objects that controls the creation, configuration, and management of dependency injection of objects (often referred to as beans), also referred to as a DI (Dependency Injection) container.

To know more about IOC Container, refer to the article – Spring – IoC Container

### 36. What is the difference between Constructor and Setter Injection?

|Features|Constructor Injection|Setter Injection|
|-------------------------------|-------------------------------|-------------------------------|
|Dependency|Dependencies are provided through constructor parameters.|Dependencies are set through setter methods after object creation.|
|Immutability|Promotes immutability as dependencies are set at creation.|Dependencies can be changed dynamically after object creation.|
|Dependency Overriding|Harder to override dependencies with different implementations.|Allows easier overriding of dependencies using different setter values.|

Below is an example of Constructor Injection, Setter Injection, and Field Injection in a Spring application with the respective configurations:

- 1. Constructor Injection:

EmployeeService.java:
```java
public class EmployeeService {
    private EmployeeRepository employeeRepository;

    public EmployeeService(EmployeeRepository employeeRepository) {
        this.employeeRepository = employeeRepository;
    }

    public void save(Employee employee) {
        employeeRepository.save(employee);
    }
}
```

EmployeeRepository.java:
```java
public class EmployeeRepository {
    public void save(Employee employee) {
        // save employee implementation
    }
}
```

- 2. Setter Injection:

EmployeeService.java:
```java
public class EmployeeService {
    private EmployeeRepository employeeRepository;

    public void setEmployeeRepository(EmployeeRepository employeeRepository) {
        this.employeeRepository = employeeRepository;
    }

    public void save(Employee employee) {
        employeeRepository.save(employee);
    }
}
```

EmployeeRepository.java:
```java
public class EmployeeRepository {
    public void save(Employee employee) {
        // save employee implementation
    }
}
```

- 3. Field Injection:

EmployeeService.java:
```java
public class EmployeeService {
    @Autowired
    private EmployeeRepository employeeRepository;

    public void save(Employee employee) {
        employeeRepository.save(employee);
    }
}
```

EmployeeRepository.java:
```java
public class EmployeeRepository {
    public void save(Employee employee) {
        // save employee implementation
    }
}
```

- Configuration for Constructor Injection:

EmployeeConfig.java:
```java
@Configuration
public class EmployeeConfig {
    @Bean
    public EmployeeRepository employeeRepository() {
        return new EmployeeRepository();
    }

    @Bean
    public EmployeeService employeeService() {
        return new EmployeeService(employeeRepository());
    }
}
```

- Configuration for Setter Injection and Field Injection:

EmployeeConfig.java:
```java
@Configuration
public class EmployeeConfig {
    @Bean
    public EmployeeRepository employeeRepository() {
        return new EmployeeRepository();
    }

    @Bean
    public EmployeeService employeeService() {
        return new EmployeeService();
    }
}
```

**Note**: For **Setter Injection** and **Field Injection**, make sure to use **`@Autowired`** annotation on the respective setter method or field.

There is no definitive answer on which type of dependency injection (Constructor Injection, Setter Injection, or Field Injection) is better as it ultimately depends on the specific requirements and context of the application being developed.

**Constructor Injection** is considered to be the most recommended and preferred method as it ensures that all dependencies are satisfied when an object is created. This means that the object is in a valid state as soon as it is created, which can help prevent runtime errors and improve code readability.

**Setter Injection**, on the other hand, allows for more flexibility as dependencies can be set after the object has been created. This can be useful in situations where optional dependencies are needed or when circular dependencies exist. However, it can also lead to objects being in an inconsistent state until all dependencies are set.

**Field Injection** injects dependencies directly into the fields of a class, which can lead to issues with encapsulation and testing. Some developers argue that Field Injection can make code harder to maintain and test due to the implicit nature of the injection.

In general, it is recommended to use Constructor Injection whenever possible, as it promotes better code design and makes dependencies explicit. However, there may be situations where Setter Injection or Field Injection are more appropriate, depending on the specific requirements of the application. Ultimately, it is important to consider the pros and cons of each method and choose the one that best fits the needs of the project.

### 37. What is Thymeleaf?

Thymeleaf is a Java-based server-side template engine used in Java web applications to render dynamic web pages. It is a popular choice for server-side templating in the Spring ecosystem, including Spring Boot.

### 38. Explain Spring Data and What is Data JPA?

Spring Data is a powerful framework that can be used to develop data-oriented applications. It aims to simplify the development of data-centric applications by offering abstractions, utilities, and integration with various data sources.

Spring Data JPA: This project provides support for accessing data from relational databases using JPA.

### 39. Explain Spring MVC

MVC stands for Model, View, and Controller. Spring MVC is a web MVC framework built on top of the Spring Framework. It provides a comprehensive programming model for building web applications.

### 40. What is Spring Bean?

An object that is managed by the Spring IoC container is referred to as a spring bean. A Spring bean can be any Java object.

### 41. What are Inner Beans in Spring?

An Inner Bean refers to a bean that is defined within the scope of another bean’s definition. It is a way to declare a bean inside the configuration of another bean, without explicitly giving it a unique identifier.

To define an Inner Bean in Spring, we can declare it as a nested **<bean>** element within the configuration of the enclosing bean.

### 42. What is Bean Wiring?

Bean wiring is a mechanism in Spring that is used to manage the dependencies between beans. It allows Spring to inject collaborating beans into each other. There are two types of Bean Wiring:

- Autowiring
- Manual wiring

In Spring framework, autowiring is a way to automatically inject dependencies into a Spring bean without explicitly defining them in the bean configuration file. This reduces the amount of configuration required and makes the code more maintainable.

There are different types of autowiring in Spring:

- No Autowiring: In this type, autowiring is disabled and you need to explicitly wire the beans using the <ref> tag in the bean configuration file.

- Autowiring by Name: In this type, the Spring container tries to match and wire a bean property with a property of the same name in the container. For example:

```java  
public class UserServiceImpl {
    private UserRepository userRepository;
    
    // Getter and setter for userRepository
}
``
If there is a bean named "userRepository" in the container, it will be injected into the UserServiceImpl bean automatically.

Autowiring by Type: In this type, the Spring container tries to match and wire a bean property by type. For example:
```java 
public class UserServiceImpl {
    @Autowired
    private UserRepository userRepository;
    
    // Getter and setter not needed
}
```
If there is a bean of type UserRepository in the container, it will be injected into the UserServiceImpl bean automatically.

- Autowiring by Constructor: In this type, Spring will try to auto-wire constructor arguments.

For example:

```java 
public class UserServiceImpl {
    private UserRepository userRepository;
    
    @Autowired
    public UserServiceImpl(UserRepository userRepository) {
        this.userRepository = userRepository;
    }
}
```
The UserRepository bean will be automatically passed as a constructor argument when the UserServiceImpl bean is created.

Overall, autowiring can greatly simplify the configuration of Spring beans and reduce the boilerplate code required for dependency injection.

### 43. What Are Spring Boot DevTools Used For?

Spring Boot DevTools provides a number of development-time features and enhancements to increase developers’ productivity and can be used for the following purposes:

- Automatic application restart
- Fast application startup:
- Actuator endpoints
- Additional development utilities

### 44. What error do you see if H2 is not present in the class path?

Below is the error we see if H2 is not present in the class path:

**java.lang.ClassNotFoundException: org.h2.Driver**

### 45. Mention the steps to connect the Spring Boot application to a database using JDBC.

To connect an external database like MySQL or Oracle to a Spring Boot application using JDBC, we need to follow below steps:

- Add the dependency for the JDBC driver of the database.
- Create an application.properties file.
- Configure the database connection properties.
- Create a JdbcTemplate bean.
- Use the JdbcTemplate bean to execute SQL queries and statements.

### 46. Mention the advantages of the YAML file over than Properties file and the different ways to load the YAML file in Spring boot.

Advantages of YAML file over Properties file:

- Easy to edit and modify.
- Conciseness
- Supports Complex data types.

Different ways to load YAML file in Spring Boot:

- Using the **@ConfigurationProperties** annotation
- Using the **YamlPropertiesFactoryBean** class

### 47. What Do you understand about Spring Data Rest?

Spring Data REST is a framework that exposes Spring Data repositories as RESTful web services. It allows us to expose repositories as REST endpoints with minimal configuration by following Spring Data REST Technologies like Spring Data and Spring MVC.

### 48. Why is Spring Data REST not recommended in real-world applications?

Here are the reasons why not to choose Spring Data REST:

- Performance – Performance may not be optimal for very large-scale applications.
- Versioning – It can be difficult to version the REST APIs exposed by Spring Data REST.
- Relationships – Handling relationships between entities can be tricky with Spring Data REST.
- Filtering – There are limited options for filtering the results returned by the endpoints.

### 49. How is Hibernate chosen as the default implementation for JPA without any configuration?

Spring Boot automatically configures Hibernate as the default JPA implementation when we add the spring-boot-starter-data-jpa dependency to our project. This dependency includes the Hibernate JAR file as well as the Spring Boot auto-configuration for JPA.

### 50. servlet vs filter vs interceptor explain and provide the differences?

**Servlet**:
- A servlet is a Java class that handles requests and responses on the server side.
- It is used to generate dynamic web content or process client requests.
- Servlets have a lifecycle managed by the Servlet container.

**Filter**:

- A filter is a Java class that is used to perform preprocessing and postprocessing of requests and responses.
- Filters are used to intercept and modify requests and responses before they reach the servlet or are sent back to the client.
- Multiple filters can be chained together to perform different operations.

**Interceptor**:

- An interceptor is a design pattern used to manage cross-cutting concerns in applications.
- Interceptors are used to intercept and process requests and responses at specific points in the application flow.
- Interceptors are often used in frameworks such as Spring MVC and Struts for logging, authentication, and other cross-cutting concerns.

**servlet vs filter vs interceptor**:

| Feature | Servlet | Filter | Interceptor | |---------------|---------------------|--------------------|--------------------| | Purpose | Generate dynamic | Perform pre and | Manage cross-cutting| | | content, process | post-processing of | concerns in | | | client requests | requests and | applications | | Lifecycle | Managed by Servlet | N/A | N/A | | | container | | | | Invocation | Directly invoked | Invoked before | Invoked at specific | | | by client requests | and after servlet | points in the | | | | execution | application flow | | Usage | Processing client | Intercepting and | Managing | | | requests, generating| modifying requests | cross-cutting | | | responses | and responses | concerns |
