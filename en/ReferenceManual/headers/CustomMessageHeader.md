# AppSteroid Custom Message API

Last updated %LAST_UPDATED%

-------------------------


## Introduction

AppSteroid Custom Message API can be used to send user-defined push notifications (APNS or GCM) to channels of users. Channels can be defined in the Fresvii Console for your application as a set of conditions. The push notifications will then be sent to the users matching these conditions.


## How to send custom messages

### 1. Set up a channel

Set up a channel in the [Fresvii Console](https://fresvii.com)


### 2. Post a custom message

Invoke the [postCustomMessage()](#com_fresvii_server_access_CustomMessageAccess_void_postCustomMessage_String_String_Map_Map_String_String_Boolean_Boolean_PostCustomMessageCallback) API for your channel and pass in a set of conditions and the data to be sent.

    // Specify the parameters that will be used to find matching users in the channel. 
    // This data is specific to the channel you created in the Fresvii Console.
    // The following is just an arbitrary example.
    HashMap<String, String> channelParams = new HashMap<String, String>();
    channelParams.put("bind_name", "A user name");  

    // Specify the data (key value pairs) that will be sent to matching users. 
    // This data is specific to your application.
    // The following is just an arbitrary example.
    HashMap<String, String> params = new HashMap<String, String>();
    params.put("my_key", "my_value");

    CustomMessageAccess.postCustomMessage(
            YOUR_CHANNEL_NAME,  // name of the channel you created in the Fresvii Console
            YOUR_ACTION,  // Name of the action
            channelParams,  // The parameters used to find matching users. 
            params,  // The data that will be sent to matching users
            YOUR_SUBJECT,  // optional subject
            YOUR_SOUND_FILE,  // optional sound file
            true,  // whether to send custom message as APNS
            true,  // whether to send custom message as GCM
            new PostCustomMessageCallback() {
                @Override
                public void onFailure(Throwable error) {
                    // TODO: Handle error
                }
                
                @Override
                public void onSuccess(AppSteroidGcmMessage message) {
                    // TODO: Handle success
                }
            });


## How to receive custom messages

### 1. Register a CustomNotificationListener

Register a  [CustomNotificationListener](GcmClient.md#com.fresvii.gcm.CustomNotificationListener) to the [GcmClient](GcmClient.md#com.fresvii.gcm.GcmClient).

    public class MyGame extends Activity implements CustomNotificationListener {
        @Override
        protected void onCreate(Bundle savedInstanceState) {
            // Any application must call AppSteroid.start() in order to work with the AppSteroid
            AppSteroid.start(
            	    super.getApplicationContext(),
            	    MY_APP_ID,
            	    MY_APP_SECRET,
            	    MY_APP_NAME,
            	    MY_GCM_SENDER_ID);
    
            ...
            
            // Add a CustomNotificationListener to the GcmClient 
            // The listener in this example will listen for any action for "custom_message" resources.
            GcmClient.getInstance().addCustomNotificationListener(
                GcmClient.RESOURCE_CUSTOM_MESSAGE, 
                GcmClient.ACTION_ANY,
                this);
        }
        
        @Override
        protected void onDestroy() {
            // Don't forget to remove the listener
            GcmClient.getInstance().removeCustomNotificationListener(
                GcmClient.RESOURCE_CUSTOM_MESSAGE, 
                GcmClient.ACTION_ANY,
                this);        }
    
        // Implement the onCustomMessage method
        @Override
        public void onCustomMessage(AppSteroidGcmMessage fresviiGcmMessage) {
            // TODO: Do your stuff when the custom message is received
        }
        
