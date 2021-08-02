# APIs


## API Design Best Practices

#### 1. What does REST stand for?

- Representational state transfer.

#### 2. REST APIs are designed around a 
_2004_.

#### 3. What is an identifer of a resource? Give an example.

- It is URI, uniform resource identifier. 

#### 4. What are the most common HTTP verbs?


- The most common operations are GET, POST, PUT, PATCH, and DELETE.

#### 5. What should the URIs be based on?

- I'm not sure, but i think based on the data itself in API and the type of service also that provided by the API.

#### 6. Give an example of a good URl
- like : */customers/1/orders/* , if i need the customers and will make the URI makes sense to the data requested by the user. 

#### 7. What does it mean to have a ‘chatty’ web API? Is this a good or a bad thing?

- When you make the client makes many requests to get a small amuont of data for each request (based on organizing the data in your API), this will make a load on your server and you have to aviod that. for sure it is bad thing.

#### 8. What status code does a successful `GET` request return?
- Status code 200 

#### 9. What status code does an unsuccessful `GET` request return?
- Status code 404 

#### 10. What status code does a successful `POST` request return?
- Status code 201 

#### 11. What status code does a successful `DELETE` request return?
- Status code 204 
