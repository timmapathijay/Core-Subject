# Spring Boot Interview Questions 
Q1. What is Spring Boot ?
Ans : 1. Spring Boot is a Java framework that makes it easier to create & run Java applications.
2. It simplifies the configuration & setup process, allowing developers to focus more on writing code for their applications.

a. Configuration 
b. Dependency Management 
c. Embedded Server 

Q2. Why Spring Boot over Spring ?
Ans : Spring boot solves challenges which exists with Spring MVC. 
1. Dependency Management - No need for adding different dependencies separately & also their compatible version headache.
2. Auto-configuration - No need for separately configuring Dispatcher Servlet, AppConfig, EnableWebMvc  & ComponentScan. Spring boot add internally by-default[@SpringBootApplication].
3. Embedded Server 

Q3. Working of Spring Boot ?
Ans : 1. Spring boot starts by scanning the starter dependencies in pom.xml. Then download & auto-configure the module as you included in pom.xml. [Download - Build , Run - Configuration]

Q4. How Spring Boot starts ?
Ans: 1. Starts by calling main() method of your main class.
2. The run() static method of SpringApplication is called. This method starts the application by creating an application context & initializing it.
@SpringBootApplication - @Configuration + @EnableAutoConfiguration+ @ComponentScan
3. Once the application context is initialized, the run() static method starts the applications embedded web server.

Q5. Top Spring Boot Annotations 
1. @SpringBootApplication - @Configuration + @EnableAutoConfiguration+ @ComponentScan
It is typically placed on the main class of the application.
2. @Component - It is used to mark a class as a Spring bean that will be managed by the Spring container.
3. @Autowired - this annotation is used to automatically inject dependencies into a spring managed bean.
4. @Service - this annotation is used to indicate that a class represents a service component in the application. It is typically used to annotate classes that contains business logic.
5. @RestController - mark class as REST controller. It is specialized version of the @Controller annotation that includes the @ResponseBody annotation by default.
6. @RequestMapping - used to map specific url to method. Used on class as well as method level.
7. @Repository - mark class as DAO(Data Access Object) , mostly used on class that has database persistent logic.

Q6. What are the Spring Boot Starters.
Ans: Starters are a collection of pre-configured dependencies that make it easier to develop particular kinds of applications.
a. Dependencies 
b. version-control
c. configuration 

eg : spring-boot-starter-parent , spring-boot-starter-test , spring-boot-starter-security , spring-boot-starter-web

Q7. What is Spring-Boot-Starter-Parent ?
Ans : Spring boot starter parent is a starter project that provides the default configuration for spring based applications.

Q8. What is Spring boot CLI & what are its benefits?
Ans : Commond line tool to create, run & manage spring boot applications.
spring version 
spring init -d dependencies project-name

Q9. What is IOC or inversion of control ?

Q10. Explain Spring Bean LifeCycle ?
Ans : Bean - Java Object
Spring bean lifecycle is maintained by IOC container 
1. Container gets started.
2. Container creates the object of bean as per request.
3. Dependencies is created.
4. Dependencies is injected.
5. Destroyed when container is closed.

@PostConstruct - annotation is used on a method that needs to be executed after dependency injection is done to perform any initialization.
@PreDestroy - annotation is used on a method as a callback notification to signal that the instance is in the process of being removed by the container.

Q11. What is Bean Factory, have you used XMLBeanFactory ?
Ans: Bean factory is a root interface for accessing a Spring bean container. It is actually a container that instantiates, configures & manages a number of beans.

Q12. What are the difference between BeanFactory & ApplicationContext in Spring ?
Ans: BeanFactory(I) [org.springframework.beans.factory]
- Fundamental container providing basic functionality for managing beans.
- Supports only Singleton and Prototype bean scopes.
- Creates bean objects on demand using lazy initialization.
ApplicationContext(I) [org.springframework.context]
- ApplicationContext(I) extends BeanFactory(I)
- Advanced container extending BeanFactory with additional features.
- Supports all types of bean scopes, including Singleton, Prototype, Request, Session, etc.
- Loads all beans and creates objects at startup using eager initialization.

Q13. Difference between @Autowired & @Inject annotation in spring ?
Ans : The @Inject annotation also serves the same purpose as @Autowired. The main difference between them is that @Inject is a standard annotation for dependency injection & @Autowired is spring specific.


Q14. Difference between @Bean & @Component annotation in Spring ?
Q15. What is autowiring in spring ? What are the autowiring modes?
Ans : Injecting the beans automatically. We don't need to write explicit injection logic.
a. no - this is default mode, it means autowiring is not enabled.
b. byName - inject the bean based on property name. It uses setter method.
c. byType - injects the bean based on the property type. It uses setter method.
b. constructor - inject the bean using constructor.

Q15. What are the different bean scopes in spring ?
1. Singleton - the bean instance will be created only once & same instance will be returned by the IOC container. It is default scope.
2. Prototype - the bean instance will be created each time when requested.
3. Request - the bean instance will be created per HTTP request.
4. Session - the bean instance will be created per HTTP session.
