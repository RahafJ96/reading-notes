# Spring

## **[Spring App Basics](https://spring.io/guides/gs/serving-web-content/)**

### Starting with Spring Initializr

- If you use Gradle, visit the [Spring Initializr](https://start.spring.io/) to generate a new project with the required dependencies (Spring Web, Thymeleaf, and Spring Boot DevTools).

### Spring Boot Devtools
To speed up this refresh cycle, *Spring Boot* offers with a handy module known as **spring-boot-devtools**. Spring Boot Devtools:
- Enables hot swapping(replace without rebooting the system).
- Switches template engines to disable caching.
- Enables LiveReload to automatically refresh the browser.
-others

### Run the Application
- @Configuration: Tags the class as a source of bean definitions for the application context.

### Test the Application
- Provide a name query string parameter by visiting http://localhost:8080/greeting?name=User. 

- The **index.html** resource is special because, if it exists, it is used as a "`welcome page,"serving-web-content/ which means it is served up as the root resource (that is, at `http://localhost:8080/
- When you restart the application, you will see the HTML at http://localhost:8080/.

### Spring Boot Devtools
- Enables [hot swapping](https://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/#howto-hotswapping).
- Switches template engines to disable caching.
- Enables LiveReload to automatically refresh the browser.
- Other reasonable defaults based on development instead of production.

<hr>

## **[Spring MVC and Thymeleaf](https://www.thymeleaf.org/doc/articles/springmvcaccessdata.html)**

### **Spring model attributes:**

`Spring MVC` calls the pieces of data that can be accessed during the execution of views model attributes. The equivalent term in Thymeleaf language is context variables.


**There are several ways of adding model attributes to a view in Spring MVC.** *Below you will find some common cases:*

- Add attribute to Model via its addAttribute method:

  ```java
    @RequestMapping(value = "message", method = RequestMethod.GET)
        public String messages(Model model) {
            model.addAttribute("messages", messageRepository.findAll());
            return "message/list";
        }
  ```

- Return ModelAndView with model attributes included:

  ```java
   @RequestMapping(value = "message", method = RequestMethod.GET)
        public ModelAndView messages() {
            ModelAndView mav = new ModelAndView("message/list");
            mav.addObject("messages", messageRepository.findAll());
            return mav;
        }
  ```

- Expose common attributes via methods annotated with @ModelAttribute:

  ```java
      @ModelAttribute("messages")
        public List<Message> messages() {
            return messageRepository.findAll();
        }
  ```
<hr>
