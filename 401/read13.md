# CRUD

## [Status Codes Based On REST Methods](https://www.moesif.com/blog/technical/api-design/Which-HTTP-Status-Code-To-Use-For-Every-CRUD-App/)

**1. In your own words, describe what each group of status code represents:**
- 100’s = These are informational status codes
- 200’s = These are the success codes
- 300’s = These are redirection codes
- 400’s = These are the client error codes
- 500’s = These are the server error codes



**2. What is a status code 202?**

- Often used for asynchronous processing. This code tells the client that the request was valid, but its processing will finish sometime in the future. The response body should include an URL to the finished resource with some information about when it will be available, or an URL to some monitoring endpoint that tells the client when the resource is available.

**3. What is a status code 308?**

- This tells the client to use another URL to access the resource and not use the current URL anymore. It’s helpful when we have multiple endpoints for one resource, but don’t want to implement reading from all of them.


**4. What code would you use if an update didn’t return data to a client?**

- 204 No Content


**5. What is the ‘Forbidden’ status code?**

- The client has authorized or doesn’t need to authorize itself, but still has no permissions to access the resource.


## [Build A REST API With Node.js, Express, & MongoDB - Quick]((https://www.youtube.com/channel/UCFbNIlppjAuEX4znoulh0Cw)) 


**1. Why do we need to pull our MongoDB database string out of our server and put it into our .env?**

- To keep it secure( for safe)


**2. What is middleware?**

- Middleware is software that provides common services and capabilities to applications outside of what’s offered by the operating system. Data management, application services, messaging, authentication, and API management are all commonly handled by middleware

**3. What does app.use(express.json()) do?**

- express. json() is a method inbuilt in express to recognize the incoming Request Object as a JSON Object. This method is called as a middleware in your application using the code: app. … urlencoded() is a method inbuilt in express to recognize the incoming Request Object as strings or arrays


**4. What does the /:id mean in a route?**


- The Route ID is a number which uniquely identifies the route. The name or title of a route is NOT unique. So if you want to refer to a specific route to mention a problem in an email, you better provide the Route ID.


**5. What is the difference beween PUT and PATCH?**

- The main difference between the PUT and PATCH method is that the PUT method uses the request URI to supply a modified version of the requested resource which replaces the original version of the resource, whereas the PATCH method supplies a set of instructions to modify the resource




**6. What does a 500 error status code mean?**

- The HyperText Transfer Protocol (HTTP) 500 Internal Server Error server error response code indicates that the server encountered an unexpected condition that prevented it from fulfilling the request. This error response is a generic “catch-all” response.

**7. What is the difference between a status 200 and a status 201**

- 201 Created  The most fitting for Create operations. This code should signal backend-side

- 200 OK - It’s the basic status code to tell the client everything went good. Since we don’t create endpoint accessible resource when creating an access token, we can use 200 as a status for that action.
