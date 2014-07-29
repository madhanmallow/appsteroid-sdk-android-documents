

# Fresvii Gaming Cloud SDK for Android #



Last updated 2014-07-29



-------------------------



## Introduction ##

Fresvii Gaming Cloud SDK for Android is an integrated backend gaming service for Android.
With Fresvii, you can easily incorporate various backend services refined to mobile games into your apps for free.





-------------------------



## Classes ##

|**Class**|**Description**|
|---|---|
|[Fresvii](#com.fresvii.Fresvii)|Main entry point for Fresvii Gaming Cloud Android SDK.|
|[Fresvii.IncomingVoiceChatBehavior](#com.fresvii.Fresvii.IncomingVoiceChatBehavior)|Specifies the behavior when receiving an incoming VoiceChat invitation|
|[AccountAccess](#com.fresvii.server.access.AccountAccess)|Provides access to Fresvii Server's Account API.|
|[AccountAccess.UserAuthEvent](#com.fresvii.server.access.AccountAccess.UserAuthEvent)|Events that inform about a user's authentication status|
|[AccountAccess.UserAuthEventListener](#com.fresvii.server.access.AccountAccess.UserAuthEventListener)|Interface that application may implement to listen for [UserAuthEvents](#com.fresvii.server.access.AccountAccess.UserAuthEvent).|
|[GroupAccess](#com.fresvii.server.access.GroupAccess)|Provides access to Fresvii Server's Group API.|
|[NotificationAccess](#com.fresvii.server.access.NotificationAccess)|Provides access to Fresvii Server's Notification API.|
|[SnsAccountAccess](#com.fresvii.server.access.SnsAccountAccess)|Provides access to Fresvii Server's SNS API.|
|[UserAccess](#com.fresvii.server.access.UserAccess)|Provides access to Fresvii Server's User API.|
|[FriendAccess](#com.fresvii.server.access.FriendAccess)|Provides access to Fresvii Server's Friend API.|
|[FailureCallback](#com.fresvii.server.access.callbacks.FailureCallback)|Callback interface to handle operation errors.|
|[SignUpUserCallback](#com.fresvii.server.access.callbacks.account.SignUpUserCallback)|Callback interface to handle [AccountAccess.signUpUser()](#com_fresvii_server_access_AccountAccess_void_signUpUser_SignUpUserCallback) results.|
|[UpdateUserCallback](#com.fresvii.server.access.callbacks.account.UpdateUserCallback)|Callback interface to handle [AccountAccess.updateUser()](#com_fresvii_server_access_AccountAccess_void_updateUser_String_String_Bitmap_UpdateUserCallback) results.|
|[LoginUserCallback](#com.fresvii.server.access.callbacks.account.LoginUserCallback)|Callback interface to handle [AccountAccess.loginUser()](#com_fresvii_server_access_AccountAccess_void_loginUser_LoginUserCallback)  results.|
|[AddUserSnsAccountCallback](#com.fresvii.server.access.callbacks.account.AddUserSnsAccountCallback)|Callback interface to handle [SnsAccountAccess](#com.fresvii.server.access.SnsAccountAccess) results.|
|[DeleteUserSnsAccountCallback](#com.fresvii.server.access.callbacks.account.DeleteUserSnsAccountCallback)|Callback interface to handle [SnsAccountAccess](#com.fresvii.server.access.SnsAccountAccess) results.|
|[GetUserSnsAccountsCallback](#com.fresvii.server.access.callbacks.account.GetUserSnsAccountsCallback)|Callback interface to handle [SnsAccountAccess](#com.fresvii.server.access.SnsAccountAccess) results.|
|[CreateMultiGroupCallback](#com.fresvii.server.access.callbacks.group.CreateMultiGroupCallback)|Callback interface to handle [GroupAccess.createMultiGroup()](#com_fresvii_server_access_GroupAccess_void_createMultiGroup_String_CreateMultiGroupCallback) results.|
|[CreatePairGroupCallback](#com.fresvii.server.access.callbacks.group.CreatePairGroupCallback)|Callback interface to handle [GroupAccess.createPairGroup()](#com_fresvii_server_access_GroupAccess_void_createPairGroup_String_CreatePairGroupCallback) results.|
|[UpdateMultiGroupCallback](#com.fresvii.server.access.callbacks.group.UpdateMultiGroupCallback)|Callback interface to handle [GroupAccess.updateMultiGroup()](#com_fresvii_server_access_GroupAccess_void_updateMultiGroup_String_String_UpdateMultiGroupCallback) results.|
|[DeleteGroupCallback](#com.fresvii.server.access.callbacks.group.DeleteGroupCallback)|Callback interface to handle [GroupAccess.deleteGroup()](#com_fresvii_server_access_GroupAccess_void_deleteGroup_String_DeleteGroupCallback) results.|
|[DeleteMemberFromMultiGroupCallback](#com.fresvii.server.access.callbacks.group.DeleteMemberFromMultiGroupCallback)|Callback interface to handle [GroupAccess.deleteMemberFromMultiGroup()](#com_fresvii_server_access_GroupAccess_void_deleteMemberFromMultiGroup_String_String_DeleteMemberFromMultiGroupCallback) results.|
|[GetGroupsCallback](#com.fresvii.server.access.callbacks.group.GetGroupsCallback)|Callback interface to handle [GroupAccess.getGroups()](#com_fresvii_server_access_GroupAccess_void_getGroups_GetGroupsCallback) results.|
|[GetGroupMembersCallback](#com.fresvii.server.access.callbacks.group.GetGroupMembersCallback)|Callback interface to handle [GroupAccess.getGroupMembers()](#com_fresvii_server_access_GroupAccess_void_getGroupMembers_String_int_GetGroupMembersCallback) results.|
|[GetGroupMessageCallback](#com.fresvii.server.access.callbacks.group.GetGroupMessageCallback)|Callback interface to handle [GroupAccess.getGroupMessage()](#com_fresvii_server_access_GroupAccess_void_getGroupMessage_String_String_GetGroupMessageCallback) results.|
|[GetGroupMessagesCallback](#com.fresvii.server.access.callbacks.group.GetGroupMessagesCallback)|Callback interface to handle [GroupAccess.getGroupMessages()](#com_fresvii_server_access_GroupAccess_void_getGroupMessages_String_int_GetGroupMessagesCallback) results.|
|[GetMessageGroupsCallback](#com.fresvii.server.access.callbacks.group.GetMessageGroupsCallback)|Callback interface to handle [GroupAccess.getMessageGroups()](#com_fresvii_server_access_GroupAccess_void_getMessageGroups_GetMessageGroupsCallback) results.|
|[AddMemberToMultiGroupCallback](#com.fresvii.server.access.callbacks.group.AddMemberToMultiGroupCallback)|Callback interface to handle [GroupAccess.addMemberToMultiGroup()](#com_fresvii_server_access_GroupAccess_void_addMemberToMultiGroup_String_String_AddMemberToMultiGroupCallback) results.|
|[SendImageMessageCallback](#com.fresvii.server.access.callbacks.group.SendImageMessageCallback)|Callback interface to handle [GroupAccess.sendImageMessage()](#com_fresvii_server_access_GroupAccess_void_sendImageMessage_String_Bitmap_SendImageMessageCallback) results.|
|[SendInGameMessageCallback](#com.fresvii.server.access.callbacks.group.SendInGameMessageCallback)|Callback interface to handle [GroupAccess.sendInGameMessage()](#com_fresvii_server_access_GroupAccess_void_sendInGameMessage_String_String_SendInGameMessageCallback) results.|
|[SendTextMessageCallback](#com.fresvii.server.access.callbacks.group.SendTextMessageCallback)|Callback interface to handle [GroupAccess.sendTextMessage()](#com_fresvii_server_access_GroupAccess_void_sendTextMessage_String_String_SendTextMessageCallback) results.|
|[SubscribeToGroupCallback](#com.fresvii.server.access.callbacks.group.SubscribeToGroupCallback)|Callback interface to handle [GroupAccess.subscribeToGroup()](#com_fresvii_server_access_GroupAccess_void_subscribeToGroup_String_SubscribeToGroupCallback) results.|
|[UnsubscribeFromGroupCallback](#com.fresvii.server.access.callbacks.group.UnsubscribeFromGroupCallback)|Callback interface to handle [GroupAccess.unsubscribeFromGroup()](#com_fresvii_server_access_GroupAccess_void_unsubscribeFromGroup_String_UnsubscribeFromGroupCallback) results.|
|[AddDeviceTokenCallback](#com.fresvii.server.access.callbacks.notification.AddDeviceTokenCallback)|Callback interface to handle NotificationAccess.addDeviceToken() results.|
|[DeleteDeviceTokenCallback](#com.fresvii.server.access.callbacks.notification.DeleteDeviceTokenCallback)|Callback interface to handle NotificationAccess.deleteDeviceToken() results.|
|[GetUserCallback](#com.fresvii.server.access.callbacks.user.GetUserCallback)|Callback interface to handle UserAccess.getUser() results.|
|[GetUsersCallback](#com.fresvii.server.access.callbacks.user.GetUsersCallback)|Callback interface to handle UserAccess.getUser() results.|
|[GetFriendsCallback](#com.fresvii.server.access.callbacks.friends.GetFriendsCallback)|Callback interface to handle [FriendAccess.getFriends()](#com_fresvii_server_access_FriendAccess_void_getFriends_GetFriendsCallback) results.|
|[GetIncomingFriendRequestsCallback](#com.fresvii.server.access.callbacks.friends.GetIncomingFriendRequestsCallback)|Callback interface to handle [FriendAccess.getIncomingFriendRequests()](#com_fresvii_server_access_FriendAccess_void_getIncomingFriendRequests_GetIncomingFriendRequestsCallback) results.|
|[GetOutgoingFriendRequestsCallback](#com.fresvii.server.access.callbacks.friends.GetOutgoingFriendRequestsCallback)|Callback interface to handle [FriendAccess.getOutgoingFriendRequests()](#com_fresvii_server_access_FriendAccess_void_getOutgoingFriendRequests_GetOutgoingFriendRequestsCallback) results.|
|[SendFriendRequestCallback](#com.fresvii.server.access.callbacks.friends.SendFriendRequestCallback)|Callback interface to handle [FriendAccess.sendFriendRequest()](#com_fresvii_server_access_FriendAccess_void_sendFriendRequest_String_SendFriendRequestCallback) results.|
|[AcceptFriendRequestCallback](#com.fresvii.server.access.callbacks.friends.AcceptFriendRequestCallback)|Callback interface to handle [FriendAccess.acceptFriendRequest()](#com_fresvii_server_access_FriendAccess_void_acceptFriendRequest_String_AcceptFriendRequestCallback) results.|
|[HideFriendRequestCallback](#com.fresvii.server.access.callbacks.friends.HideFriendRequestCallback)|Callback interface to handle [FriendAccess.hideFriendRequest()](#com_fresvii_server_access_FriendAccess_void_hideFriendRequest_String_HideFriendRequestCallback) results.|
|[UnfriendCallback](#com.fresvii.server.access.callbacks.friends.UnfriendCallback)|Callback interface to handle [FriendAccess.unfriend()](#com_fresvii_server_access_FriendAccess_void_unfriend_String_UnfriendCallback) results.|
|[GcmClient](#com.fresvii.gcm.GcmClient)|The GcmClient is used to register for and handle GMC notifications.|
|[GroupNotificationListener](#com.fresvii.gcm.GroupNotificationListener)|Application may implement this interface to handle group GCM notifications.|
|[FriendRequestNotificationListener](#com.fresvii.gcm.FriendRequestNotificationListener)|Application may implement this interface to handle friend request GCM notifications.|
|[ForumNotificationListener](#com.fresvii.gcm.ForumNotificationListener)|Application may implement this interface to handle forum GCM notifications.|
|[VoiceChatNotificationListener](#com.fresvii.gcm.VoiceChatNotificationListener)|Application may implement this interface to handle VoiceChat GCM notifications.|
|[CustomNotificationListener](#com.fresvii.gcm.CustomNotificationListener)|Application may implement this interface to handle custom GCM notifications.|
|[VoiceChatConference](#com.fresvii.voicechat.VoiceChatConference)|Class used to manage a VoiceChat conference.|
|[VoiceChatConference.CallState](#com.fresvii.voicechat.VoiceChatConference.CallState)|Represents the state of a call in the conference.|
|[VoiceChatConference.ConferenceState](#com.fresvii.voicechat.VoiceChatConference.ConferenceState)|Represents the state of the conference.|
|[VoiceChatConference.ConferenceRole](#com.fresvii.voicechat.VoiceChatConference.ConferenceRole)|Represents the conference role.|
|[VoiceChatConferenceCallback](#com.fresvii.voicechat.VoiceChatConferenceCallback)|Callback interface to handle several [VoiceChatConference](#com.fresvii.voicechat.VoiceChatConference) results.|
|[VoiceChatConferenceListener](#com.fresvii.voicechat.VoiceChatConferenceListener)|Application may implement this interface to handle [VoiceChatConference](#com.fresvii.voicechat.VoiceChatConference) events.|
|[FresviiCurrentUser](#com.fresvii.components.FresviiCurrentUser)|Represents the user logged in to Fresvii Server on this device.|
|[FresviiGroup](#com.fresvii.components.FresviiGroup)|Represents a Fresvii Group used for text chat, voice chat etc.|
|[FresviiUser](#com.fresvii.components.FresviiUser)|Represents a Fresvii user.|
|[FresviiGcmMessage](#com.fresvii.gcm.FresviiGcmMessage)|Represents a Fresvii GCM Message|
|[FresviiGcmMessage.MessageType](#com.fresvii.gcm.FresviiGcmMessage.MessageType)|Known GCM message types which will receive special treatment.|
|[FresviiGcmMessage.Resource](#com.fresvii.gcm.FresviiGcmMessage.Resource)|GCM message resources specified in Fresvii Push Specifications|
|[FresviiGcmMessage.Action](#com.fresvii.gcm.FresviiGcmMessage.Action)|GCM message actions specified in Fresvii Push Specifications|



-------------------------



## <a name="com.fresvii.Fresvii"> Class Fresvii </a> ##



```
public class Fresvii extends Object
```

**Hierarchy:**  


```
java.lang.Object  
    com.fresvii.Fresvii
```



**Description:**  
Main entry point for Fresvii Gaming Cloud Android SDK.



**Author:**  
matsushimakatsuhito



**Version:**  
1.0



**Since:**  
2014-02-14




### Field Summary ###



None.




### Method Summary ###

|**Method**|**Description**|
|---|---|
|[public static boolean isStarted()](#com_fresvii_Fresvii_boolean_isStarted_)|Checks if the Fresvii SDK has been started.|
|[public static void start(Context context, String appIdentifier, String appSecretKey, String appName)](#com_fresvii_Fresvii_void_start_Context_String_String_String)|Used to start the Fresvii SDK.|
|[public static void start(Context applicationContext, String appIdentifier, String appSecretKey, String appName, boolean automaticallyLogInUserIfUserExists, boolean automaticallySignUpNewUserIfNoUserExists)](#com_fresvii_Fresvii_void_start_Context_String_String_String_boolean_boolean)|Used to start the Fresvii SDK.|
|[public static void setTimeout(int timeout)](#com_fresvii_Fresvii_void_setTimeout_int)|Sets the timeout period for network communications.|
|[public static void setIncomingVoiceChatBehavior(Fresvii.IncomingVoiceChatBehavior behavior)](#com_fresvii_Fresvii_void_setIncomingVoiceChatBehavior_Fresvii_IncomingVoiceChatBehavior)|Sets the default behavior in case of incoming VoiceChat invitation.|


### Method Detail ###




### <a name="com_fresvii_Fresvii_boolean_isStarted_"> isStarted </a> ###



```
public static boolean isStarted()
```



Checks if the Fresvii SDK has been started.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|boolean|true if the Fresvii SDK has been started, false otherwise.|



### <a name="com_fresvii_Fresvii_void_start_Context_String_String_String"> start </a> ###



```
public static void start(Context context,  
                         String appIdentifier,  
                         String appSecretKey,  
                         String appName)
```



Used to start the Fresvii SDK.
 When you use this method to start the Fresvii SDK, 
 a new Fresvii user will be automatically signed up and logged in if there is no existing user yet.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|Context context|Application context|
|String appIdentifier|Fresvii Application ID of your application|
|String appSecretKey|Secret Key of your application|
|String appName|Name of your application|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|


#### Example ####

```
Fresvii.start(getContext(), YOUR_FRESVII_APP_ID, YOUR_APP_NAME);
```





### <a name="com_fresvii_Fresvii_void_start_Context_String_String_String_boolean_boolean"> start </a> ###



```
public static void start(Context applicationContext,  
                         String appIdentifier,  
                         String appSecretKey,  
                         String appName,  
                         boolean automaticallyLogInUserIfUserExists,  
                         boolean automaticallySignUpNewUserIfNoUserExists)
```



Used to start the Fresvii SDK.
 Using this method to start the Fresvii SDK allows you to specify if the Fresvii SDK
 should automatically sign up and log in a new Fresvii user if there is no existing user yet,
 or if you wish to handle user management manually in your application instead.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|Context applicationContext|Application context|
|String appIdentifier|Fresvii Application ID of your application|
|String appSecretKey|Secret Key of your application|
|String appName|Name of your application|
|boolean automaticallyLogInUserIfUserExists|Specify if the Fresvii SDK should automatically log in an existing Fresvii user|
|boolean automaticallySignUpNewUserIfNoUserExists|Specify if the Fresvii SDK should automatically sign up a new Fresvii user if no user exists yet.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_Fresvii_void_setTimeout_int"> setTimeout </a> ###



```
public static void setTimeout(int timeout)
```



Sets the timeout period for network communications.
 The default value is 10 seconds.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|int timeout|Timeout (in seconds).|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_Fresvii_void_setIncomingVoiceChatBehavior_Fresvii_IncomingVoiceChatBehavior"> setIncomingVoiceChatBehavior </a> ###



```
public static void setIncomingVoiceChatBehavior(Fresvii.IncomingVoiceChatBehavior behavior)
```



Sets the default behavior in case of incoming VoiceChat invitation.
 E.g., should the VoiceChat be auto-connected, or should the user be asked?
 The default behavior is to ask the user.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|[Fresvii.IncomingVoiceChatBehavior](#com.fresvii.Fresvii.IncomingVoiceChatBehavior) behavior|The desired default behavior in case of incoming VoiceChat invitation.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|




-------------------------



## <a name="com.fresvii.Fresvii.IncomingVoiceChatBehavior"> Enum Fresvii.IncomingVoiceChatBehavior </a> ##



```
public static final class Fresvii.IncomingVoiceChatBehavior extends Enum
```

**Hierarchy:**  


```
java.lang.Object  
    java.lang.Enum  
        com.fresvii.Fresvii.IncomingVoiceChatBehavior
```



**Description:**  
Specifies the behavior when receiving an incoming VoiceChat invitation




### Field Summary ###

|**Field**|**Description**|
|---|---|
|ASK|Display a notification and ask the user if to accept the VoiceChat invitation.|
|AUTO_ACCEPT|Automatically accept the VoiceChat invitation.|
|DO_NOTHING|Do nothing. Select this if you wish to ignore incoming VoiceChat invitations,  or handle incoming VoiceChat invitations in your own application.|



### Method Summary ###



None.



### Method Detail ###



None.





-------------------------



## <a name="com.fresvii.server.access.AccountAccess"> Class AccountAccess </a> ##



```
public class AccountAccess extends Object
```

**Hierarchy:**  


```
java.lang.Object  
    com.fresvii.server.access.AccountAccess
```



**Description:**  
Provides access to Fresvii Server's Account API.
 Can be used to sign up and log in Fresvii users.



**Author:**  
matsushimakatsuhito



**Version:**  
1.0



**Since:**  
2014-02-18




### Field Summary ###



None.




### Method Summary ###

|**Method**|**Description**|
|---|---|
|[public static void addUserAuthEventListener(AccountAccess.UserAuthEventListener userAuthEventListener)](#com_fresvii_server_access_AccountAccess_void_addUserAuthEventListener_AccountAccess_UserAuthEventListener)|Adds a [UserAuthEventListener](#com.fresvii.server.access.AccountAccess.UserAuthEventListener) that will be informed about [UserAuthEvents](#com.fresvii.server.access.AccountAccess.UserAuthEvent).|
|[public static void removeUserAuthEventListener(AccountAccess.UserAuthEventListener userAuthEventListener)](#com_fresvii_server_access_AccountAccess_void_removeUserAuthEventListener_AccountAccess_UserAuthEventListener)|Removes the specified [UserAuthEventListener](#com.fresvii.server.access.AccountAccess.UserAuthEventListener).|
|[public static void signUpUser(SignUpUserCallback callback)](#com_fresvii_server_access_AccountAccess_void_signUpUser_SignUpUserCallback)|Signs up a new Fresvii user.|
|[public static void signUpUser(String userName, SignUpUserCallback callback)](#com_fresvii_server_access_AccountAccess_void_signUpUser_String_SignUpUserCallback)|Signs up a new Fresvii user.|
|[public static void signUpUser(String userName, String description, Bitmap profileImageBitmap, SignUpUserCallback callback)](#com_fresvii_server_access_AccountAccess_void_signUpUser_String_String_Bitmap_SignUpUserCallback)|Signs up a new Fresvii user.|
|[public static void updateUser(String updatedUserName, String updatedDescription, Bitmap updatedProfileImageBitmap, UpdateUserCallback callback)](#com_fresvii_server_access_AccountAccess_void_updateUser_String_String_Bitmap_UpdateUserCallback)|Updates an existing Fresvii user with the specified new values.|
|[public static void loginUser(LoginUserCallback callback)](#com_fresvii_server_access_AccountAccess_void_loginUser_LoginUserCallback)|Logs in the current user.|
|[public static void loginUser(int lifetime, LoginUserCallback callback)](#com_fresvii_server_access_AccountAccess_void_loginUser_int_LoginUserCallback)|Logs in the current user.|
|[public static void refreshSession(RefreshSessionCallback callback)](#com_fresvii_server_access_AccountAccess_void_refreshSession_RefreshSessionCallback)|Refreshes the session of the current user.|
|[public static com.fresvii.components.FresviiCurrentUser getCurrentLoggedInUser()](#com_fresvii_server_access_AccountAccess_com_fresvii_components_FresviiCurrentUser_getCurrentLoggedInUser_)|Convenience method to retrieve the current user's singleton object.|


### Method Detail ###




### <a name="com_fresvii_server_access_AccountAccess_void_addUserAuthEventListener_AccountAccess_UserAuthEventListener"> addUserAuthEventListener </a> ###



```
public static void addUserAuthEventListener(AccountAccess.UserAuthEventListener userAuthEventListener)
```



Adds a [UserAuthEventListener](#com.fresvii.server.access.AccountAccess.UserAuthEventListener) that will be informed about [UserAuthEvents](#com.fresvii.server.access.AccountAccess.UserAuthEvent).



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|[AccountAccess.UserAuthEventListener](#com.fresvii.server.access.AccountAccess.UserAuthEventListener) userAuthEventListener|The listener to be added.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_server_access_AccountAccess_void_removeUserAuthEventListener_AccountAccess_UserAuthEventListener"> removeUserAuthEventListener </a> ###



```
public static void removeUserAuthEventListener(AccountAccess.UserAuthEventListener userAuthEventListener)
```



Removes the specified [UserAuthEventListener](#com.fresvii.server.access.AccountAccess.UserAuthEventListener).



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|[AccountAccess.UserAuthEventListener](#com.fresvii.server.access.AccountAccess.UserAuthEventListener) userAuthEventListener|The listener to be removed.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_server_access_AccountAccess_void_signUpUser_SignUpUserCallback"> signUpUser </a> ###



```
public static void signUpUser(SignUpUserCallback callback)
```



Signs up a new Fresvii user.
 Uses default values for userName, description and profile picture.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|[SignUpUserCallback](#com.fresvii.server.access.callbacks.account.SignUpUserCallback) callback|[Callback](#com.fresvii.server.access.callbacks.account.SignUpUserCallback) to be informed about the result of the operation.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_server_access_AccountAccess_void_signUpUser_String_SignUpUserCallback"> signUpUser </a> ###



```
public static void signUpUser(String userName,  
                              SignUpUserCallback callback)
```



Signs up a new Fresvii user.
 Uses default values for description and profile picture.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|String userName|Name of the user.|
|[SignUpUserCallback](#com.fresvii.server.access.callbacks.account.SignUpUserCallback) callback|[Callback](#com.fresvii.server.access.callbacks.account.SignUpUserCallback) to be informed about the result of the operation.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_server_access_AccountAccess_void_signUpUser_String_String_Bitmap_SignUpUserCallback"> signUpUser </a> ###



```
public static void signUpUser(String userName,  
                              String description,  
                              Bitmap profileImageBitmap,  
                              SignUpUserCallback callback)
```



Signs up a new Fresvii user.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|String userName|Name of the user.|
|String description|Description of the user.|
|Bitmap profileImageBitmap|Profile picture of the user.|
|[SignUpUserCallback](#com.fresvii.server.access.callbacks.account.SignUpUserCallback) callback|[Callback](#com.fresvii.server.access.callbacks.account.SignUpUserCallback) to be informed about the result of the operation.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_server_access_AccountAccess_void_updateUser_String_String_Bitmap_UpdateUserCallback"> updateUser </a> ###



```
public static void updateUser(String updatedUserName,  
                              String updatedDescription,  
                              Bitmap updatedProfileImageBitmap,  
                              UpdateUserCallback callback)
```



Updates an existing Fresvii user with the specified new values.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|String updatedUserName|Updated name of the user.|
|String updatedDescription|Updated description of the user.|
|Bitmap updatedProfileImageBitmap|Updated profile picture of the user.|
|[UpdateUserCallback](#com.fresvii.server.access.callbacks.account.UpdateUserCallback) callback|[Callback](#com.fresvii.server.access.callbacks.account.UpdateUserCallback) to be informed about the result of the operation.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_server_access_AccountAccess_void_loginUser_LoginUserCallback"> loginUser </a> ###



```
public static void loginUser(LoginUserCallback callback)
```



Logs in the current user.
 Uses the default lifetime (1 day).



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|[LoginUserCallback](#com.fresvii.server.access.callbacks.account.LoginUserCallback) callback|[Callback](#com.fresvii.server.access.callbacks.account.LoginUserCallback) to be informed about the result of the operation.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_server_access_AccountAccess_void_loginUser_int_LoginUserCallback"> loginUser </a> ###



```
public static void loginUser(int lifetime,  
                             LoginUserCallback callback)
```



Logs in the current user.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|int lifetime|Timespan after which the session expires. Can be set from 10 seconds to 86400 seconds (1 day).|
|[LoginUserCallback](#com.fresvii.server.access.callbacks.account.LoginUserCallback) callback|[Callback](#com.fresvii.server.access.callbacks.account.LoginUserCallback) to be informed about the result of the operation.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_server_access_AccountAccess_void_refreshSession_RefreshSessionCallback"> refreshSession </a> ###



```
public static void refreshSession(RefreshSessionCallback callback)
```



Refreshes the session of the current user.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|RefreshSessionCallback callback|Callback to be informed about the result of the operation.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_server_access_AccountAccess_com_fresvii_components_FresviiCurrentUser_getCurrentLoggedInUser_"> getCurrentLoggedInUser </a> ###



```
public static com.fresvii.components.FresviiCurrentUser getCurrentLoggedInUser()
```



Convenience method to retrieve the current user's singleton object.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|FresviiCurrentUser|The current user.|




-------------------------



## <a name="com.fresvii.server.access.AccountAccess.UserAuthEvent"> Enum AccountAccess.UserAuthEvent </a> ##



```
public static final class AccountAccess.UserAuthEvent extends Enum
```

**Hierarchy:**  


```
java.lang.Object  
    java.lang.Enum  
        com.fresvii.server.access.AccountAccess.UserAuthEvent
```



**Description:**  
Events that inform about a user's authentication status




### Field Summary ###

|**Field**|**Description**|
|---|---|
|USER_SIGNED_UP|Event fired when user successfully signed up.|
|USER_LOGGED_IN|Event fired when user successfully logged in.|



### Method Summary ###



None.



### Method Detail ###



None.





-------------------------



## <a name="com.fresvii.server.access.AccountAccess.UserAuthEventListener"> Interface AccountAccess.UserAuthEventListener </a> ##



```
public static interface AccountAccess.UserAuthEventListener
```

**Hierarchy:**  


```
com.fresvii.server.access.AccountAccess.UserAuthEventListener
```



**Description:**  
Interface that application may implement to listen for [UserAuthEvents](#com.fresvii.server.access.AccountAccess.UserAuthEvent).




### Field Summary ###



None.




### Method Summary ###

|**Method**|**Description**|
|---|---|
|[public void onUserAuthEvent(String userId, AccountAccess.UserAuthEvent event)](#com_fresvii_server_access_AccountAccess_UserAuthEventListener_void_onUserAuthEvent_String_AccountAccess_UserAuthEvent)|Called when a UserAuthEvent occurs.|


### Method Detail ###




### <a name="com_fresvii_server_access_AccountAccess_UserAuthEventListener_void_onUserAuthEvent_String_AccountAccess_UserAuthEvent"> onUserAuthEvent </a> ###



```
public void onUserAuthEvent(String userId,  
                            AccountAccess.UserAuthEvent event)
```



Called when a UserAuthEvent occurs.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|String userId|ID of the user associated with the event.|
|[AccountAccess.UserAuthEvent](#com.fresvii.server.access.AccountAccess.UserAuthEvent) event|The event that occurred.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|




-------------------------



## <a name="com.fresvii.server.access.GroupAccess"> Class GroupAccess </a> ##



```
public class GroupAccess extends Object
```

**Hierarchy:**  


```
java.lang.Object  
    com.fresvii.server.access.GroupAccess
```



**Description:**  
Provides access to Fresvii Server's Group API.
 Can be used to create or delete groups, and add or remove members from groups, etc.



**Author:**  
Marcus Froeschl



**Version:**  
1.0



**Since:**  
2014-05-26




### Field Summary ###



None.




### Method Summary ###

|**Method**|**Description**|
|---|---|
|[public static void createMultiGroup(String name, CreateMultiGroupCallback callback)](#com_fresvii_server_access_GroupAccess_void_createMultiGroup_String_CreateMultiGroupCallback)|Creates a MultiGroup.|
|[public static void updateMultiGroup(String groupId, String name, UpdateMultiGroupCallback callback)](#com_fresvii_server_access_GroupAccess_void_updateMultiGroup_String_String_UpdateMultiGroupCallback)|Updates a MultiGroup.|
|[public static void deleteGroup(String groupId, DeleteGroupCallback callback)](#com_fresvii_server_access_GroupAccess_void_deleteGroup_String_DeleteGroupCallback)|Deletes a Group (MultiGroup or PairGroup).|
|[public static void subscribeToGroup(String groupId, SubscribeToGroupCallback callback)](#com_fresvii_server_access_GroupAccess_void_subscribeToGroup_String_SubscribeToGroupCallback)|Subscribes to a group (MultiGroup or PairGroup) in order to receive notifications from that group.|
|[public static void unsubscribeFromGroup(String groupId, UnsubscribeFromGroupCallback callback)](#com_fresvii_server_access_GroupAccess_void_unsubscribeFromGroup_String_UnsubscribeFromGroupCallback)|Unsubscribes from a group (MultiGroup or PairGroup) in order to no longer receive notifications from that group.|
|[public static void getGroups(GetGroupsCallback callback)](#com_fresvii_server_access_GroupAccess_void_getGroups_GetGroupsCallback)|Retrieves a list of Groups from the initial page.|
|[public static void getGroups(int page, GetGroupsCallback callback)](#com_fresvii_server_access_GroupAccess_void_getGroups_int_GetGroupsCallback)|Retrieves a list of MultiGroups from the specified page.|
|[public static void getMessageGroups(GetMessageGroupsCallback callback)](#com_fresvii_server_access_GroupAccess_void_getMessageGroups_GetMessageGroupsCallback)|Retrieves the first page of a list of all of the chats (MessageGroups) the user is involved in.|
|[public static void getMessageGroups(int page, GetMessageGroupsCallback callback)](#com_fresvii_server_access_GroupAccess_void_getMessageGroups_int_GetMessageGroupsCallback)|Retrieves a list of all of the chats (MessageGroups) the user is involved in.|
|[public static void getGroupMembers(String groupId, GetGroupMembersCallback callback)](#com_fresvii_server_access_GroupAccess_void_getGroupMembers_String_GetGroupMembersCallback)|Retrieves a list of members for a group from the initial page.|
|[public static void getGroupMembers(String groupId, int page, GetGroupMembersCallback callback)](#com_fresvii_server_access_GroupAccess_void_getGroupMembers_String_int_GetGroupMembersCallback)|Retrieves a list of members for a group from the specified page|
|[public static void addMemberToMultiGroup(String groupId, String userId, AddMemberToMultiGroupCallback callback)](#com_fresvii_server_access_GroupAccess_void_addMemberToMultiGroup_String_String_AddMemberToMultiGroupCallback)|Adds a member to a MultiGroup.|
|[public static void deleteMemberFromMultiGroup(String groupId, String userId, DeleteMemberFromMultiGroupCallback callback)](#com_fresvii_server_access_GroupAccess_void_deleteMemberFromMultiGroup_String_String_DeleteMemberFromMultiGroupCallback)|Deletes a member from a MultiGroup.|
|[public static void createPairGroup(String userId, CreatePairGroupCallback callback)](#com_fresvii_server_access_GroupAccess_void_createPairGroup_String_CreatePairGroupCallback)|Creates a PairGroup.|
|[public static void getGroupMessages(String groupId, GetGroupMessagesCallback callback)](#com_fresvii_server_access_GroupAccess_void_getGroupMessages_String_GetGroupMessagesCallback)|Retrieves the first page of a list of messages for a group|
|[public static void getGroupMessages(String groupId, int page, GetGroupMessagesCallback callback)](#com_fresvii_server_access_GroupAccess_void_getGroupMessages_String_int_GetGroupMessagesCallback)|Retrieves a list of messages for a group from the specified page|
|[public static void sendTextMessage(String groupId, String text, SendTextMessageCallback callback)](#com_fresvii_server_access_GroupAccess_void_sendTextMessage_String_String_SendTextMessageCallback)|Sends a text message to a group.|
|[public static void sendTextMessage(String groupId, String text, Date createdAt, SendTextMessageCallback callback)](#com_fresvii_server_access_GroupAccess_void_sendTextMessage_String_String_Date_SendTextMessageCallback)|Sends a text message to a group.|
|[public static void sendImageMessage(String groupId, Bitmap image, SendImageMessageCallback callback)](#com_fresvii_server_access_GroupAccess_void_sendImageMessage_String_Bitmap_SendImageMessageCallback)|Sends an image message to a group.|
|[public static void sendImageMessage(String groupId, Bitmap image, Date createdAt, SendImageMessageCallback callback)](#com_fresvii_server_access_GroupAccess_void_sendImageMessage_String_Bitmap_Date_SendImageMessageCallback)|Sends an image message to a group.|
|[public static void sendInGameMessage(String groupId, String text, SendInGameMessageCallback callback)](#com_fresvii_server_access_GroupAccess_void_sendInGameMessage_String_String_SendInGameMessageCallback)|Sends an ingame message to a group.|
|[public static void sendInGameMessage(String groupId, String text, Date createdAt, SendInGameMessageCallback callback)](#com_fresvii_server_access_GroupAccess_void_sendInGameMessage_String_String_Date_SendInGameMessageCallback)|Sends an ingame message to a group.|
|[public static void getGroupMessage(String groupId, String messageId, GetGroupMessageCallback callback)](#com_fresvii_server_access_GroupAccess_void_getGroupMessage_String_String_GetGroupMessageCallback)|Retrieves a specific group message|
|[public static void deleteGroupMessage(String groupId, String messageId, DeleteGroupMessageCallback callback)](#com_fresvii_server_access_GroupAccess_void_deleteGroupMessage_String_String_DeleteGroupMessageCallback)|Retrieves a specific group message|


### Method Detail ###




### <a name="com_fresvii_server_access_GroupAccess_void_createMultiGroup_String_CreateMultiGroupCallback"> createMultiGroup </a> ###



```
public static void createMultiGroup(String name,  
                                    CreateMultiGroupCallback callback)
```



Creates a MultiGroup.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|String name|Optional name for the group.|
|[CreateMultiGroupCallback](#com.fresvii.server.access.callbacks.group.CreateMultiGroupCallback) callback|[Callback](#com.fresvii.server.access.callbacks.group.CreateMultiGroupCallback) to be informed about the result of the operation.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_server_access_GroupAccess_void_updateMultiGroup_String_String_UpdateMultiGroupCallback"> updateMultiGroup </a> ###



```
public static void updateMultiGroup(String groupId,  
                                    String name,  
                                    UpdateMultiGroupCallback callback)
```



Updates a MultiGroup.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|String groupId|ID of the group to be deleted.|
|String name|Optional name for the group.|
|[UpdateMultiGroupCallback](#com.fresvii.server.access.callbacks.group.UpdateMultiGroupCallback) callback|[Callback](#com.fresvii.server.access.callbacks.group.UpdateMultiGroupCallback) to be informed about the result of the operation.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_server_access_GroupAccess_void_deleteGroup_String_DeleteGroupCallback"> deleteGroup </a> ###



```
public static void deleteGroup(String groupId,  
                               DeleteGroupCallback callback)
```



Deletes a Group (MultiGroup or PairGroup).



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|String groupId|ID of the group to be deleted.|
|[DeleteGroupCallback](#com.fresvii.server.access.callbacks.group.DeleteGroupCallback) callback|[Callback](#com.fresvii.server.access.callbacks.group.DeleteGroupCallback) to be informed about the result of the operation.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_server_access_GroupAccess_void_subscribeToGroup_String_SubscribeToGroupCallback"> subscribeToGroup </a> ###



```
public static void subscribeToGroup(String groupId,  
                                    SubscribeToGroupCallback callback)
```



Subscribes to a group (MultiGroup or PairGroup) in order to receive notifications from that group.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|String groupId|ID of the group to be subscribed.|
|[SubscribeToGroupCallback](#com.fresvii.server.access.callbacks.group.SubscribeToGroupCallback) callback|[Callback](#com.fresvii.server.access.callbacks.group.SubscribeToGroupCallback) to be informed about the result of the operation.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_server_access_GroupAccess_void_unsubscribeFromGroup_String_UnsubscribeFromGroupCallback"> unsubscribeFromGroup </a> ###



```
public static void unsubscribeFromGroup(String groupId,  
                                        UnsubscribeFromGroupCallback callback)
```



Unsubscribes from a group (MultiGroup or PairGroup) in order to no longer receive notifications from that group.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|String groupId|ID of the group to be unsubscribed.|
|[UnsubscribeFromGroupCallback](#com.fresvii.server.access.callbacks.group.UnsubscribeFromGroupCallback) callback|[Callback](#com.fresvii.server.access.callbacks.group.UnsubscribeFromGroupCallback) to be informed about the result of the operation.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_server_access_GroupAccess_void_getGroups_GetGroupsCallback"> getGroups </a> ###



```
public static void getGroups(GetGroupsCallback callback)
```



Retrieves a list of Groups from the initial page.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|[GetGroupsCallback](#com.fresvii.server.access.callbacks.group.GetGroupsCallback) callback|[Callback](#com.fresvii.server.access.callbacks.group.GetGroupsCallback) to be informed about the result of the operation.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_server_access_GroupAccess_void_getGroups_int_GetGroupsCallback"> getGroups </a> ###



```
public static void getGroups(int page,  
                             GetGroupsCallback callback)
```



Retrieves a list of MultiGroups from the specified page.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|int page|Page offset.|
|[GetGroupsCallback](#com.fresvii.server.access.callbacks.group.GetGroupsCallback) callback|[Callback](#com.fresvii.server.access.callbacks.group.GetGroupsCallback) to be informed about the result of the operation.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_server_access_GroupAccess_void_getMessageGroups_GetMessageGroupsCallback"> getMessageGroups </a> ###



```
public static void getMessageGroups(GetMessageGroupsCallback callback)
```



Retrieves the first page of a list of all of the chats (MessageGroups) the user is involved in.
 Also retrieves additional info such as the users involved in the chat, and the last message.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|[GetMessageGroupsCallback](#com.fresvii.server.access.callbacks.group.GetMessageGroupsCallback) callback|[Callback](#com.fresvii.server.access.callbacks.group.GetMessageGroupsCallback) to be informed about the result of the operation.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_server_access_GroupAccess_void_getMessageGroups_int_GetMessageGroupsCallback"> getMessageGroups </a> ###



```
public static void getMessageGroups(int page,  
                                    GetMessageGroupsCallback callback)
```



Retrieves a list of all of the chats (MessageGroups) the user is involved in.
 Also retrieves additional info such as the users involved in the chat, and the last message.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|int page|Page offset.|
|[GetMessageGroupsCallback](#com.fresvii.server.access.callbacks.group.GetMessageGroupsCallback) callback|[Callback](#com.fresvii.server.access.callbacks.group.GetMessageGroupsCallback) to be informed about the result of the operation.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_server_access_GroupAccess_void_getGroupMembers_String_GetGroupMembersCallback"> getGroupMembers </a> ###



```
public static void getGroupMembers(String groupId,  
                                   GetGroupMembersCallback callback)
```



Retrieves a list of members for a group from the initial page.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|String groupId|ID of the group who's members are to be retrieved.|
|[GetGroupMembersCallback](#com.fresvii.server.access.callbacks.group.GetGroupMembersCallback) callback|[Callback](#com.fresvii.server.access.callbacks.group.GetGroupMembersCallback) to be informed about the result of the operation.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_server_access_GroupAccess_void_getGroupMembers_String_int_GetGroupMembersCallback"> getGroupMembers </a> ###



```
public static void getGroupMembers(String groupId,  
                                   int page,  
                                   GetGroupMembersCallback callback)
```



Retrieves a list of members for a group from the specified page



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|String groupId|ID of the group who's members are to be retrieved.|
|int page|Page offset.|
|[GetGroupMembersCallback](#com.fresvii.server.access.callbacks.group.GetGroupMembersCallback) callback|[Callback](#com.fresvii.server.access.callbacks.group.GetGroupMembersCallback) to be informed about the result of the operation.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_server_access_GroupAccess_void_addMemberToMultiGroup_String_String_AddMemberToMultiGroupCallback"> addMemberToMultiGroup </a> ###



```
public static void addMemberToMultiGroup(String groupId,  
                                         String userId,  
                                         AddMemberToMultiGroupCallback callback)
```



Adds a member to a MultiGroup.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|String groupId|ID of the group to which the member should be added.|
|String userId|ID of the user to be added.|
|[AddMemberToMultiGroupCallback](#com.fresvii.server.access.callbacks.group.AddMemberToMultiGroupCallback) callback|[Callback](#com.fresvii.server.access.callbacks.group.AddMemberToMultiGroupCallback) to be informed about the result of the operation.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_server_access_GroupAccess_void_deleteMemberFromMultiGroup_String_String_DeleteMemberFromMultiGroupCallback"> deleteMemberFromMultiGroup </a> ###



```
public static void deleteMemberFromMultiGroup(String groupId,  
                                              String userId,  
                                              DeleteMemberFromMultiGroupCallback callback)
```



Deletes a member from a MultiGroup.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|String groupId|ID of the group from which the member should be deleted.|
|String userId|ID of the user to be deleted from the group.|
|[DeleteMemberFromMultiGroupCallback](#com.fresvii.server.access.callbacks.group.DeleteMemberFromMultiGroupCallback) callback|[Callback](#com.fresvii.server.access.callbacks.group.DeleteMemberFromMultiGroupCallback) to be informed about the result of the operation.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_server_access_GroupAccess_void_createPairGroup_String_CreatePairGroupCallback"> createPairGroup </a> ###



```
public static void createPairGroup(String userId,  
                                   CreatePairGroupCallback callback)
```



Creates a PairGroup.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|String userId|[Callback](#com.fresvii.server.access.callbacks.group.CreatePairGroupCallback) to be informed about the result of the operation.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_server_access_GroupAccess_void_getGroupMessages_String_GetGroupMessagesCallback"> getGroupMessages </a> ###



```
public static void getGroupMessages(String groupId,  
                                    GetGroupMessagesCallback callback)
```



Retrieves the first page of a list of messages for a group



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|String groupId|ID of the group who's messages are to be retrieved.|
|[GetGroupMessagesCallback](#com.fresvii.server.access.callbacks.group.GetGroupMessagesCallback) callback|[Callback](#com.fresvii.server.access.callbacks.group.GetGroupMessagesCallback) to be informed about the result of the operation.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_server_access_GroupAccess_void_getGroupMessages_String_int_GetGroupMessagesCallback"> getGroupMessages </a> ###



```
public static void getGroupMessages(String groupId,  
                                    int page,  
                                    GetGroupMessagesCallback callback)
```



Retrieves a list of messages for a group from the specified page



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|String groupId|ID of the group who's messages are to be retrieved.|
|int page|Page offset.|
|[GetGroupMessagesCallback](#com.fresvii.server.access.callbacks.group.GetGroupMessagesCallback) callback|[Callback](#com.fresvii.server.access.callbacks.group.GetGroupMessagesCallback) to be informed about the result of the operation.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_server_access_GroupAccess_void_sendTextMessage_String_String_SendTextMessageCallback"> sendTextMessage </a> ###



```
public static void sendTextMessage(String groupId,  
                                   String text,  
                                   SendTextMessageCallback callback)
```



Sends a text message to a group.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|String groupId|ID of the group.|
|String text|Text message.|
|[SendTextMessageCallback](#com.fresvii.server.access.callbacks.group.SendTextMessageCallback) callback|[Callback](#com.fresvii.server.access.callbacks.group.SendTextMessageCallback) to be informed about the result of the operation.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_server_access_GroupAccess_void_sendTextMessage_String_String_Date_SendTextMessageCallback"> sendTextMessage </a> ###



```
public static void sendTextMessage(String groupId,  
                                   String text,  
                                   Date createdAt,  
                                   SendTextMessageCallback callback)
```



Sends a text message to a group.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|String groupId|ID of the group.|
|String text|Text message.|
|Date createdAt|Date the text message was created (optional).|
|[SendTextMessageCallback](#com.fresvii.server.access.callbacks.group.SendTextMessageCallback) callback|[Callback](#com.fresvii.server.access.callbacks.group.SendTextMessageCallback) to be informed about the result of the operation.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_server_access_GroupAccess_void_sendImageMessage_String_Bitmap_SendImageMessageCallback"> sendImageMessage </a> ###



```
public static void sendImageMessage(String groupId,  
                                    Bitmap image,  
                                    SendImageMessageCallback callback)
```



Sends an image message to a group.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|String groupId|ID of the group.|
|Bitmap image|Image.|
|[SendImageMessageCallback](#com.fresvii.server.access.callbacks.group.SendImageMessageCallback) callback|[Callback](#com.fresvii.server.access.callbacks.group.SendImageMessageCallback) to be informed about the result of the operation.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_server_access_GroupAccess_void_sendImageMessage_String_Bitmap_Date_SendImageMessageCallback"> sendImageMessage </a> ###



```
public static void sendImageMessage(String groupId,  
                                    Bitmap image,  
                                    Date createdAt,  
                                    SendImageMessageCallback callback)
```



Sends an image message to a group.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|String groupId|ID of the group.|
|Bitmap image|Image.|
|Date createdAt|Date the image message was created (optional).|
|[SendImageMessageCallback](#com.fresvii.server.access.callbacks.group.SendImageMessageCallback) callback|[Callback](#com.fresvii.server.access.callbacks.group.SendImageMessageCallback) to be informed about the result of the operation.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_server_access_GroupAccess_void_sendInGameMessage_String_String_SendInGameMessageCallback"> sendInGameMessage </a> ###



```
public static void sendInGameMessage(String groupId,  
                                     String text,  
                                     SendInGameMessageCallback callback)
```



Sends an ingame message to a group.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|String groupId|ID of the group.|
|String text|Text message.|
|[SendInGameMessageCallback](#com.fresvii.server.access.callbacks.group.SendInGameMessageCallback) callback|[Callback](#com.fresvii.server.access.callbacks.group.SendTextMessageCallback) to be informed about the result of the operation.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_server_access_GroupAccess_void_sendInGameMessage_String_String_Date_SendInGameMessageCallback"> sendInGameMessage </a> ###



```
public static void sendInGameMessage(String groupId,  
                                     String text,  
                                     Date createdAt,  
                                     SendInGameMessageCallback callback)
```



Sends an ingame message to a group.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|String groupId|ID of the group.|
|String text|Text message.|
|Date createdAt|Date the ingame message was created (optional).|
|[SendInGameMessageCallback](#com.fresvii.server.access.callbacks.group.SendInGameMessageCallback) callback|[Callback](#com.fresvii.server.access.callbacks.group.SendInGameMessageCallback) to be informed about the result of the operation.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_server_access_GroupAccess_void_getGroupMessage_String_String_GetGroupMessageCallback"> getGroupMessage </a> ###



```
public static void getGroupMessage(String groupId,  
                                   String messageId,  
                                   GetGroupMessageCallback callback)
```



Retrieves a specific group message



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|String groupId|ID of the group who's message is to be retrieved.|
|String messageId|ID of the message to be retrieved.|
|[GetGroupMessageCallback](#com.fresvii.server.access.callbacks.group.GetGroupMessageCallback) callback|[Callback](#com.fresvii.server.access.callbacks.group.GetGroupMessageCallback) to be informed about the result of the operation.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_server_access_GroupAccess_void_deleteGroupMessage_String_String_DeleteGroupMessageCallback"> deleteGroupMessage </a> ###



```
public static void deleteGroupMessage(String groupId,  
                                      String messageId,  
                                      DeleteGroupMessageCallback callback)
```



Retrieves a specific group message



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|String groupId|ID of the group who's message is to be retrieved.|
|String messageId|ID of the message to be retrieved.|
|DeleteGroupMessageCallback callback|Callback to be informed about the result of the operation.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|




-------------------------



## <a name="com.fresvii.server.access.NotificationAccess"> Class NotificationAccess </a> ##



```
public class NotificationAccess extends Object
```

**Hierarchy:**  


```
java.lang.Object  
    com.fresvii.server.access.NotificationAccess
```



**Description:**  
Provides access to Fresvii Server's Notification API.
 Can be used to register or delete device tokens for receiving GCM notifications to/from the Fesvii server.



**Author:**  
matsushimakatsuhito, Marcus Froeschl



**Version:**  
1.1



**Since:**  
2014-02-18




### Field Summary ###



None.




### Method Summary ###

|**Method**|**Description**|
|---|---|
|[public static void addDeviceToken(AddDeviceTokenCallback callback)](#com_fresvii_server_access_NotificationAccess_void_addDeviceToken_AddDeviceTokenCallback)|Adds this device's GCM token to the Fresvii Server,|
|[public static void deleteDeviceToken(DeleteDeviceTokenCallback callback)](#com_fresvii_server_access_NotificationAccess_void_deleteDeviceToken_DeleteDeviceTokenCallback)|Deletes this device's GCM token from the Fresvii Server,|


### Method Detail ###




### <a name="com_fresvii_server_access_NotificationAccess_void_addDeviceToken_AddDeviceTokenCallback"> addDeviceToken </a> ###



```
public static void addDeviceToken(AddDeviceTokenCallback callback)
```



Adds this device's GCM token to the Fresvii Server,
 thus registering this device to receive GCM notifications.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|[AddDeviceTokenCallback](#com.fresvii.server.access.callbacks.notification.AddDeviceTokenCallback) callback|[Callback](#com.fresvii.server.access.callbacks.notification.AddDeviceTokenCallback) to be informed about the result of the operation.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_server_access_NotificationAccess_void_deleteDeviceToken_DeleteDeviceTokenCallback"> deleteDeviceToken </a> ###



```
public static void deleteDeviceToken(DeleteDeviceTokenCallback callback)
```



Deletes this device's GCM token from the Fresvii Server,
 thus unregistering this device so it no longer will receive GCM notifications.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|[DeleteDeviceTokenCallback](#com.fresvii.server.access.callbacks.notification.DeleteDeviceTokenCallback) callback|[Callback](#com.fresvii.server.access.callbacks.notification.DeleteDeviceTokenCallback) to be informed about the result of the operation.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|




-------------------------



## <a name="com.fresvii.server.access.SnsAccountAccess"> Class SnsAccountAccess </a> ##



```
public class SnsAccountAccess extends Object
```

**Hierarchy:**  


```
java.lang.Object  
    com.fresvii.server.access.SnsAccountAccess
```



**Description:**  
Provides access to Fresvii Server's SNS API.
 Can be used to register, delete, and retrieve login user SNS accounts.



**Author:**  
matsushimakatsuhito



**Version:**  
1.0



**Since:**  
2014-04-20




### Field Summary ###



None.




### Method Summary ###

|**Method**|**Description**|
|---|---|
|[public static void addUserSnsAccount(String provider, String uid, AddUserSnsAccountCallback callback)](#com_fresvii_server_access_SnsAccountAccess_void_addUserSnsAccount_String_String_AddUserSnsAccountCallback)|Adds an SNS account.|
|[public static void deleteUserSnsAccount(String snsAccountId, DeleteUserSnsAccountCallback callback)](#com_fresvii_server_access_SnsAccountAccess_void_deleteUserSnsAccount_String_DeleteUserSnsAccountCallback)|Deletes an SNS account.|
|[public static void getUserSnsAccounts(GetUserSnsAccountsCallback callback)](#com_fresvii_server_access_SnsAccountAccess_void_getUserSnsAccounts_GetUserSnsAccountsCallback)|Retrieves a list of SNS Accounts.|


### Method Detail ###




### <a name="com_fresvii_server_access_SnsAccountAccess_void_addUserSnsAccount_String_String_AddUserSnsAccountCallback"> addUserSnsAccount </a> ###



```
public static void addUserSnsAccount(String provider,  
                                     String uid,  
                                     AddUserSnsAccountCallback callback)
```



Adds an SNS account.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|String provider|Provider|
|String uid|UID|
|[AddUserSnsAccountCallback](#com.fresvii.server.access.callbacks.account.AddUserSnsAccountCallback) callback|[Callback](#com.fresvii.server.access.callbacks.account.AddUserSnsAccountCallback) to be informed about the result of the operation.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_server_access_SnsAccountAccess_void_deleteUserSnsAccount_String_DeleteUserSnsAccountCallback"> deleteUserSnsAccount </a> ###



```
public static void deleteUserSnsAccount(String snsAccountId,  
                                        DeleteUserSnsAccountCallback callback)
```



Deletes an SNS account.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|String snsAccountId|ID of the SNS Account to be deleted.|
|[DeleteUserSnsAccountCallback](#com.fresvii.server.access.callbacks.account.DeleteUserSnsAccountCallback) callback|Callback to be informed about the result of the operation.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_server_access_SnsAccountAccess_void_getUserSnsAccounts_GetUserSnsAccountsCallback"> getUserSnsAccounts </a> ###



```
public static void getUserSnsAccounts(GetUserSnsAccountsCallback callback)
```



Retrieves a list of SNS Accounts.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|[GetUserSnsAccountsCallback](#com.fresvii.server.access.callbacks.account.GetUserSnsAccountsCallback) callback|[Callback](#com.fresvii.server.access.callbacks.account.GetUserSnsAccountsCallback) to be informed about the result of the operation.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|




-------------------------



## <a name="com.fresvii.server.access.UserAccess"> Class UserAccess </a> ##



```
public class UserAccess extends Object
```

**Hierarchy:**  


```
java.lang.Object  
    com.fresvii.server.access.UserAccess
```



**Description:**  
Provides access to Fresvii Server's User API.
 Can be used to retrieve information on a specific user, or retrieve a list of users matching conditions.



**Author:**  
matsushimakatsuhito



**Version:**  
1.0



**Since:**  
2014-02-18




### Field Summary ###



None.




### Method Summary ###

|**Method**|**Description**|
|---|---|
|[public static void getUser(String userIdOrCode, GetUserCallback callback)](#com_fresvii_server_access_UserAccess_void_getUser_String_GetUserCallback)|Retrieves a specific user.|
|[public static void getUsers(String provider, String uid, GetUsersCallback callback)](#com_fresvii_server_access_UserAccess_void_getUsers_String_String_GetUsersCallback)|Retrieves a list of users that match providers and UID.|


### Method Detail ###




### <a name="com_fresvii_server_access_UserAccess_void_getUser_String_GetUserCallback"> getUser </a> ###



```
public static void getUser(String userIdOrCode,  
                           GetUserCallback callback)
```



Retrieves a specific user.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|String userIdOrCode|User ID or User code of the user to be retrieved.|
|[GetUserCallback](#com.fresvii.server.access.callbacks.user.GetUserCallback) callback|[Callback](#com.fresvii.server.access.callbacks.user.GetUserCallback) to be informed about the result of the operation.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_server_access_UserAccess_void_getUsers_String_String_GetUsersCallback"> getUsers </a> ###



```
public static void getUsers(String provider,  
                            String uid,  
                            GetUsersCallback callback)
```



Retrieves a list of users that match providers and UID.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|String provider|Provider|
|String uid|UID|
|[GetUsersCallback](#com.fresvii.server.access.callbacks.user.GetUsersCallback) callback|[Callback](#com.fresvii.server.access.callbacks.user.GetUsersCallback) to be informed about the result of the operation.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|




-------------------------



## <a name="com.fresvii.server.access.FriendAccess"> Class FriendAccess </a> ##



```
public class FriendAccess extends Object
```

**Hierarchy:**  


```
java.lang.Object  
    com.fresvii.server.access.FriendAccess
```



**Description:**  
Provides access to Fresvii Server's Friend API.
 Can be used to retrieve list of friends, request or remove friends, etc.



**Author:**  
Marcus Froeschl



**Version:**  
1.0



**Since:**  
2014-07-15




### Field Summary ###



None.




### Method Summary ###

|**Method**|**Description**|
|---|---|
|[public static void getFriends(GetFriendsCallback callback)](#com_fresvii_server_access_FriendAccess_void_getFriends_GetFriendsCallback)|Retrieves a list of Friends for the current user from the initial page.|
|[public static void getFriends(int page, GetFriendsCallback callback)](#com_fresvii_server_access_FriendAccess_void_getFriends_int_GetFriendsCallback)|Retrieves a list of Friends for the current user from the specified page.|
|[public static void getFriends(String userId, GetFriendsCallback callback)](#com_fresvii_server_access_FriendAccess_void_getFriends_String_GetFriendsCallback)|Retrieves a list of Friends for a specific user from the initial page.|
|[public static void getFriends(String userId, int page, GetFriendsCallback callback)](#com_fresvii_server_access_FriendAccess_void_getFriends_String_int_GetFriendsCallback)|Retrieves a list of Friends for a specific user from the specified page.|
|[public static void sendFriendRequest(String userId, SendFriendRequestCallback callback)](#com_fresvii_server_access_FriendAccess_void_sendFriendRequest_String_SendFriendRequestCallback)|Sends a friend request to a user|
|[public static void acceptFriendRequest(String userId, AcceptFriendRequestCallback callback)](#com_fresvii_server_access_FriendAccess_void_acceptFriendRequest_String_AcceptFriendRequestCallback)|Accepts a friend request from a user|
|[public static void hideFriendRequest(String userId, HideFriendRequestCallback callback)](#com_fresvii_server_access_FriendAccess_void_hideFriendRequest_String_HideFriendRequestCallback)|Hides a friend request from a user|
|[public static void getOutgoingFriendRequests(GetOutgoingFriendRequestsCallback callback)](#com_fresvii_server_access_FriendAccess_void_getOutgoingFriendRequests_GetOutgoingFriendRequestsCallback)|Retrieves a list of outgoing friend requests from the initial page.|
|[public static void getOutgoingFriendRequests(int page, GetOutgoingFriendRequestsCallback callback)](#com_fresvii_server_access_FriendAccess_void_getOutgoingFriendRequests_int_GetOutgoingFriendRequestsCallback)|Retrieves a list of outgoing friend requests from the specified page.|
|[public static void getIncomingFriendRequests(GetIncomingFriendRequestsCallback callback)](#com_fresvii_server_access_FriendAccess_void_getIncomingFriendRequests_GetIncomingFriendRequestsCallback)|Retrieves a list of incoming friend requests from the initial page.|
|[public static void getIncomingFriendRequests(int page, GetIncomingFriendRequestsCallback callback)](#com_fresvii_server_access_FriendAccess_void_getIncomingFriendRequests_int_GetIncomingFriendRequestsCallback)|Retrieves a list of incoming friend requests from the specified page.|
|[public static void unfriend(String userId, UnfriendCallback callback)](#com_fresvii_server_access_FriendAccess_void_unfriend_String_UnfriendCallback)|Unfriends a user.|


### Method Detail ###




### <a name="com_fresvii_server_access_FriendAccess_void_getFriends_GetFriendsCallback"> getFriends </a> ###



```
public static void getFriends(GetFriendsCallback callback)
```



Retrieves a list of Friends for the current user from the initial page.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|[GetFriendsCallback](#com.fresvii.server.access.callbacks.friends.GetFriendsCallback) callback|[Callback](#com.fresvii.server.access.callbacks.friends.GetFriendsCallback) to be informed about the result of the operation.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_server_access_FriendAccess_void_getFriends_int_GetFriendsCallback"> getFriends </a> ###



```
public static void getFriends(int page,  
                              GetFriendsCallback callback)
```



Retrieves a list of Friends for the current user from the specified page.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|int page|Page offset.|
|[GetFriendsCallback](#com.fresvii.server.access.callbacks.friends.GetFriendsCallback) callback|[Callback](#com.fresvii.server.access.callbacks.friends.GetFriendsCallback) to be informed about the result of the operation.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_server_access_FriendAccess_void_getFriends_String_GetFriendsCallback"> getFriends </a> ###



```
public static void getFriends(String userId,  
                              GetFriendsCallback callback)
```



Retrieves a list of Friends for a specific user from the initial page.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|String userId|ID of the user who's friends are to be retrieved.|
|[GetFriendsCallback](#com.fresvii.server.access.callbacks.friends.GetFriendsCallback) callback|[Callback](#com.fresvii.server.access.callbacks.friends.GetFriendsCallback) to be informed about the result of the operation.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_server_access_FriendAccess_void_getFriends_String_int_GetFriendsCallback"> getFriends </a> ###



```
public static void getFriends(String userId,  
                              int page,  
                              GetFriendsCallback callback)
```



Retrieves a list of Friends for a specific user from the specified page.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|String userId|ID of the user who's friends are to be retrieved.|
|int page|Page offset.|
|[GetFriendsCallback](#com.fresvii.server.access.callbacks.friends.GetFriendsCallback) callback|[Callback](#com.fresvii.server.access.callbacks.friends.GetFriendsCallback) to be informed about the result of the operation.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_server_access_FriendAccess_void_sendFriendRequest_String_SendFriendRequestCallback"> sendFriendRequest </a> ###



```
public static void sendFriendRequest(String userId,  
                                     SendFriendRequestCallback callback)
```



Sends a friend request to a user



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|String userId|ID of the user to send the friend request to.|
|[SendFriendRequestCallback](#com.fresvii.server.access.callbacks.friends.SendFriendRequestCallback) callback|[Callback](#com.fresvii.server.access.callbacks.friends.SendFriendRequestCallback) to be informed about the result of the operation.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_server_access_FriendAccess_void_acceptFriendRequest_String_AcceptFriendRequestCallback"> acceptFriendRequest </a> ###



```
public static void acceptFriendRequest(String userId,  
                                       AcceptFriendRequestCallback callback)
```



Accepts a friend request from a user



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|String userId|ID of the user who's friend request should be accepted.|
|[AcceptFriendRequestCallback](#com.fresvii.server.access.callbacks.friends.AcceptFriendRequestCallback) callback|[Callback](#com.fresvii.server.access.callbacks.friends.AcceptFriendRequestCallback) to be informed about the result of the operation.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_server_access_FriendAccess_void_hideFriendRequest_String_HideFriendRequestCallback"> hideFriendRequest </a> ###



```
public static void hideFriendRequest(String userId,  
                                     HideFriendRequestCallback callback)
```



Hides a friend request from a user



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|String userId|ID of the user who's friend request should be hidden.|
|[HideFriendRequestCallback](#com.fresvii.server.access.callbacks.friends.HideFriendRequestCallback) callback|[Callback](#com.fresvii.server.access.callbacks.friends.HideFriendRequestCallback) to be informed about the result of the operation.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_server_access_FriendAccess_void_getOutgoingFriendRequests_GetOutgoingFriendRequestsCallback"> getOutgoingFriendRequests </a> ###



```
public static void getOutgoingFriendRequests(GetOutgoingFriendRequestsCallback callback)
```



Retrieves a list of outgoing friend requests from the initial page.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|[GetOutgoingFriendRequestsCallback](#com.fresvii.server.access.callbacks.friends.GetOutgoingFriendRequestsCallback) callback|[Callback](#com.fresvii.server.access.callbacks.friends.GetOutgoingFriendRequestsCallback) to be informed about the result of the operation.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_server_access_FriendAccess_void_getOutgoingFriendRequests_int_GetOutgoingFriendRequestsCallback"> getOutgoingFriendRequests </a> ###



```
public static void getOutgoingFriendRequests(int page,  
                                             GetOutgoingFriendRequestsCallback callback)
```



Retrieves a list of outgoing friend requests from the specified page.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|int page|Page offset.|
|[GetOutgoingFriendRequestsCallback](#com.fresvii.server.access.callbacks.friends.GetOutgoingFriendRequestsCallback) callback|[Callback](#com.fresvii.server.access.callbacks.friends.GetOutgoingFriendRequestsCallback) to be informed about the result of the operation.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_server_access_FriendAccess_void_getIncomingFriendRequests_GetIncomingFriendRequestsCallback"> getIncomingFriendRequests </a> ###



```
public static void getIncomingFriendRequests(GetIncomingFriendRequestsCallback callback)
```



Retrieves a list of incoming friend requests from the initial page.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|[GetIncomingFriendRequestsCallback](#com.fresvii.server.access.callbacks.friends.GetIncomingFriendRequestsCallback) callback|[Callback](#com.fresvii.server.access.callbacks.friends.GetIncomingFriendRequestsCallback) to be informed about the result of the operation.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_server_access_FriendAccess_void_getIncomingFriendRequests_int_GetIncomingFriendRequestsCallback"> getIncomingFriendRequests </a> ###



```
public static void getIncomingFriendRequests(int page,  
                                             GetIncomingFriendRequestsCallback callback)
```



Retrieves a list of incoming friend requests from the specified page.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|int page|Page offset.|
|[GetIncomingFriendRequestsCallback](#com.fresvii.server.access.callbacks.friends.GetIncomingFriendRequestsCallback) callback|[Callback](#com.fresvii.server.access.callbacks.friends.GetIncomingFriendRequestsCallback) to be informed about the result of the operation.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_server_access_FriendAccess_void_unfriend_String_UnfriendCallback"> unfriend </a> ###



```
public static void unfriend(String userId,  
                            UnfriendCallback callback)
```



Unfriends a user.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|String userId|ID of the user to unfriend.|
|[UnfriendCallback](#com.fresvii.server.access.callbacks.friends.UnfriendCallback) callback|[Callback](#com.fresvii.server.access.callbacks.friends.UnfriendCallback) to be informed about the result of the operation.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|




-------------------------



## <a name="com.fresvii.server.access.callbacks.FailureCallback"> Interface FailureCallback </a> ##



```
public interface FailureCallback
```

**Hierarchy:**  


```
com.fresvii.server.access.callbacks.FailureCallback
```



**Description:**  
Callback interface to handle operation errors.



**Author:**  
Matthias Kollmer



**Version:**  
1.0




### Field Summary ###



None.




### Method Summary ###

|**Method**|**Description**|
|---|---|
|[public void onFailure(Throwable error)](#com_fresvii_server_access_callbacks_FailureCallback_void_onFailure_Throwable)|Callback invoked when the associated operation ended with an error.|


### Method Detail ###




### <a name="com_fresvii_server_access_callbacks_FailureCallback_void_onFailure_Throwable"> onFailure </a> ###



```
public void onFailure(Throwable error)
```



Callback invoked when the associated operation ended with an error.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|Throwable error|Error object.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|




-------------------------



## <a name="com.fresvii.server.access.callbacks.account.SignUpUserCallback"> Interface SignUpUserCallback </a> ##



```
public interface SignUpUserCallback implements FailureCallback
```

**Hierarchy:**  


```
com.fresvii.server.access.callbacks.account.SignUpUserCallback
```



**Description:**  
Callback interface to handle [AccountAccess.signUpUser()](#com_fresvii_server_access_AccountAccess_void_signUpUser_SignUpUserCallback) results.



**Author:**  
Matthias Kollmer



**Version:**  
1.0




### Field Summary ###



None.




### Method Summary ###

|**Method**|**Description**|
|---|---|
|[public void onSuccess(FresviiCurrentUser currentUser)](#com_fresvii_server_access_callbacks_account_SignUpUserCallback_void_onSuccess_FresviiCurrentUser)|Callback invoked when operation succeeds.|


### Method Detail ###




### <a name="com_fresvii_server_access_callbacks_account_SignUpUserCallback_void_onSuccess_FresviiCurrentUser"> onSuccess </a> ###



```
public void onSuccess(FresviiCurrentUser currentUser)
```



Callback invoked when operation succeeds.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|[FresviiCurrentUser](#com.fresvii.components.FresviiCurrentUser) currentUser|The user who was successfully signed in.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|




-------------------------



## <a name="com.fresvii.server.access.callbacks.account.UpdateUserCallback"> Interface UpdateUserCallback </a> ##



```
public interface UpdateUserCallback implements FailureCallback
```

**Hierarchy:**  


```
com.fresvii.server.access.callbacks.account.UpdateUserCallback
```



**Description:**  
Callback interface to handle [AccountAccess.updateUser()](#com_fresvii_server_access_AccountAccess_void_updateUser_String_String_Bitmap_UpdateUserCallback) results.



**Author:**  
Matthias Kollmer



**Version:**  
1.0




### Field Summary ###



None.




### Method Summary ###

|**Method**|**Description**|
|---|---|
|[public void onSuccess(FresviiCurrentUser currentUser)](#com_fresvii_server_access_callbacks_account_UpdateUserCallback_void_onSuccess_FresviiCurrentUser)|Callback invoked when operation succeeds.|


### Method Detail ###




### <a name="com_fresvii_server_access_callbacks_account_UpdateUserCallback_void_onSuccess_FresviiCurrentUser"> onSuccess </a> ###



```
public void onSuccess(FresviiCurrentUser currentUser)
```



Callback invoked when operation succeeds.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|[FresviiCurrentUser](#com.fresvii.components.FresviiCurrentUser) currentUser|The user who was successfully updated.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|




-------------------------



## <a name="com.fresvii.server.access.callbacks.account.LoginUserCallback"> Interface LoginUserCallback </a> ##



```
public interface LoginUserCallback implements FailureCallback
```

**Hierarchy:**  


```
com.fresvii.server.access.callbacks.account.LoginUserCallback
```



**Description:**  
Callback interface to handle [AccountAccess.loginUser()](#com_fresvii_server_access_AccountAccess_void_loginUser_LoginUserCallback)  results.



**Author:**  
Matthias Kollmer



**Version:**  
1.0




### Field Summary ###



None.




### Method Summary ###

|**Method**|**Description**|
|---|---|
|[public void onSuccess(FresviiCurrentUser currentUser)](#com_fresvii_server_access_callbacks_account_LoginUserCallback_void_onSuccess_FresviiCurrentUser)|Callback invoked when operation succeeds.|


### Method Detail ###




### <a name="com_fresvii_server_access_callbacks_account_LoginUserCallback_void_onSuccess_FresviiCurrentUser"> onSuccess </a> ###



```
public void onSuccess(FresviiCurrentUser currentUser)
```



Callback invoked when operation succeeds.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|[FresviiCurrentUser](#com.fresvii.components.FresviiCurrentUser) currentUser|The user who was successfully logged in.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|




-------------------------



## <a name="com.fresvii.server.access.callbacks.account.AddUserSnsAccountCallback"> Interface AddUserSnsAccountCallback </a> ##



```
public interface AddUserSnsAccountCallback implements FailureCallback
```

**Hierarchy:**  


```
com.fresvii.server.access.callbacks.account.AddUserSnsAccountCallback
```



**Description:**  
Callback interface to handle [SnsAccountAccess](#com.fresvii.server.access.SnsAccountAccess) results.



**Author:**  
Matthias Kollmer



**Version:**  
1.0




### Field Summary ###



None.




### Method Summary ###

|**Method**|**Description**|
|---|---|
|[public void onSuccess(FresviiSnsAccount snsAccount)](#com_fresvii_server_access_callbacks_account_AddUserSnsAccountCallback_void_onSuccess_FresviiSnsAccount)|Callback invoked when operation succeeds.|


### Method Detail ###




### <a name="com_fresvii_server_access_callbacks_account_AddUserSnsAccountCallback_void_onSuccess_FresviiSnsAccount"> onSuccess </a> ###



```
public void onSuccess(FresviiSnsAccount snsAccount)
```



Callback invoked when operation succeeds.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|




-------------------------



## <a name="com.fresvii.server.access.callbacks.account.DeleteUserSnsAccountCallback"> Interface DeleteUserSnsAccountCallback </a> ##



```
public interface DeleteUserSnsAccountCallback implements FailureCallback
```

**Hierarchy:**  


```
com.fresvii.server.access.callbacks.account.DeleteUserSnsAccountCallback
```



**Description:**  
Callback interface to handle [SnsAccountAccess](#com.fresvii.server.access.SnsAccountAccess) results.



**Author:**  
Matthias Kollmer



**Version:**  
1.0




### Field Summary ###



None.




### Method Summary ###

|**Method**|**Description**|
|---|---|
|[public void onSuccess()](#com_fresvii_server_access_callbacks_account_DeleteUserSnsAccountCallback_void_onSuccess_)|Callback invoked when operation succeeds.|


### Method Detail ###




### <a name="com_fresvii_server_access_callbacks_account_DeleteUserSnsAccountCallback_void_onSuccess_"> onSuccess </a> ###



```
public void onSuccess()
```



Callback invoked when operation succeeds.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|




-------------------------



## <a name="com.fresvii.server.access.callbacks.account.GetUserSnsAccountsCallback"> Interface GetUserSnsAccountsCallback </a> ##



```
public interface GetUserSnsAccountsCallback implements FailureCallback
```

**Hierarchy:**  


```
com.fresvii.server.access.callbacks.account.GetUserSnsAccountsCallback
```



**Description:**  
Callback interface to handle [SnsAccountAccess](#com.fresvii.server.access.SnsAccountAccess) results.



**Author:**  
Matthias Kollmer



**Version:**  
1.0




### Field Summary ###



None.




### Method Summary ###

|**Method**|**Description**|
|---|---|
|[public void onSuccess(List userSnsAccounts)](#com_fresvii_server_access_callbacks_account_GetUserSnsAccountsCallback_void_onSuccess_List)|Callback invoked when operation succeeds.|


### Method Detail ###




### <a name="com_fresvii_server_access_callbacks_account_GetUserSnsAccountsCallback_void_onSuccess_List"> onSuccess </a> ###



```
public void onSuccess(List userSnsAccounts)
```



Callback invoked when operation succeeds.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|




-------------------------



## <a name="com.fresvii.server.access.callbacks.group.CreateMultiGroupCallback"> Interface CreateMultiGroupCallback </a> ##



```
public interface CreateMultiGroupCallback implements FailureCallback
```

**Hierarchy:**  


```
com.fresvii.server.access.callbacks.group.CreateMultiGroupCallback
```



**Description:**  
Callback interface to handle [GroupAccess.createMultiGroup()](#com_fresvii_server_access_GroupAccess_void_createMultiGroup_String_CreateMultiGroupCallback) results.



**Author:**  
Marcus Froeschl



**Version:**  
1.0




### Field Summary ###



None.




### Method Summary ###

|**Method**|**Description**|
|---|---|
|[public void onSuccess(FresviiGroup group)](#com_fresvii_server_access_callbacks_group_CreateMultiGroupCallback_void_onSuccess_FresviiGroup)|Callback invoked when operation succeeds.|


### Method Detail ###




### <a name="com_fresvii_server_access_callbacks_group_CreateMultiGroupCallback_void_onSuccess_FresviiGroup"> onSuccess </a> ###



```
public void onSuccess(FresviiGroup group)
```



Callback invoked when operation succeeds.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|[FresviiGroup](#com.fresvii.components.FresviiGroup) group|The group that was created.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|




-------------------------



## <a name="com.fresvii.server.access.callbacks.group.CreatePairGroupCallback"> Interface CreatePairGroupCallback </a> ##



```
public interface CreatePairGroupCallback implements FailureCallback
```

**Hierarchy:**  


```
com.fresvii.server.access.callbacks.group.CreatePairGroupCallback
```



**Description:**  
Callback interface to handle [GroupAccess.createPairGroup()](#com_fresvii_server_access_GroupAccess_void_createPairGroup_String_CreatePairGroupCallback) results.



**Author:**  
Marcus Froeschl



**Version:**  
1.0




### Field Summary ###



None.




### Method Summary ###

|**Method**|**Description**|
|---|---|
|[public void onSuccess(FresviiGroup group)](#com_fresvii_server_access_callbacks_group_CreatePairGroupCallback_void_onSuccess_FresviiGroup)|Callback invoked when operation succeeds.|


### Method Detail ###




### <a name="com_fresvii_server_access_callbacks_group_CreatePairGroupCallback_void_onSuccess_FresviiGroup"> onSuccess </a> ###



```
public void onSuccess(FresviiGroup group)
```



Callback invoked when operation succeeds.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|[FresviiGroup](#com.fresvii.components.FresviiGroup) group|The group that was created.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|




-------------------------



## <a name="com.fresvii.server.access.callbacks.group.UpdateMultiGroupCallback"> Interface UpdateMultiGroupCallback </a> ##



```
public interface UpdateMultiGroupCallback implements FailureCallback
```

**Hierarchy:**  


```
com.fresvii.server.access.callbacks.group.UpdateMultiGroupCallback
```



**Description:**  
Callback interface to handle [GroupAccess.updateMultiGroup()](#com_fresvii_server_access_GroupAccess_void_updateMultiGroup_String_String_UpdateMultiGroupCallback) results.



**Author:**  
Marcus Froeschl



**Version:**  
1.0




### Field Summary ###



None.




### Method Summary ###

|**Method**|**Description**|
|---|---|
|[public void onSuccess(FresviiGroup group)](#com_fresvii_server_access_callbacks_group_UpdateMultiGroupCallback_void_onSuccess_FresviiGroup)|Callback invoked when operation succeeds.|


### Method Detail ###




### <a name="com_fresvii_server_access_callbacks_group_UpdateMultiGroupCallback_void_onSuccess_FresviiGroup"> onSuccess </a> ###



```
public void onSuccess(FresviiGroup group)
```



Callback invoked when operation succeeds.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|[FresviiGroup](#com.fresvii.components.FresviiGroup) group|The group that was updated.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|




-------------------------



## <a name="com.fresvii.server.access.callbacks.group.DeleteGroupCallback"> Interface DeleteGroupCallback </a> ##



```
public interface DeleteGroupCallback implements FailureCallback
```

**Hierarchy:**  


```
com.fresvii.server.access.callbacks.group.DeleteGroupCallback
```



**Description:**  
Callback interface to handle [GroupAccess.deleteGroup()](#com_fresvii_server_access_GroupAccess_void_deleteGroup_String_DeleteGroupCallback) results.



**Author:**  
Marcus Froeschl



**Version:**  
1.0




### Field Summary ###



None.




### Method Summary ###

|**Method**|**Description**|
|---|---|
|[public void onSuccess()](#com_fresvii_server_access_callbacks_group_DeleteGroupCallback_void_onSuccess_)|Callback invoked when operation succeeds.|


### Method Detail ###




### <a name="com_fresvii_server_access_callbacks_group_DeleteGroupCallback_void_onSuccess_"> onSuccess </a> ###



```
public void onSuccess()
```



Callback invoked when operation succeeds.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|




-------------------------



## <a name="com.fresvii.server.access.callbacks.group.DeleteMemberFromMultiGroupCallback"> Interface DeleteMemberFromMultiGroupCallback </a> ##



```
public interface DeleteMemberFromMultiGroupCallback implements FailureCallback
```

**Hierarchy:**  


```
com.fresvii.server.access.callbacks.group.DeleteMemberFromMultiGroupCallback
```



**Description:**  
Callback interface to handle [GroupAccess.deleteMemberFromMultiGroup()](#com_fresvii_server_access_GroupAccess_void_deleteMemberFromMultiGroup_String_String_DeleteMemberFromMultiGroupCallback) results.



**Author:**  
Marcus Froeschl



**Version:**  
1.0




### Field Summary ###



None.




### Method Summary ###

|**Method**|**Description**|
|---|---|
|[public void onSuccess()](#com_fresvii_server_access_callbacks_group_DeleteMemberFromMultiGroupCallback_void_onSuccess_)|Callback invoked when operation succeeds.|


### Method Detail ###




### <a name="com_fresvii_server_access_callbacks_group_DeleteMemberFromMultiGroupCallback_void_onSuccess_"> onSuccess </a> ###



```
public void onSuccess()
```



Callback invoked when operation succeeds.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|




-------------------------



## <a name="com.fresvii.server.access.callbacks.group.GetGroupsCallback"> Interface GetGroupsCallback </a> ##



```
public interface GetGroupsCallback implements FailureCallback
```

**Hierarchy:**  


```
com.fresvii.server.access.callbacks.group.GetGroupsCallback
```



**Description:**  
Callback interface to handle [GroupAccess.getGroups()](#com_fresvii_server_access_GroupAccess_void_getGroups_GetGroupsCallback) results.



**Author:**  
Marcus Froeschl



**Version:**  
1.0




### Field Summary ###



None.




### Method Summary ###

|**Method**|**Description**|
|---|---|
|[public void onSuccess(int currentPage, List groups, int totalCount, int perPage, int totalPages, int nextPage)](#com_fresvii_server_access_callbacks_group_GetGroupsCallback_void_onSuccess_int_List_int_int_int_int)|Callback invoked when operation succeeds.|


### Method Detail ###




### <a name="com_fresvii_server_access_callbacks_group_GetGroupsCallback_void_onSuccess_int_List_int_int_int_int"> onSuccess </a> ###



```
public void onSuccess(int currentPage,  
                      List groups,  
                      int totalCount,  
                      int perPage,  
                      int totalPages,  
                      int nextPage)
```



Callback invoked when operation succeeds.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|int currentPage|Index of the current page.|
|List groups|List of groups retrieved.|
|int totalCount|Total number of members.|
|int perPage|Number of members per page.|
|int totalPages|Total number of pages.|
|int nextPage|Index of the next page.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|




-------------------------



## <a name="com.fresvii.server.access.callbacks.group.GetGroupMembersCallback"> Interface GetGroupMembersCallback </a> ##



```
public interface GetGroupMembersCallback implements FailureCallback
```

**Hierarchy:**  


```
com.fresvii.server.access.callbacks.group.GetGroupMembersCallback
```



**Description:**  
Callback interface to handle [GroupAccess.getGroupMembers()](#com_fresvii_server_access_GroupAccess_void_getGroupMembers_String_int_GetGroupMembersCallback) results.



**Author:**  
Marcus Froeschl



**Version:**  
1.0




### Field Summary ###



None.




### Method Summary ###

|**Method**|**Description**|
|---|---|
|[public void onSuccess(int currentPage, List members, int totalCount, int perPage, int totalPages, int nextPage)](#com_fresvii_server_access_callbacks_group_GetGroupMembersCallback_void_onSuccess_int_List_int_int_int_int)|Callback invoked when operation succeeds.|


### Method Detail ###




### <a name="com_fresvii_server_access_callbacks_group_GetGroupMembersCallback_void_onSuccess_int_List_int_int_int_int"> onSuccess </a> ###



```
public void onSuccess(int currentPage,  
                      List members,  
                      int totalCount,  
                      int perPage,  
                      int totalPages,  
                      int nextPage)
```



Callback invoked when operation succeeds.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|int currentPage|Index of the current page.|
|List members|List of members retrieved.|
|int totalCount|Total number of members.|
|int perPage|Number of members per page.|
|int totalPages|Total number of pages.|
|int nextPage|Index of the next page.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|




-------------------------



## <a name="com.fresvii.server.access.callbacks.group.GetGroupMessageCallback"> Interface GetGroupMessageCallback </a> ##



```
public interface GetGroupMessageCallback implements FailureCallback
```

**Hierarchy:**  


```
com.fresvii.server.access.callbacks.group.GetGroupMessageCallback
```



**Description:**  
Callback interface to handle [GroupAccess.getGroupMessage()](#com_fresvii_server_access_GroupAccess_void_getGroupMessage_String_String_GetGroupMessageCallback) results.



**Author:**  
Marcus Froeschl



**Version:**  
1.0




### Field Summary ###



None.




### Method Summary ###

|**Method**|**Description**|
|---|---|
|[public void onSuccess(FresviiMessage message)](#com_fresvii_server_access_callbacks_group_GetGroupMessageCallback_void_onSuccess_FresviiMessage)|Callback invoked when operation succeeds.|


### Method Detail ###




### <a name="com_fresvii_server_access_callbacks_group_GetGroupMessageCallback_void_onSuccess_FresviiMessage"> onSuccess </a> ###



```
public void onSuccess(FresviiMessage message)
```



Callback invoked when operation succeeds.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|FresviiMessage message|The retrieved message.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|




-------------------------



## <a name="com.fresvii.server.access.callbacks.group.GetGroupMessagesCallback"> Interface GetGroupMessagesCallback </a> ##



```
public interface GetGroupMessagesCallback implements FailureCallback
```

**Hierarchy:**  


```
com.fresvii.server.access.callbacks.group.GetGroupMessagesCallback
```



**Description:**  
Callback interface to handle [GroupAccess.getGroupMessages()](#com_fresvii_server_access_GroupAccess_void_getGroupMessages_String_int_GetGroupMessagesCallback) results.



**Author:**  
Marcus Froeschl



**Version:**  
1.0




### Field Summary ###



None.




### Method Summary ###

|**Method**|**Description**|
|---|---|
|[public void onSuccess(int currentPage, List messages, int totalCount, int perPage, int totalPages, int nextPage)](#com_fresvii_server_access_callbacks_group_GetGroupMessagesCallback_void_onSuccess_int_List_int_int_int_int)|Callback invoked when operation succeeds.|


### Method Detail ###




### <a name="com_fresvii_server_access_callbacks_group_GetGroupMessagesCallback_void_onSuccess_int_List_int_int_int_int"> onSuccess </a> ###



```
public void onSuccess(int currentPage,  
                      List messages,  
                      int totalCount,  
                      int perPage,  
                      int totalPages,  
                      int nextPage)
```



Callback invoked when operation succeeds.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|int currentPage|Index of the current page.|
|List messages|List of messages retrieved.|
|int totalCount|Total number of members.|
|int perPage|Number of members per page.|
|int totalPages|Total number of pages.|
|int nextPage|Index of the next page.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|




-------------------------



## <a name="com.fresvii.server.access.callbacks.group.GetMessageGroupsCallback"> Interface GetMessageGroupsCallback </a> ##



```
public interface GetMessageGroupsCallback implements FailureCallback
```

**Hierarchy:**  


```
com.fresvii.server.access.callbacks.group.GetMessageGroupsCallback
```



**Description:**  
Callback interface to handle [GroupAccess.getMessageGroups()](#com_fresvii_server_access_GroupAccess_void_getMessageGroups_GetMessageGroupsCallback) results.



**Author:**  
Marcus Froeschl



**Version:**  
1.0




### Field Summary ###



None.




### Method Summary ###

|**Method**|**Description**|
|---|---|
|[public void onSuccess(int currentPage, List groups, int totalCount, int perPage, int totalPages, int nextPage)](#com_fresvii_server_access_callbacks_group_GetMessageGroupsCallback_void_onSuccess_int_List_int_int_int_int)|Callback invoked when operation succeeds.|


### Method Detail ###




### <a name="com_fresvii_server_access_callbacks_group_GetMessageGroupsCallback_void_onSuccess_int_List_int_int_int_int"> onSuccess </a> ###



```
public void onSuccess(int currentPage,  
                      List groups,  
                      int totalCount,  
                      int perPage,  
                      int totalPages,  
                      int nextPage)
```



Callback invoked when operation succeeds.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|int currentPage|Index of the current page.|
|List groups|List of groups with messages.|
|int totalCount|Total number of members.|
|int perPage|Number of members per page.|
|int totalPages|Total number of pages.|
|int nextPage|Index of the next page.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|




-------------------------



## <a name="com.fresvii.server.access.callbacks.group.AddMemberToMultiGroupCallback"> Interface AddMemberToMultiGroupCallback </a> ##



```
public interface AddMemberToMultiGroupCallback implements FailureCallback
```

**Hierarchy:**  


```
com.fresvii.server.access.callbacks.group.AddMemberToMultiGroupCallback
```



**Description:**  
Callback interface to handle [GroupAccess.addMemberToMultiGroup()](#com_fresvii_server_access_GroupAccess_void_addMemberToMultiGroup_String_String_AddMemberToMultiGroupCallback) results.



**Author:**  
Marcus Froeschl



**Version:**  
1.0




### Field Summary ###



None.




### Method Summary ###

|**Method**|**Description**|
|---|---|
|[public void onSuccess(FresviiGroup group)](#com_fresvii_server_access_callbacks_group_AddMemberToMultiGroupCallback_void_onSuccess_FresviiGroup)|Callback invoked when operation succeeds.|


### Method Detail ###




### <a name="com_fresvii_server_access_callbacks_group_AddMemberToMultiGroupCallback_void_onSuccess_FresviiGroup"> onSuccess </a> ###



```
public void onSuccess(FresviiGroup group)
```



Callback invoked when operation succeeds.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|[FresviiGroup](#com.fresvii.components.FresviiGroup) group|The group the member was added to.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|




-------------------------



## <a name="com.fresvii.server.access.callbacks.group.SendImageMessageCallback"> Interface SendImageMessageCallback </a> ##



```
public interface SendImageMessageCallback implements FailureCallback
```

**Hierarchy:**  


```
com.fresvii.server.access.callbacks.group.SendImageMessageCallback
```



**Description:**  
Callback interface to handle [GroupAccess.sendImageMessage()](#com_fresvii_server_access_GroupAccess_void_sendImageMessage_String_Bitmap_SendImageMessageCallback) results.



**Author:**  
Marcus Froeschl



**Version:**  
1.0




### Field Summary ###



None.




### Method Summary ###

|**Method**|**Description**|
|---|---|
|[public void onSuccess(FresviiMessage group)](#com_fresvii_server_access_callbacks_group_SendImageMessageCallback_void_onSuccess_FresviiMessage)|Callback invoked when operation succeeds.|


### Method Detail ###




### <a name="com_fresvii_server_access_callbacks_group_SendImageMessageCallback_void_onSuccess_FresviiMessage"> onSuccess </a> ###



```
public void onSuccess(FresviiMessage group)
```



Callback invoked when operation succeeds.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|FresviiMessage group|The group that was created.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|




-------------------------



## <a name="com.fresvii.server.access.callbacks.group.SendInGameMessageCallback"> Interface SendInGameMessageCallback </a> ##



```
public interface SendInGameMessageCallback implements FailureCallback
```

**Hierarchy:**  


```
com.fresvii.server.access.callbacks.group.SendInGameMessageCallback
```



**Description:**  
Callback interface to handle [GroupAccess.sendInGameMessage()](#com_fresvii_server_access_GroupAccess_void_sendInGameMessage_String_String_SendInGameMessageCallback) results.



**Author:**  
Marcus Froeschl



**Version:**  
1.0




### Field Summary ###



None.




### Method Summary ###

|**Method**|**Description**|
|---|---|
|[public void onSuccess(FresviiMessage message)](#com_fresvii_server_access_callbacks_group_SendInGameMessageCallback_void_onSuccess_FresviiMessage)|Callback invoked when operation succeeds.|


### Method Detail ###




### <a name="com_fresvii_server_access_callbacks_group_SendInGameMessageCallback_void_onSuccess_FresviiMessage"> onSuccess </a> ###



```
public void onSuccess(FresviiMessage message)
```



Callback invoked when operation succeeds.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|FresviiMessage message|The group that was created.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|




-------------------------



## <a name="com.fresvii.server.access.callbacks.group.SendTextMessageCallback"> Interface SendTextMessageCallback </a> ##



```
public interface SendTextMessageCallback implements FailureCallback
```

**Hierarchy:**  


```
com.fresvii.server.access.callbacks.group.SendTextMessageCallback
```



**Description:**  
Callback interface to handle [GroupAccess.sendTextMessage()](#com_fresvii_server_access_GroupAccess_void_sendTextMessage_String_String_SendTextMessageCallback) results.



**Author:**  
Marcus Froeschl



**Version:**  
1.0




### Field Summary ###



None.




### Method Summary ###

|**Method**|**Description**|
|---|---|
|[public void onSuccess(FresviiMessage group)](#com_fresvii_server_access_callbacks_group_SendTextMessageCallback_void_onSuccess_FresviiMessage)|Callback invoked when operation succeeds.|


### Method Detail ###




### <a name="com_fresvii_server_access_callbacks_group_SendTextMessageCallback_void_onSuccess_FresviiMessage"> onSuccess </a> ###



```
public void onSuccess(FresviiMessage group)
```



Callback invoked when operation succeeds.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|FresviiMessage group|The group that was created.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|




-------------------------



## <a name="com.fresvii.server.access.callbacks.group.SubscribeToGroupCallback"> Interface SubscribeToGroupCallback </a> ##



```
public interface SubscribeToGroupCallback implements FailureCallback
```

**Hierarchy:**  


```
com.fresvii.server.access.callbacks.group.SubscribeToGroupCallback
```



**Description:**  
Callback interface to handle [GroupAccess.subscribeToGroup()](#com_fresvii_server_access_GroupAccess_void_subscribeToGroup_String_SubscribeToGroupCallback) results.



**Author:**  
Marcus Froeschl



**Version:**  
1.0




### Field Summary ###



None.




### Method Summary ###

|**Method**|**Description**|
|---|---|
|[public void onSuccess(FresviiGroup group)](#com_fresvii_server_access_callbacks_group_SubscribeToGroupCallback_void_onSuccess_FresviiGroup)|Callback invoked when operation succeeds.|


### Method Detail ###




### <a name="com_fresvii_server_access_callbacks_group_SubscribeToGroupCallback_void_onSuccess_FresviiGroup"> onSuccess </a> ###



```
public void onSuccess(FresviiGroup group)
```



Callback invoked when operation succeeds.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|[FresviiGroup](#com.fresvii.components.FresviiGroup) group|The group that was subscribed.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|




-------------------------



## <a name="com.fresvii.server.access.callbacks.group.UnsubscribeFromGroupCallback"> Interface UnsubscribeFromGroupCallback </a> ##



```
public interface UnsubscribeFromGroupCallback implements FailureCallback
```

**Hierarchy:**  


```
com.fresvii.server.access.callbacks.group.UnsubscribeFromGroupCallback
```



**Description:**  
Callback interface to handle [GroupAccess.unsubscribeFromGroup()](#com_fresvii_server_access_GroupAccess_void_unsubscribeFromGroup_String_UnsubscribeFromGroupCallback) results.



**Author:**  
Marcus Froeschl



**Version:**  
1.0




### Field Summary ###



None.




### Method Summary ###

|**Method**|**Description**|
|---|---|
|[public void onSuccess(FresviiGroup group)](#com_fresvii_server_access_callbacks_group_UnsubscribeFromGroupCallback_void_onSuccess_FresviiGroup)|Callback invoked when operation succeeds.|


### Method Detail ###




### <a name="com_fresvii_server_access_callbacks_group_UnsubscribeFromGroupCallback_void_onSuccess_FresviiGroup"> onSuccess </a> ###



```
public void onSuccess(FresviiGroup group)
```



Callback invoked when operation succeeds.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|[FresviiGroup](#com.fresvii.components.FresviiGroup) group|The group that was unsubscribed.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|




-------------------------



## <a name="com.fresvii.server.access.callbacks.notification.AddDeviceTokenCallback"> Interface AddDeviceTokenCallback </a> ##



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




### Field Summary ###



None.




### Method Summary ###

|**Method**|**Description**|
|---|---|
|[public void onSuccess()](#com_fresvii_server_access_callbacks_notification_AddDeviceTokenCallback_void_onSuccess_)|Callback invoked when operation succeeds.|


### Method Detail ###




### <a name="com_fresvii_server_access_callbacks_notification_AddDeviceTokenCallback_void_onSuccess_"> onSuccess </a> ###



```
public void onSuccess()
```



Callback invoked when operation succeeds.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|




-------------------------



## <a name="com.fresvii.server.access.callbacks.notification.DeleteDeviceTokenCallback"> Interface DeleteDeviceTokenCallback </a> ##



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




### Field Summary ###



None.




### Method Summary ###

|**Method**|**Description**|
|---|---|
|[public void onSuccess()](#com_fresvii_server_access_callbacks_notification_DeleteDeviceTokenCallback_void_onSuccess_)|Callback invoked when operation succeeds.|


### Method Detail ###




### <a name="com_fresvii_server_access_callbacks_notification_DeleteDeviceTokenCallback_void_onSuccess_"> onSuccess </a> ###



```
public void onSuccess()
```



Callback invoked when operation succeeds.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|




-------------------------



## <a name="com.fresvii.server.access.callbacks.user.GetUserCallback"> Interface GetUserCallback </a> ##



```
public interface GetUserCallback implements FailureCallback
```

**Hierarchy:**  


```
com.fresvii.server.access.callbacks.user.GetUserCallback
```



**Description:**  
Callback interface to handle UserAccess.getUser() results.



**Author:**  
Matthias Kollmer



**Version:**  
1.0




### Field Summary ###



None.




### Method Summary ###

|**Method**|**Description**|
|---|---|
|[public void onSuccess(FresviiUser user)](#com_fresvii_server_access_callbacks_user_GetUserCallback_void_onSuccess_FresviiUser)|Callback invoked when operation succeeds.|


### Method Detail ###




### <a name="com_fresvii_server_access_callbacks_user_GetUserCallback_void_onSuccess_FresviiUser"> onSuccess </a> ###



```
public void onSuccess(FresviiUser user)
```



Callback invoked when operation succeeds.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|[FresviiUser](#com.fresvii.components.FresviiUser) user|The user retrieved.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|




-------------------------



## <a name="com.fresvii.server.access.callbacks.user.GetUsersCallback"> Interface GetUsersCallback </a> ##



```
public interface GetUsersCallback implements FailureCallback
```

**Hierarchy:**  


```
com.fresvii.server.access.callbacks.user.GetUsersCallback
```



**Description:**  
Callback interface to handle UserAccess.getUser() results.



**Author:**  
Matthias Kollmer



**Version:**  
1.0




### Field Summary ###



None.




### Method Summary ###

|**Method**|**Description**|
|---|---|
|[public void onSuccess(List users)](#com_fresvii_server_access_callbacks_user_GetUsersCallback_void_onSuccess_List)|Callback invoked when operation succeeds.|


### Method Detail ###




### <a name="com_fresvii_server_access_callbacks_user_GetUsersCallback_void_onSuccess_List"> onSuccess </a> ###



```
public void onSuccess(List users)
```



Callback invoked when operation succeeds.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|List users|The users retrieved.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|




-------------------------



## <a name="com.fresvii.server.access.callbacks.friends.GetFriendsCallback"> Interface GetFriendsCallback </a> ##



```
public interface GetFriendsCallback implements FailureCallback
```

**Hierarchy:**  


```
com.fresvii.server.access.callbacks.friends.GetFriendsCallback
```



**Description:**  
Callback interface to handle [FriendAccess.getFriends()](#com_fresvii_server_access_FriendAccess_void_getFriends_GetFriendsCallback) results.



**Author:**  
Marcus Froeschl



**Version:**  
1.0




### Field Summary ###



None.




### Method Summary ###

|**Method**|**Description**|
|---|---|
|[public void onSuccess(int currentPage, List friends, int totalCount, int perPage, int totalPages, int nextPage)](#com_fresvii_server_access_callbacks_friends_GetFriendsCallback_void_onSuccess_int_List_int_int_int_int)|Callback invoked when operation succeeds.|


### Method Detail ###




### <a name="com_fresvii_server_access_callbacks_friends_GetFriendsCallback_void_onSuccess_int_List_int_int_int_int"> onSuccess </a> ###



```
public void onSuccess(int currentPage,  
                      List friends,  
                      int totalCount,  
                      int perPage,  
                      int totalPages,  
                      int nextPage)
```



Callback invoked when operation succeeds.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|int currentPage|Index of the current page.|
|List friends|List of friends retrieved.|
|int totalCount|Total number of members.|
|int perPage|Number of members per page.|
|int totalPages|Total number of pages.|
|int nextPage|Index of the next page.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|




-------------------------



## <a name="com.fresvii.server.access.callbacks.friends.GetIncomingFriendRequestsCallback"> Interface GetIncomingFriendRequestsCallback </a> ##



```
public interface GetIncomingFriendRequestsCallback implements FailureCallback
```

**Hierarchy:**  


```
com.fresvii.server.access.callbacks.friends.GetIncomingFriendRequestsCallback
```



**Description:**  
Callback interface to handle [FriendAccess.getIncomingFriendRequests()](#com_fresvii_server_access_FriendAccess_void_getIncomingFriendRequests_GetIncomingFriendRequestsCallback) results.



**Author:**  
Marcus Froeschl



**Version:**  
1.0




### Field Summary ###



None.




### Method Summary ###

|**Method**|**Description**|
|---|---|
|[public void onSuccess(int currentPage, List friendRequests, int totalCount, int perPage, int totalPages, int nextPage)](#com_fresvii_server_access_callbacks_friends_GetIncomingFriendRequestsCallback_void_onSuccess_int_List_int_int_int_int)|Callback invoked when operation succeeds.|


### Method Detail ###




### <a name="com_fresvii_server_access_callbacks_friends_GetIncomingFriendRequestsCallback_void_onSuccess_int_List_int_int_int_int"> onSuccess </a> ###



```
public void onSuccess(int currentPage,  
                      List friendRequests,  
                      int totalCount,  
                      int perPage,  
                      int totalPages,  
                      int nextPage)
```



Callback invoked when operation succeeds.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|int currentPage|Index of the current page.|
|List friendRequests|List of friends retrieved.|
|int totalCount|Total number of members.|
|int perPage|Number of members per page.|
|int totalPages|Total number of pages.|
|int nextPage|Index of the next page.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|




-------------------------



## <a name="com.fresvii.server.access.callbacks.friends.GetOutgoingFriendRequestsCallback"> Interface GetOutgoingFriendRequestsCallback </a> ##



```
public interface GetOutgoingFriendRequestsCallback implements FailureCallback
```

**Hierarchy:**  


```
com.fresvii.server.access.callbacks.friends.GetOutgoingFriendRequestsCallback
```



**Description:**  
Callback interface to handle [FriendAccess.getOutgoingFriendRequests()](#com_fresvii_server_access_FriendAccess_void_getOutgoingFriendRequests_GetOutgoingFriendRequestsCallback) results.



**Author:**  
Marcus Froeschl



**Version:**  
1.0




### Field Summary ###



None.




### Method Summary ###

|**Method**|**Description**|
|---|---|
|[public void onSuccess(int currentPage, List friends, int totalCount, int perPage, int totalPages, int nextPage)](#com_fresvii_server_access_callbacks_friends_GetOutgoingFriendRequestsCallback_void_onSuccess_int_List_int_int_int_int)|Callback invoked when operation succeeds.|


### Method Detail ###




### <a name="com_fresvii_server_access_callbacks_friends_GetOutgoingFriendRequestsCallback_void_onSuccess_int_List_int_int_int_int"> onSuccess </a> ###



```
public void onSuccess(int currentPage,  
                      List friends,  
                      int totalCount,  
                      int perPage,  
                      int totalPages,  
                      int nextPage)
```



Callback invoked when operation succeeds.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|int currentPage|Index of the current page.|
|List friends|List of friends retrieved.|
|int totalCount|Total number of members.|
|int perPage|Number of members per page.|
|int totalPages|Total number of pages.|
|int nextPage|Index of the next page.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|




-------------------------



## <a name="com.fresvii.server.access.callbacks.friends.SendFriendRequestCallback"> Interface SendFriendRequestCallback </a> ##



```
public interface SendFriendRequestCallback implements FailureCallback
```

**Hierarchy:**  


```
com.fresvii.server.access.callbacks.friends.SendFriendRequestCallback
```



**Description:**  
Callback interface to handle [FriendAccess.sendFriendRequest()](#com_fresvii_server_access_FriendAccess_void_sendFriendRequest_String_SendFriendRequestCallback) results.



**Author:**  
Marcus Froeschl



**Version:**  
1.0




### Field Summary ###



None.




### Method Summary ###

|**Method**|**Description**|
|---|---|
|[public void onSuccess(FresviiUser user)](#com_fresvii_server_access_callbacks_friends_SendFriendRequestCallback_void_onSuccess_FresviiUser)|Callback invoked when operation succeeds.|


### Method Detail ###




### <a name="com_fresvii_server_access_callbacks_friends_SendFriendRequestCallback_void_onSuccess_FresviiUser"> onSuccess </a> ###



```
public void onSuccess(FresviiUser user)
```



Callback invoked when operation succeeds.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|[FresviiUser](#com.fresvii.components.FresviiUser) user|The user who's friendship was requested.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|




-------------------------



## <a name="com.fresvii.server.access.callbacks.friends.AcceptFriendRequestCallback"> Interface AcceptFriendRequestCallback </a> ##



```
public interface AcceptFriendRequestCallback implements FailureCallback
```

**Hierarchy:**  


```
com.fresvii.server.access.callbacks.friends.AcceptFriendRequestCallback
```



**Description:**  
Callback interface to handle [FriendAccess.acceptFriendRequest()](#com_fresvii_server_access_FriendAccess_void_acceptFriendRequest_String_AcceptFriendRequestCallback) results.



**Author:**  
Marcus Froeschl



**Version:**  
1.0




### Field Summary ###



None.




### Method Summary ###

|**Method**|**Description**|
|---|---|
|[public void onSuccess(FresviiUser user)](#com_fresvii_server_access_callbacks_friends_AcceptFriendRequestCallback_void_onSuccess_FresviiUser)|Callback invoked when operation succeeds.|


### Method Detail ###




### <a name="com_fresvii_server_access_callbacks_friends_AcceptFriendRequestCallback_void_onSuccess_FresviiUser"> onSuccess </a> ###



```
public void onSuccess(FresviiUser user)
```



Callback invoked when operation succeeds.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|[FresviiUser](#com.fresvii.components.FresviiUser) user|The friend who was accepted.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|




-------------------------



## <a name="com.fresvii.server.access.callbacks.friends.HideFriendRequestCallback"> Interface HideFriendRequestCallback </a> ##



```
public interface HideFriendRequestCallback implements FailureCallback
```

**Hierarchy:**  


```
com.fresvii.server.access.callbacks.friends.HideFriendRequestCallback
```



**Description:**  
Callback interface to handle [FriendAccess.hideFriendRequest()](#com_fresvii_server_access_FriendAccess_void_hideFriendRequest_String_HideFriendRequestCallback) results.



**Author:**  
Marcus Froeschl



**Version:**  
1.0




### Field Summary ###



None.




### Method Summary ###

|**Method**|**Description**|
|---|---|
|[public void onSuccess(FresviiUser user)](#com_fresvii_server_access_callbacks_friends_HideFriendRequestCallback_void_onSuccess_FresviiUser)|Callback invoked when operation succeeds.|


### Method Detail ###




### <a name="com_fresvii_server_access_callbacks_friends_HideFriendRequestCallback_void_onSuccess_FresviiUser"> onSuccess </a> ###



```
public void onSuccess(FresviiUser user)
```



Callback invoked when operation succeeds.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|[FresviiUser](#com.fresvii.components.FresviiUser) user|The friend who was hidden.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|




-------------------------



## <a name="com.fresvii.server.access.callbacks.friends.UnfriendCallback"> Interface UnfriendCallback </a> ##



```
public interface UnfriendCallback implements FailureCallback
```

**Hierarchy:**  


```
com.fresvii.server.access.callbacks.friends.UnfriendCallback
```



**Description:**  
Callback interface to handle [FriendAccess.unfriend()](#com_fresvii_server_access_FriendAccess_void_unfriend_String_UnfriendCallback) results.



**Author:**  
Marcus Froeschl



**Version:**  
1.0




### Field Summary ###



None.




### Method Summary ###

|**Method**|**Description**|
|---|---|
|[public void onSuccess()](#com_fresvii_server_access_callbacks_friends_UnfriendCallback_void_onSuccess_)|Callback invoked when operation succeeds.|


### Method Detail ###




### <a name="com_fresvii_server_access_callbacks_friends_UnfriendCallback_void_onSuccess_"> onSuccess </a> ###



```
public void onSuccess()
```



Callback invoked when operation succeeds.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|




-------------------------



## <a name="com.fresvii.gcm.GcmClient"> Class GcmClient </a> ##



```
public class GcmClient extends Object
```

**Hierarchy:**  


```
java.lang.Object  
    com.fresvii.gcm.GcmClient
```



**Description:**  
The GcmClient is used to register for and handle GMC notifications.
 If you wish to receive GCM notifications, e.g. for GroupChat, Forum updates etc. in your application, 
 you will have to properly start the GcmClient.



**Author:**  
Tetsuro Higuchi, Marcus Froeschl



**Version:**  
1.0



**Since:**  
2014-05-27




### Field Summary ###



None.




### Method Summary ###

|**Method**|**Description**|
|---|---|
|[public static com.fresvii.gcm.GcmClient getInstance()](#com_fresvii_gcm_GcmClient_com_fresvii_gcm_GcmClient_getInstance_)|Retrieves the instance of the singleton object. Use this to access the GcmClient.|
|[public void addGroupNotificationListener(GroupNotificationListener listener)](#com_fresvii_gcm_GcmClient_void_addGroupNotificationListener_GroupNotificationListener)|Application can add a [GroupNotificationListener](#com.fresvii.gcm.GroupNotificationListener) to be informed about custom GCM message notifications.|
|[public void removeGroupNotificationListener(GroupNotificationListener listener)](#com_fresvii_gcm_GcmClient_void_removeGroupNotificationListener_GroupNotificationListener)|Removes a [GroupNotificationListener](#com.fresvii.gcm.GroupNotificationListener).|
|[public void addFriendRequestNotificationListener(FriendRequestNotificationListener listener)](#com_fresvii_gcm_GcmClient_void_addFriendRequestNotificationListener_FriendRequestNotificationListener)|Application can add a [FriendRequestNotificationListener](#com.fresvii.gcm.FriendRequestNotificationListener) to be informed about custom GCM message notifications.|
|[public void removeFriendRequestNotificationListener(FriendRequestNotificationListener listener)](#com_fresvii_gcm_GcmClient_void_removeFriendRequestNotificationListener_FriendRequestNotificationListener)|Removes a [CustomNotificationListener](#com.fresvii.gcm.CustomNotificationListener).|
|[public void addForumNotificationListener(ForumNotificationListener listener)](#com_fresvii_gcm_GcmClient_void_addForumNotificationListener_ForumNotificationListener)|Application can add a [ForumNotificationListener](#com.fresvii.gcm.ForumNotificationListener) to be informed about custom GCM message notifications.|
|[public void removeForumNotificationListener(ForumNotificationListener listener)](#com_fresvii_gcm_GcmClient_void_removeForumNotificationListener_ForumNotificationListener)|Removes a [ForumNotificationListener](#com.fresvii.gcm.ForumNotificationListener).|
|[public void addVoiceChatNotificationListener(VoiceChatNotificationListener listener)](#com_fresvii_gcm_GcmClient_void_addVoiceChatNotificationListener_VoiceChatNotificationListener)|Application can add a [VoiceChatNotificationListener](#com.fresvii.gcm.VoiceChatNotificationListener) to be informed about custom GCM message notifications.|
|[public void removeCustomNotificationListener(VoiceChatNotificationListener listener)](#com_fresvii_gcm_GcmClient_void_removeCustomNotificationListener_VoiceChatNotificationListener)|Removes a [VoiceChatNotificationListener](#com.fresvii.gcm.VoiceChatNotificationListener).|
|[public void addCustomNotificationListener(String resource, CustomNotificationListener listener)](#com_fresvii_gcm_GcmClient_void_addCustomNotificationListener_String_CustomNotificationListener)|Application can add a [CustomNotificationListener](#com.fresvii.gcm.CustomNotificationListener) to be informed about custom GCM message notifications.|
|[public void removeCustomNotificationListener(String resource, CustomNotificationListener listener)](#com_fresvii_gcm_GcmClient_void_removeCustomNotificationListener_String_CustomNotificationListener)|Removes a [CustomNotificationListener](#com.fresvii.gcm.CustomNotificationListener).|
|[public void registerAndAddDeviceToken(String gcmSenderId)](#com_fresvii_gcm_GcmClient_void_registerAndAddDeviceToken_String)|Registers this device for GCM service, |


### Method Detail ###




### <a name="com_fresvii_gcm_GcmClient_com_fresvii_gcm_GcmClient_getInstance_"> getInstance </a> ###



```
public static com.fresvii.gcm.GcmClient getInstance()
```



Retrieves the instance of the singleton object. Use this to access the GcmClient.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|GcmClient|Instance of the singleton object.|



### <a name="com_fresvii_gcm_GcmClient_void_addGroupNotificationListener_GroupNotificationListener"> addGroupNotificationListener </a> ###



```
public void addGroupNotificationListener(GroupNotificationListener listener)
```



Application can add a [GroupNotificationListener](#com.fresvii.gcm.GroupNotificationListener) to be informed about custom GCM message notifications.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|[GroupNotificationListener](#com.fresvii.gcm.GroupNotificationListener) listener|[GroupNotificationListener](#com.fresvii.gcm.GroupNotificationListener).|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_gcm_GcmClient_void_removeGroupNotificationListener_GroupNotificationListener"> removeGroupNotificationListener </a> ###



```
public void removeGroupNotificationListener(GroupNotificationListener listener)
```



Removes a [GroupNotificationListener](#com.fresvii.gcm.GroupNotificationListener).



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|[GroupNotificationListener](#com.fresvii.gcm.GroupNotificationListener) listener|[GroupNotificationListener](#com.fresvii.gcm.GroupNotificationListener).|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_gcm_GcmClient_void_addFriendRequestNotificationListener_FriendRequestNotificationListener"> addFriendRequestNotificationListener </a> ###



```
public void addFriendRequestNotificationListener(FriendRequestNotificationListener listener)
```



Application can add a [FriendRequestNotificationListener](#com.fresvii.gcm.FriendRequestNotificationListener) to be informed about custom GCM message notifications.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|[FriendRequestNotificationListener](#com.fresvii.gcm.FriendRequestNotificationListener) listener|[FriendRequestNotificationListener](#com.fresvii.gcm.FriendRequestNotificationListener).|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_gcm_GcmClient_void_removeFriendRequestNotificationListener_FriendRequestNotificationListener"> removeFriendRequestNotificationListener </a> ###



```
public void removeFriendRequestNotificationListener(FriendRequestNotificationListener listener)
```



Removes a [CustomNotificationListener](#com.fresvii.gcm.CustomNotificationListener).



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|[FriendRequestNotificationListener](#com.fresvii.gcm.FriendRequestNotificationListener) listener|[CustomNotificationListener](#com.fresvii.gcm.CustomNotificationListener).|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_gcm_GcmClient_void_addForumNotificationListener_ForumNotificationListener"> addForumNotificationListener </a> ###



```
public void addForumNotificationListener(ForumNotificationListener listener)
```



Application can add a [ForumNotificationListener](#com.fresvii.gcm.ForumNotificationListener) to be informed about custom GCM message notifications.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|[ForumNotificationListener](#com.fresvii.gcm.ForumNotificationListener) listener|[ForumNotificationListener](#com.fresvii.gcm.ForumNotificationListener).|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_gcm_GcmClient_void_removeForumNotificationListener_ForumNotificationListener"> removeForumNotificationListener </a> ###



```
public void removeForumNotificationListener(ForumNotificationListener listener)
```



Removes a [ForumNotificationListener](#com.fresvii.gcm.ForumNotificationListener).



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|[ForumNotificationListener](#com.fresvii.gcm.ForumNotificationListener) listener|[ForumNotificationListener](#com.fresvii.gcm.ForumNotificationListener).|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_gcm_GcmClient_void_addVoiceChatNotificationListener_VoiceChatNotificationListener"> addVoiceChatNotificationListener </a> ###



```
public void addVoiceChatNotificationListener(VoiceChatNotificationListener listener)
```



Application can add a [VoiceChatNotificationListener](#com.fresvii.gcm.VoiceChatNotificationListener) to be informed about custom GCM message notifications.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|[VoiceChatNotificationListener](#com.fresvii.gcm.VoiceChatNotificationListener) listener|[VoiceChatNotificationListener](#com.fresvii.gcm.VoiceChatNotificationListener).|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_gcm_GcmClient_void_removeCustomNotificationListener_VoiceChatNotificationListener"> removeCustomNotificationListener </a> ###



```
public void removeCustomNotificationListener(VoiceChatNotificationListener listener)
```



Removes a [VoiceChatNotificationListener](#com.fresvii.gcm.VoiceChatNotificationListener).



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|[VoiceChatNotificationListener](#com.fresvii.gcm.VoiceChatNotificationListener) listener|[VoiceChatNotificationListener](#com.fresvii.gcm.VoiceChatNotificationListener).|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_gcm_GcmClient_void_addCustomNotificationListener_String_CustomNotificationListener"> addCustomNotificationListener </a> ###



```
public void addCustomNotificationListener(String resource,  
                                          CustomNotificationListener listener)
```



Application can add a [CustomNotificationListener](#com.fresvii.gcm.CustomNotificationListener) to be informed about custom GCM message notifications.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|String resource|The resource for which we should be listening for.|
|[CustomNotificationListener](#com.fresvii.gcm.CustomNotificationListener) listener|[CustomNotificationListener](#com.fresvii.gcm.CustomNotificationListener).|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_gcm_GcmClient_void_removeCustomNotificationListener_String_CustomNotificationListener"> removeCustomNotificationListener </a> ###



```
public void removeCustomNotificationListener(String resource,  
                                             CustomNotificationListener listener)
```



Removes a [CustomNotificationListener](#com.fresvii.gcm.CustomNotificationListener).



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|String resource|The resource for which we should no longer be listening for.|
|[CustomNotificationListener](#com.fresvii.gcm.CustomNotificationListener) listener|[CustomNotificationListener](#com.fresvii.gcm.CustomNotificationListener).|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_gcm_GcmClient_void_registerAndAddDeviceToken_String"> registerAndAddDeviceToken </a> ###



```
public void registerAndAddDeviceToken(String gcmSenderId)
```



Registers this device for GCM service, 
 and sends the device's GCM Registration ID to the Fresvii Server
 so that the application can receive GCM message notifications.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



#### GcmClient Example ####  

1. Add the following permissions to your *"AndroidManifest.xml"* file:

```
<uses-permission android:name="android.permission.WAKE_LOCK" />
<uses-permission android:name="com.google.android.c2dm.permission.RECEIVE" />

<permission
        android:name="com.example.gcm.permission.C2D_MESSAGE"
        android:protectionLevel="signature" />
<uses-permission android:name="com.example.gcm.permission.C2D_MESSAGE" />
<uses-permission android:name="com.example.gcm.c2dm.permission.RECEIVE" />
```

2. Add the following Receivers and Services to your *"AndroidManifest.xml"* file: 

```
<receiver
        android:name="com.fresvii.gcm.GcmBroadcastReceiver"
        android:permission="com.google.android.c2dm.permission.SEND" >
    <intent-filter>
        <action android:name="com.google.android.c2dm.intent.RECEIVE" />
        <category android:name="com.example.gcm" />
    </intent-filter>
</receiver>

<service android:name="com.fresvii.gcm.GcmIntentService" />
```
    
3. Implement the *UserAuthEventListener* interface, e.g. in your Activity. Then register the *GcmClient* in the  *onUserAuthEvent()* method in order to receive GCM notifications:

```
public class MyActivity extends Activity implements UserAuthEventListener {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        // Any application *must* call Fresvii.start() in order to work with the Fresvii Android SDK
        Fresvii.start(super.getApplicationContext(), MainActivity.getAppropriateAppId(), APP_NAME, false, false);
    
        // Add a UserAuthEventListener
        AccountAccess.addUserAuthEventListener(this);
    
        ...
    }

    @Override
    public void onUserAuthEvent(String userId, UserAuthEvent event) {
        if ( event == UserAuthEvent.USER_SIGNED_UP ) {
            try {
                // Application *may* initialize GCM client if it wants to receive GCM notifications from Fresvii server
                // We have to be *logged in* to do this
                GcmClient.getInstance().registerAndAddDeviceToken(MY_GCM_SENDER_ID);
            } catch ( InvalidParameterException e ) {
                ManagedLog.e(LOG_MODULE, "Invalid parameter");
            }
        }
    }
    
    ...
}
```





-------------------------



## <a name="com.fresvii.gcm.GroupNotificationListener"> Interface GroupNotificationListener </a> ##



```
public interface GroupNotificationListener
```

**Hierarchy:**  


```
com.fresvii.gcm.GroupNotificationListener
```



**Description:**  
Application may implement this interface to handle group GCM notifications.



**Author:**  
Marcus Froeschl



**Version:**  
1.0



**Since:**  
2014-07-20




### Field Summary ###



None.




### Method Summary ###

|**Method**|**Description**|
|---|---|
|[public void onGroupTextMessage(FresviiMessage message, FresviiGcmMessage fresviiGcmMessage)](#com_fresvii_gcm_GroupNotificationListener_void_onGroupTextMessage_FresviiMessage_FresviiGcmMessage)|Called when a Group Text Message Notification is received.|
|[public void onGroupImageMessage(FresviiMessage message, FresviiGcmMessage fresviiGcmMessage)](#com_fresvii_gcm_GroupNotificationListener_void_onGroupImageMessage_FresviiMessage_FresviiGcmMessage)|Called when a Group Image Message Notification is received.|
|[public void onGroupInGameMessage(FresviiMessage message, FresviiGcmMessage fresviiGcmMessage)](#com_fresvii_gcm_GroupNotificationListener_void_onGroupInGameMessage_FresviiMessage_FresviiGcmMessage)|Called when a Group InGame Message Notification is received.|


### Method Detail ###




### <a name="com_fresvii_gcm_GroupNotificationListener_void_onGroupTextMessage_FresviiMessage_FresviiGcmMessage"> onGroupTextMessage </a> ###



```
public void onGroupTextMessage(FresviiMessage message,  
                               FresviiGcmMessage fresviiGcmMessage)
```



Called when a Group Text Message Notification is received.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|FresviiMessage message|The text message associated with the event.|
|[FresviiGcmMessage](#com.fresvii.gcm.FresviiGcmMessage) fresviiGcmMessage|The full original GCM message if application wishes to do more detailed parsing.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_gcm_GroupNotificationListener_void_onGroupImageMessage_FresviiMessage_FresviiGcmMessage"> onGroupImageMessage </a> ###



```
public void onGroupImageMessage(FresviiMessage message,  
                                FresviiGcmMessage fresviiGcmMessage)
```



Called when a Group Image Message Notification is received.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|FresviiMessage message|The image message associated with the event.|
|[FresviiGcmMessage](#com.fresvii.gcm.FresviiGcmMessage) fresviiGcmMessage|The full original GCM message if application wishes to do more detailed parsing.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_gcm_GroupNotificationListener_void_onGroupInGameMessage_FresviiMessage_FresviiGcmMessage"> onGroupInGameMessage </a> ###



```
public void onGroupInGameMessage(FresviiMessage message,  
                                 FresviiGcmMessage fresviiGcmMessage)
```



Called when a Group InGame Message Notification is received.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|FresviiMessage message|The ingame message associated with the event.|
|[FresviiGcmMessage](#com.fresvii.gcm.FresviiGcmMessage) fresviiGcmMessage|The full original GCM message if application wishes to do more detailed parsing.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|




-------------------------



## <a name="com.fresvii.gcm.FriendRequestNotificationListener"> Interface FriendRequestNotificationListener </a> ##



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




### Field Summary ###



None.




### Method Summary ###

|**Method**|**Description**|
|---|---|
|[public void onNewFriendRequest(FresviiUser user, FresviiGcmMessage fresviiGcmMessage)](#com_fresvii_gcm_FriendRequestNotificationListener_void_onNewFriendRequest_FresviiUser_FresviiGcmMessage)|Called when a new Friend Request is received.|
|[public void onFriendRequestUpdated(FresviiUser user, FresviiGcmMessage fresviiGcmMessage)](#com_fresvii_gcm_FriendRequestNotificationListener_void_onFriendRequestUpdated_FresviiUser_FresviiGcmMessage)|Called when an existing Friend Request was updated.|


### Method Detail ###




### <a name="com_fresvii_gcm_FriendRequestNotificationListener_void_onNewFriendRequest_FresviiUser_FresviiGcmMessage"> onNewFriendRequest </a> ###



```
public void onNewFriendRequest(FresviiUser user,  
                               FresviiGcmMessage fresviiGcmMessage)
```



Called when a new Friend Request is received.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|[FresviiUser](#com.fresvii.components.FresviiUser) user|The user who requests to be our friend.|
|[FresviiGcmMessage](#com.fresvii.gcm.FresviiGcmMessage) fresviiGcmMessage|The full original GCM message if application wishes to do more detailed parsing.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_gcm_FriendRequestNotificationListener_void_onFriendRequestUpdated_FresviiUser_FresviiGcmMessage"> onFriendRequestUpdated </a> ###



```
public void onFriendRequestUpdated(FresviiUser user,  
                                   FresviiGcmMessage fresviiGcmMessage)
```



Called when an existing Friend Request was updated.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|[FresviiUser](#com.fresvii.components.FresviiUser) user|The user who requests to be our friend.|
|[FresviiGcmMessage](#com.fresvii.gcm.FresviiGcmMessage) fresviiGcmMessage|The full original GCM message if application wishes to do more detailed parsing.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|




-------------------------



## <a name="com.fresvii.gcm.ForumNotificationListener"> Interface ForumNotificationListener </a> ##



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




### Field Summary ###



None.




### Method Summary ###

|**Method**|**Description**|
|---|---|
|[public void onNewForumComment(FresviiForumComment comment, FresviiGcmMessage fresviiGcmMessage)](#com_fresvii_gcm_ForumNotificationListener_void_onNewForumComment_FresviiForumComment_FresviiGcmMessage)|Called when a new comment was written to a Fresvii forum thread you are subscribed to.|


### Method Detail ###




### <a name="com_fresvii_gcm_ForumNotificationListener_void_onNewForumComment_FresviiForumComment_FresviiGcmMessage"> onNewForumComment </a> ###



```
public void onNewForumComment(FresviiForumComment comment,  
                              FresviiGcmMessage fresviiGcmMessage)
```



Called when a new comment was written to a Fresvii forum thread you are subscribed to.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|FresviiForumComment comment|The new forum comment.|
|[FresviiGcmMessage](#com.fresvii.gcm.FresviiGcmMessage) fresviiGcmMessage|The full original GCM message if application wishes to do more detailed parsing.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|




-------------------------



## <a name="com.fresvii.gcm.VoiceChatNotificationListener"> Interface VoiceChatNotificationListener </a> ##



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




### Field Summary ###



None.




### Method Summary ###

|**Method**|**Description**|
|---|---|
|[public void onConferenceCreated(FresviiConference conference, FresviiGcmMessage fresviiGcmMessage)](#com_fresvii_gcm_VoiceChatNotificationListener_void_onConferenceCreated_FresviiConference_FresviiGcmMessage)|Called when a new VoiceChat conference was created. |


### Method Detail ###




### <a name="com_fresvii_gcm_VoiceChatNotificationListener_void_onConferenceCreated_FresviiConference_FresviiGcmMessage"> onConferenceCreated </a> ###



```
public void onConferenceCreated(FresviiConference conference,  
                                FresviiGcmMessage fresviiGcmMessage)
```



Called when a new VoiceChat conference was created. 
 This means you have been invited to a VoiceChat conference. 
 By default, Fresvii SDK will automatically handle VoiceChat invitations, so the application normally does not have to handle this invitation.
 However, application may call [Fresvii.setIncomingVoiceChatBehavior()](#com_fresvii_Fresvii_void_setIncomingVoiceChatBehavior_Fresvii_IncomingVoiceChatBehavior) to change this behavior,
 and handle VoiceChat invitations here.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|FresviiConference conference|The conference that was created.|
|[FresviiGcmMessage](#com.fresvii.gcm.FresviiGcmMessage) fresviiGcmMessage|The full original GCM message if application wishes to do more detailed parsing.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|




-------------------------



## <a name="com.fresvii.gcm.CustomNotificationListener"> Interface CustomNotificationListener </a> ##



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




### Field Summary ###



None.




### Method Summary ###

|**Method**|**Description**|
|---|---|
|[public void onCustomMessage(FresviiGcmMessage fresviiGcmMessage)](#com_fresvii_gcm_CustomNotificationListener_void_onCustomMessage_FresviiGcmMessage)|Called when a custom GCM notification message was received.|


### Method Detail ###




### <a name="com_fresvii_gcm_CustomNotificationListener_void_onCustomMessage_FresviiGcmMessage"> onCustomMessage </a> ###



```
public void onCustomMessage(FresviiGcmMessage fresviiGcmMessage)
```



Called when a custom GCM notification message was received.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|[FresviiGcmMessage](#com.fresvii.gcm.FresviiGcmMessage) fresviiGcmMessage|The custom message that was received.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|




-------------------------



## <a name="com.fresvii.voicechat.VoiceChatConference"> Class VoiceChatConference </a> ##



```
public class VoiceChatConference extends Object
```

**Hierarchy:**  


```
java.lang.Object  
    com.fresvii.voicechat.VoiceChatConference
```



**Description:**  
Class used to manage a VoiceChat conference.
 There can be only 1 conference at a time.



**Author:**  
Marcus Froeschl



**Version:**  
1.0



**Since:**  
2014-05-20




### Field Summary ###



None.




### Method Summary ###

|**Method**|**Description**|
|---|---|
|[public static com.fresvii.voicechat.VoiceChatConference getInstance()](#com_fresvii_voicechat_VoiceChatConference_com_fresvii_voicechat_VoiceChatConference_getInstance_)|Retrieves the instance of the singleton object. Use this to access the VoiceChatConference.|
|[public void addVoiceChatConferenceListener(VoiceChatConferenceListener listener)](#com_fresvii_voicechat_VoiceChatConference_void_addVoiceChatConferenceListener_VoiceChatConferenceListener)|Application can add a [VoiceChatConferenceListener](#com.fresvii.voicechat.VoiceChatConferenceListener) to be informed about VoiceChatConference events|
|[public void removeVoiceChatConferenceListener(VoiceChatConferenceListener listener)](#com_fresvii_voicechat_VoiceChatConference_void_removeVoiceChatConferenceListener_VoiceChatConferenceListener)|Removes a [VoiceChatConferenceListener](#com.fresvii.voicechat.VoiceChatConferenceListener).|
|[public void doesConferenceExist(String groupId, DoesConferenceExistCallback callback)](#com_fresvii_voicechat_VoiceChatConference_void_doesConferenceExist_String_DoesConferenceExistCallback)|Checks if a conference for this group already exists on the Fresvii server|
|[public void host(String groupId, VoiceChatConferenceCallback hostCallback)](#com_fresvii_voicechat_VoiceChatConference_void_host_String_VoiceChatConferenceCallback)|Hosts a conference.|
|[public void join(String groupId, String hostId, VoiceChatConferenceCallback joinCallback)](#com_fresvii_voicechat_VoiceChatConference_void_join_String_String_VoiceChatConferenceCallback)|Joins a conference.|
|[public void leave(VoiceChatConferenceCallback leaveCallback)](#com_fresvii_voicechat_VoiceChatConference_void_leave_VoiceChatConferenceCallback)|Leaves the voicechat conference.|
|[public void addGuest(String guestId, VoiceChatConferenceCallback addGuestCallback)](#com_fresvii_voicechat_VoiceChatConference_void_addGuest_String_VoiceChatConferenceCallback)|Adds a guest to the conference.|
|[public void removeGuest(String guestId, VoiceChatConferenceCallback removeGuestCallback)](#com_fresvii_voicechat_VoiceChatConference_void_removeGuest_String_VoiceChatConferenceCallback)|Removes a guest from the conference.|
|[public void mute(VoiceChatConferenceCallback muteCallback)](#com_fresvii_voicechat_VoiceChatConference_void_mute_VoiceChatConferenceCallback)|Mutes the conference.|
|[public void unmute(VoiceChatConferenceCallback unmuteCallback)](#com_fresvii_voicechat_VoiceChatConference_void_unmute_VoiceChatConferenceCallback)|Unmutes the conference.|


### Method Detail ###




### <a name="com_fresvii_voicechat_VoiceChatConference_com_fresvii_voicechat_VoiceChatConference_getInstance_"> getInstance </a> ###



```
public static com.fresvii.voicechat.VoiceChatConference getInstance()
```



Retrieves the instance of the singleton object. Use this to access the VoiceChatConference.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|VoiceChatConference|Instance of the singleton object.|



### <a name="com_fresvii_voicechat_VoiceChatConference_void_addVoiceChatConferenceListener_VoiceChatConferenceListener"> addVoiceChatConferenceListener </a> ###



```
public void addVoiceChatConferenceListener(VoiceChatConferenceListener listener)
```



Application can add a [VoiceChatConferenceListener](#com.fresvii.voicechat.VoiceChatConferenceListener) to be informed about VoiceChatConference events



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|[VoiceChatConferenceListener](#com.fresvii.voicechat.VoiceChatConferenceListener) listener|[VoiceChatConferenceListener](#com.fresvii.voicechat.VoiceChatConferenceListener) to be informed about VoiceChatConference events.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_voicechat_VoiceChatConference_void_removeVoiceChatConferenceListener_VoiceChatConferenceListener"> removeVoiceChatConferenceListener </a> ###



```
public void removeVoiceChatConferenceListener(VoiceChatConferenceListener listener)
```



Removes a [VoiceChatConferenceListener](#com.fresvii.voicechat.VoiceChatConferenceListener).



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|[VoiceChatConferenceListener](#com.fresvii.voicechat.VoiceChatConferenceListener) listener|[VoiceChatConferenceListener](#com.fresvii.voicechat.VoiceChatConferenceListener) to be removed.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_voicechat_VoiceChatConference_void_doesConferenceExist_String_DoesConferenceExistCallback"> doesConferenceExist </a> ###



```
public void doesConferenceExist(String groupId,  
                                DoesConferenceExistCallback callback)
```



Checks if a conference for this group already exists on the Fresvii server



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|String groupId|Fresvii groupId|
|DoesConferenceExistCallback callback|Callback to be informed about the result of the operation.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_voicechat_VoiceChatConference_void_host_String_VoiceChatConferenceCallback"> host </a> ###



```
public void host(String groupId,  
                 VoiceChatConferenceCallback hostCallback)
```



Hosts a conference.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|String groupId|Fresvii groupId|
|[VoiceChatConferenceCallback](#com.fresvii.voicechat.VoiceChatConferenceCallback) hostCallback|Callback to be informed about the result of the operation.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_voicechat_VoiceChatConference_void_join_String_String_VoiceChatConferenceCallback"> join </a> ###



```
public void join(String groupId,  
                 String hostId,  
                 VoiceChatConferenceCallback joinCallback)
```



Joins a conference.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|String groupId|Fresvii groupId.|
|String hostId|Fresvii user ID of the conference host.|
|[VoiceChatConferenceCallback](#com.fresvii.voicechat.VoiceChatConferenceCallback) joinCallback|Callback to be informed about the result of the operation.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_voicechat_VoiceChatConference_void_leave_VoiceChatConferenceCallback"> leave </a> ###



```
public void leave(VoiceChatConferenceCallback leaveCallback)
```



Leaves the voicechat conference.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|[VoiceChatConferenceCallback](#com.fresvii.voicechat.VoiceChatConferenceCallback) leaveCallback|Callback to be informed about the result of the operation.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_voicechat_VoiceChatConference_void_addGuest_String_VoiceChatConferenceCallback"> addGuest </a> ###



```
public void addGuest(String guestId,  
                     VoiceChatConferenceCallback addGuestCallback)
```



Adds a guest to the conference.
 Only works if we did host the conference.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|String guestId|Fresvii guestId|
|[VoiceChatConferenceCallback](#com.fresvii.voicechat.VoiceChatConferenceCallback) addGuestCallback|Callback to be informed about the result of the operation.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_voicechat_VoiceChatConference_void_removeGuest_String_VoiceChatConferenceCallback"> removeGuest </a> ###



```
public void removeGuest(String guestId,  
                        VoiceChatConferenceCallback removeGuestCallback)
```



Removes a guest from the conference.
 Only works if we did host the conference.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|String guestId|Fresvii guestId|
|[VoiceChatConferenceCallback](#com.fresvii.voicechat.VoiceChatConferenceCallback) removeGuestCallback|Callback to be informed about the result of the operation.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_voicechat_VoiceChatConference_void_mute_VoiceChatConferenceCallback"> mute </a> ###



```
public void mute(VoiceChatConferenceCallback muteCallback)
```



Mutes the conference.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|[VoiceChatConferenceCallback](#com.fresvii.voicechat.VoiceChatConferenceCallback) muteCallback|Callback to be informed about the result of the operation.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_voicechat_VoiceChatConference_void_unmute_VoiceChatConferenceCallback"> unmute </a> ###



```
public void unmute(VoiceChatConferenceCallback unmuteCallback)
```



Unmutes the conference.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|[VoiceChatConferenceCallback](#com.fresvii.voicechat.VoiceChatConferenceCallback) unmuteCallback|Callback to be informed about the result of the operation.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



#### VoiceChatConference Example ####  

1. Add the VoiceChat libraries to the *libs/armeabi* folder of you *FresviiSDK* project in the Eclipse workspace.

    There are 3 libraries you have to include:
    
    - *libvoicechat.so*
    - *libsipmanager.so*
    - *libgnustl_shared.so* 

2. Add the following permissions to your *"AndroidManifest.xml"* file:

    ```
    <uses-permission android:name="android.permission.WAKE_LOCK" />
    <uses-permission android:name="android.permission.RECORD_AUDIO" />
    <uses-permission android:name="com.google.android.c2dm.permission.RECEIVE" />
    
    <permission
            android:name="com.example.gcm.permission.C2D_MESSAGE"
            android:protectionLevel="signature" />
    <uses-permission android:name="com.example.gcm.permission.C2D_MESSAGE" />
    <uses-permission android:name="com.example.gcm.c2dm.permission.RECEIVE" />
    ```

3. Add the following Receivers and Services to your *"AndroidManifest.xml"* file: 

    ```
        <receiver
                android:name="com.fresvii.gcm.GcmBroadcastReceiver"
                android:permission="com.google.android.c2dm.permission.SEND" >
            <intent-filter>
                <action android:name="com.google.android.c2dm.intent.RECEIVE" />
                <category android:name="com.example.gcm" />
            </intent-filter>
        </receiver>
        
        <receiver
                android:name="com.fresvii.gcm.NotificationActionReceiver" >
            <intent-filter>
                <action android:name="com.fresvii.gcm.NotificationActionReceiver.intent.ACCEPT_VOICE_CHAT" />
            </intent-filter>
        </receiver>
        
        <service android:name="com.fresvii.gcm.GcmIntentService" />
    ```

4. Register a GcmClient as described in [GcmClient](#com.fresvii.gcm.GcmClient) 
    
5. To start a VoiceChat, first you have to create a Fresvii Group, e.g. a PairGroup: 

    ```
        public void hostVoiceChatConference(String partnerUserId) {
            // First, create a Group with the partner(s) you wish to have a VoiceChat conference with
            // Here, we are using a PairGroup for a quick 1 on 1 VoiceChat
            GroupAccess.createPairGroup(partnerUserId, new CreatePairGroupCallback() {
                @Override
                public void onSuccess(FresviiGroup group) {
                    // Success! The PairGroup has been created.
                    // Now you can host a VoiceChat conference. 
                    VoiceChatConference.getInstance().host(group.getIdOrDefault(), new VoiceChatConferenceCallback() {
                        @Override
                        public void onSuccess() {
                            // Success! The partner(s) will now receive a GCM VoiceChat notification. 
                            // They can join the conference by accepting the invitation. 
                        }
                
                        @Override
                        public void onError(Throwable error) {
                          // Error handling
                        }
                    });
                }
                
                @Override
                public void onFailure(Throwable error) {
                    // Error handling
                }
            });
        }
    ```
    
6. After you hosted the VoiceChat conference, the partner(s) will receive a GCM VoiceChat notification. They can join the conference by accepting the invitation. 
7. Now you should be talking to your VoiceChat partner(s)!
8. Either participant (host or guests) can leave the VoiceChat conference like this:

    ```
        public void leaveVoiceChatConference() {
            VoiceChatConference.getInstance().leave(new VoiceChatConferenceCallback() {
                @Override
                public void onSuccess() {
                    // Success
                }
                
                @Override
                public void onError(final Throwable error) {
                    // Error handling
                }
            });
        }
    ```

    





-------------------------



## <a name="com.fresvii.voicechat.VoiceChatConference.CallState"> Enum VoiceChatConference.CallState </a> ##



```
public static final class VoiceChatConference.CallState extends Enum
```

**Hierarchy:**  


```
java.lang.Object  
    java.lang.Enum  
        com.fresvii.voicechat.VoiceChatConference.CallState
```



**Description:**  
Represents the state of a call in the conference.




### Field Summary ###

|**Field**|**Description**|
|---|---|
|IDLE|The call is idle.|
|PROGRESSING|The call is progressing, i.e. dialing or ringing.|
|CONNECTED|The call is connected.|



### Method Summary ###



None.



### Method Detail ###



None.





-------------------------



## <a name="com.fresvii.voicechat.VoiceChatConference.ConferenceState"> Enum VoiceChatConference.ConferenceState </a> ##



```
public static final class VoiceChatConference.ConferenceState extends Enum
```

**Hierarchy:**  


```
java.lang.Object  
    java.lang.Enum  
        com.fresvii.voicechat.VoiceChatConference.ConferenceState
```



**Description:**  
Represents the state of the conference.




### Field Summary ###

|**Field**|**Description**|
|---|---|
|DESTROYED|The conference is destroyed.|
|CREATED|The conference is created.|



### Method Summary ###



None.



### Method Detail ###



None.





-------------------------



## <a name="com.fresvii.voicechat.VoiceChatConference.ConferenceRole"> Enum VoiceChatConference.ConferenceRole </a> ##



```
public static final class VoiceChatConference.ConferenceRole extends Enum
```

**Hierarchy:**  


```
java.lang.Object  
    java.lang.Enum  
        com.fresvii.voicechat.VoiceChatConference.ConferenceRole
```



**Description:**  
Represents the conference role.




### Field Summary ###

|**Field**|**Description**|
|---|---|
|NONE|There currently is no conference.|
|HOST|We are the host of the current conference.|
|GUEST|We are a guest in the current conference.|



### Method Summary ###



None.



### Method Detail ###



None.





-------------------------



## <a name="com.fresvii.voicechat.VoiceChatConferenceCallback"> Interface VoiceChatConferenceCallback </a> ##



```
public interface VoiceChatConferenceCallback implements FailureCallback
```

**Hierarchy:**  


```
com.fresvii.voicechat.VoiceChatConferenceCallback
```



**Description:**  
Callback interface to handle several [VoiceChatConference](#com.fresvii.voicechat.VoiceChatConference) results.



**Author:**  
Marcus Froeschl



**Version:**  
1.0




### Field Summary ###



None.




### Method Summary ###

|**Method**|**Description**|
|---|---|
|[public void onSuccess()](#com_fresvii_voicechat_VoiceChatConferenceCallback_void_onSuccess_)|Callback invoked when operation succeeds.|


### Method Detail ###




### <a name="com_fresvii_voicechat_VoiceChatConferenceCallback_void_onSuccess_"> onSuccess </a> ###



```
public void onSuccess()
```



Callback invoked when operation succeeds.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|




-------------------------



## <a name="com.fresvii.voicechat.VoiceChatConferenceListener"> Interface VoiceChatConferenceListener </a> ##



```
public interface VoiceChatConferenceListener
```

**Hierarchy:**  


```
com.fresvii.voicechat.VoiceChatConferenceListener
```



**Description:**  
Application may implement this interface to handle [VoiceChatConference](#com.fresvii.voicechat.VoiceChatConference) events.



**Author:**  
Marcus Froeschl



**Version:**  
1.0



**Since:**  
2014-06-02




### Field Summary ###



None.




### Method Summary ###

|**Method**|**Description**|
|---|---|
|[public void onCallStateChanged(String groupId, String partnerId, VoiceChatConference.CallState callState)](#com_fresvii_voicechat_VoiceChatConferenceListener_void_onCallStateChanged_String_String_VoiceChatConference_CallState)|Called when the state of a call in the VoiceChat conference changes.|
|[public void onConferenceStateChanged(VoiceChatConference.ConferenceState conferenceState)](#com_fresvii_voicechat_VoiceChatConferenceListener_void_onConferenceStateChanged_VoiceChatConference_ConferenceState)|Called when the state of the conference changes.|
|[public void onError(Throwable error)](#com_fresvii_voicechat_VoiceChatConferenceListener_void_onError_Throwable)|Called when an error occurred during the conference.|


### Method Detail ###




### <a name="com_fresvii_voicechat_VoiceChatConferenceListener_void_onCallStateChanged_String_String_VoiceChatConference_CallState"> onCallStateChanged </a> ###



```
public void onCallStateChanged(String groupId,  
                               String partnerId,  
                               VoiceChatConference.CallState callState)
```



Called when the state of a call in the VoiceChat conference changes.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|String groupId|The Fresvii group ID of the associated group.|
|String partnerId|The Fresvii user ID of the associated call partner.|
|[VoiceChatConference.CallState](#com.fresvii.voicechat.VoiceChatConference.CallState) callState|The state of the call.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_voicechat_VoiceChatConferenceListener_void_onConferenceStateChanged_VoiceChatConference_ConferenceState"> onConferenceStateChanged </a> ###



```
public void onConferenceStateChanged(VoiceChatConference.ConferenceState conferenceState)
```



Called when the state of the conference changes.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|[VoiceChatConference.ConferenceState](#com.fresvii.voicechat.VoiceChatConference.ConferenceState) conferenceState|The state of the conference.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_voicechat_VoiceChatConferenceListener_void_onError_Throwable"> onError </a> ###



```
public void onError(Throwable error)
```



Called when an error occurred during the conference.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|Throwable error|The error that occurred.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|




-------------------------



## <a name="com.fresvii.components.FresviiCurrentUser"> Class FresviiCurrentUser </a> ##



```
public class FresviiCurrentUser extends FresviiUser
```

**Hierarchy:**  


```
java.lang.Object  
    com.fresvii.components.FresviiComponent  
        com.fresvii.components.FresviiUser  
            com.fresvii.components.FresviiCurrentUser
```



**Description:**  
Represents the user logged in to Fresvii Server on this device.
 This is a subclass of User where login user information is stored.
 Login users are always individuals, so this is a singleton object.



**Author:**  
matsushimakatsuhito



**Version:**  
1.0



**Since:**  
2014-04-20




### Field Summary ###



None.




### Method Summary ###

|**Method**|**Description**|
|---|---|
|[public static com.fresvii.components.FresviiCurrentUser getInstance()](#com_fresvii_components_FresviiCurrentUser_com_fresvii_components_FresviiCurrentUser_getInstance_)|Retrieves the instance of the singleton object. Use this to access the CurrentUser.|
|[public boolean isCurrentUser(FresviiUser user)](#com_fresvii_components_FresviiCurrentUser_boolean_isCurrentUser_FresviiUser)|Checks if the specified user is the current user.|
|[public boolean isCurrentUser(String userId)](#com_fresvii_components_FresviiCurrentUser_boolean_isCurrentUser_String)|Checks if the specified user ID is the user ID of the current user.|
|[public java.util.Date getSessionExpirationDate()](#com_fresvii_components_FresviiCurrentUser_java_util_Date_getSessionExpirationDate_)|Retrieves the date when the current user's session expires.|
|[public void autoSignUpAndLogin()](#com_fresvii_components_FresviiCurrentUser_void_autoSignUpAndLogin_)|Convenience method that will automatically sign up and log in a new user if there currently is no signed up user.|
|[public void refreshSessionIfExpired()](#com_fresvii_components_FresviiCurrentUser_void_refreshSessionIfExpired_)|Convenience method that will automatically refresh the current user's session if the session has expired.|
|[public void setUpdatedName(String updatedName)](#com_fresvii_components_FresviiCurrentUser_void_setUpdatedName_String)|Updates the current user's name. |
|[public void setUpdatedDescription(String updatedDescription)](#com_fresvii_components_FresviiCurrentUser_void_setUpdatedDescription_String)|Updates the current user's description. |
|[public void setUpdatedProfileImage(Bitmap updatedProfileImage)](#com_fresvii_components_FresviiCurrentUser_void_setUpdatedProfileImage_Bitmap)|Updates the current user's profile image. |
|[public boolean isSignedUp()](#com_fresvii_components_FresviiCurrentUser_boolean_isSignedUp_)|Checks if there is a signed up current user.|
|[public boolean isLoggedIn()](#com_fresvii_components_FresviiCurrentUser_boolean_isLoggedIn_)|Checks if the current user is logged in.|
|[public boolean isSessionExpired()](#com_fresvii_components_FresviiCurrentUser_boolean_isSessionExpired_)|Checks if the session of the current user has expired.|
|[public void clearUpdates()](#com_fresvii_components_FresviiCurrentUser_void_clearUpdates_)|Clears all pending changes to the current user's name, description and profile image.|
|[public boolean hasUpdates()](#com_fresvii_components_FresviiCurrentUser_boolean_hasUpdates_)|Checks if there are any pending updates to the current user's name, description or profile image.|
|[public void saveUpdates(UpdateUserCallback callback)](#com_fresvii_components_FresviiCurrentUser_void_saveUpdates_UpdateUserCallback)|Stores all any pending updates to the current user's name, description or profile image to the server.|


### Method Detail ###




### <a name="com_fresvii_components_FresviiCurrentUser_com_fresvii_components_FresviiCurrentUser_getInstance_"> getInstance </a> ###



```
public static com.fresvii.components.FresviiCurrentUser getInstance()
```



Retrieves the instance of the singleton object. Use this to access the CurrentUser.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|FresviiCurrentUser|Instance of the singleton object.|



### <a name="com_fresvii_components_FresviiCurrentUser_boolean_isCurrentUser_FresviiUser"> isCurrentUser </a> ###



```
public boolean isCurrentUser(FresviiUser user)
```



Checks if the specified user is the current user.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|[FresviiUser](#com.fresvii.components.FresviiUser) user|User to be checked.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|boolean|true if the specified user is the current user, false otherwise|



### <a name="com_fresvii_components_FresviiCurrentUser_boolean_isCurrentUser_String"> isCurrentUser </a> ###



```
public boolean isCurrentUser(String userId)
```



Checks if the specified user ID is the user ID of the current user.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|String userId|User ID to be checked.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|boolean|true if the specified user id is the user ID of the current user, false otherwise|



### <a name="com_fresvii_components_FresviiCurrentUser_java_util_Date_getSessionExpirationDate_"> getSessionExpirationDate </a> ###



```
public java.util.Date getSessionExpirationDate()
```



Retrieves the date when the current user's session expires.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|Date|Date when the current user's session expires|



### <a name="com_fresvii_components_FresviiCurrentUser_void_autoSignUpAndLogin_"> autoSignUpAndLogin </a> ###



```
public void autoSignUpAndLogin()
```



Convenience method that will automatically sign up and log in a new user if there currently is no signed up user.
 If there is a signed up user, the user's session will be automatically refreshed if required.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_components_FresviiCurrentUser_void_refreshSessionIfExpired_"> refreshSessionIfExpired </a> ###



```
public void refreshSessionIfExpired()
```



Convenience method that will automatically refresh the current user's session if the session has expired.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_components_FresviiCurrentUser_void_setUpdatedName_String"> setUpdatedName </a> ###



```
public void setUpdatedName(String updatedName)
```



Updates the current user's name. 
 saveAdjustments() will store changes to the server.
 To cancel changes, use clearAdjustments().



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|String updatedName|Name to be used when saving adjustments.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_components_FresviiCurrentUser_void_setUpdatedDescription_String"> setUpdatedDescription </a> ###



```
public void setUpdatedDescription(String updatedDescription)
```



Updates the current user's description. 
 saveAdjustments() will store changes to the server.
 To cancel changes, use clearAdjustments().



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|String updatedDescription|Description name to be used when saving adjustments.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_components_FresviiCurrentUser_void_setUpdatedProfileImage_Bitmap"> setUpdatedProfileImage </a> ###



```
public void setUpdatedProfileImage(Bitmap updatedProfileImage)
```



Updates the current user's profile image. 
 saveAdjustments() will store changes to the server.
 To cancel changes, use clearAdjustments().



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|Bitmap updatedProfileImage|Profile image name to be used when saving adjustments.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_components_FresviiCurrentUser_boolean_isSignedUp_"> isSignedUp </a> ###



```
public boolean isSignedUp()
```



Checks if there is a signed up current user.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|boolean|true if signed up, false otherwise.|



### <a name="com_fresvii_components_FresviiCurrentUser_boolean_isLoggedIn_"> isLoggedIn </a> ###



```
public boolean isLoggedIn()
```



Checks if the current user is logged in.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|boolean|true if logged in, false otherwise.|



### <a name="com_fresvii_components_FresviiCurrentUser_boolean_isSessionExpired_"> isSessionExpired </a> ###



```
public boolean isSessionExpired()
```



Checks if the session of the current user has expired.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|boolean|true if the session has expired, false otherwise.|



### <a name="com_fresvii_components_FresviiCurrentUser_void_clearUpdates_"> clearUpdates </a> ###



```
public void clearUpdates()
```



Clears all pending changes to the current user's name, description and profile image.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|



### <a name="com_fresvii_components_FresviiCurrentUser_boolean_hasUpdates_"> hasUpdates </a> ###



```
public boolean hasUpdates()
```



Checks if there are any pending updates to the current user's name, description or profile image.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|boolean|true if there are any pending adjustments, false if there are no pending adjustments.|



### <a name="com_fresvii_components_FresviiCurrentUser_void_saveUpdates_UpdateUserCallback"> saveUpdates </a> ###



```
public void saveUpdates(UpdateUserCallback callback)
```



Stores all any pending updates to the current user's name, description or profile image to the server.



#### Parameters ####

|**Parameter**|**Description**|
|---|---|
|[UpdateUserCallback](#com.fresvii.server.access.callbacks.account.UpdateUserCallback) callback|UpdateUserCallback to be informed about the result of this operation.|


#### Returns ####

|**Return Type**|**Description**|
|---|---|
|void|-|




-------------------------



## <a name="com.fresvii.components.FresviiGroup"> Class FresviiGroup </a> ##



```
public class FresviiGroup extends Object
```

**Hierarchy:**  


```
java.lang.Object  
    com.fresvii.components.FresviiGroup
```



**Description:**  
Represents a Fresvii Group used for text chat, voice chat etc.



**Author:**  
Marcus Froeschl



**Version:**  
1.0



**Since:**  
2014-05-26




### Field Summary ###



None.




### Method Summary ###

|**Method**|**Description**|
|---|---|
|[public java.lang.String getId()](#com_fresvii_components_FresviiGroup_java_lang_String_getId_)|Retrieves the group's ID.|
|[public java.lang.String getIdOrDefault()](#com_fresvii_components_FresviiGroup_java_lang_String_getIdOrDefault_)|Retrieves the group's ID, or a default value if the group's ID is null.|
|[public java.lang.String getName()](#com_fresvii_components_FresviiGroup_java_lang_String_getName_)|Retrieves the group's name.|
|[public java.lang.String getNameOrDefault()](#com_fresvii_components_FresviiGroup_java_lang_String_getNameOrDefault_)|Retrieves the group's name, or a default value if the group's name is null.|
|[public java.util.Date getCreatedAt()](#com_fresvii_components_FresviiGroup_java_util_Date_getCreatedAt_)|Retrieves the date at which the group was created.|
|[public java.util.Date getCreatedAtOrDefault()](#com_fresvii_components_FresviiGroup_java_util_Date_getCreatedAtOrDefault_)|Retrieves the date at which the group was created, or a default value if the group's createdAt date is null.|
|[public java.util.Date getUpdatedAt()](#com_fresvii_components_FresviiGroup_java_util_Date_getUpdatedAt_)|Retrieves the date at which the group was updated.|
|[public java.util.Date getUpdatedAtOrDefault()](#com_fresvii_components_FresviiGroup_java_util_Date_getUpdatedAtOrDefault_)|Retrieves the date at which the group was updated, or a default value if the group's updatedAt date is null.|
|[public java.lang.Boolean isCurrentUserSubscribedToGroup()](#com_fresvii_components_FresviiGroup_java_lang_Boolean_isCurrentUserSubscribedToGroup_)|Retrieves the group's "subscribed" property.|
|[public java.lang.Boolean isCurrentUserSubscribedToGroupOrDefault()](#com_fresvii_components_FresviiGroup_java_lang_Boolean_isCurrentUserSubscribedToGroupOrDefault_)|Retrieves the group's "subscribed" property, or a default value if the group's "subscribed" property is null.|
|[public java.lang.Boolean isPairGroup()](#com_fresvii_components_FresviiGroup_java_lang_Boolean_isPairGroup_)|Retrieves the group's "pair" property.|
|[public java.lang.Boolean isPairGroupOrDefault()](#com_fresvii_components_FresviiGroup_java_lang_Boolean_isPairGroupOrDefault_)|Retrieves the group's "pair" property, or a default value if the group's "pair" property is null.|
|[public java.lang.Integer getMemberCount()](#com_fresvii_components_FresviiGroup_java_lang_Integer_getMemberCount_)|Retrieves the group's member count.|
|[public java.lang.Integer getMemberCountOrDefault()](#com_fresvii_components_FresviiGroup_java_lang_Integer_getMemberCountOrDefault_)|Retrieves the group's member count, or a default value if the group's member count is null.|
|[public com.fresvii.components.FresviiMessage getLatestMessage()](#com_fresvii_components_FresviiGroup_com_fresvii_components_FresviiMessage_getLatestMessage_)|Retrieves the group's latest message.|
|[public com.fresvii.components.FresviiMessage getLatestMessageOrDefault()](#com_fresvii_components_FresviiGroup_com_fresvii_components_FresviiMessage_getLatestMessageOrDefault_)|Retrieves the group's latest message, or a default value if the group's latest message is null.|
|[public java.util.List getMessageUsers()](#com_fresvii_components_FresviiGroup_java_util_List_getMessageUsers_)|Retrieves the group's message users.|
|[public java.util.List getmessageUsersOrDefault()](#com_fresvii_components_FresviiGroup_java_util_List_getmessageUsersOrDefault_)|Retrieves the group's message user list, or a default value if the group's message user list is null.|


### Method Detail ###




### <a name="com_fresvii_components_FresviiGroup_java_lang_String_getId_"> getId </a> ###



```
public java.lang.String getId()
```



Retrieves the group's ID.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|String|The group's ID.|



### <a name="com_fresvii_components_FresviiGroup_java_lang_String_getIdOrDefault_"> getIdOrDefault </a> ###



```
public java.lang.String getIdOrDefault()
```



Retrieves the group's ID, or a default value if the group's ID is null.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|String|The group's ID, or a default value|



### <a name="com_fresvii_components_FresviiGroup_java_lang_String_getName_"> getName </a> ###



```
public java.lang.String getName()
```



Retrieves the group's name.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|String|The group's name.|



### <a name="com_fresvii_components_FresviiGroup_java_lang_String_getNameOrDefault_"> getNameOrDefault </a> ###



```
public java.lang.String getNameOrDefault()
```



Retrieves the group's name, or a default value if the group's name is null.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|String|The group's name, or a default value|



### <a name="com_fresvii_components_FresviiGroup_java_util_Date_getCreatedAt_"> getCreatedAt </a> ###



```
public java.util.Date getCreatedAt()
```



Retrieves the date at which the group was created.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|Date|The date at which the group was created.|



### <a name="com_fresvii_components_FresviiGroup_java_util_Date_getCreatedAtOrDefault_"> getCreatedAtOrDefault </a> ###



```
public java.util.Date getCreatedAtOrDefault()
```



Retrieves the date at which the group was created, or a default value if the group's createdAt date is null.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|Date|The date at which the group was created, or a default value|



### <a name="com_fresvii_components_FresviiGroup_java_util_Date_getUpdatedAt_"> getUpdatedAt </a> ###



```
public java.util.Date getUpdatedAt()
```



Retrieves the date at which the group was updated.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|Date|The date at which the group was updated.|



### <a name="com_fresvii_components_FresviiGroup_java_util_Date_getUpdatedAtOrDefault_"> getUpdatedAtOrDefault </a> ###



```
public java.util.Date getUpdatedAtOrDefault()
```



Retrieves the date at which the group was updated, or a default value if the group's updatedAt date is null.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|Date|The date at which the group was updated, or a default value|



### <a name="com_fresvii_components_FresviiGroup_java_lang_Boolean_isCurrentUserSubscribedToGroup_"> isCurrentUserSubscribedToGroup </a> ###



```
public java.lang.Boolean isCurrentUserSubscribedToGroup()
```



Retrieves the group's "subscribed" property.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|Boolean|The group's "subscribed" property.|



### <a name="com_fresvii_components_FresviiGroup_java_lang_Boolean_isCurrentUserSubscribedToGroupOrDefault_"> isCurrentUserSubscribedToGroupOrDefault </a> ###



```
public java.lang.Boolean isCurrentUserSubscribedToGroupOrDefault()
```



Retrieves the group's "subscribed" property, or a default value if the group's "subscribed" property is null.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|Boolean|The group's "subscribed" property, or a default value|



### <a name="com_fresvii_components_FresviiGroup_java_lang_Boolean_isPairGroup_"> isPairGroup </a> ###



```
public java.lang.Boolean isPairGroup()
```



Retrieves the group's "pair" property.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|Boolean|The group's "pair" property.|



### <a name="com_fresvii_components_FresviiGroup_java_lang_Boolean_isPairGroupOrDefault_"> isPairGroupOrDefault </a> ###



```
public java.lang.Boolean isPairGroupOrDefault()
```



Retrieves the group's "pair" property, or a default value if the group's "pair" property is null.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|Boolean|The group's "pair" property, or a default value|



### <a name="com_fresvii_components_FresviiGroup_java_lang_Integer_getMemberCount_"> getMemberCount </a> ###



```
public java.lang.Integer getMemberCount()
```



Retrieves the group's member count.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|Integer|The group's member count.|



### <a name="com_fresvii_components_FresviiGroup_java_lang_Integer_getMemberCountOrDefault_"> getMemberCountOrDefault </a> ###



```
public java.lang.Integer getMemberCountOrDefault()
```



Retrieves the group's member count, or a default value if the group's member count is null.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|Integer|The group's member count, or a default value|



### <a name="com_fresvii_components_FresviiGroup_com_fresvii_components_FresviiMessage_getLatestMessage_"> getLatestMessage </a> ###



```
public com.fresvii.components.FresviiMessage getLatestMessage()
```



Retrieves the group's latest message.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|FresviiMessage|The group's latest message.|



### <a name="com_fresvii_components_FresviiGroup_com_fresvii_components_FresviiMessage_getLatestMessageOrDefault_"> getLatestMessageOrDefault </a> ###



```
public com.fresvii.components.FresviiMessage getLatestMessageOrDefault()
```



Retrieves the group's latest message, or a default value if the group's latest message is null.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|FresviiMessage|The group's latest message, or a default value|



### <a name="com_fresvii_components_FresviiGroup_java_util_List_getMessageUsers_"> getMessageUsers </a> ###



```
public java.util.List getMessageUsers()
```



Retrieves the group's message users.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|List|The group's message users.|



### <a name="com_fresvii_components_FresviiGroup_java_util_List_getmessageUsersOrDefault_"> getmessageUsersOrDefault </a> ###



```
public java.util.List getmessageUsersOrDefault()
```



Retrieves the group's message user list, or a default value if the group's message user list is null.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|List|The group's message user list, or a default value|




-------------------------



## <a name="com.fresvii.components.FresviiUser"> Class FresviiUser </a> ##



```
public class FresviiUser extends FresviiComponent
```

**Hierarchy:**  


```
java.lang.Object  
    com.fresvii.components.FresviiComponent  
        com.fresvii.components.FresviiUser
```



**Description:**  
Represents a Fresvii user.



**Author:**  
matsushimakatsuhito



**Version:**  
1.0



**Since:**  
2014-02-18




### Field Summary ###



None.




### Method Summary ###

|**Method**|**Description**|
|---|---|
|[public java.lang.String getId()](#com_fresvii_components_FresviiUser_java_lang_String_getId_)|Retrieves the user's ID.|
|[public java.lang.String getIdOrDefault()](#com_fresvii_components_FresviiUser_java_lang_String_getIdOrDefault_)|Retrieves the user's ID, or a default value if the user's ID is null.|
|[public java.lang.String getName()](#com_fresvii_components_FresviiUser_java_lang_String_getName_)|Retrieves the user's name.|
|[public java.lang.String getNameOrDefault()](#com_fresvii_components_FresviiUser_java_lang_String_getNameOrDefault_)|Retrieves the user's name, or a default value if the user's name is null.|
|[public java.lang.String getCode()](#com_fresvii_components_FresviiUser_java_lang_String_getCode_)|Retrieves the user's code.|
|[public java.lang.String getCodeOrDefault()](#com_fresvii_components_FresviiUser_java_lang_String_getCodeOrDefault_)|Retrieves the user's code, or a default value if the user's code is null.|
|[public java.lang.String getToken()](#com_fresvii_components_FresviiUser_java_lang_String_getToken_)|Retrieves the user's token.|
|[public java.lang.String getTokenOrDefault()](#com_fresvii_components_FresviiUser_java_lang_String_getTokenOrDefault_)|Retrieves the user's token, or a default value if the user's token is null.|
|[public java.lang.String getDescription()](#com_fresvii_components_FresviiUser_java_lang_String_getDescription_)|Retrieves the user's description.|
|[public java.lang.String getDescriptionOrDefault()](#com_fresvii_components_FresviiUser_java_lang_String_getDescriptionOrDefault_)|Retrieves the user's description, or a default value if the user's description is null.|
|[public java.lang.String getProfileImageUrl()](#com_fresvii_components_FresviiUser_java_lang_String_getProfileImageUrl_)|Retrieves the user's profile image URL.|
|[public java.lang.String getProfileImageUrlOrDefault()](#com_fresvii_components_FresviiUser_java_lang_String_getProfileImageUrlOrDefault_)|Retrieves the user's profile image URL, or a default value if the user's profile image URL is null.|
|[public java.lang.String getFriendStatus()](#com_fresvii_components_FresviiUser_java_lang_String_getFriendStatus_)|Retrieves the user's friend status.|
|[public java.lang.String getFriendStatusOrDefault()](#com_fresvii_components_FresviiUser_java_lang_String_getFriendStatusOrDefault_)|Retrieves the user's friend status, or a default value if the user's friend status is null.|


### Method Detail ###




### <a name="com_fresvii_components_FresviiUser_java_lang_String_getId_"> getId </a> ###



```
public java.lang.String getId()
```



Retrieves the user's ID.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|String|The user's ID.|



### <a name="com_fresvii_components_FresviiUser_java_lang_String_getIdOrDefault_"> getIdOrDefault </a> ###



```
public java.lang.String getIdOrDefault()
```



Retrieves the user's ID, or a default value if the user's ID is null.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|String|The user's ID, or a default value|



### <a name="com_fresvii_components_FresviiUser_java_lang_String_getName_"> getName </a> ###



```
public java.lang.String getName()
```



Retrieves the user's name.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|String|The user's name.|



### <a name="com_fresvii_components_FresviiUser_java_lang_String_getNameOrDefault_"> getNameOrDefault </a> ###



```
public java.lang.String getNameOrDefault()
```



Retrieves the user's name, or a default value if the user's name is null.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|String|The user's name, or a default value|



### <a name="com_fresvii_components_FresviiUser_java_lang_String_getCode_"> getCode </a> ###



```
public java.lang.String getCode()
```



Retrieves the user's code.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|String|The user's code.|



### <a name="com_fresvii_components_FresviiUser_java_lang_String_getCodeOrDefault_"> getCodeOrDefault </a> ###



```
public java.lang.String getCodeOrDefault()
```



Retrieves the user's code, or a default value if the user's code is null.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|String|The user's code, or a default value|



### <a name="com_fresvii_components_FresviiUser_java_lang_String_getToken_"> getToken </a> ###



```
public java.lang.String getToken()
```



Retrieves the user's token.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|String|The user's token.|



### <a name="com_fresvii_components_FresviiUser_java_lang_String_getTokenOrDefault_"> getTokenOrDefault </a> ###



```
public java.lang.String getTokenOrDefault()
```



Retrieves the user's token, or a default value if the user's token is null.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|String|The user's token, or a default value|



### <a name="com_fresvii_components_FresviiUser_java_lang_String_getDescription_"> getDescription </a> ###



```
public java.lang.String getDescription()
```



Retrieves the user's description.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|String|The user's description.|



### <a name="com_fresvii_components_FresviiUser_java_lang_String_getDescriptionOrDefault_"> getDescriptionOrDefault </a> ###



```
public java.lang.String getDescriptionOrDefault()
```



Retrieves the user's description, or a default value if the user's description is null.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|String|The user's description, or a default value|



### <a name="com_fresvii_components_FresviiUser_java_lang_String_getProfileImageUrl_"> getProfileImageUrl </a> ###



```
public java.lang.String getProfileImageUrl()
```



Retrieves the user's profile image URL.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|String|The user's profile image URL.|



### <a name="com_fresvii_components_FresviiUser_java_lang_String_getProfileImageUrlOrDefault_"> getProfileImageUrlOrDefault </a> ###



```
public java.lang.String getProfileImageUrlOrDefault()
```



Retrieves the user's profile image URL, or a default value if the user's profile image URL is null.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|String|The user's profile image URL, or a default value|



### <a name="com_fresvii_components_FresviiUser_java_lang_String_getFriendStatus_"> getFriendStatus </a> ###



```
public java.lang.String getFriendStatus()
```



Retrieves the user's friend status.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|String|The user's friend status.|



### <a name="com_fresvii_components_FresviiUser_java_lang_String_getFriendStatusOrDefault_"> getFriendStatusOrDefault </a> ###



```
public java.lang.String getFriendStatusOrDefault()
```



Retrieves the user's friend status, or a default value if the user's friend status is null.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|String|The user's friend status, or a default value|




-------------------------



## <a name="com.fresvii.gcm.FresviiGcmMessage"> Class FresviiGcmMessage </a> ##



```
public class FresviiGcmMessage extends Object
```

**Hierarchy:**  


```
java.lang.Object  
    com.fresvii.gcm.FresviiGcmMessage
```



**Description:**  
Represents a Fresvii GCM Message



**Author:**  
Marcus Froeschl



**Version:**  
1.0



**Since:**  
2014-06-02




### Field Summary ###



None.




### Method Summary ###

|**Method**|**Description**|
|---|---|
|[public com.fresvii.gcm.FresviiGcmMessage.MessageType getMessageType()](#com_fresvii_gcm_FresviiGcmMessage_com_fresvii_gcm_FresviiGcmMessage_MessageType_getMessageType_)|Retrieves the message's type.|
|[public com.fresvii.gcm.FresviiGcmMessage.Resource getResource()](#com_fresvii_gcm_FresviiGcmMessage_com_fresvii_gcm_FresviiGcmMessage_Resource_getResource_)|Retrieves the resource associated with this message.|
|[public com.fresvii.gcm.FresviiGcmMessage.Action getAction()](#com_fresvii_gcm_FresviiGcmMessage_com_fresvii_gcm_FresviiGcmMessage_Action_getAction_)|Retrieves the action that was performed on the resource.|
|[public java.lang.String getResourcePath()](#com_fresvii_gcm_FresviiGcmMessage_java_lang_String_getResourcePath_)|Retrieves the message's resource path.|
|[public java.lang.String getId()](#com_fresvii_gcm_FresviiGcmMessage_java_lang_String_getId_)|Retrieves the message's ID.|
|[public java.lang.String getTitle()](#com_fresvii_gcm_FresviiGcmMessage_java_lang_String_getTitle_)|Retrieves the message's title.|
|[public java.lang.String getSound()](#com_fresvii_gcm_FresviiGcmMessage_java_lang_String_getSound_)|Retrieves the message's sound.|
|[public java.lang.String getVersion()](#com_fresvii_gcm_FresviiGcmMessage_java_lang_String_getVersion_)|Retrieves the message's version.|
|[public java.lang.String getObject()](#com_fresvii_gcm_FresviiGcmMessage_java_lang_String_getObject_)|Retrieves the object associated with the message as a JSON String.|
|[public android.content.Context getContext()](#com_fresvii_gcm_FresviiGcmMessage_android_content_Context_getContext_)|Retrieves the context in which this GCM message was received.|


### Method Detail ###




### <a name="com_fresvii_gcm_FresviiGcmMessage_com_fresvii_gcm_FresviiGcmMessage_MessageType_getMessageType_"> getMessageType </a> ###



```
public com.fresvii.gcm.FresviiGcmMessage.MessageType getMessageType()
```



Retrieves the message's type.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|FresviiGcmMessage.MessageType|The message's type.|



### <a name="com_fresvii_gcm_FresviiGcmMessage_com_fresvii_gcm_FresviiGcmMessage_Resource_getResource_"> getResource </a> ###



```
public com.fresvii.gcm.FresviiGcmMessage.Resource getResource()
```



Retrieves the resource associated with this message.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|FresviiGcmMessage.Resource|The resource associated with this message.|



### <a name="com_fresvii_gcm_FresviiGcmMessage_com_fresvii_gcm_FresviiGcmMessage_Action_getAction_"> getAction </a> ###



```
public com.fresvii.gcm.FresviiGcmMessage.Action getAction()
```



Retrieves the action that was performed on the resource.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|FresviiGcmMessage.Action|The action that was performed on the resource.|



### <a name="com_fresvii_gcm_FresviiGcmMessage_java_lang_String_getResourcePath_"> getResourcePath </a> ###



```
public java.lang.String getResourcePath()
```



Retrieves the message's resource path.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|String|The message's resource path.|



### <a name="com_fresvii_gcm_FresviiGcmMessage_java_lang_String_getId_"> getId </a> ###



```
public java.lang.String getId()
```



Retrieves the message's ID.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|String|The message's ID.|



### <a name="com_fresvii_gcm_FresviiGcmMessage_java_lang_String_getTitle_"> getTitle </a> ###



```
public java.lang.String getTitle()
```



Retrieves the message's title.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|String|The message's title.|



### <a name="com_fresvii_gcm_FresviiGcmMessage_java_lang_String_getSound_"> getSound </a> ###



```
public java.lang.String getSound()
```



Retrieves the message's sound.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|String|The message's sound.|



### <a name="com_fresvii_gcm_FresviiGcmMessage_java_lang_String_getVersion_"> getVersion </a> ###



```
public java.lang.String getVersion()
```



Retrieves the message's version.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|String|The message's version.|



### <a name="com_fresvii_gcm_FresviiGcmMessage_java_lang_String_getObject_"> getObject </a> ###



```
public java.lang.String getObject()
```



Retrieves the object associated with the message as a JSON String.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|String|The object associated with the message.|



### <a name="com_fresvii_gcm_FresviiGcmMessage_android_content_Context_getContext_"> getContext </a> ###



```
public android.content.Context getContext()
```



Retrieves the context in which this GCM message was received.



#### Returns ####

|**Return Type**|**Description**|
|---|---|
|Context|Message context.|




-------------------------



## <a name="com.fresvii.gcm.FresviiGcmMessage.MessageType"> Enum FresviiGcmMessage.MessageType </a> ##



```
public static final class FresviiGcmMessage.MessageType extends Enum
```

**Hierarchy:**  


```
java.lang.Object  
    java.lang.Enum  
        com.fresvii.gcm.FresviiGcmMessage.MessageType
```



**Description:**  
Known GCM message types which will receive special treatment.




### Field Summary ###

|**Field**|**Description**|
|---|---|
|CUSTOM|A custom GCM message (user defined message).|
|NEW_COMMENT|A message for a new forum comment.|
|OFFICIAL_THREAD|A message for an official thread.|
|GROUP_TEXT_MESSAGE|A group text message.|
|GROUP_IMAGE_MESSAGE|An image message.|
|GROUP_IN_GAME_MESSAGE|An ingame message.|
|CONFERENCE_CREATED|A message for [VoiceChatConference](#com.fresvii.voicechat.VoiceChatConference) invitation.|
|NEW_FRIEND_REQUEST|A message for a new friend request.|
|FRIEND_REQUEST_UPDATE|A message for an updated friend request.|
|DIRECT_MESSAGE|A direct message.|



### Method Summary ###



None.



### Method Detail ###



None.





-------------------------



## <a name="com.fresvii.gcm.FresviiGcmMessage.Resource"> Enum FresviiGcmMessage.Resource </a> ##



```
public static final class FresviiGcmMessage.Resource extends Enum
```

**Hierarchy:**  


```
java.lang.Object  
    java.lang.Enum  
        com.fresvii.gcm.FresviiGcmMessage.Resource
```



**Description:**  
GCM message resources specified in Fresvii Push Specifications




### Field Summary ###

|**Field**|**Description**|
|---|---|
|CUSTOM|A custom resource (user defined resource).|
|NONE|No resource.|
|FORUM_COMMENT|A forum comment resource.|
|FORUM_THREAD|A forum thread resource.|
|FRIEND_REQUEST|A friend request resource.|
|GROUP_TEXT_MESSAGE|A group text message resource.|
|GROUP_IMAGE_MESSAGE|A group image message resource.|
|GROUP_IN_GAME_MESSAGE|A group ingame message resource.|
|GROUP_CONFERENCE|A conference resource.|



### Method Summary ###



None.



### Method Detail ###



None.





-------------------------



## <a name="com.fresvii.gcm.FresviiGcmMessage.Action"> Enum FresviiGcmMessage.Action </a> ##



```
public static final class FresviiGcmMessage.Action extends Enum
```

**Hierarchy:**  


```
java.lang.Object  
    java.lang.Enum  
        com.fresvii.gcm.FresviiGcmMessage.Action
```



**Description:**  
GCM message actions specified in Fresvii Push Specifications




### Field Summary ###

|**Field**|**Description**|
|---|---|
|CUSTOM|A custom action (user defined action).|
|NONE|No action|
|CREATED|Created action|
|UPDATED|Updated action|



### Method Summary ###



None.



### Method Detail ###



None.



