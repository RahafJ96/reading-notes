# Application Fundamentals

* Android apps can be written using Kotlin, Java, and C++ languages.
* The Android SDK tools compile the code along with any data and resource files into an APK or an Android App Bundle
* Android package :  is an archive file with an .apk suffix, contains the contents of an Android app that are required at runtime and it is the file that Android-powered devices use to install the app.
* Android App Bundle : is an archive file with an .aab suffix, contains the contents of an Android app project including some additional metadata that is not required at runtime.
* Each Android app lives in its own security sandbox

<hr/>

## Android security features
- Each Android app, protected by the following Android security features:
1. The Android operating system is a multi-user Linux system in which each app is a different user.
2. By default, the system assigns each app a unique Linux user ID (the ID is used only by the system and is unknown to the app). The system sets permissions for all the files in an app so that only the user ID assigned to that app can access them.
3. Each process has its own virtual machine (VM), so an app's code runs in isolation from other apps.
4. By default, every app runs in its own Linux process. The Android system starts the process when any of the app's components need to be executed, and then shuts down the process when it's no longer needed or when the system must recover memory for other apps.

<hr/>

### The principle of least privilege

* That is, each app, by default, has access only to the components that it requires to do its work and no more.
* This creates a very secure environment in which an app cannot access parts of the system for which it is not given permission.

### The ways for an app to share data with other apps

* It's possible to arrange for two apps to share the same Linux user ID in which case they are able to access each other's files.
* To conserve system resources, apps with the same user ID can also arrange to run in the same Linux process and share the same VM.
* An app can request permission to access device data such as the device's location, camera, and Bluetooth connection.

<hr/>

## App components
### There are four different types of app components:

**1. Activities**
- Is the entry point for interacting with the user.
- It represents a single screen with a user interface. 

**2. Services**
- Is a general-purpose entry point for keeping an app running in the background for all kinds of reasons.
- It is a component that runs in the background to perform long-running operations or to perform work for remote processes.
- A service does not provide a user interface.

**3. Broadcast receivers**
- Is a component that enables the system to deliver events to the app outside of a regular user flow, allowing the app to respond to system-wide broadcast announcements.
- Because broadcast receivers are another well-defined entry into the app, the system can deliver broadcasts even to apps that aren't currently running. 

- A broadcast receiver is implemented as a subclass of BroadcastReceiver and each broadcast is delivered as an Intent object.

**4. Content providers**
- A content provider manages a shared set of app data that you can store in the file system, in a SQLite database, on the web, or on any other persistent storage location that your app can access. 
- Through the content provider, other apps can query or modify the data if the content provider allows it.

<hr/>

## Activating components
- Three of the four component types—activities, services, and broadcast receivers—are activated by an asynchronous message called an intent. 
- Intents bind individual components to each other at runtime. You can think of them as the messengers that request an action from other components, whether the component belongs to your app or another.
- An intent is created with an Intent object, which defines a message to activate either a specific component (explicit intent) or a specific type of component (implicit intent).


### There are separate methods for activating each type of component:

* You can start an activity or give it something new to do by passing an Intent to startActivity() or startActivityForResult()
* you can use the JobScheduler class to schedule actions. 
* earlier Android versions, you can start a service (or give new instructions to an ongoing service) by passing an Intent to startService(). You can bind to the service by passing an Intent to bindService().
* You can initiate a broadcast by passing an Intent to methods such as sendBroadcast(), sendOrderedBroadcast(), or sendStickyBroadcast().
* You can perform a query to a content provider by calling query() on a ContentResolver.

<hr/>

### The manifest file

* Before the Android system can start an app component, the system must know that the component exists by reading the app's manifest file, AndroidManifest.xml.
* The manifest does a number of things in addition to declaring the app's components, such as the following:

1. Identifies any user permissions the app requires, such as Internet access or read-access to the user's contacts.
2. Declares the minimum API Level required by the app, based on which APIs the app uses.
3. Declares hardware and software features used or required by the app, such as a camera, bluetooth services, or a multitouch screen.
4. Declares API libraries the app needs to be linked against (other than the Android framework APIs), such as the Google Maps library.

<hr/>

## App resources
- For every resource that you include in your Android project, the SDK build tools define a unique integer ID, which you can use to reference the resource from your app code or from other resources defined in XML.

- For example, if your app contains an image file named logo.png (saved in the res/drawable/ directory), the SDK tools generate a resource ID named R.drawable.logo. This ID maps to an app-specific integer, which you can use to reference the image and insert it in your user interface.