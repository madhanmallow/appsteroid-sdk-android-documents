# AppSteroid Custom Message API

Last updated 2014-10-08

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
                this);
        }
    
        // Implement the onCustomMessage method
        @Override
        public void onCustomMessage(AppSteroidGcmMessage fresviiGcmMessage) {
            // TODO: Do your stuff when the custom message is received
        }
        


---  

## Classes

|Class|Description|
|---|---|
|[CustomMessageAccess](#com.fresvii.server.access.CustomMessageAccess)|Provides access to Fresvii Server's Leaderboard API.|
|[GetCustomMessagesCallback](#com.fresvii.server.access.callbacks.custommessage.GetCustomMessagesCallback)|Callback interface to handle [CustomMessageAccess.getCustomMessages()](#com_fresvii_server_access_CustomMessageAccess_void_getCustomMessages_int_GetCustomMessagesCallback) results.|
|[PostCustomMessageCallback](#com.fresvii.server.access.callbacks.custommessage.PostCustomMessageCallback)|Callback interface to handle [CustomMessageAccess.postCustomMessage()](#com_fresvii_server_access_CustomMessageAccess_void_postCustomMessage_String_String_Map_Map_String_String_Boolean_Boolean_PostCustomMessageCallback) results.|



---  

## <a name="com.fresvii.server.access.CustomMessageAccess"> Class CustomMessageAccess </a>

```
public class CustomMessageAccess extends Object
```

**Hierarchy:**  

```
java.lang.Object  
    com.fresvii.server.access.CustomMessageAccess
```

**Description:**  
Provides access to Fresvii Server's Leaderboard API.  Can be used to retrieve or manipulate leaderboards, rankings, and scores.

**Author:**  
Marcus Froeschl

**Version:**  
1.0

**Since:**  
2014-08-19


### Method Summary

|Method|Description|
|---|---|
|[public static void getCustomMessages(GetCustomMessagesCallback callback)](#com_fresvii_server_access_CustomMessageAccess_void_getCustomMessages_GetCustomMessagesCallback)|Retrieves a list of custom messages from the initial page.|
|[public static void getCustomMessages(int page, GetCustomMessagesCallback callback)](#com_fresvii_server_access_CustomMessageAccess_void_getCustomMessages_int_GetCustomMessagesCallback)|Retrieves a list of custom messages from the specified page.|
|[public static void postCustomMessage(String channelName, String action, Map channelParams, Map params, String subject, String sound, Boolean apnsEnabled, Boolean gcmEnabled, PostCustomMessageCallback callback)](#com_fresvii_server_access_CustomMessageAccess_void_postCustomMessage_String_String_Map_Map_String_String_Boolean_Boolean_PostCustomMessageCallback)|Posts a custom message to a channel.|



### Method Detail
 


## <a name="com_fresvii_server_access_CustomMessageAccess_void_getCustomMessages_GetCustomMessagesCallback"> getCustomMessages </a>

```
public static void getCustomMessages(GetCustomMessagesCallback callback)
```

Retrieves a list of custom messages from the initial page.

#### Parameters

|Parameter|Description|
|---|---|
|[GetCustomMessagesCallback](#com.fresvii.server.access.callbacks.custommessage.GetCustomMessagesCallback) callback|[Callback](#com.fresvii.server.access.callbacks.custommessage.GetCustomMessagesCallback) to be informed about the result of the operation.|



## <a name="com_fresvii_server_access_CustomMessageAccess_void_getCustomMessages_int_GetCustomMessagesCallback"> getCustomMessages </a>

```
public static void getCustomMessages(int page,  
                                     GetCustomMessagesCallback callback)
```

Retrieves a list of custom messages from the specified page.

#### Parameters

|Parameter|Description|
|---|---|
|int page|Page offset.|
|[GetCustomMessagesCallback](#com.fresvii.server.access.callbacks.custommessage.GetCustomMessagesCallback) callback|[Callback](#com.fresvii.server.access.callbacks.custommessage.GetCustomMessagesCallback) to be informed about the result of the operation.|



## <a name="com_fresvii_server_access_CustomMessageAccess_void_postCustomMessage_String_String_Map_Map_String_String_Boolean_Boolean_PostCustomMessageCallback"> postCustomMessage </a>

```
public static void postCustomMessage(String channelName,  
                                     String action,  
                                     Map channelParams,  
                                     Map params,  
                                     String subject,  
                                     String sound,  
                                     Boolean apnsEnabled,  
                                     Boolean gcmEnabled,  
                                     PostCustomMessageCallback callback)
```

Posts a custom message to a channel.

#### Parameters

|Parameter|Description|
|---|---|
|String channelName|Name of the channel you created in the Fresvii Console.|
|String action|Name of the action. Only characters [a-zA-Z] are allowed.|
|Map channelParams|Optional parameters used to find matching users. This data is specific to the channel you created in the Fresvii Console.|
|Map params|Optional data that will be sent to matching users.|
|String subject|Optional subject of the message.|
|String sound|Optional sound file to be played when message is received.|
|Boolean apnsEnabled|Optional. Specifies whether to send this message via APNS. Default is true.|
|Boolean gcmEnabled|Optional. Specifies whether to send this message via GCM. Default is true.|
|[PostCustomMessageCallback](#com.fresvii.server.access.callbacks.custommessage.PostCustomMessageCallback) callback|[Callback](#com.fresvii.server.access.callbacks.custommessage.PostCustomMessageCallback) to be informed about the result of the operation.|




---  

## <a name="com.fresvii.server.access.callbacks.custommessage.GetCustomMessagesCallback"> Interface GetCustomMessagesCallback </a>

```
public interface GetCustomMessagesCallback implements FailureCallback
```

**Hierarchy:**  

```
com.fresvii.server.access.callbacks.custommessage.GetCustomMessagesCallback
```

**Description:**  
Callback interface to handle [CustomMessageAccess.getCustomMessages()](#com_fresvii_server_access_CustomMessageAccess_void_getCustomMessages_int_GetCustomMessagesCallback) results.

**Author:**  
Marcus Froeschl

**Version:**  
1.0




### Method Summary

|Method|Description|
|---|---|
|[public void onSuccess(AppSteroidListMetaInfo metaInfo, List messages)](#com_fresvii_server_access_callbacks_custommessage_GetCustomMessagesCallback_void_onSuccess_AppSteroidListMetaInfo_List)|Callback invoked when operation succeeds.|



### Method Detail
 


## <a name="com_fresvii_server_access_callbacks_custommessage_GetCustomMessagesCallback_void_onSuccess_AppSteroidListMetaInfo_List"> onSuccess </a>

```
public void onSuccess(AppSteroidListMetaInfo metaInfo,  
                      List messages)
```

Callback invoked when operation succeeds.

#### Parameters

|Parameter|Description|
|---|---|
|[AppSteroidListMetaInfo](AndroidSDK.md#com.fresvii.components.AppSteroidListMetaInfo) metaInfo|List meta information.|
|List messages|List of leaderboards retrieved.|




---  

## <a name="com.fresvii.server.access.callbacks.custommessage.PostCustomMessageCallback"> Interface PostCustomMessageCallback </a>

```
public interface PostCustomMessageCallback implements FailureCallback
```

**Hierarchy:**  

```
com.fresvii.server.access.callbacks.custommessage.PostCustomMessageCallback
```

**Description:**  
Callback interface to handle [CustomMessageAccess.postCustomMessage()](#com_fresvii_server_access_CustomMessageAccess_void_postCustomMessage_String_String_Map_Map_String_String_Boolean_Boolean_PostCustomMessageCallback) results.

**Author:**  
Marcus Froeschl

**Version:**  
1.0




### Method Summary

|Method|Description|
|---|---|
|[public void onSuccess(AppSteroidGcmMessage message)](#com_fresvii_server_access_callbacks_custommessage_PostCustomMessageCallback_void_onSuccess_AppSteroidGcmMessage)|Callback invoked when operation succeeds.|



### Method Detail
 


## <a name="com_fresvii_server_access_callbacks_custommessage_PostCustomMessageCallback_void_onSuccess_AppSteroidGcmMessage"> onSuccess </a>

```
public void onSuccess(AppSteroidGcmMessage message)
```

Callback invoked when operation succeeds.

#### Parameters

|Parameter|Description|
|---|---|
|[AppSteroidGcmMessage](GcmClient.md#com.fresvii.gcm.AppSteroidGcmMessage) message|The score that was posted.|



