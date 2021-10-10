# **Spring RESTful Routing & Static Files**

## **[Spring RequestMapping](https://www.baeldung.com/spring-requestmapping)**

## **1. @RequestMapping Basics**

### ***@RequestMapping — by Path***

- Define the Request URI to access the REST Endpoints

```java
@RequestMapping(value = "/ex/foos", method = RequestMethod.GET)
@ResponseBody
public String getFoosBySimplePath() {
    return "Get some Foos";
}
```

### ***@RequestMapping — the HTTP Method***

- The HTTP method parameter has no default

```java
@RequestMapping(value = "/ex/foos", method = POST)
@ResponseBody
public String postFoos() {
    return "Post some Foos";
}
```

## **2. RequestMapping and HTTP Headers**

### ***@RequestMapping With the headers Attribute***

- The mapping can be narrowed even further by specifying a header for the request:

```java
@RequestMapping(value = "/ex/foos", headers = "key=val", method = GET)
@ResponseBody
public String getFoosWithHeader() {
    return "Get some Foos with Header";
}
```

### ***@RequestMapping Consumes and Produce***

```java
@RequestMapping(
  value = "/ex/foos", 
  method = GET, 
  headers = "Accept=application/json")
@ResponseBody
public String getFoosAsJsonFromBrowser() {
    return "Get some Foos with Header Old";
}
```

## **3. RequestMapping With Path Variables**

- Parts of the mapping URI can be bound to variables via the `@PathVariable` annotation.
    - `Single @PathVariable`
    - `Multiple @PathVariable`
    - ` @PathVariable With Regex`

## **4. @RequestMapping With Request Parameters**

- allows easy mapping of URL parameters with the `@RequestParam` annotation.
- `@RequestMapping` allows easy mapping of URL parameters with the `@RequestParam` annotation.

```java
@RequestMapping(value = "/ex/bars", method = GET)
@ResponseBody
public String getBarBySimplePathWithRequestParam(
  @RequestParam("id") long id) {
    return "Get a specific Bar with id=" + id;
}
```

## **5. RequestMapping Corner Cases**

- ***`@RequestMapping` — Multiple Paths Mapped to the Same Controller Method :is usually used for a single controller method***

- ***`@RequestMapping` — Multiple HTTP Request Methods to the Same Controller Method***

- ***`@RequestMapping` — a Fallback for All Requests***

> Multiple requests using different HTTP verbs can be mapped to the same controller method.

> To implement a simple fallback for all requests using a particular HTTP method

### Ambiguous Mapping Error

- The ambiguous mapping error occurs when Spring evaluates two or more request mappings to be the same for different controller methods. A request mapping is the same when it has the same HTTP method, URL, parameters, headers, and media type.

<hr>

# **[Accessing Data with JPA](https://spring.io/guides/gs/accessing-data-jpa/)**

These notes fro how to build an application that stores Customer POJOs (Plain Old Java Objects) in a memory-based database.

- To generate a new project with the required dependencies (Spring Data JPA and H2 H2 Database).for *Gradle* users, visit the [Spring Initializr](https://start.spring.io/)

- The class is annotated with `@Entity`, indicating that it is a JPA entity. (Because no `@Table` annotation exists, it is assumed that this entity is mapped to a table of the class name.)

## Create an Application Class

- `@SpringBootApplication` : it is convenience annotation that use to auto-configuration, component scan and be able to define extra configuration on application class.

- `@EnableAutoConfiguration` : Tells Spring Boot to start adding beans based on classpath settings, other beans, and various property settings.

- `@Configuration` : Allow to register extra beans in the context or import additional configuration classes.

- `@ComponentScan` : Enable @Component scan on the package where the application is located.
