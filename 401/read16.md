# Spring Authentication

## [Spring Security Architecture](https://spring.io/guides/topicals/spring-security-architecture/)

### 1. Authentication and Access Control
- **Authentication**
```java
public interface AuthenticationManager {

  Authentication authenticate(Authentication authentication)
    throws AuthenticationException;
}
```

- **Authorization, AKA: Access Control**

The main strategy interface for authentication is **AuthenticationManager**, which has only one method:
```java
public interface AuthenticationManager {

  Authentication authenticate(Authentication authentication)
    throws AuthenticationException;
}
```
- An **AuthenticationManager** can do one of 3 things in its **authenticate()** method:
1. Return an **Authentication** (normally with authenticated=true), if input represents a valid principal.

2. Throw an **AuthenticationException (which is a runtime exception.)** if input represents an invalid principal.

3. Return **null** if it cannot decide.


- The most commonly used implementation of **AuthenticationManager** is **ProviderManager**, which delegates to a chain of **AuthenticationProvider** instances. 
- **An AuthenticationProvider** is a bit like an AuthenticationManager, but it has an extra method to allow the caller to query whether it supports a given Authentication type:
```java
public interface AuthenticationProvider {

	Authentication authenticate(Authentication authentication)
			throws AuthenticationException;

	boolean supports(Class<?> authentication);
}
```
![ProviderManager](https://raw.githubusercontent.com/spring-guides/top-spring-security-architecture/main/images/authentication.png) 


### 2. Customizing Authentication Managers

- The most commonly used configuration helper is the **AuthenticationManagerBuilder**.

```java
@Configuration
public class ApplicationSecurity extends WebSecurityConfigurerAdapter {

   ... // web stuff here

  @Autowired
  public void initialize(AuthenticationManagerBuilder builder, DataSource dataSource) {
    builder.jdbcAuthentication().dataSource(dataSource).withUser("dave")
      .password("secret").roles("USER");
  }

}
```
- The AuthenticationManagerBuilder is @Autowired into a method in a @Bean.

```java
@Configuration
public class ApplicationSecurity extends WebSecurityConfigurerAdapter {

  @Autowired
  DataSource dataSource;

   ... // web stuff here

  @Override
  public void configure(AuthenticationManagerBuilder builder) {
    builder.jdbcAuthentication().dataSource(dataSource).withUser("dave")
      .password("secret").roles("USER");
  }

}
```
- If we had used an **@Override** of a method in the **configurer**, the **AuthenticationManagerBuilder** would be used only to build a “local” **AuthenticationManager**, which would be a child of the global one.
- In a Spring Boot application, **you can @Autowired the global one into another bean, but you cannot do that with the local one unless you explicitly expose it yourself.**




### 3. Authorization or Access Control

- The core Authorization is **AccessDecisionManager**. 
- There are three implementations provided by the framework and all three delegate to a chain of **AccessDecisionVoter** instances.


### 4. Web Security
The typical layering of the handlers for a single HTTP request:

![Client](https://raw.githubusercontent.com/spring-guides/top-spring-security-architecture/main/images/filters.png) 

- The client sends a request to the application, and the container decides which filters and which servlet apply to it based on the path of the request URI.

- At most, one servlet can handle a single request, but filters form a chain, so they are ordered. 

- The order of the filter chain is very important, and Spring Boot manages it through two mechanisms: **@Beans** of type Filter can have an **@Order** or implement **Ordered**, and they can be part of a **FilterRegistrationBean** that itself has an order as part of its API. 

- In a Spring Boot application, the security filter is a **@Bean** in the **ApplicationContext**, and it is installed by default so that it is applied to every request. 


---
## [Spring Auth cheat sheet](https://github.com/codefellows/seattle-java-401d2/blob/master/SpringAuthCheatSheet.md)

- a cheat sheet for Spring Authentication 