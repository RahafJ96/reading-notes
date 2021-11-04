# Espresso

## [Espresso](https://developer.android.com/training/testing/espresso) 
- Use Espresso to write concise, beautiful, and reliable Android UI tests.

- Espresso tests run optimally fast! It lets you leave your waits, syncs, sleeps, and polls behind while it manipulates and asserts on the application UI when it is at rest.

### Target audience
- Espresso is targeted at developers. 
- While it can be used for black-box testing, Espresso’s full power is unlocked by those who are familiar with the codebase under test.

### Synchronization capabilities
- Each time your test invokes onView(), Espresso waits to perform the corresponding UI action or assertion until the following synchronization conditions are met:

- The message queue is empty.
- There are no instances of AsyncTask currently executing a task.
- All developer-defined idling resources are idle.


### Packages
- **espresso-core** - Contains core and basic View matchers, actions, and assertions. See Basics and Recipes.
- **espresso-web** - Contains resources for WebView support.
- **espresso-idling-resource** - Espresso's mechanism for synchronization with background jobs.
- **espresso-contrib** - External contributions that contain DatePicker, RecyclerView and Drawer actions, accessibility checks, and CountingIdlingResource.
- **espresso-intents** - Extension to validate and stub intents for hermetic testing.
- **espresso-remote** - Location of Espresso's multi-process functionality.
<hr/>

## [Ridiculous superpower: the Espresso Test Recorder](https://developer.android.com/studio/test/espresso-test-recorder) 

- **The Espresso Test Recorder tool** lets you create **UI tests** for your app without writing any test code. 

- The Espresso API encourages you to create concise and reliable UI tests based on user actions. 

## Turn off animations on your test device
- Before using Espresso Test Recorder, make sure you turn off animations on your test device to prevent unexpected results.

## Record an Espresso test
- **Espresso tests consist of two primary components:** 
 UI interactions and assertions on View elements. 
- Assertions verify the existence or contents of visual elements on the screen.
> For example, an Espresso test for the Notes testing app might include UI interactions for clicking on a button and writing a new note but would use assertions to verify the existence of the button and the contents of the note.


### Record UI interactions
- **To start recording a test with Espresso Test Recorder, proceed as follows:**

1. Click Run > Record Espresso Test.
2. In the Select Deployment Target window, choose the device on which you want to record the test.
3. Espresso Test Recorder triggers a build of your project, and the app must install and launch before Espresso Test Recorder allows you to interact with it.

### Add assertions to verify UI elements
- **Assertions verify the existence or contents of a View element through three main types:**

1. text is: Checks the text content of the selected View element
2. exists: Checks that the View element is present in the current View hierarchy visible on the screen
3. does not exist: Checks that the View element is not present in the current View hierarchy

