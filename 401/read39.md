# [Kinesis](https://docs.amplify.aws/lib/analytics/getting-started/q/platform/android/)


## Getting started
- The **Analytics category** -> used to collect analytics data for your App.
- The Analytics category comes with built-in support for **Amazon Pinpoint** and **Amazon Kinesis** (Kinesis only available in the Amplify JavaScript library).

## Goal
To setup and configure your application with Amplify Analytics and record an analytics event.

## Prerequisites
- [Install and configure Amplify CLI](https://docs.amplify.aws/cli/start/install/)
- An Android application targeting Android API level 16 (Android 4.1) or above.
[project setup walkthrough](https://docs.amplify.aws/lib/project-setup/create-application/q/platform/android/)

## Set up Analytics backend
1. `amplify add analytics`
```
? Select an Analytics provider (Use arrow keys)
    `Amazon Pinpoint`
? Provide your pinpoint resource name:
    `yourPinpointResourceName`
? Apps need authorization to send analytics events. Do you want to allow guests and unauthenticated users to send analytics events? (we recommend you allow this when getting started)
    `Yes`
```

2. `amplify push`

## Install Amplify Libraries
- Inside `build.gradle (Module: app)`:
```
dependencies {
    // Add these lines in `dependencies`
    implementation 'com.amplifyframework:aws-analytics-pinpoint:1.24.0'
    implementation 'com.amplifyframework:aws-auth-cognito:1.24.0'
}
```

## Initialize Amplify Analytics


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

## Record events

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

## View Analytics console
`amplify console analytics`
