# Notifications

* Amazon SNS is a highly available, durable, secure, fully managed pub/sub messaging service that enables you to decouple microservices, distributed systems, and event-driven serverless applications. Amazon SNS provides topics for high-throughput, push-based, many-to-many messaging.

**Benefits and features**

1. Reliably deliver messages with durability

2. Automatically scale your workload

3. Keep messages private and secure

4. Simplify your architecture with Message Filtering

**[Prerequisites of SNS](https://aws.amazon.com/sns/getting-started/)**
### To get start with Simple Notification Service (SNS) :

* Step 1: Create a topic

* Step 2: Create a subscription to the topic

* Step 3: Publish a message to the topic

* Step 4: Delete the subscription and topic

## [SNS with Amplify and Firebase](https://docs.amplify.aws/)

### Usage of SNS(adding Push Notifications into their mobile app) with amplify:

1. `Asynchronous actions`
2. `Scheduled reminders`
3. `Instant messaging`

---
## [How ro create platform application in Amazon Simple Notification Service (Amazon SNS) to send push notifications to Android devices.](https://aws.amazon.com/premiumsupport/knowledge-center/create-android-push-messaging-sns/) 

### Add your project to Firebase
- To create your Android platform application in Amazon SNS, you must have credentials from Firebase Cloud Messaging (FCM).

### Copy your FCM project's API key

1. In the Firebase console, choose your project.

2. Choose Project settings.

3. Choose Cloud Messaging.

4. Copy your FCM project's API key to your clipboard.

### Create a platform application in Amazon SNS
1. Open the Amazon SNS console.

2. Choose Mobile. Then, choose Push notifications.

3. Choose Create platform application.

4. On the Create platform application page, under Details, do the following:
    - Enter the name of your application.
    - Choose Firebase Cloud Messaging (FCM).
    - Enter the server key that you copied earlier, Under Firebase Cloud Messaging Credentials

5. (Optional) Set up event notifications and delivery status logging.

6. Choose Create platform application.



