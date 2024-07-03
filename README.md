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
    public boolean preHandle(HttpServletRequest httpServletRequest,
               HttpServletResponse httpServletResponse, Object o) throws Exception {
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
    public void postHandle(HttpServletRequest httpServletRequest,
                     HttpServletResponse httpServletResponse,
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
    public void afterCompletion(HttpServletRequest httpServletRequest,
                           HttpServletResponse httpServletResponse,
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

#### Features

@RequestMapping

@GetMapping

Annotations

@RequestMapping

@GetMapping

#### Purpose

Handles various types of HTTP requests (GET, POST, etc.)

Specifically handles HTTP GET requests.

#### Example

@RequestMapping(value = “/example”, method = RequestMethod.GET)

@GetMapping(“/example”)

### 24. What are the differences between @SpringBootApplication and @EnableAutoConfiguration annotation?

#### Features

@SpringBootApplication

@EnableAutoConfiguration

#### When to use

When we want to use auto-configuration

When we want to customize auto-configuration

#### Entry point

Typically used on the main class of a Spring Boot application, serving as the entry point.

Can be used on any configuration class or in conjunction with @SpringBootApplication.

#### Component Scanning

Includes @ComponentScan annotation to enable component scanning.

Does not perform component scanning by itself.

#### Example

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

| Feature | Servlet | Filter | Interceptor | 
|--------------|-----------------------------------------------|----------------------------------------------|----------------------------------------------| 
| Type | Interface | Interface | Interface | 
| Purpose | Handle client requests and responses | Intercept and manipulate requests and responses| Intercept and manipulate requests and responses| 
| Sequence | Executes before filters and interceptors | Executes before and after servlets, and other filters | Executes before and after servlets, filters, and other interceptors| | Configuration| Defined in web.xml or via annotations | Defined in web.xml or via annotations | Usually configured using annotations in Spring| 
| Context | Servlet API | Servlet API | Spring framework or other frameworks | 
| Scope | Application-wide | Application-wide | Typically used at controller level in Spring | 
| Example | HttpServlet | javax.servlet.Filter | HandlerInterceptor |

### 51. Setter Dependency Injection (SDI) vs. Constructor Dependency Injection (CDI)

| Setter DI | Constructor DI |
|--------------|-----------------------------------------------|
| Poor readability as it adds a lot of boiler plate codes in the application.|Good readability as it is separately present in the code.|	
| The bean must include getter and setter methods for the properties.|The bean class must declare a matching constructor with arguments. Otherwise, BeanCreationException will be thrown.|
| Requires addition of @Autowired annotation, above the setter in the code and hence, it increases the coupling between the class and the DI container.|	Best in the case of loose coupling with the DI container as it is not even required to add @Autowired annotation in the code.(Implicit constructor injections for single constructor scenarios after spring 4.0)|
|Circular dependencies or partial dependencies result with Setter DI because object creation happens before the injections.|	No scope for circular or partial dependency because dependencies are resolved before object creation itself.|
|Preferred option when properties are less and mutable objects can be created.|	Preferred option when properties on the bean are more and immutable objects (eg: financial processes) are important for application.|

### 52. What is Spring Dependency Injection? Need for Dependency Injection ? Types of Spring Dependency Injection with example and compare with both xml and annotation based configuration with example.

Spring Dependency Injection is a design pattern used in Spring Framework where the components of an application are provided with their dependencies rather than being responsible for creating them. Dependency Injection helps in decoupling the code and making it easier to test and maintain.

The need for Dependency Injection arises when the components of an application have dependencies on other components or services. Using Dependency Injection, these dependencies can be injected into the components at runtime, making the code more modular and flexible.

There are two types of Dependency Injection in Spring Framework:

- Constructor Injection: In Constructor Injection, dependencies are provided to a component through its constructor.
Example of Constructor Injection:
```java
 
public class UserService {
    private UserRepository userRepository;
    
    public UserService(UserRepository userRepository) {
        this.userRepository = userRepository;
    }
}
```
- Setter Injection: In Setter Injection, dependencies are provided to a component through setter methods.
Example of Setter Injection:
```java
 
public class UserService {
    private UserRepository userRepository;
    
    public void setUserRepository(UserRepository userRepository) {
        this.userRepository = userRepository;
    }
}
```
Now, let's compare XML-based configuration and Annotation-based configuration in Spring Dependency Injection:
```xml
- XML-Based Configuration:
 
<bean id="userRepository" class="com.example.UserRepositoryImpl" />
<bean id="userService" class="com.example.UserService">
    <property name="userRepository" ref="userRepository" />
</bean>
```
- Annotation-Based Configuration:
```java
@Component
public class UserRepositoryImpl implements UserRepository {
    // implementation
}

@Component
public class UserService {
    @Autowired
    private UserRepository userRepository;
    // other methods
}
```
In both XML-based and Annotation-based configurations, we are configuring the dependencies for UserService. However, in XML-based configuration, we need to explicitly define the dependencies in an XML file. On the other hand, in Annotation-based configuration, we use annotations like @Component and @Autowired to define and inject dependencies.

Overall, Dependency Injection in Spring Framework helps in achieving loose coupling between components, making the code more maintainable and testable. The choice between XML-based and Annotation-based configuration depends on the preference and requirements of the developers.


#### Spring – IoC Container

The Spring framework can be considered as a collection of sub-frameworks, also referred to as layers, such as Spring AOP, Spring ORM, Spring Web Flow, and Spring Web MVC. You can use any of these modules separately while constructing a Web application. The modules may also be grouped together to provide better functionalities in a web application. 

Prior to penetrating down to Spring to container do remember that Spring provides two types of Containers namely as follows:

- BeanFactory Container
- ApplicationContext Container
The features of the Spring framework such as IoC, AOP, and transaction management, make it unique among the list of frameworks. Some of the most important features of the Spring framework are as follows:

- IoC container
- Data Access Framework
- Spring MVC
- Transaction Management
- Spring Web Services
- JDBC abstraction layer
- Spring TestContext framework
  
Spring IoC Container is the core of Spring Framework. It creates the objects, configures and assembles their dependencies, manages their entire life cycle. The Container uses Dependency Injection(DI) to manage the components that make up the application. It gets the information about the objects from a configuration file(XML) or Java Code or Java Annotations and Java POJO class. These objects are called Beans. Since the Controlling of Java objects and their lifecycle is not done by the developers, hence the name Inversion Of Control. 

Note: Spring IoC generally directly refers to a core container that uses the DI/DC pattern to implicitly provide an object reference in a class during runtime. The IoC container contains assembler code that handles the configuration management of application objects. 

The following diagram depicts how the Container makes use of Configuration metadata and Java POJO classes to manage beans.

So finally let us discuss out some major differences between BeanFactory vs ApplicationContext in order to get a clear cutaway understanding of the spring IoC container which is as shown below in a tabular format below as follows:

|Feature | BeanFactory | ApplicationContext|
|-------------------|-------------------|-------------------|
|Annotation Support	|No |Yes|
|Bean Instantiation/Wiring	|Yes|Yes|
|Internationalization|No|Yes|
|Enterprise Services	|No|Yes|
|ApplicationEvent publication	|No |Yes|
|Automatic BeanPostProcessor registration|No|Yes|
|Loading Mechanism|	Lazy loading|	Aggressive loading|
|Automatic BeanFactoryPostProcessor registration|No|Yes|

#### 1. What is Spring Boot? How it is Different from Spring Framework?
Spring boot modules
Spring boot modules
Spring Boot is a Spring framework module that provides RAD (Rapid Application Development) features to the Spring framework with the help of starter templates and auto-configuration features which are very powerful and work flawlessly.

Spring Boot starters take an opinionated view of the Spring platform and third-party libraries. It means that as soon as we include any dependency into an application, spring boot assumes its general purpose and automatically configures the most used classes in the library as spring beans with sensible defaults.

For example, if we create a WebMVC application, only including the maven dependency spring-boot-starter-web brings all jars/libraries used for building web, including RESTful, applications using Spring WebMVC. It also includes Tomcat as the default embedded server.

It also provides a range of non-functional features such as embedded servers, security, metrics, health checks, and externalized configuration out of the box without extra configurations.

Suppose we have to identify the difference between the Spring framework and Spring boot. In that case, we can say that Spring Boot is an extension of the Spring framework, which eliminated the boilerplate configurations required for setting up a working production-ready application.

It takes an opinionated view of the Spring and third-party libraries imported into the project and configures the behavior for us.

#### 2. What are the New Features in Spring Boot 3?
There are several new features in Spring boot 3 which is based on Spring 6. It changes a lot of things we need to take care of during the application development in the future.

The main features or changes introduced in Spring 6 (also applicable to Spring Boot 3) are as follows:

Upgraded baseline Java version to Java 17. Older versions are not supported. Additionally, in the future, Spring 6 will adopt more exciting features such as Project Loom while retaining a JDK 17 baseline.
Replaced Java EE with Jakarta EE; the minimum supported version is Jakarta EE9. 
Native support for declarative HTTP client interface using @HttpExchange annotations.
New ProblemDetail API for compliance with Problem Details for HTTP APIs specification [RFC 7807].
Expect first-class support for JPMS (Java Platform Module System) which will allow more strict accessibility in the application code and libraries.
Enhanced support for native compilation, a move towards making cloud-native applications more efficient.
Bakes observability into Spring to further encourage cloud-native development.
#### 3. Advantages and Disadvantages of Spring Boot?
Advantages:
The best advantage of Spring Boot is that it provides simplified & version-conflict-free dependency management through the starter POMs and opinionated auto-configuration of most commonly used libraries and behaviors.

The embedded jars enable package the web applications as jar files that we can run anywhere.

The actuator module provides HTTP endpoints to access application internals like detailed performance metrics, health status, etc.

Disadvantages:
On the disadvantages side, they are very few. Still, many developers may see the transitive dependencies included with starter poms as a burden to deployment packaging.

Also, its auto-configuration feature may enable many such features that we may never use in the application lifecycle. They will sit there all the time, initialized and fully configured. It may cause some unnecessary resource utilization.

#### 4. How Can We Set Up a Spring Boot Application With Maven?
The easiest and recommended way to set up a new Spring boot application is using the Spring Initializr tool. It ensures that we are using the latest artifact versions, automatically. The tool can generate the project with various configurations such as Java version, Maven or Gradle build, jar or war packaging, etc. We can also select all the features our application needs, such as Web, JPA, H2 etc.


Another way to create a project is to Create New Maven Project wizard in IDEs such as Eclipse or IntelliJ. After creating the maven project, we need to include the spring-boot-starter-parent dependency in the pom.xml file, if the tool didn’t include it already.

pom.xml
pom.xml<parent>
  <groupId>org.springframework.boot</groupId>
  <artifactId>spring-boot-starter-parent</artifactId>
  <version>3.1.2</version>
  <relativePath/> <!-- lookup parent from repository -->
</parent>

#### 5. What is AutoConfiguration? How to Enable or Disable a Certain Configuration?
Spring boot autoconfiguration scans the classpath, finds the libraries in the classpath and then attempts to guess the best default configuration for them, and finally configure all such beans.

Autoconfiguration tries to be as intelligent as possible and backs away as we define more of our own custom configuration. Autoconfiguration is always applied after user-defined custom beans have been registered.

Autoconfiguration works with the help of @Conditional annotations such as @ConditionalOnBean and @ConditionalOnClass.

For example, look at AopAutoConfiguration class. If classpath scanning finds EnableAspectJAutoProxy, Aspect, Advice and AnnotatedElement classes and spring.aop.auto=false is not present in the properties file, then Spring boot will configure the Spring AOP module for us.

@Configuration
@ConditionalOnClass({ EnableAspectJAutoProxy.class,
			Aspect.class,
			Advice.class,
			AnnotatedElement.class })
@ConditionalOnProperty(prefix = "spring.aop",
			name = "auto",
			havingValue = "true",
			matchIfMissing = true)
public class AopAutoConfiguration
{
	//code
}

To enable an autoconfiguration, just importing the correct starter dependency is enough. Everything else works as discussed above.

To disable an autoconfiguration, use the exclude attribute of the @EnableAutoConfiguration annotation. For instance, this code snippet disables the DataSourceAutoConfiguration:

@EnableAutoConfiguration(exclude = DataSourceAutoConfiguration.class)
public class MyConfiguration { }

#### 6. What are Starter Dependencies?
Spring Boot starters are maven templates that contain a collection of all the relevant transitive dependencies that are needed to start a particular functionality.

For example, If we want to create a Spring WebMVC application, we would have included all required dependencies ourselves in a traditional setup. It leaves the chances of version conflict which ultimately results in ClassCastException.

With Spring boot, to create a WebMVC application, all we need to import is spring-boot-starter-web dependency. Transitively, this starter brings in all other required dependencies to build a web application, for example, spring-webmvc, spring-web, hibernate-validator, tomcat-embed-core, tomcat-embed-el, tomcat-embed-websocket, jackson-databind, jackson-datatype-jdk8, jackson-datatype-jsr310 and jackson-module-parameter-names.

<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-web</artifactId>
</dependency>

#### 7. What are Some Important Spring Boot Annotations?
The most commonly used and important spring boot annotations are as below:

@ComponentScan – enables component scanning in the application classpath.
@EnableAutoConfiguration – enables auto-configuration mechanism that attempts to guess and configure beans that you are likely to need.
@Configuration – indicates that a class declares one or more @Bean methods to generate bean definitions and service requests for those beans at runtime.
@SpringBootApplication – is a composite annotation composed of the above 3 annotations. This enables auto-configuration mechanism, enable component scanning and register extra beans in the context.
@ImportAutoConfiguration – imports and apply only the specified auto-configuration classes. We should use this when we don’t want to enable the default autoconfiguration.
@AutoConfigureBefore, @AutoConfigureAfter, @AutoConfigureOrder – shall be used if the configuration needs to be applied in a specific order (before of after).
@Conditional – annotations such as @ConditionalOnBean, @ConditionalOnWebApplication or @ConditionalOnClass allow to register a bean only when the condition is met.
#### 8. How to Create a REST API?
Creating a REST API is part of the Spring WebMVC module that is imported via spring-boot-starter-web dependency. With the web module, we get the annotations for creating REST APIs such as @RestController, @GetMapping, @PostMapping etc.

The following is the simplest REST API which returns the message “Hello World!” when we access the API at URL “/hello”.

import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.RestController;

@RestController
public class HelloWorldController {

  @GetMapping("hello")
  String hello() {
    return "Hello, World!";
  }
}

In a real-world application, we start with defining the REST resource model which is generally a POJO object with necessary fields and accessor methods.

class Employee {

  private Long id;
  private String name;
  private String role;

  //Getters, Setters, constructors, toString, other fields
}

Next, we write the REST controllers that handle the requests coming to resource mapping URLs. At this step, we connect to autowired DAO and other components to fetch the data from backend systems and return the response along with appropriate response codes.

import java.util.List;
import org.springframework.web.bind.annotation.DeleteMapping;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.PathVariable;
import org.springframework.web.bind.annotation.PostMapping;
import org.springframework.web.bind.annotation.PutMapping;
import org.springframework.web.bind.annotation.RequestBody;
import org.springframework.web.bind.annotation.RestController;

@RestController
class EmployeeController {

  private final EmployeeRepository repository;

  EmployeeController(EmployeeRepository repository) {
    this.repository = repository;
  }

  //Get All Employees
  @GetMapping("/employees")
  List<Employee> all() {
    return repository.findAll();
  }

  //Create an Employee
  @PostMapping("/employees")
  Employee newEmployee(@RequestBody Employee newEmployee) {
    return repository.save(newEmployee);
  }

  //Other methods
}

Also, we can use the annotations, such as @ControllerAdvice, to create a central exception handling mechanism.

Optionally, based on requirements, we can plug-in additional functionalities such as request validations and HATEOAS.

#### 9. Difference between @RestController and @Controller annotations?
The @Controller annotation serves as a specialization of @Component, allowing for implementation classes to be auto-detected through classpath scanning. The @RequestMapping annotated methods, in the controller class, act as request handlers for the mapped URLs.

If we need to return raw JSON or XML from the @Controller class methods, we need to annotate the method with @ResponseBody that indicates a method return value should be bound to the web response body.

The @RestController is a composite annotation that is a combination of @Controller and @ResponseBody. When we annotate a class with @RestController, all the handler methods automatically have @ResponseBody annotation applied. So all handler methods automatically return the raw JSON/XML response bodies.

@RestController = @Controller + @ResponseBody

#### 10. What is the difference between @RequestMapping and @GetMapping?
The @GetMapping is a specialized composed version of @RequestMapping annotation that is used on handler methods for HTTP GET APIs.

@GetMapping = @RequestMapping(method = { RequestMethod.GET })

Similarly, @PostMapping annotation maps HTTP POST requests onto specific handler methods. It is a shorter form to write @RequestMapping(method = RequestMethod.POST)}.

#### 11. How do you add a Filter to an application?
To create a filter, we simply need to implement the javax.servlet.Filter interface. Also, for Spring to recognize a filter, we need to define it as a bean with the @Component annotation.

Based on application needs, we override the filter methods init(), doFilter() and destroy().

@Component
public class TraceLoggingFilter implements Filter {

    @Override
    public void doFilter(
      ServletRequest request, 
      ServletResponse response, 
      FilterChain chain) throws IOException, ServletException {

      //...
    }
}

To apply the filter on URL patterns, we need to register it as FilterRegistrationBean.

@Bean
public FilterRegistrationBean<TraceLoggingFilter> tracingFilter()
{
    FilterRegistrationBean<TraceLoggingFilter> filterBean 
    	= new FilterRegistrationBean<>();
    filterBean.setFilter(new TraceLoggingFilter());
    filterBean.addUrlPatterns("/*");
    filterBean.setOrder(1);
    return filterBean;    
}

#### 12. Explain Embedded Server Support in Spring Boot
Spring boot applications include embedded servers as part of spring-boot-starter-web dependency and configure Tomcat as the default embedded server. It means that we can run a web application from the command prompt without setting up any complex server infrastructure.

If we want, we can exclude Tomcat and include any other embedded server. Or we can exclude the server environment altogether. It is all configuration-based.

For example, the below configuration excludes Tomcat and includes jetty as the embedded server.

<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-web</artifactId>
    <exclusions>
        <exclusion>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-tomcat</artifactId>
        </exclusion>
    </exclusions>
</dependency>
  
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-jetty</artifactId>
</dependency>
#### 13. Can We Disable the Default Web Server?
Yes, we can disable all embedded servers from a spring boot application. We need to look into the maven dependency tree and exclude the Tomcat library from whichever dependency is including it.

Another way to disable all embedded servers is by using the property spring.main.web-application-type to none in application.properties file.

 spring.main.web-application-type=none

A similar configuration can be done using the Java configuration when starting the application by setting the application type to NONE.

SpringApplication application = new SpringApplication(MainApplication.class);
application.setWebApplicationType(WebApplicationType.NONE);
application.run(args);

#### 14. How to Enable Debug Logging?
The easiest way to enable debug logging is to set it through the properties file:
```
debug=true
```
- For trace level logging
```
trace=true 
```
We can pass the debug flag during application startup as well.
```
java -jar application.jar --debug
```
#### 15. How to Check all the Environment Properties in the Application?
The easiest way to list down all the properties in an application is by including the actuator module and accessing the URL endpoint /env.

Do not forget to enable the endpoint in the properties configuration.
```
management.endpoints.web.exposure.include=env
```
#### 16. How do we Define and Load Properties?
Spring boot provides many ways to set up and access properties in an application.

Typically, spring boot reads and applies all configurations from the application.properties file from the classpath.
To specify a different file name or location, use the startup argument spring.config.location. For example, --spring.config.location=config/*.properties will load the properties files from the config folder.
The @PropertySource annotation is a convenient mechanism for adding property sources. Note that it is a repeatable annotation so we can apply this annotation multiple times in a class. In the event of a property name collision, the last source read takes precedence.
@Configuration
@PropertySource("classpath:foo.properties")
@PropertySource("classpath:bar.properties")
public class AppProperties {
    //...
}

We can use @Value annotation to inject a property directly into a field.
@Value( "${jdbc.url}" )
private String jdbcUrl;

To load the test-specific properties file, the most straightforward way is to use the @TestPropertySource annotation.
To load the profile-specific properties files, application-{environment}.properties file in the src/main/resources directory, and then set a Spring profile with the same environment name.
#### 17. How to Connect to the Database using JPA?
To work with JPA-based repositories, first, we need to include spring-boot-starter and spring-boot-starter-data-jpa dependencies. These starters have all the autoconfiguration and hibernate-related dependencies.

Spring Boot configures Hibernate as the default JPA provider, so the application will automatically have all necessary beans such as entityManagerFactory.

For connecting with a database, we need to specify the datasource configuration in the application.properties file.
```
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
spring.datasource.username=root
spring.datasource.password=sa
spring.datasource.url=jdbc:mysql://localhost:3306/testDb?createDatabaseIfNotExist=true
```
Also, note that Spring boot uses HikariCP as the default connection pool. So if you need to change the connection pool, configure the respective properties.

#### 18. Why do we use Spring Boot Maven Plugin?
The plugin provides Spring Boot support in Maven, letting us package executable jar or war archives and run an application in-place. To use it, we must use Maven 3.2 (or later).

The plugin provides several goals to work with a Spring Boot application:

spring-boot:repackage: create a jar or war file that is auto-executable. It can replace the regular artifact or can be attached to the build lifecycle with a separate classifier.
spring-boot:run: run your Spring Boot application with several options to pass parameters to it.
spring-boot:start and stop: integrate your Spring Boot application to the integration-test phase so that the application starts before it.
spring-boot:build-info: generate a build information that can be used by the Actuator.
#### 19. How to Package an Application as Executable .jar or .war File?
Executable jars (sometimes called”fat jar”) are archives containing the compiled classes and all of the jar dependencies that the application needs to run.

To create an executable jar, we shall add spring-boot-maven-plugin in pom.xml. By default, this plugin package the application as .jar file only.
```pom
<build>
    <plugins>
        <plugin>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-maven-plugin</artifactId>
        </plugin>
    </plugins>
</build>
```
The first logical step to create a war file is to declare the packaging type ‘war’ in pom.xml file.

The second thing is set the scope of embedded server dependency to ‘provided‘ because server dependencies will be provided by the application server where we will deploy the war file.
```pom
<packaging>war</packaging>
 
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-tomcat</artifactId>
    <scope>provided</scope>
</dependency>
```
#### 20. How to Configure Logging in Spring Boot?
Spring Boot uses Commons Logging for all logging internal to the framework and thus it is a mandatory dependency. For other logging needs, Spring boot supports default configuration for Java Util Logging, Log4J2, and Logback.

When added directly or transitively, spring-boot-starter-logging module configures the default logging with Logback and SLF4J.

The default logging uses a console logger with a log level set to DEBUG, which we can change in the custom logback.xml file.

To use Log4j2, we must exclude spring-boot-starter-logging module and import spring-boot-starter-log4j2 module. The custom configuration can be done in the log4j2.xml file.
```pom
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-web</artifactId>
    <exclusions>
        <exclusion>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-logging</artifactId>
        </exclusion>
    </exclusions>
</dependency>
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-log4j2</artifactId>
</dependency>
```
#### 21. What is the Spring Actuator? What are its Advantages?
Spring boot’s actuator module allows us to monitor and manage application usages in the production environment, without coding and configuration for any of them. This monitoring and management information is exposed via REST-like endpoint URLs.

The simplest way to enable the features is to add a dependency to the spring-boot-starter-actuator starter pom file.
```pom
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-actuator</artifactId>
</dependency>
```
The actuator module includes several built-in endpoints and lets us add our own. Further, each individual endpoint can be enabled or disabled as well.

Some of the important and widely used actuator endpoints are given below:

Endpoint	Usage
/env	Returns list of properties in the current environment
/health	Returns application health information.
/auditevents	Returns all auto-configuration candidates and the reason why they ‘were’ or ‘were not’ applied.
/beans	Returns a complete list of all the Spring beans in your application.
/trace	Returns trace logs (by default the last 100 HTTP requests).
/dump	It performs a thread dump.
/metrics	It shows several useful metrics information like JVM memory used, system CPU usage, open files, and much more.
#### 22. What are Relaxed Bindings?
Spring Boot uses some relaxed rules for resolving configuration property names such that we can write a simple property name in multiple ways.

For example, a simple property log.level.my-package can be written in the following ways and all are correct and will be resolved by framework for its value based on property source.
```
log.level.my-package = debug    	//Kebab case
log.level.my_package = debug 		//Underscore notation
log.level.myPackage = debug 		//Camel case
LOG.LEVEL.MY-PACKAGE = debug 		//Upper case format
```
Following is a list of the relaxed binding rules per property source.

Property Source	Types Allowed
Properties Files	Camel case, kebab case, or underscore notation
YAML Files	Camel case, kebab case, or underscore notation
Environment Variables	Upper case format with an underscore as the delimiter. _ should not be used within a property name
System Properties	Camel case, kebab case, or underscore notation
#### 23. How to Perform Unit Testing and Integration Testing?
Typically any software application is divided into different modules and components. When one such component is tested in isolation, it is called unit testing.

Unit tests do not verify whether the application code works with external dependencies correctly. It focuses on a single component and mocks all dependencies this component interacts with.

We can perform unit testing help of specialized annotations such as :

@JdbcTest – can be used for a typical JDBC test when a test focuses only on jdbc-based components.
@JsonTest – It is used when a test focuses only on JSON serialization.
@RestClientTest – is used to test REST clients.
@WebMvcTest – used for Spring MVC tests with configuration relevant to only MVC tests.
Integration tests can put the whole application in scope or only certain components – based on what is being tested. They may need to require resources like database instances and hardware to be allocated for them. However, these interactions can be mocked out as well to improve the test performance.

In integration testing, we shall focus on testing complete request processing from the controller to the persistence layer.

The @SpringBootTest annotation helps in writing integration tests. It starts the embedded server and fully initializes the application context. We can inject the dependencies in the test class using @Autowired annotation.

We can also provide test-specific beans configuration using nested @Configuration class or explicit @TestConfiguration classes.

It also registers a TestRestTemplate and/or WebTestClient bean for use in web tests.
```java
@SpringBootTest(classes = SpringBootDemoApplication.class, 
        webEnvironment = WebEnvironment.RANDOM_PORT)
public class EmployeeControllerIntegrationTests 
{
    @LocalServerPort
    private int port;
  
    @Autowired
    private TestRestTemplate restTemplate;
  
    //tests
}
```
#### 24. What are Spring Profiles?
We can assume profiles as the various runtime environments where we will deploy the application, and we expect the application to behave differently. For example, localhost, dev, test and prod.

Spring profiles allow us to map our beans to different profiles. Based on the profile, only mapped beans will be activated and other beans will be deactivated.

To create a new profile, we can use the @Profile annotation. In the given example, we have configured two profiles localhost and non-localhost environments for datasource configuration.
```java
@Profile("localhost")
public class LocalhostDatasourceConfig {
   //...
}

@Profile("!localhost")
public class DatasourceConfig {
   //...
}
```
To activate a profile, we can pass the Spring.profiles.active property during the application startup. This property can also be defined using the system property in the respective machines.

java -jar app.jar -Dspring.profiles.active=localhost

We can specify the default profile using the property spring.profiles.default.

#### 25. What Is Spring Boot DevTools Used For?
The Spring boot dev tools module provides many useful developer features for improving the development experience such as caching static resources, automatic restarts, live reload, global settings and running remote applications.

To enable dev tools, add the spring-boot-devtools dependency in the build file.

Read the linked article to know the complete list of features offered by the dev tools module.

#### 26. How to enable Hot Deployment and Live Reload on the browser?
Most modern IDEs support hot-swapping of bytecode, and most code changes should reload cleanly with no side effects. Additionally, the spring-boot-devtools module includes support for automatic application restarts whenever files on the classpath change.

By default, any entry on the classpath that points to a folder is monitored for changes. Note that certain resources, such as static assets and view templates, do not need to restart the application.

The spring-boot-devtools module includes an embedded LiveReload server that can be used to trigger a browser refresh when a resource is changed. LiveReload browser extensions are freely available for Chrome, Firefox and Safari from livereload.com.

To enable/disable LiveReload server, change value of spring.devtools.livereload.enabled property to true (default value) or false.

#### 27. What is a Cross-Site Request Forgery attack?
CSRF stands for Cross-Site Request Forgery or Session Riding. It targets an end-user to, unknowingly, execute unwanted actions on a web application in which they are currently authenticated.

The unwanted actions are generally the form of URL requests that may happen either by clicking on injected links by the bad actor or by image URLs that do not need even a click.

In a Spring boot applications, CSRF protection is enabled by default. We can disable it using the following spring HttpSecurity interface configuration.
```java
@Override
protected void configure(HttpSecurity http) throws Exception {
    http
      .csrf().disable();
}
```
#### 28. Explain CORS in Spring Boot
CORS (Cross-origin resource sharing) allows a webpage to request additional resources into the browser from other domains e.g. fonts, CSS or static images from CDN. CORS helps in serving web content from multiple domains into browsers that usually have the same-origin security policy.

In Spring,  @CrossOrigin annotation marks the annotated method or type as permitting cross-origin requests. If applied to a controller, all the handler methods permit the cross-origin requests.
```java
@CrossOrigin(origins = "*", allowedHeaders = "*")
@Controller
public class HomeController 
{
    //
}

//or

@Controller
public class HomeController 
{
    @CrossOrigin(origins = "*", allowedHeaders = "*")
    @GetMapping(path="/")
    public String homeInit(Model model) {
        return "home";
    }
}
```
To enable CORS for the whole application, use WebMvcConfigurer to add CorsRegistry.
```java
@Configuration
@EnableWebMvc
public class CorsConfiguration implements WebMvcConfigurer
{
    @Override
    public void addCorsMappings(CorsRegistry registry) {
        registry.addMapping("/**")
                .allowedMethods("GET", "POST");
    }
}
```
#### 29. How to enable HTTPS/SSL support in Spring Boot?
The SSL support in spring boot project can be added via application.properties and by adding the below entries.
```
server.port=8443
server.ssl.key-alias=selfsigned_localhost_sslserver
server.ssl.key-password=changeit
server.ssl.key-store=classpath:ssl-server.jks
server.ssl.key-store-provider=SUN
server.ssl.key-store-type=JKS
```
