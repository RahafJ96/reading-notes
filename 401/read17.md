# [Spring Boot and OAuth2](https://spring.io/guides/tutorials/spring-boot-oauth2/)

There are several samples building on each other, adding new features at each step:

- `simple:` a very basic static app with just a home page and unconditional login via Spring Boot’s OAuth 2.0 configuration properties (if you visit the home page, you will be automatically redirected to GitHub).

- `click:` adds an explicit link that the user has to click to login.

- `logout:` adds a logout link as well for authenticated users.

- `two-providers:` adds a second login provider so the user can choose on the home page which one to use.

- `custom-error:` adds an error message for unauthenticated users, and a custom authentication based on GitHub’s API.

<hr>

```java
$ cd simple
$ ../mvnw package
$ java -jar target/*.jar
```
You can also run all the apps on the command line using `mvn spring-boot:run` or by building the jar file and running it with `mvn package` and `java -jar target/*.jar`.

<hr>

## How to create Single Sign On With GitHub

1. Creating a New Project
    * create a Spring Boot application
2. Add a Home Page
    * create index.html in the src/main/resources/static folder
3. Securing the Application with GitHub and Spring Security
    * add Spring Security as a dependency
    * you should include the Spring Security OAuth 2.0 Client starter
    * configure your app to use GitHub as the authentication provider by this step :
        1. Add a New GitHub app
        2. Configure application.yml
        3. Boot up the application
4. Add a Welcome Page
    * modify the simple app you just built by adding an explicit link to login with GitHub.
    * Instead of being redirected immediately, the new link will be visible on the home page
    * the user can choose to login or to stay unauthenticated.
    * Only when the user has clicked on the link will the secure content be rendered.
5. Conditional Content on the Home Page
    * To render content on the condition that the user is authenticated, you have the option of either server-side or client-side rendering.
6. Making the Home Page Public
    * To make the link visible, we also need to switch off the security on the home page by extending WebSecurityConfigurerAdapter.
    * Spring Boot attaches special meaning to a WebSecurityConfigurerAdapter on the class annotated with @SpringBootApplication
    * It uses it to configure the security filter chain that carries the OAuth 2.0 authentication processor.
7. Add a Logout Button
    * we modify the click app we built by adding a button that allows the user to log out of the app.
    * transforming the app from a read-only resource to a read-write one (logging out requires a state change)
    * Client Side Changes:need to provide a logout button and some JavaScript to call back to the server to ask for the authentication to be cancelled
    * Adding a Logout Endpoint: Spring Security has built in support for a /logout endpoint which will do the right thing for us
8. Adding the CSRF Token in the Client
    * you’ll need to explicitly add the CSRF token, which you just made available as a cookie from the backend.

## How to Add a Local User Database
* It is easy to do in two steps.

1. Choose a backend for your database, and set up some repositories (using Spring Data, say) for a custom User object that suits your needs and can be populated, fully or partially, from external authentication.
2. Implement and expose OAuth2UserService to call the Authorization Server as well as your database.
