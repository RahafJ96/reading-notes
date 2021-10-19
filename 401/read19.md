# Spring and Sockets

## [Using WebSocket to build an interactive web application](https://spring.io/guides/gs/messaging-stomp-websocket/)

### How to complete this guide?

- Create a repo, after that clone int in your machine.
- Create a Web Controller.


## Manual Initialization 

1- Navigate to `https://start.spring.io.` This service pulls in all the dependencies you need for an application and does most of the setup for you.

2- Choose either Gradle or Maven and the language you want to use. This guide assumes that you chose Java.

3- Click Dependencies and select Spring Web, Thymeleaf, and Spring Boot DevTools.

4- Click Generate.

5- Download the resulting ZIP file, which is an archive of a web application that is configured with your choices.4

## Create a Message-handling Controller

In Spring’s approach to working with STOMP messaging, STOMP messages can be routed to `@Controller` classes. 

The following listing shows:
```java
package com.example.messagingstompwebsocket;

import org.springframework.messaging.handler.annotation.MessageMapping;
import org.springframework.messaging.handler.annotation.SendTo;
import org.springframework.stereotype.Controller;
import org.springframework.web.util.HtmlUtils;

     @Controller
     public class GreetingController {


     @MessageMapping("/hello")
     @SendTo("/topic/greetings")
     public Greeting greeting(HelloMessage message) throws   Exception {
     Thread.sleep(1000); // simulated delay
      return new Greeting("Hello, " + HtmlUtils.htmlEscape(message.getName()) + "!");
      }

      }
      
```
The `@MessageMapping` annotation ensures that, if a message is sent to the `/hello` destination, the `greeting()` method is called.

## Configure Spring for STOMP messaging

You can configure Spring to enable WebSocket and STOMP messaging.
```java
package com.example.messagingstompwebsocket;

     import org.springframework.context.annotation.Configuration;
     import org.springframework.messaging.simp.config.MessageBrokerRegistry;
     import org.springframework.web.socket.config.annotation.EnableWebSocketMessageBroker;
     import org.springframework.web.socket.config.annotation.StompEndpointRegistry;
     import org.springframework.web.socket.config.annotation.WebSocketMessageBrokerConfigurer;

     @Configuration
     @EnableWebSocketMessageBroker
     public class WebSocketConfig implements WebSocketMessageBrokerConfigurer {

      @Override
      public void configureMessageBroker(MessageBrokerRegistry config) {
     config.enableSimpleBroker("/topic");
     config.setApplicationDestinationPrefixes("/app");
     }

     @Override
     public void registerStompEndpoints(StompEndpointRegistry registry) {
      registry.addEndpoint("/gs-guide-websocket").withSockJS();
     }
     
     }
     
```
>`WebSocketConfig` is annotated with `@Configuration` to indicate that it is a Spring configuration class. It is also annotated with `@EnableWebSocketMessageBroker`. As its name suggests, `@EnableWebSocketMessageBroker` enables WebSocket message handling, backed by a message broker.   