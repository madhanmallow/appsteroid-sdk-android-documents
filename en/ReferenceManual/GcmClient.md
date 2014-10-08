
# AppSteroid GcmClient API

Last updated 2014-10-08

-------------------------

## Introduction

AppSteroid GcmClient API can be used to receive GCM Notifications of events such as incoming text messages, new forum messages, and many more.

The [AppSteroid.start()](AndroidSDK.md#com_fresvii_AppSteroid_void_start_Context_String_String_String_String) method will automatically start the GcmClient any time the user logs in.
So in most cases, you won't have to worry about working with the GcmClient class, unless you wish to perform a specific task, such as registering a GCM NotificationListener.
Just continue reading the document on [Receiving GCM Notifications](../GetStarted/GcmNotifications.md) instead.


---  

## Classes

|Class|Description|
|---|---|
|[GcmClient](#com.fresvii.gcm.GcmClient)|The GcmClient is used to register for and handle GMC notifications.|
|[GcmClient.RegisterAndAddDeviceTokenCallback](#com.fresvii.gcm.GcmClient.RegisterAndAddDeviceTokenCallback)|Callback interface to handle [GcmClient.registerAndAddDeviceToken()](#com_fresvii_gcm_GcmClient_void_registerAndAddDeviceToken_String_GcmClient_RegisterAndAddDeviceTokenCallback) results.|
|[GcmClient.PauseCallback](#com.fresvii.gcm.GcmClient.PauseCallback)|Callback interface to handle [GcmClient.pause()](#com_fresvii_gcm_GcmClient_void_pause_GcmClient_PauseCallback) results.|
|[GcmClient.ResumeCallback](#com.fresvii.gcm.GcmClient.ResumeCallback)|Callback interface to handle [GcmClient.resume()](#com_fresvii_gcm_GcmClient_void_resume_GcmClient_ResumeCallback) results.|
|[AppSteroidGcmMessage](#com.fresvii.gcm.AppSteroidGcmMessage)|Represents a Fresvii GCM Message|
|[AppSteroidGcmMessage.MessageType](#com.fresvii.gcm.AppSteroidGcmMessage.MessageType)|Known GCM message types which will receive special treatment.|
|[AppSteroidGcmMessage.Resource](#com.fresvii.gcm.AppSteroidGcmMessage.Resource)|GCM message resources specified in Fresvii Push Specifications|
|[AppSteroidGcmMessage.Action](#com.fresvii.gcm.AppSteroidGcmMessage.Action)|GCM message actions specified in Fresvii Push Specifications|
|[GroupChatNotificationListener](#com.fresvii.gcm.GroupChatNotificationListener)|Application may implement this interface to handle group GCM notifications.|
|[FriendRequestNotificationListener](#com.fresvii.gcm.FriendRequestNotificationListener)|Application may implement this interface to handle friend request GCM notifications.|
|[ForumNotificationListener](#com.fresvii.gcm.ForumNotificationListener)|Application may implement this interface to handle forum GCM notifications.|
|[VoiceChatNotificationListener](#com.fresvii.gcm.VoiceChatNotificationListener)|Application may implement this interface to handle VoiceChat GCM notifications.|
|[MatchmakingNotificationListener](#com.fresvii.gcm.MatchmakingNotificationListener)|Application may implement this interface to handle friend request GCM notifications.|
|[CustomNotificationListener](#com.fresvii.gcm.CustomNotificationListener)|Application may implement this interface to handle custom GCM notifications.|
|[NotificationAccess](#com.fresvii.server.access.NotificationAccess)|Provides access to Fresvii Server's Notification API.|
|[AddDeviceTokenCallback](#com.fresvii.server.access.callbacks.notification.AddDeviceTokenCallback)|Callback interface to handle NotificationAccess.addDeviceToken() results.|
|[DeleteDeviceTokenCallback](#com.fresvii.server.access.callbacks.notification.DeleteDeviceTokenCallback)|Callback interface to handle NotificationAccess.deleteDeviceToken() results.|



---  

## <a name="com.fresvii.gcm.GcmClient"> Class GcmClient </a>

```
public class GcmClient extends Object implements AccountAccess.UserAuthEventListener
```

**Hierarchy:**  

```
java.lang.Object  
    com.fresvii.gcm.GcmClient
```

**Description:**  
The GcmClient is used to register for and handle GMC notifications.  If you wish to receive GCM notifications, e.g. for GroupChat, Forum updates etc. in your application,   you will have to properly start the GcmClient.

**Author:**  
Tetsuro Higuchi, Marcus Froeschl

**Version:**  
1.0

**Since:**  
2014-05-27


### Field Summary

|Field|Description|
|---|---|
|ACTION_ANY|If you specify this action when registering a CustomNotificationListener, it indicates that you wish to listen for any action.|
|RESOURCE_ANY|If you specify this resource when registering a CustomNotificationListener, it indicates that you wish to listen for any resource.|
|RESOURCE_CUSTOM_MESSAGE|If you specify this resource when registering a CustomNotificationListener, it indicates that you wish to listen for resources of the type "custom_message".|



### Method Summary

|Method|Description|
|---|---|
|[public void addCustomNotificationListener(String resource, String action, CustomNotificationListener listener)](#com_fresvii_gcm_GcmClient_void_addCustomNotificationListener_String_String_CustomNotificationListener)|Application can add a [CustomNotificationListener](#com.fresvii.gcm.CustomNotificationListener) to be informed about custom GCM message notifications.|
|[public void addForumNotificationListener(ForumNotificationListener listener)](#com_fresvii_gcm_GcmClient_void_addForumNotificationListener_ForumNotificationListener)|Application can add a [ForumNotificationListener](#com.fresvii.gcm.ForumNotificationListener) to be informed about custom GCM message notifications.|
|[public void addFriendRequestNotificationListener(FriendRequestNotificationListener listener)](#com_fresvii_gcm_GcmClient_void_addFriendRequestNotificationListener_FriendRequestNotificationListener)|Application can add a [FriendRequestNotificationListener](#com.fresvii.gcm.FriendRequestNotificationListener) to be informed about custom GCM message notifications.|
|[public void addGroupChatNotificationListener(GroupChatNotificationListener listener)](#com_fresvii_gcm_GcmClient_void_addGroupChatNotificationListener_GroupChatNotificationListener)|Application can add a [GroupChatNotificationListener](#com.fresvii.gcm.GroupChatNotificationListener) to be informed about custom GCM message notifications.|
|[public void addMatchmakingNotificationListener(MatchmakingNotificationListener listener)](#com_fresvii_gcm_GcmClient_void_addMatchmakingNotificationListener_MatchmakingNotificationListener)|Application can add a [MatchmakingNotificationListener](#com.fresvii.gcm.MatchmakingNotificationListener) to be informed about Matchmaking GCM message notifications.|
|[public void addVoiceChatNotificationListener(VoiceChatNotificationListener listener)](#com_fresvii_gcm_GcmClient_void_addVoiceChatNotificationListener_VoiceChatNotificationListener)|Application can add a [VoiceChatNotificationListener](#com.fresvii.gcm.VoiceChatNotificationListener) to be informed about VoiceChat GCM message notifications.|
|[public static GcmClient getInstance()](#com_fresvii_gcm_GcmClient_com_fresvii_gcm_GcmClient_getInstance_)|Retrieves the instance of the singleton object. Use this to access the GcmClient.|
|[public void initialize()](#com_fresvii_gcm_GcmClient_void_initialize_)|Initializes the GcmClient.|
|[public void pause(GcmClient.PauseCallback callback)](#com_fresvii_gcm_GcmClient_void_pause_GcmClient_PauseCallback)|Call this method if you no longer wish to receive any GCM notifications.|
|[public void registerAndAddDeviceToken(String gcmSenderId, GcmClient.RegisterAndAddDeviceTokenCallback callback)](#com_fresvii_gcm_GcmClient_void_registerAndAddDeviceToken_String_GcmClient_RegisterAndAddDeviceTokenCallback)|Registers this device for GCM service, |
|[public void removeCustomNotificationListener(String resource, String action, CustomNotificationListener listener)](#com_fresvii_gcm_GcmClient_void_removeCustomNotificationListener_String_String_CustomNotificationListener)|Removes a [CustomNotificationListener](#com.fresvii.gcm.CustomNotificationListener).|
|[public void removeForumNotificationListener(ForumNotificationListener listener)](#com_fresvii_gcm_GcmClient_void_removeForumNotificationListener_ForumNotificationListener)|Removes a [ForumNotificationListener](#com.fresvii.gcm.ForumNotificationListener).|
|[public void removeFriendRequestNotificationListener(FriendRequestNotificationListener listener)](#com_fresvii_gcm_GcmClient_void_removeFriendRequestNotificationListener_FriendRequestNotificationListener)|Removes a [CustomNotificationListener](#com.fresvii.gcm.CustomNotificationListener).|
|[public void removeGroupChatNotificationListener(GroupChatNotificationListener listener)](#com_fresvii_gcm_GcmClient_void_removeGroupChatNotificationListener_GroupChatNotificationListener)|Removes a [GroupChatNotificationListener](#com.fresvii.gcm.GroupChatNotificationListener).|
|[public void removeMatchmakingNotificationListener(MatchmakingNotificationListener listener)](#com_fresvii_gcm_GcmClient_void_removeMatchmakingNotificationListener_MatchmakingNotificationListener)|Removes a [MatchmakingNotificationListener](#com.fresvii.gcm.MatchmakingNotificationListener).|
|[public void removeVoiceChatNotificationListener(VoiceChatNotificationListener listener)](#com_fresvii_gcm_GcmClient_void_removeVoiceChatNotificationListener_VoiceChatNotificationListener)|Removes a [VoiceChatNotificationListener](#com.fresvii.gcm.VoiceChatNotificationListener).|
|[public void resume(GcmClient.ResumeCallback callback)](#com_fresvii_gcm_GcmClient_void_resume_GcmClient_ResumeCallback)|Call this method if you wish to resume receiving GCM notifications after you paused them.|



### Method Detail
 


## <a name="com_fresvii_gcm_GcmClient_void_addCustomNotificationListener_String_String_CustomNotificationListener"> addCustomNotificationListener </a>

```
public void addCustomNotificationListener(String resource,  
                                          String action,  
                                          CustomNotificationListener listener)
```

Application can add a [CustomNotificationListener](#com.fresvii.gcm.CustomNotificationListener) to be informed about custom GCM message notifications.

#### Parameters

|Parameter|Description|
|---|---|
|String resource|The resource for which we should be listening for. "*" means any resource.|
|String action|The resource for which we should be listening for. "*" means any action.|
|[CustomNotificationListener](#com.fresvii.gcm.CustomNotificationListener) listener|[CustomNotificationListener](#com.fresvii.gcm.CustomNotificationListener).|



## <a name="com_fresvii_gcm_GcmClient_void_addForumNotificationListener_ForumNotificationListener"> addForumNotificationListener </a>

```
public void addForumNotificationListener(ForumNotificationListener listener)
```

Application can add a [ForumNotificationListener](#com.fresvii.gcm.ForumNotificationListener) to be informed about custom GCM message notifications.

#### Parameters

|Parameter|Description|
|---|---|
|[ForumNotificationListener](#com.fresvii.gcm.ForumNotificationListener) listener|[ForumNotificationListener](#com.fresvii.gcm.ForumNotificationListener).|



## <a name="com_fresvii_gcm_GcmClient_void_addFriendRequestNotificationListener_FriendRequestNotificationListener"> addFriendRequestNotificationListener </a>

```
public void addFriendRequestNotificationListener(FriendRequestNotificationListener listener)
```

Application can add a [FriendRequestNotificationListener](#com.fresvii.gcm.FriendRequestNotificationListener) to be informed about custom GCM message notifications.

#### Parameters

|Parameter|Description|
|---|---|
|[FriendRequestNotificationListener](#com.fresvii.gcm.FriendRequestNotificationListener) listener|[FriendRequestNotificationListener](#com.fresvii.gcm.FriendRequestNotificationListener).|



## <a name="com_fresvii_gcm_GcmClient_void_addGroupChatNotificationListener_GroupChatNotificationListener"> addGroupChatNotificationListener </a>

```
public void addGroupChatNotificationListener(GroupChatNotificationListener listener)
```

Application can add a [GroupChatNotificationListener](#com.fresvii.gcm.GroupChatNotificationListener) to be informed about custom GCM message notifications.

#### Parameters

|Parameter|Description|
|---|---|
|[GroupChatNotificationListener](#com.fresvii.gcm.GroupChatNotificationListener) listener|[GroupChatNotificationListener](#com.fresvii.gcm.GroupChatNotificationListener).|



## <a name="com_fresvii_gcm_GcmClient_void_addMatchmakingNotificationListener_MatchmakingNotificationListener"> addMatchmakingNotificationListener </a>

```
public void addMatchmakingNotificationListener(MatchmakingNotificationListener listener)
```

Application can add a [MatchmakingNotificationListener](#com.fresvii.gcm.MatchmakingNotificationListener) to be informed about Matchmaking GCM message notifications.

#### Parameters

|Parameter|Description|
|---|---|
|[MatchmakingNotificationListener](#com.fresvii.gcm.MatchmakingNotificationListener) listener|[MatchmakingNotificationListener](#com.fresvii.gcm.MatchmakingNotificationListener).|



## <a name="com_fresvii_gcm_GcmClient_void_addVoiceChatNotificationListener_VoiceChatNotificationListener"> addVoiceChatNotificationListener </a>

```
public void addVoiceChatNotificationListener(VoiceChatNotificationListener listener)
```

Application can add a [VoiceChatNotificationListener](#com.fresvii.gcm.VoiceChatNotificationListener) to be informed about VoiceChat GCM message notifications.

#### Parameters

|Parameter|Description|
|---|---|
|[VoiceChatNotificationListener](#com.fresvii.gcm.VoiceChatNotificationListener) listener|[VoiceChatNotificationListener](#com.fresvii.gcm.VoiceChatNotificationListener).|



## <a name="com_fresvii_gcm_GcmClient_com_fresvii_gcm_GcmClient_getInstance_"> getInstance </a>

```
public static GcmClient getInstance()
```

Retrieves the instance of the singleton object. Use this to access the GcmClient.

#### Returns

|Return Type|Description|
|---|---|
|GcmClient|Instance of the singleton object.|


## <a name="com_fresvii_gcm_GcmClient_void_initialize_"> initialize </a>

```
public void initialize()
```

Initializes the GcmClient.


## <a name="com_fresvii_gcm_GcmClient_void_pause_GcmClient_PauseCallback"> pause </a>

```
public void pause(GcmClient.PauseCallback callback)
```

Call this method if you no longer wish to receive any GCM notifications.  E.g. you can use this method to disable GCM notifications when the player is in a game match, and thus busy.  Or you can disable GCM notifications when you shut down your app,   if you want the user to receive notifications only while your app is running.

#### Parameters

|Parameter|Description|
|---|---|
|[GcmClient.PauseCallback](#com.fresvii.gcm.GcmClient.PauseCallback) callback|[Callback](#com.fresvii.gcm.GcmClient.PauseCallback) to be informed about the result of the operation.|



## <a name="com_fresvii_gcm_GcmClient_void_registerAndAddDeviceToken_String_GcmClient_RegisterAndAddDeviceTokenCallback"> registerAndAddDeviceToken </a>

```
public void registerAndAddDeviceToken(String gcmSenderId,  
                                      GcmClient.RegisterAndAddDeviceTokenCallback callback)
```

Registers this device for GCM service,   and sends the device's GCM Registration ID to the Fresvii Server  so that the application can receive GCM message notifications.

#### Parameters

|Parameter|Description|
|---|---|
|String gcmSenderId|Your GCM Sender ID.|
|[GcmClient.RegisterAndAddDeviceTokenCallback](#com.fresvii.gcm.GcmClient.RegisterAndAddDeviceTokenCallback) callback|[Callback](#com.fresvii.gcm.GcmClient.RegisterAndAddDeviceTokenCallback) to be informed about the result of the operation.|



## <a name="com_fresvii_gcm_GcmClient_void_removeCustomNotificationListener_String_String_CustomNotificationListener"> removeCustomNotificationListener </a>

```
public void removeCustomNotificationListener(String resource,  
                                             String action,  
                                             CustomNotificationListener listener)
```

Removes a [CustomNotificationListener](#com.fresvii.gcm.CustomNotificationListener).

#### Parameters

|Parameter|Description|
|---|---|
|String resource|The resource for which we should no longer be listening for. The value must match the value used when adding the listener.|
|String action|The action for which we should no longer be listening for. The value must match the value used when adding the listener.|
|[CustomNotificationListener](#com.fresvii.gcm.CustomNotificationListener) listener|[CustomNotificationListener](#com.fresvii.gcm.CustomNotificationListener).|



## <a name="com_fresvii_gcm_GcmClient_void_removeForumNotificationListener_ForumNotificationListener"> removeForumNotificationListener </a>

```
public void removeForumNotificationListener(ForumNotificationListener listener)
```

Removes a [ForumNotificationListener](#com.fresvii.gcm.ForumNotificationListener).

#### Parameters

|Parameter|Description|
|---|---|
|[ForumNotificationListener](#com.fresvii.gcm.ForumNotificationListener) listener|[ForumNotificationListener](#com.fresvii.gcm.ForumNotificationListener).|



## <a name="com_fresvii_gcm_GcmClient_void_removeFriendRequestNotificationListener_FriendRequestNotificationListener"> removeFriendRequestNotificationListener </a>

```
public void removeFriendRequestNotificationListener(FriendRequestNotificationListener listener)
```

Removes a [CustomNotificationListener](#com.fresvii.gcm.CustomNotificationListener).

#### Parameters

|Parameter|Description|
|---|---|
|[FriendRequestNotificationListener](#com.fresvii.gcm.FriendRequestNotificationListener) listener|[CustomNotificationListener](#com.fresvii.gcm.CustomNotificationListener).|



## <a name="com_fresvii_gcm_GcmClient_void_removeGroupChatNotificationListener_GroupChatNotificationListener"> removeGroupChatNotificationListener </a>

```
public void removeGroupChatNotificationListener(GroupChatNotificationListener listener)
```

Removes a [GroupChatNotificationListener](#com.fresvii.gcm.GroupChatNotificationListener).

#### Parameters

|Parameter|Description|
|---|---|
|[GroupChatNotificationListener](#com.fresvii.gcm.GroupChatNotificationListener) listener|[GroupChatNotificationListener](#com.fresvii.gcm.GroupChatNotificationListener).|



## <a name="com_fresvii_gcm_GcmClient_void_removeMatchmakingNotificationListener_MatchmakingNotificationListener"> removeMatchmakingNotificationListener </a>

```
public void removeMatchmakingNotificationListener(MatchmakingNotificationListener listener)
```

Removes a [MatchmakingNotificationListener](#com.fresvii.gcm.MatchmakingNotificationListener).

#### Parameters

|Parameter|Description|
|---|---|
|[MatchmakingNotificationListener](#com.fresvii.gcm.MatchmakingNotificationListener) listener|[MatchmakingNotificationListener](#com.fresvii.gcm.MatchmakingNotificationListener).|



## <a name="com_fresvii_gcm_GcmClient_void_removeVoiceChatNotificationListener_VoiceChatNotificationListener"> removeVoiceChatNotificationListener </a>

```
public void removeVoiceChatNotificationListener(VoiceChatNotificationListener listener)
```

Removes a [VoiceChatNotificationListener](#com.fresvii.gcm.VoiceChatNotificationListener).

#### Parameters

|Parameter|Description|
|---|---|
|[VoiceChatNotificationListener](#com.fresvii.gcm.VoiceChatNotificationListener) listener|[VoiceChatNotificationListener](#com.fresvii.gcm.VoiceChatNotificationListener).|



## <a name="com_fresvii_gcm_GcmClient_void_resume_GcmClient_ResumeCallback"> resume </a>

```
public void resume(GcmClient.ResumeCallback callback)
```

Call this method if you wish to resume receiving GCM notifications after you paused them.  E.g. you can use this method to enable GCM notifications after the player finishes a game match, and is no longer busy.

#### Parameters

|Parameter|Description|
|---|---|
|[GcmClient.ResumeCallback](#com.fresvii.gcm.GcmClient.ResumeCallback) callback|[Callback](#com.fresvii.gcm.GcmClient.ResumeCallback) to be informed about the result of the operation.|




---  

## <a name="com.fresvii.gcm.GcmClient.RegisterAndAddDeviceTokenCallback"> Interface GcmClient.RegisterAndAddDeviceTokenCallback </a>

```
public static interface GcmClient.RegisterAndAddDeviceTokenCallback implements FailureCallback
```

**Hierarchy:**  

```
com.fresvii.gcm.GcmClient.RegisterAndAddDeviceTokenCallback
```

**Description:**  
Callback interface to handle [GcmClient.registerAndAddDeviceToken()](#com_fresvii_gcm_GcmClient_void_registerAndAddDeviceToken_String_GcmClient_RegisterAndAddDeviceTokenCallback) results.








### Method Summary

|Method|Description|
|---|---|
|[public void onSuccess()](#com_fresvii_gcm_GcmClient_RegisterAndAddDeviceTokenCallback_void_onSuccess_)|Callback invoked when operation succeeds.|



### Method Detail
 


## <a name="com_fresvii_gcm_GcmClient_RegisterAndAddDeviceTokenCallback_void_onSuccess_"> onSuccess </a>

```
public void onSuccess()
```

Callback invoked when operation succeeds.



---  

## <a name="com.fresvii.gcm.GcmClient.PauseCallback"> Interface GcmClient.PauseCallback </a>

```
public static interface GcmClient.PauseCallback implements FailureCallback
```

**Hierarchy:**  

```
com.fresvii.gcm.GcmClient.PauseCallback
```

**Description:**  
Callback interface to handle [GcmClient.pause()](#com_fresvii_gcm_GcmClient_void_pause_GcmClient_PauseCallback) results.








### Method Summary

|Method|Description|
|---|---|
|[public void onSuccess()](#com_fresvii_gcm_GcmClient_PauseCallback_void_onSuccess_)|Callback invoked when operation succeeds.|



### Method Detail
 


## <a name="com_fresvii_gcm_GcmClient_PauseCallback_void_onSuccess_"> onSuccess </a>

```
public void onSuccess()
```

Callback invoked when operation succeeds.



---  

## <a name="com.fresvii.gcm.GcmClient.ResumeCallback"> Interface GcmClient.ResumeCallback </a>

```
public static interface GcmClient.ResumeCallback implements FailureCallback
```

**Hierarchy:**  

```
com.fresvii.gcm.GcmClient.ResumeCallback
```

**Description:**  
Callback interface to handle [GcmClient.resume()](#com_fresvii_gcm_GcmClient_void_resume_GcmClient_ResumeCallback) results.








### Method Summary

|Method|Description|
|---|---|
|[public void onSuccess()](#com_fresvii_gcm_GcmClient_ResumeCallback_void_onSuccess_)|Callback invoked when operation succeeds.|



### Method Detail
 


## <a name="com_fresvii_gcm_GcmClient_ResumeCallback_void_onSuccess_"> onSuccess </a>

```
public void onSuccess()
```

Callback invoked when operation succeeds.



---  

## <a name="com.fresvii.gcm.AppSteroidGcmMessage"> Class AppSteroidGcmMessage </a>

```
public class AppSteroidGcmMessage extends Object
```

**Hierarchy:**  

```
java.lang.Object  
    com.fresvii.gcm.AppSteroidGcmMessage
```

**Description:**  
Represents a Fresvii GCM Message

**Author:**  
Marcus Froeschl

**Version:**  
1.0

**Since:**  
2014-06-02


### Method Summary

|Method|Description|
|---|---|
|[public AppSteroidGcmMessage.Action getAction()](#com_fresvii_gcm_AppSteroidGcmMessage_com_fresvii_gcm_AppSteroidGcmMessage_Action_getAction_)|Retrieves the action that was performed on the resource.|
|[public String getActionString()](#com_fresvii_gcm_AppSteroidGcmMessage_java_lang_String_getActionString_)|Retrieves the message's action String.|
|[public Context getContext()](#com_fresvii_gcm_AppSteroidGcmMessage_android_content_Context_getContext_)|Retrieves the context in which this GCM message was received.|
|[public String getId()](#com_fresvii_gcm_AppSteroidGcmMessage_java_lang_String_getId_)|Retrieves the message's ID.|
|[public AppSteroidGcmMessage.MessageType getMessageType()](#com_fresvii_gcm_AppSteroidGcmMessage_com_fresvii_gcm_AppSteroidGcmMessage_MessageType_getMessageType_)|Retrieves the message's type.|
|[public String getObject()](#com_fresvii_gcm_AppSteroidGcmMessage_java_lang_String_getObject_)|Retrieves the object associated with the message as a JSON String.|
|[public AppSteroidGcmMessage.Resource getResource()](#com_fresvii_gcm_AppSteroidGcmMessage_com_fresvii_gcm_AppSteroidGcmMessage_Resource_getResource_)|Retrieves the resource associated with this message.|
|[public String getResourcePath()](#com_fresvii_gcm_AppSteroidGcmMessage_java_lang_String_getResourcePath_)|Retrieves the message's resource path.|
|[public String getSound()](#com_fresvii_gcm_AppSteroidGcmMessage_java_lang_String_getSound_)|Retrieves the message's sound.|
|[public String getTitle()](#com_fresvii_gcm_AppSteroidGcmMessage_java_lang_String_getTitle_)|Retrieves the message's title.|
|[public String getVersion()](#com_fresvii_gcm_AppSteroidGcmMessage_java_lang_String_getVersion_)|Retrieves the message's version.|



### Method Detail
 


## <a name="com_fresvii_gcm_AppSteroidGcmMessage_com_fresvii_gcm_AppSteroidGcmMessage_Action_getAction_"> getAction </a>

```
public AppSteroidGcmMessage.Action getAction()
```

Retrieves the action that was performed on the resource.

#### Returns

|Return Type|Description|
|---|---|
|AppSteroidGcmMessage.Action|The action that was performed on the resource.|


## <a name="com_fresvii_gcm_AppSteroidGcmMessage_java_lang_String_getActionString_"> getActionString </a>

```
public String getActionString()
```

Retrieves the message's action String.

#### Returns

|Return Type|Description|
|---|---|
|String|The message's action String.|


## <a name="com_fresvii_gcm_AppSteroidGcmMessage_android_content_Context_getContext_"> getContext </a>

```
public Context getContext()
```

Retrieves the context in which this GCM message was received.

#### Returns

|Return Type|Description|
|---|---|
|Context|Message context.|


## <a name="com_fresvii_gcm_AppSteroidGcmMessage_java_lang_String_getId_"> getId </a>

```
public String getId()
```

Retrieves the message's ID.

#### Returns

|Return Type|Description|
|---|---|
|String|The message's ID.|


## <a name="com_fresvii_gcm_AppSteroidGcmMessage_com_fresvii_gcm_AppSteroidGcmMessage_MessageType_getMessageType_"> getMessageType </a>

```
public AppSteroidGcmMessage.MessageType getMessageType()
```

Retrieves the message's type.

#### Returns

|Return Type|Description|
|---|---|
|AppSteroidGcmMessage.MessageType|The message's type.|


## <a name="com_fresvii_gcm_AppSteroidGcmMessage_java_lang_String_getObject_"> getObject </a>

```
public String getObject()
```

Retrieves the object associated with the message as a JSON String.

#### Returns

|Return Type|Description|
|---|---|
|String|The object associated with the message.|


## <a name="com_fresvii_gcm_AppSteroidGcmMessage_com_fresvii_gcm_AppSteroidGcmMessage_Resource_getResource_"> getResource </a>

```
public AppSteroidGcmMessage.Resource getResource()
```

Retrieves the resource associated with this message.

#### Returns

|Return Type|Description|
|---|---|
|AppSteroidGcmMessage.Resource|The resource associated with this message.|


## <a name="com_fresvii_gcm_AppSteroidGcmMessage_java_lang_String_getResourcePath_"> getResourcePath </a>

```
public String getResourcePath()
```

Retrieves the message's resource path.

#### Returns

|Return Type|Description|
|---|---|
|String|The message's resource path.|


## <a name="com_fresvii_gcm_AppSteroidGcmMessage_java_lang_String_getSound_"> getSound </a>

```
public String getSound()
```

Retrieves the message's sound.

#### Returns

|Return Type|Description|
|---|---|
|String|The message's sound.|


## <a name="com_fresvii_gcm_AppSteroidGcmMessage_java_lang_String_getTitle_"> getTitle </a>

```
public String getTitle()
```

Retrieves the message's title.

#### Returns

|Return Type|Description|
|---|---|
|String|The message's title.|


## <a name="com_fresvii_gcm_AppSteroidGcmMessage_java_lang_String_getVersion_"> getVersion </a>

```
public String getVersion()
```

Retrieves the message's version.

#### Returns

|Return Type|Description|
|---|---|
|String|The message's version.|



---  

## <a name="com.fresvii.gcm.AppSteroidGcmMessage.MessageType"> Enum AppSteroidGcmMessage.MessageType </a>

```
public static final class AppSteroidGcmMessage.MessageType extends Enum
```

**Hierarchy:**  

```
java.lang.Object  
    java.lang.Enum  
        com.fresvii.gcm.AppSteroidGcmMessage.MessageType
```

**Description:**  
Known GCM message types which will receive special treatment.








### Field Summary

|Field|Description|
|---|---|
|CONFERENCE_CREATED|A message for [VoiceChatConference](VoiceChat.md#com.fresvii.voicechat.VoiceChatConference) invitation.|
|CUSTOM|A custom GCM message (user defined message).|
|DIRECT_MESSAGE_CREATED|A direct message.|
|FORUM_COMMENT_CREATED|A message for a new forum comment.|
|FRIEND_REQUEST_CREATED|A message for a new friend request.|
|FRIEND_REQUEST_UPDATED|A message for an updated friend request.|
|GROUP_IMAGE_MESSAGE_CREATED|An image message.|
|GROUP_IN_GAME_MESSAGE_CREATED|An ingame message.|
|GROUP_TEXT_MESSAGE_CREATED|A group text message.|
|MATCHMAKING_GAME_CONTEXT_CREATED|A message for a new game context.|
|MATCHMAKING_INVITATION_CREATED|A message for a new game invitation.|
|MATCHMAKING_INVITATION_UPDATED|A message for an updated game invitation.|
|MATCHMAKING_MATCH_UPDATED|A message for an updated match.|
|OFFICIAL_THREAD_CREATED|A message for an official thread.|




---  

## <a name="com.fresvii.gcm.AppSteroidGcmMessage.Resource"> Enum AppSteroidGcmMessage.Resource </a>

```
public static final class AppSteroidGcmMessage.Resource extends Enum
```

**Hierarchy:**  

```
java.lang.Object  
    java.lang.Enum  
        com.fresvii.gcm.AppSteroidGcmMessage.Resource
```

**Description:**  
GCM message resources specified in Fresvii Push Specifications








### Field Summary

|Field|Description|
|---|---|
|CUSTOM|A custom resource (user defined resource).|
|FORUM_COMMENT|A forum comment resource.|
|FORUM_THREAD|A forum thread resource.|
|FRIEND_REQUEST|A friend request resource.|
|GROUP_CONFERENCE|A conference resource.|
|GROUP_IMAGE_MESSAGE|A group image message resource.|
|GROUP_IN_GAME_MESSAGE|A group ingame message resource.|
|GROUP_TEXT_MESSAGE|A group text message resource.|
|MATCHMAKING_GAME_CONTEXT|A game context|
|MATCHMAKING_GAME_INVITATION|A game invitation|
|MATCHMAKING_MATCH|A match resource.|
|NONE|No resource.|




---  

## <a name="com.fresvii.gcm.AppSteroidGcmMessage.Action"> Enum AppSteroidGcmMessage.Action </a>

```
public static final class AppSteroidGcmMessage.Action extends Enum
```

**Hierarchy:**  

```
java.lang.Object  
    java.lang.Enum  
        com.fresvii.gcm.AppSteroidGcmMessage.Action
```

**Description:**  
GCM message actions specified in Fresvii Push Specifications








### Field Summary

|Field|Description|
|---|---|
|CREATED|Created action|
|CUSTOM|A custom action (user defined action).|
|NONE|No action|
|UPDATED|Updated action|




---  

## <a name="com.fresvii.gcm.GroupChatNotificationListener"> Interface GroupChatNotificationListener </a>

```
public interface GroupChatNotificationListener
```

**Hierarchy:**  

```
com.fresvii.gcm.GroupChatNotificationListener
```

**Description:**  
Application may implement this interface to handle group GCM notifications.

**Author:**  
Marcus Froeschl

**Version:**  
1.0

**Since:**  
2014-07-20


### Method Summary

|Method|Description|
|---|---|
|[public void onGroupImageMessage(AppSteroidMessage message, AppSteroidGcmMessage fresviiGcmMessage)](#com_fresvii_gcm_GroupChatNotificationListener_void_onGroupImageMessage_AppSteroidMessage_AppSteroidGcmMessage)|Called when a Group Image Message Notification is received.|
|[public void onGroupInGameMessage(AppSteroidMessage message, AppSteroidGcmMessage fresviiGcmMessage)](#com_fresvii_gcm_GroupChatNotificationListener_void_onGroupInGameMessage_AppSteroidMessage_AppSteroidGcmMessage)|Called when a Group InGame Message Notification is received.|
|[public void onGroupTextMessage(AppSteroidMessage message, AppSteroidGcmMessage fresviiGcmMessage)](#com_fresvii_gcm_GroupChatNotificationListener_void_onGroupTextMessage_AppSteroidMessage_AppSteroidGcmMessage)|Called when a Group Text Message Notification is received.|



### Method Detail
 


## <a name="com_fresvii_gcm_GroupChatNotificationListener_void_onGroupImageMessage_AppSteroidMessage_AppSteroidGcmMessage"> onGroupImageMessage </a>

```
public void onGroupImageMessage(AppSteroidMessage message,  
                                AppSteroidGcmMessage fresviiGcmMessage)
```

Called when a Group Image Message Notification is received.

#### Parameters

|Parameter|Description|
|---|---|
|[AppSteroidMessage](GroupChat.md#com.fresvii.components.AppSteroidMessage) message|The image message associated with the event.|
|[AppSteroidGcmMessage](#com.fresvii.gcm.AppSteroidGcmMessage) fresviiGcmMessage|The full original GCM message if application wishes to do more detailed parsing.|



## <a name="com_fresvii_gcm_GroupChatNotificationListener_void_onGroupInGameMessage_AppSteroidMessage_AppSteroidGcmMessage"> onGroupInGameMessage </a>

```
public void onGroupInGameMessage(AppSteroidMessage message,  
                                 AppSteroidGcmMessage fresviiGcmMessage)
```

Called when a Group InGame Message Notification is received.

#### Parameters

|Parameter|Description|
|---|---|
|[AppSteroidMessage](GroupChat.md#com.fresvii.components.AppSteroidMessage) message|The ingame message associated with the event.|
|[AppSteroidGcmMessage](#com.fresvii.gcm.AppSteroidGcmMessage) fresviiGcmMessage|The full original GCM message if application wishes to do more detailed parsing.|



## <a name="com_fresvii_gcm_GroupChatNotificationListener_void_onGroupTextMessage_AppSteroidMessage_AppSteroidGcmMessage"> onGroupTextMessage </a>

```
public void onGroupTextMessage(AppSteroidMessage message,  
                               AppSteroidGcmMessage fresviiGcmMessage)
```

Called when a Group Text Message Notification is received.

#### Parameters

|Parameter|Description|
|---|---|
|[AppSteroidMessage](GroupChat.md#com.fresvii.components.AppSteroidMessage) message|The text message associated with the event.|
|[AppSteroidGcmMessage](#com.fresvii.gcm.AppSteroidGcmMessage) fresviiGcmMessage|The full original GCM message if application wishes to do more detailed parsing.|




---  

## <a name="com.fresvii.gcm.FriendRequestNotificationListener"> Interface FriendRequestNotificationListener </a>

```
public interface FriendRequestNotificationListener
```

**Hierarchy:**  

```
com.fresvii.gcm.FriendRequestNotificationListener
```

**Description:**  
Application may implement this interface to handle friend request GCM notifications.

**Author:**  
Marcus Froeschl

**Version:**  
1.0

**Since:**  
2014-07-20


### Method Summary

|Method|Description|
|---|---|
|[public void onFriendRequestUpdated(AppSteroidUser user, AppSteroidGcmMessage fresviiGcmMessage)](#com_fresvii_gcm_FriendRequestNotificationListener_void_onFriendRequestUpdated_AppSteroidUser_AppSteroidGcmMessage)|Called when an existing Friend Request was updated.|
|[public void onNewFriendRequest(AppSteroidUser user, AppSteroidGcmMessage fresviiGcmMessage)](#com_fresvii_gcm_FriendRequestNotificationListener_void_onNewFriendRequest_AppSteroidUser_AppSteroidGcmMessage)|Called when a new Friend Request is received.|



### Method Detail
 


## <a name="com_fresvii_gcm_FriendRequestNotificationListener_void_onFriendRequestUpdated_AppSteroidUser_AppSteroidGcmMessage"> onFriendRequestUpdated </a>

```
public void onFriendRequestUpdated(AppSteroidUser user,  
                                   AppSteroidGcmMessage fresviiGcmMessage)
```

Called when an existing Friend Request was updated.

#### Parameters

|Parameter|Description|
|---|---|
|[AppSteroidUser](User.md#com.fresvii.components.AppSteroidUser) user|The user who requests to be our friend.|
|[AppSteroidGcmMessage](#com.fresvii.gcm.AppSteroidGcmMessage) fresviiGcmMessage|The full original GCM message if application wishes to do more detailed parsing.|



## <a name="com_fresvii_gcm_FriendRequestNotificationListener_void_onNewFriendRequest_AppSteroidUser_AppSteroidGcmMessage"> onNewFriendRequest </a>

```
public void onNewFriendRequest(AppSteroidUser user,  
                               AppSteroidGcmMessage fresviiGcmMessage)
```

Called when a new Friend Request is received.

#### Parameters

|Parameter|Description|
|---|---|
|[AppSteroidUser](User.md#com.fresvii.components.AppSteroidUser) user|The user who requests to be our friend.|
|[AppSteroidGcmMessage](#com.fresvii.gcm.AppSteroidGcmMessage) fresviiGcmMessage|The full original GCM message if application wishes to do more detailed parsing.|




---  

## <a name="com.fresvii.gcm.ForumNotificationListener"> Interface ForumNotificationListener </a>

```
public interface ForumNotificationListener
```

**Hierarchy:**  

```
com.fresvii.gcm.ForumNotificationListener
```

**Description:**  
Application may implement this interface to handle forum GCM notifications.

**Author:**  
Marcus Froeschl

**Version:**  
1.0

**Since:**  
2014-07-20


### Method Summary

|Method|Description|
|---|---|
|[public void onNewForumComment(AppSteroidForumComment comment, AppSteroidGcmMessage fresviiGcmMessage)](#com_fresvii_gcm_ForumNotificationListener_void_onNewForumComment_AppSteroidForumComment_AppSteroidGcmMessage)|Called when a new comment was written to a Fresvii forum thread you are subscribed to.|



### Method Detail
 


## <a name="com_fresvii_gcm_ForumNotificationListener_void_onNewForumComment_AppSteroidForumComment_AppSteroidGcmMessage"> onNewForumComment </a>

```
public void onNewForumComment(AppSteroidForumComment comment,  
                              AppSteroidGcmMessage fresviiGcmMessage)
```

Called when a new comment was written to a Fresvii forum thread you are subscribed to.

#### Parameters

|Parameter|Description|
|---|---|
|AppSteroidForumComment comment|The new forum comment.|
|[AppSteroidGcmMessage](#com.fresvii.gcm.AppSteroidGcmMessage) fresviiGcmMessage|The full original GCM message if application wishes to do more detailed parsing.|




---  

## <a name="com.fresvii.gcm.VoiceChatNotificationListener"> Interface VoiceChatNotificationListener </a>

```
public interface VoiceChatNotificationListener
```

**Hierarchy:**  

```
com.fresvii.gcm.VoiceChatNotificationListener
```

**Description:**  
Application may implement this interface to handle VoiceChat GCM notifications.

**Author:**  
Marcus Froeschl

**Version:**  
1.0

**Since:**  
2014-07-20


### Method Summary

|Method|Description|
|---|---|
|[public void onConferenceCreated(AppSteroidConference conference, AppSteroidGcmMessage fresviiGcmMessage)](#com_fresvii_gcm_VoiceChatNotificationListener_void_onConferenceCreated_AppSteroidConference_AppSteroidGcmMessage)|Called when a new VoiceChat conference was created. |



### Method Detail
 


## <a name="com_fresvii_gcm_VoiceChatNotificationListener_void_onConferenceCreated_AppSteroidConference_AppSteroidGcmMessage"> onConferenceCreated </a>

```
public void onConferenceCreated(AppSteroidConference conference,  
                                AppSteroidGcmMessage fresviiGcmMessage)
```

Called when a new VoiceChat conference was created.   This means you have been invited to a VoiceChat conference.   By default, Fresvii SDK will automatically handle VoiceChat invitations, so the application normally does not have to handle this invitation.  However, application may call [VoiceChatConfig.setIncomingVoiceChatBehavior()](VoiceChat.md#com_fresvii_voicechat_VoiceChatConfig_void_setIncomingVoiceChatBehavior_VoiceChatConfig_IncomingVoiceChatBehavior) to change this behavior,  and handle VoiceChat invitations here.

#### Parameters

|Parameter|Description|
|---|---|
|AppSteroidConference conference|The conference that was created.|
|[AppSteroidGcmMessage](#com.fresvii.gcm.AppSteroidGcmMessage) fresviiGcmMessage|The full original GCM message if application wishes to do more detailed parsing.|




---  

## <a name="com.fresvii.gcm.MatchmakingNotificationListener"> Interface MatchmakingNotificationListener </a>

```
public interface MatchmakingNotificationListener
```

**Hierarchy:**  

```
com.fresvii.gcm.MatchmakingNotificationListener
```

**Description:**  
Application may implement this interface to handle friend request GCM notifications.

**Author:**  
Marcus Froeschl

**Version:**  
1.0

**Since:**  
2014-07-20


### Method Summary

|Method|Description|
|---|---|
|[public void onGameContextCreated(AppSteroidGameContext gameContext, AppSteroidGcmMessage fresviiGcmMessage)](#com_fresvii_gcm_MatchmakingNotificationListener_void_onGameContextCreated_AppSteroidGameContext_AppSteroidGcmMessage)|Called when a game context was created|
|[public void onInvitationCreated(AppSteroidMatchmakingInvitation invitation, AppSteroidGcmMessage fresviiGcmMessage)](#com_fresvii_gcm_MatchmakingNotificationListener_void_onInvitationCreated_AppSteroidMatchmakingInvitation_AppSteroidGcmMessage)|Called when a game invitation was created|
|[public void onInvitationUpdated(AppSteroidMatchmakingInvitation invitation, AppSteroidGcmMessage fresviiGcmMessage)](#com_fresvii_gcm_MatchmakingNotificationListener_void_onInvitationUpdated_AppSteroidMatchmakingInvitation_AppSteroidGcmMessage)|Called when a game invitation was updated|
|[public void onMatchUpdated(AppSteroidMatch match, AppSteroidGcmMessage fresviiGcmMessage)](#com_fresvii_gcm_MatchmakingNotificationListener_void_onMatchUpdated_AppSteroidMatch_AppSteroidGcmMessage)|Called when a match was updated.|
|[public void onUserAcceptedMatchmakingInvitation(String invitationId)](#com_fresvii_gcm_MatchmakingNotificationListener_void_onUserAcceptedMatchmakingInvitation_String)|Called when the user accepts a game invitation in the OS notification bar.|



### Method Detail
 


## <a name="com_fresvii_gcm_MatchmakingNotificationListener_void_onGameContextCreated_AppSteroidGameContext_AppSteroidGcmMessage"> onGameContextCreated </a>

```
public void onGameContextCreated(AppSteroidGameContext gameContext,  
                                 AppSteroidGcmMessage fresviiGcmMessage)
```

Called when a game context was created

#### Parameters

|Parameter|Description|
|---|---|
|[AppSteroidGameContext](Matchmaking.md#com.fresvii.components.AppSteroidGameContext) gameContext|The game context|
|[AppSteroidGcmMessage](#com.fresvii.gcm.AppSteroidGcmMessage) fresviiGcmMessage|The full original GCM message if application wishes to do more detailed parsing.|



## <a name="com_fresvii_gcm_MatchmakingNotificationListener_void_onInvitationCreated_AppSteroidMatchmakingInvitation_AppSteroidGcmMessage"> onInvitationCreated </a>

```
public void onInvitationCreated(AppSteroidMatchmakingInvitation invitation,  
                                AppSteroidGcmMessage fresviiGcmMessage)
```

Called when a game invitation was created

#### Parameters

|Parameter|Description|
|---|---|
|[AppSteroidMatchmakingInvitation](Matchmaking.md#com.fresvii.components.AppSteroidMatchmakingInvitation) invitation|The invitation.|
|[AppSteroidGcmMessage](#com.fresvii.gcm.AppSteroidGcmMessage) fresviiGcmMessage|The full original GCM message if application wishes to do more detailed parsing.|



## <a name="com_fresvii_gcm_MatchmakingNotificationListener_void_onInvitationUpdated_AppSteroidMatchmakingInvitation_AppSteroidGcmMessage"> onInvitationUpdated </a>

```
public void onInvitationUpdated(AppSteroidMatchmakingInvitation invitation,  
                                AppSteroidGcmMessage fresviiGcmMessage)
```

Called when a game invitation was updated

#### Parameters

|Parameter|Description|
|---|---|
|[AppSteroidMatchmakingInvitation](Matchmaking.md#com.fresvii.components.AppSteroidMatchmakingInvitation) invitation|The invitation.|
|[AppSteroidGcmMessage](#com.fresvii.gcm.AppSteroidGcmMessage) fresviiGcmMessage|The full original GCM message if application wishes to do more detailed parsing.|



## <a name="com_fresvii_gcm_MatchmakingNotificationListener_void_onMatchUpdated_AppSteroidMatch_AppSteroidGcmMessage"> onMatchUpdated </a>

```
public void onMatchUpdated(AppSteroidMatch match,  
                           AppSteroidGcmMessage fresviiGcmMessage)
```

Called when a match was updated.

#### Parameters

|Parameter|Description|
|---|---|
|[AppSteroidMatch](Matchmaking.md#com.fresvii.components.AppSteroidMatch) match|The match that was updated.|
|[AppSteroidGcmMessage](#com.fresvii.gcm.AppSteroidGcmMessage) fresviiGcmMessage|The full original GCM message if application wishes to do more detailed parsing.|



## <a name="com_fresvii_gcm_MatchmakingNotificationListener_void_onUserAcceptedMatchmakingInvitation_String"> onUserAcceptedMatchmakingInvitation </a>

```
public void onUserAcceptedMatchmakingInvitation(String invitationId)
```

Called when the user accepts a game invitation in the OS notification bar.

#### Parameters

|Parameter|Description|
|---|---|
|String invitationId|The ID of the invitation that was accepted.|




---  

## <a name="com.fresvii.gcm.CustomNotificationListener"> Interface CustomNotificationListener </a>

```
public interface CustomNotificationListener
```

**Hierarchy:**  

```
com.fresvii.gcm.CustomNotificationListener
```

**Description:**  
Application may implement this interface to handle custom GCM notifications.

**Author:**  
Marcus Froeschl

**Version:**  
1.0

**Since:**  
2014-07-20


### Method Summary

|Method|Description|
|---|---|
|[public void onCustomMessage(AppSteroidGcmMessage fresviiidGcmMessage)](#com_fresvii_gcm_CustomNotificationListener_void_onCustomMessage_AppSteroidGcmMessage)|Called when a custom GCM notification message was received.|



### Method Detail
 


## <a name="com_fresvii_gcm_CustomNotificationListener_void_onCustomMessage_AppSteroidGcmMessage"> onCustomMessage </a>

```
public void onCustomMessage(AppSteroidGcmMessage fresviiidGcmMessage)
```

Called when a custom GCM notification message was received.

#### Parameters

|Parameter|Description|
|---|---|
|[AppSteroidGcmMessage](#com.fresvii.gcm.AppSteroidGcmMessage) fresviiidGcmMessage|The custom message that was received.|




---  

## <a name="com.fresvii.server.access.NotificationAccess"> Class NotificationAccess </a>

```
public class NotificationAccess extends Object
```

**Hierarchy:**  

```
java.lang.Object  
    com.fresvii.server.access.NotificationAccess
```

**Description:**  
Provides access to Fresvii Server's Notification API.  Can be used to register or delete device tokens for receiving GCM notifications to/from the Fesvii server.

**Author:**  
matsushimakatsuhito, Marcus Froeschl

**Version:**  
1.1

**Since:**  
2014-02-18


### Method Summary

|Method|Description|
|---|---|
|[public static void addDeviceToken(AddDeviceTokenCallback callback)](#com_fresvii_server_access_NotificationAccess_void_addDeviceToken_AddDeviceTokenCallback)|Adds this device's GCM token to the Fresvii Server,|
|[public static void deleteDeviceToken(DeleteDeviceTokenCallback callback)](#com_fresvii_server_access_NotificationAccess_void_deleteDeviceToken_DeleteDeviceTokenCallback)|Deletes this device's GCM token from the Fresvii Server,|



### Method Detail
 


## <a name="com_fresvii_server_access_NotificationAccess_void_addDeviceToken_AddDeviceTokenCallback"> addDeviceToken </a>

```
public static void addDeviceToken(AddDeviceTokenCallback callback)
```

Adds this device's GCM token to the Fresvii Server,  thus registering this device to receive GCM notifications.

#### Parameters

|Parameter|Description|
|---|---|
|[AddDeviceTokenCallback](#com.fresvii.server.access.callbacks.notification.AddDeviceTokenCallback) callback|[Callback](#com.fresvii.server.access.callbacks.notification.AddDeviceTokenCallback) to be informed about the result of the operation.|



## <a name="com_fresvii_server_access_NotificationAccess_void_deleteDeviceToken_DeleteDeviceTokenCallback"> deleteDeviceToken </a>

```
public static void deleteDeviceToken(DeleteDeviceTokenCallback callback)
```

Deletes this device's GCM token from the Fresvii Server,  thus unregistering this device so it no longer will receive GCM notifications.

#### Parameters

|Parameter|Description|
|---|---|
|[DeleteDeviceTokenCallback](#com.fresvii.server.access.callbacks.notification.DeleteDeviceTokenCallback) callback|[Callback](#com.fresvii.server.access.callbacks.notification.DeleteDeviceTokenCallback) to be informed about the result of the operation.|




---  

## <a name="com.fresvii.server.access.callbacks.notification.AddDeviceTokenCallback"> Interface AddDeviceTokenCallback </a>

```
public interface AddDeviceTokenCallback implements FailureCallback
```

**Hierarchy:**  

```
com.fresvii.server.access.callbacks.notification.AddDeviceTokenCallback
```

**Description:**  
Callback interface to handle NotificationAccess.addDeviceToken() results.

**Author:**  
Marcus Froeschl

**Version:**  
1.0




### Method Summary

|Method|Description|
|---|---|
|[public void onSuccess()](#com_fresvii_server_access_callbacks_notification_AddDeviceTokenCallback_void_onSuccess_)|Callback invoked when operation succeeds.|



### Method Detail
 


## <a name="com_fresvii_server_access_callbacks_notification_AddDeviceTokenCallback_void_onSuccess_"> onSuccess </a>

```
public void onSuccess()
```

Callback invoked when operation succeeds.



---  

## <a name="com.fresvii.server.access.callbacks.notification.DeleteDeviceTokenCallback"> Interface DeleteDeviceTokenCallback </a>

```
public interface DeleteDeviceTokenCallback implements FailureCallback
```

**Hierarchy:**  

```
com.fresvii.server.access.callbacks.notification.DeleteDeviceTokenCallback
```

**Description:**  
Callback interface to handle NotificationAccess.deleteDeviceToken() results.

**Author:**  
Marcus Froeschl

**Version:**  
1.0




### Method Summary

|Method|Description|
|---|---|
|[public void onSuccess()](#com_fresvii_server_access_callbacks_notification_DeleteDeviceTokenCallback_void_onSuccess_)|Callback invoked when operation succeeds.|



### Method Detail
 


## <a name="com_fresvii_server_access_callbacks_notification_DeleteDeviceTokenCallback_void_onSuccess_"> onSuccess </a>

```
public void onSuccess()
```

Callback invoked when operation succeeds.


