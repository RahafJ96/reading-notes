# [Kinesis](https://docs.amplify.aws/lib/analytics/getting-started/q/platform/android/)
* With Amazon Kinesis, you can ingest real-time data such as video, audio, application logs, website clickstreams, and IoT telemetry data for machine learning, analytics, and other applications. Amazon Kinesis enables you to process and analyze data as it arrives and respond instantly instead of having to wait until all your data is collected before the processing can begin.

### Set up Analytics backend

Run the following command in your project's root folder:
1. `amplify add analytics`

     amplify add analytics

     ? Select an Analytics provider (Use arrow keys)
     `Amazon Pinpoint`
     ? Provide your pinpoint resource name: 
     `yourPinpointResourceName`
     ? Apps need authorization to send analytics events. Do you want to allow guests and unauthenticated users to send analytics events? (we recommend you allow this when getting started) 
     `Yes`


2. `amplify push`


### Prerequisites
- [Install and configure Amplify CLI](https://docs.amplify.aws/cli/start/install/)
- An Android application targeting Android API level 16 (Android 4.1) or above.
[project setup walkthrough](https://docs.amplify.aws/lib/project-setup/create-application/q/platform/android/)

### Install Amplify Libraries
- Inside `build.gradle (Module: app)`:
```
dependencies {
    // Add these lines in `dependencies`
    implementation 'com.amplifyframework:aws-analytics-pinpoint:1.24.0'
    implementation 'com.amplifyframework:aws-auth-cognito:1.24.0'
}
```

### Initialize Amplify Analytics


- How the class should look like :
```
public class MyAmplifyApp extends Application {
    @Override
    public void onCreate() {
        super.onCreate();

        try {
            // Add these lines to add the AWSCognitoAuthPlugin and AWSPinpointAnalyticsPlugin plugins
            Amplify.addPlugin(new AWSCognitoAuthPlugin());
            Amplify.addPlugin(new AWSPinpointAnalyticsPlugin(this));
            Amplify.configure(getApplicationContext());

            Log.i("MyAmplifyApp", "Initialized Amplify");
        } catch (AmplifyException error) {
            Log.e("MyAmplifyApp", "Could not initialize Amplify", error);
        }
    }
}
```

#### Record events

```
AnalyticsEvent event = AnalyticsEvent.builder()
    .name("PasswordReset")
    .addProperty("Channel", "SMS")
    .addProperty("Successful", true)
    .addProperty("ProcessDuration", 792)
    .addProperty("UserAge", 120.3)
    .build();

Amplify.Analytics.recordEvent(event);
```

### View Analytics console
`amplify console analytics`
