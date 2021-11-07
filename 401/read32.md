# Serverless and Amplify

## [Intro to Serverless](https://hackernoon.com/what-is-serverless-architecture-what-are-its-pros-and-cons-cc4b804022e9)


### So, What is Serverless?
- Serverless is a cloud computing execution model where the cloud provider dynamically manages the allocation and provisioning of servers.

`Serverless applications are event-driven cloud-based systems where application development rely solely on a combination of third-party services, client-side logic and cloud-hosted remote procedure calls (Functions as a Service).`

- Most of the cloud providers have invested heavily in serverless and thats a lot of money.
- **Here are some of the currently available cloud services:**

1. ### Traditional vs. Serverless Architecture

![Traditional vs. Serverless Architecture](https://hackernoon.com/hn-images/1*x_v5NRC3TTMt1MaYl1gMUg.jpeg) 

- For years your applications have run on servers which you had to patch, update, and continuously look after late nights and early mornings due to all the unimaginable errors that broke your production.
- Serverless tends to be unlike that, you no longer need to worry about the underlying servers. Reason being, they are not managed by you anymore and with management out of the picture the responsibility falls on the Cloud vendors. 

- **Pricing**
Serverless is reduces cost.


- **Networking**
The downside is that Serverless functions are accessed only as private APIs. To access these you must set up an API Gateway. This doesn’t have an impact on your pricing or process, but it means you cannot directly access them through the usual IP.

The winner here is Traditional Architecture.

- **3rd Party Dependencies**
Most, if not all of your projects have external dependencies, they rely on libraries that are not built into the language or framework you use. 

The winner here is based on the context. For simple applications with few dependencies, Serverless is the winner; for anything more complex, Traditional Architecture is the winner.

- **Environments**
Setting up different environments for Serverless is as easy as setting up a single environment. 

- **Timeout**
With Serverless, there’s a hard 300-second timeout limit.
Too complex or long-running functions aren’t good for Serverless.
A hard limit on this time makes Serverless unusable for applications that have variable execution times, and for certain services which require information from an external source.

The winner here is Traditional Architecture.

- **Scale**
Scaling process for Serverless is automatic and seamless, so there is a lack of control or entire absence of control. 

It’s a tie between Serverless and Traditional Architecture.

2. ### Functions as a Service (FaaS)
**FaaS** is an implementation of Serverless architectures where engineers can deploy an individual function or a piece of business logic.

- **Principles of FaaS:**
- Complete management of servers
- Invocation based billing
- Event-driven and instantaneously scalable

3. ### The Serverless App
A Serverless app consists of a web server, Lambda functions (FaaS), security token service (STS), user authentication and database.

![The Serverless App](https://hackernoon.com/hn-images/1*TIrjN7EjLUVJmJ6YvHR7Dg.png) 

- **Client Application** —  client side UI.

- **Web Server** — Amazon S3 provides a robust and simple web server. All of the static HTML, CSS and JS files for our application can be served from S3.

- **Lambda functions (FaaS)** — They are the key enablers in Serverless architecture. Some popular examples of FaaS are AWS Lambda, Google Cloud Functions and Microsoft Azure Functions. 

- **Security Token Service (STS)** — generates temporary AWS credentials (API key and secret key) for users of the application. These temporary credentials are used by the client application to invoke the AWS API (and thus invoke Lambda).

- **User Authentication** — AWS Cognito is an identity service which is integrated with AWS Lambda. 

- **Database** — AWS DynamoDB provides a fully managed NoSQL database. DynamoDB is not essential for a serverless application but is used as an example here.


## [AWS Amplify Kool-Aid](https://aws.amazon.com/amplify/)

- AWS Amplify is a set of tools and services that can be used together or on their own, to help front-end web and mobile developers build scalable full stack applications, powered by AWS.

- Amplify supports popular web frameworks including JavaScript, React, Angular, Vue, Next.js, and mobile platforms including Android, iOS, React Native, Ionic, Flutter. Get to market faster with AWS Amplify.

### Benefits
- Configure backends fast.
- Seamlessly connect frontends.
- Deploy in a few clicks.
- Easily manage content.

## [GraphQL Intro](https://docs.amplify.aws/cli/graphql-transformer/overview/)
- Helps you quickly create backends for your web and mobile applications on AWS. 
- With the GraphQL Transform, you define your application's data model using the GraphQL Schema Definition Language (SDL) and the library handles converting your SDL definition into a set of fully descriptive AWS CloudFormation templates that implement your data model.

- **For example:**
```
type Blog @model {
  id: ID!
  name: String!
  posts: [Post] @connection(name: "BlogPosts")
}
ype Post @model {
  id: ID!
  title: String!
  blog: Blog @connection(name: "BlogPosts")
  comments: [Comment] @connection(name: "PostComments")
}
type Comment @model {
  id: ID!
  content: String
  post: Post @connection(name: "PostComments")
}
```

### Create a GraphQL API

1. `amplify init`
2. `amplify add api`
- Select GraphQL
- When asked if you have a schema, say No
- Select one of the default samples; you can change this later
- Choose to edit the schema and it will open the new schema.graphql in your editor
3. `amplify push`