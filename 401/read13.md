# Related Resources and Integration Testing
## The relations btween Entity classes:
> Working with Relationships in Spring Data REST:

### 1. One-to-One Relationship
- it defines using the @OneToOne annotation

### 2. One-to-Many Relationship
- Defined using the @OneToMany, and @ManyToOne annotations
- can have the optional @RestResource annotation to customize the association resource.

### 3. Many-to-Many Relationship
- Defined using `@ManyToMany` annotation.

> The Repository

- Let's create a repository interface to manage the Author entity:

  ```java
    public interface AuthorRepository extends CrudRepository<Author, Long> {

    }
  ```

### 4. Many-to-One Relationship

- A **Many-To-One** relationship represents a single-valued association where a collection of entities can be associated with the similar entity. Hence, in relational database any more than one row of an entity can refer to the similar rows of another entity.

- A Many-to-One relationship between two entities is defined by using the `@ManyToOne` annotation in Spring Data JPA.

> Spring MVC Test Configuration

- Enable Spring in Tests with JUnit 5
- Writing Integration Tests

<hr>

## Integration Testing:
- We use the following dependencies for testing in spring :
    - Spring Test.
    - Junit Jupiter.

- We use the Web application context annotation to wire the object of it which will add all the beans, controllers and classes.

- MockMVC class encapsulates beans of web application and makes them ready for testing.

- to Verify testing configuration we should verify that : 
    - Check if web application context is loaded.
    - check the right servlet context is instance of the web application context.

- We use perform method which will make a get request.
- followed by andDo(Print()) will print the request and response.
- andExpect(view().name("test.html")) will expect a specific view to be returned.
- We can also sending requests with perform method including path variables with this syntax perform("request/{id}" , "123")
- Also sending post requests can be achieved using mockMvc Library the same mechanism for get requests.


### Integration Testing in Spring
Some integration test we can write:
- Verify View Name
- Verify Response Body
- Send GET Request With Path Variable
- Send GET Request With Query Parameters