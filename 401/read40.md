# Intent Filters

## Allowing Other Apps to Start Your Activity

To allow other apps to start your activity in this way, you need to add an `<intent-filter>` element in your manifest file for the corresponding `<activity>` element.

**Add an Intent Filter**
- *Action*
A string naming the action to perform. Usually one of the platform-defined values such as `ACTION_SEND` or `ACTION_VIEW`.
Specify this in your intent filter with the `<action>` element. 
- *Data*
A description of the data associated with the intent.
Specify this in your intent filter with the `<data>` element. 
- *Category*
There are several different categories supported by the system, but most are rarely used. 
Specify this in your intent filter with the `<category>` element.

For example, here's an activity with an intent filter that handles the `ACTION_SEND` intent when the data type is either text or an image:

     <activity android:name="ShareActivity">
      <intent-filter>
        <action android:name="android.intent.action.SEND"/>
        <category android:name="android.intent.category.DEFAULT"/>
        <data android:mimeType="text/plain"/>
        <data android:mimeType="image/*"/>
      </intent-filter>
     </activity>

For example, suppose your activity handles both text and images for both the `ACTION_SEND` and `ACTION_SENDTO` intents.  

     <activity android:name="ShareActivity">
      <!-- filter for sending text; accepts SENDTO action with sms URI schemes -->
       <intent-filter>
        <action android:name="android.intent.action.SENDTO"/>
        <category android:name="android.intent.category.DEFAULT"/>
        <data android:scheme="sms" />
        <data android:scheme="smsto" />
      </intent-filter>
      <!-- filter for sending text or images; accepts SEND action and text or image data -->
      <intent-filter>
        <action android:name="android.intent.action.SEND"/>
        <category android:name="android.intent.category.DEFAULT"/>
        <data android:mimeType="image/*"/>
        <data android:mimeType="text/plain"/>
       </intent-filter>
     </activity>

## Handle the Intent in Your Activity
* Call `getIntent()` to retrieve the Intent that started the activity. For example:

      @Override
      protected void onCreate(Bundle savedInstanceState) {
       super.onCreate(savedInstanceState);

       setContentView(R.layout.main);

       // Get the intent that started this activity
       Intent intent = getIntent();
       Uri data = intent.getData();

       // Figure out what to do based on the intent type
       if (intent.getType().indexOf("image/") != -1) {
        // Handle intents with image data ...
       } else if (intent.getType().equals("text/plain")) {
        // Handle intents with text ...
      }
     }

## Return a Result
* Call `setResult()` to specify the result code and result Intent. When your operation is done and the user should return to the original activity, call `finish()` to close (and destroy) your activity. For example:

      // Create intent to deliver some kind of result data
      Intent result = new Intent("com.example.RESULT_ACTION", Uri.parse("content://result_uri"));
      setResult(Activity.RESULT_OK, result);
      finish();
