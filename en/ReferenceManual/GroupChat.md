
# AppSteroid Group Chat API

Last updated 2014-12-01

-------------------------

## Introduction

AppSteroid Group Chat API can be used to send and retrieve several types of AppSteroid Chat messages.


---  

## Classes

|Class|Description|
|---|---|
|[GroupChatAccess](#com.fresvii.server.access.GroupChatAccess)|Provides access to Fresvii Server's Group Chat API.|
|[AppSteroidMessage](#com.fresvii.components.AppSteroidMessage)|Represents a Fresvii Text Message, Image Message or InGame Message.|
|[SendImageMessageCallback](#com.fresvii.server.access.callbacks.groupchat.SendImageMessageCallback)|Callback interface to handle [GroupChatAccess.sendImageMessage()](#com_fresvii_server_access_GroupChatAccess_void_sendImageMessage_String_Bitmap_SendImageMessageCallback) results.|
|[SendInGameMessageCallback](#com.fresvii.server.access.callbacks.groupchat.SendInGameMessageCallback)|Callback interface to handle [GroupChatAccess.sendInGameMessage()](#com_fresvii_server_access_GroupChatAccess_void_sendInGameMessage_String_String_SendInGameMessageCallback) results.|
|[SendTextMessageCallback](#com.fresvii.server.access.callbacks.groupchat.SendTextMessageCallback)|Callback interface to handle [GroupChatAccess.sendTextMessage()](#com_fresvii_server_access_GroupChatAccess_void_sendTextMessage_String_String_SendTextMessageCallback) results.|
|[GetGroupMessageCallback](#com.fresvii.server.access.callbacks.groupchat.GetGroupMessageCallback)|Callback interface to handle [GroupChatAccess.getGroupMessage()](#com_fresvii_server_access_GroupChatAccess_void_getGroupMessage_String_String_GetGroupMessageCallback) results.|
|[GetGroupMessagesCallback](#com.fresvii.server.access.callbacks.groupchat.GetGroupMessagesCallback)|Callback interface to handle [GroupChatAccess.getGroupMessages()](#com_fresvii_server_access_GroupChatAccess_void_getGroupMessages_String_int_GetGroupMessagesCallback) results.|
|[GetMessageGroupsCallback](#com.fresvii.server.access.callbacks.groupchat.GetMessageGroupsCallback)|Callback interface to handle [GroupChatAccess.getMessageGroups()](#com_fresvii_server_access_GroupChatAccess_void_getMessageGroups_GetMessageGroupsCallback) results.|
|[DeleteGroupMessageCallback](#com.fresvii.server.access.callbacks.groupchat.DeleteGroupMessageCallback)|Callback interface to handle [GroupChatAccess.deleteGroupMessage()](#com_fresvii_server_access_GroupChatAccess_void_deleteGroupMessage_String_String_DeleteGroupMessageCallback) results.|



---  

## <a name="com.fresvii.server.access.GroupChatAccess"> Class GroupChatAccess </a>

```
public class GroupChatAccess extends Object
```

**Hierarchy:**  

```
java.lang.Object  
    com.fresvii.server.access.GroupChatAccess
```

**Description:**  
Provides access to Fresvii Server's Group Chat API.  Can be used to send or retrieve text, image or in game messages, etc.

**Author:**  
Marcus Froeschl

**Version:**  
1.0

**Since:**  
2014-05-26


### Method Summary

|Method|Description|
|---|---|
|[public static void deleteGroupMessage(String groupId, String messageId, DeleteGroupMessageCallback callback)](#com_fresvii_server_access_GroupChatAccess_void_deleteGroupMessage_String_String_DeleteGroupMessageCallback)|Retrieves a specific group message|
|[public static void getGroupMessage(String groupId, String messageId, GetGroupMessageCallback callback)](#com_fresvii_server_access_GroupChatAccess_void_getGroupMessage_String_String_GetGroupMessageCallback)|Retrieves a specific group message|
|[public static void getGroupMessages(String groupId, GetGroupMessagesCallback callback)](#com_fresvii_server_access_GroupChatAccess_void_getGroupMessages_String_GetGroupMessagesCallback)|Retrieves the first page of a list of messages for a group|
|[public static void getGroupMessages(String groupId, int page, GetGroupMessagesCallback callback)](#com_fresvii_server_access_GroupChatAccess_void_getGroupMessages_String_int_GetGroupMessagesCallback)|Retrieves a list of messages for a group from the specified page|
|[public static void getMessageGroups(GetMessageGroupsCallback callback)](#com_fresvii_server_access_GroupChatAccess_void_getMessageGroups_GetMessageGroupsCallback)|Retrieves the first page of a list of all of the chats (MessageGroups) the user is involved in.|
|[public static void getMessageGroups(int page, GetMessageGroupsCallback callback)](#com_fresvii_server_access_GroupChatAccess_void_getMessageGroups_int_GetMessageGroupsCallback)|Retrieves a list of all of the chats (MessageGroups) the user is involved in.|
|[public static void sendImageMessage(String groupId, Bitmap image, SendImageMessageCallback callback)](#com_fresvii_server_access_GroupChatAccess_void_sendImageMessage_String_Bitmap_SendImageMessageCallback)|Sends an image message to a group.|
|[public static void sendImageMessage(String groupId, Bitmap image, Date createdAt, SendImageMessageCallback callback)](#com_fresvii_server_access_GroupChatAccess_void_sendImageMessage_String_Bitmap_Date_SendImageMessageCallback)|Sends an image message to a group.|
|[public static void sendInGameMessage(String groupId, String text, SendInGameMessageCallback callback)](#com_fresvii_server_access_GroupChatAccess_void_sendInGameMessage_String_String_SendInGameMessageCallback)|Sends an ingame message to a group.|
|[public static void sendInGameMessage(String groupId, String text, Date createdAt, SendInGameMessageCallback callback)](#com_fresvii_server_access_GroupChatAccess_void_sendInGameMessage_String_String_Date_SendInGameMessageCallback)|Sends an ingame message to a group.|
|[public static void sendTextMessage(String groupId, String text, SendTextMessageCallback callback)](#com_fresvii_server_access_GroupChatAccess_void_sendTextMessage_String_String_SendTextMessageCallback)|Sends a text message to a group.|
|[public static void sendTextMessage(String groupId, String text, Date createdAt, SendTextMessageCallback callback)](#com_fresvii_server_access_GroupChatAccess_void_sendTextMessage_String_String_Date_SendTextMessageCallback)|Sends a text message to a group.|



### Method Detail
 


## <a name="com_fresvii_server_access_GroupChatAccess_void_deleteGroupMessage_String_String_DeleteGroupMessageCallback"> deleteGroupMessage </a>

```
public static void deleteGroupMessage(String groupId,  
                                      String messageId,  
                                      DeleteGroupMessageCallback callback)
```

Retrieves a specific group message

#### Parameters

|Parameter|Description|
|---|---|
|String groupId|ID of the group who's message is to be retrieved.|
|String messageId|ID of the message to be retrieved.|
|[DeleteGroupMessageCallback](#com.fresvii.server.access.callbacks.groupchat.DeleteGroupMessageCallback) callback|[Callback](#com.fresvii.server.access.callbacks.groupchat.DeleteGroupMessageCallback) to be informed about the result of the operation.|



## <a name="com_fresvii_server_access_GroupChatAccess_void_getGroupMessage_String_String_GetGroupMessageCallback"> getGroupMessage </a>

```
public static void getGroupMessage(String groupId,  
                                   String messageId,  
                                   GetGroupMessageCallback callback)
```

Retrieves a specific group message

#### Parameters

|Parameter|Description|
|---|---|
|String groupId|ID of the group who's message is to be retrieved.|
|String messageId|ID of the message to be retrieved.|
|[GetGroupMessageCallback](#com.fresvii.server.access.callbacks.groupchat.GetGroupMessageCallback) callback|[Callback](#com.fresvii.server.access.callbacks.groupchat.GetGroupMessageCallback) to be informed about the result of the operation.|



## <a name="com_fresvii_server_access_GroupChatAccess_void_getGroupMessages_String_GetGroupMessagesCallback"> getGroupMessages </a>

```
public static void getGroupMessages(String groupId,  
                                    GetGroupMessagesCallback callback)
```

Retrieves the first page of a list of messages for a group

#### Parameters

|Parameter|Description|
|---|---|
|String groupId|ID of the group who's messages are to be retrieved.|
|[GetGroupMessagesCallback](#com.fresvii.server.access.callbacks.groupchat.GetGroupMessagesCallback) callback|[Callback](#com.fresvii.server.access.callbacks.groupchat.GetGroupMessagesCallback) to be informed about the result of the operation.|



## <a name="com_fresvii_server_access_GroupChatAccess_void_getGroupMessages_String_int_GetGroupMessagesCallback"> getGroupMessages </a>

```
public static void getGroupMessages(String groupId,  
                                    int page,  
                                    GetGroupMessagesCallback callback)
```

Retrieves a list of messages for a group from the specified page

#### Parameters

|Parameter|Description|
|---|---|
|String groupId|ID of the group who's messages are to be retrieved.|
|int page|Page offset.|
|[GetGroupMessagesCallback](#com.fresvii.server.access.callbacks.groupchat.GetGroupMessagesCallback) callback|[Callback](#com.fresvii.server.access.callbacks.groupchat.GetGroupMessagesCallback) to be informed about the result of the operation.|



## <a name="com_fresvii_server_access_GroupChatAccess_void_getMessageGroups_GetMessageGroupsCallback"> getMessageGroups </a>

```
public static void getMessageGroups(GetMessageGroupsCallback callback)
```

Retrieves the first page of a list of all of the chats (MessageGroups) the user is involved in.  Also retrieves additional info such as the users involved in the chat, and the last message.

#### Parameters

|Parameter|Description|
|---|---|
|[GetMessageGroupsCallback](#com.fresvii.server.access.callbacks.groupchat.GetMessageGroupsCallback) callback|[Callback](#com.fresvii.server.access.callbacks.groupchat.GetMessageGroupsCallback) to be informed about the result of the operation.|



## <a name="com_fresvii_server_access_GroupChatAccess_void_getMessageGroups_int_GetMessageGroupsCallback"> getMessageGroups </a>

```
public static void getMessageGroups(int page,  
                                    GetMessageGroupsCallback callback)
```

Retrieves a list of all of the chats (MessageGroups) the user is involved in.  Also retrieves additional info such as the users involved in the chat, and the last message.

#### Parameters

|Parameter|Description|
|---|---|
|int page|Page offset.|
|[GetMessageGroupsCallback](#com.fresvii.server.access.callbacks.groupchat.GetMessageGroupsCallback) callback|[Callback](#com.fresvii.server.access.callbacks.groupchat.GetMessageGroupsCallback) to be informed about the result of the operation.|



## <a name="com_fresvii_server_access_GroupChatAccess_void_sendImageMessage_String_Bitmap_SendImageMessageCallback"> sendImageMessage </a>

```
public static void sendImageMessage(String groupId,  
                                    Bitmap image,  
                                    SendImageMessageCallback callback)
```

Sends an image message to a group.

#### Parameters

|Parameter|Description|
|---|---|
|String groupId|ID of the group.|
|Bitmap image|Image.|
|[SendImageMessageCallback](#com.fresvii.server.access.callbacks.groupchat.SendImageMessageCallback) callback|[Callback](#com.fresvii.server.access.callbacks.groupchat.SendImageMessageCallback) to be informed about the result of the operation.|



## <a name="com_fresvii_server_access_GroupChatAccess_void_sendImageMessage_String_Bitmap_Date_SendImageMessageCallback"> sendImageMessage </a>

```
public static void sendImageMessage(String groupId,  
                                    Bitmap image,  
                                    Date createdAt,  
                                    SendImageMessageCallback callback)
```

Sends an image message to a group.

#### Parameters

|Parameter|Description|
|---|---|
|String groupId|ID of the group.|
|Bitmap image|Image.|
|Date createdAt|Date the image message was created (optional).|
|[SendImageMessageCallback](#com.fresvii.server.access.callbacks.groupchat.SendImageMessageCallback) callback|[Callback](#com.fresvii.server.access.callbacks.groupchat.SendImageMessageCallback) to be informed about the result of the operation.|



## <a name="com_fresvii_server_access_GroupChatAccess_void_sendInGameMessage_String_String_SendInGameMessageCallback"> sendInGameMessage </a>

```
public static void sendInGameMessage(String groupId,  
                                     String text,  
                                     SendInGameMessageCallback callback)
```

Sends an ingame message to a group.

#### Parameters

|Parameter|Description|
|---|---|
|String groupId|ID of the group.|
|String text|Text message.|
|[SendInGameMessageCallback](#com.fresvii.server.access.callbacks.groupchat.SendInGameMessageCallback) callback|[Callback](#com.fresvii.server.access.callbacks.groupchat.SendTextMessageCallback) to be informed about the result of the operation.|



## <a name="com_fresvii_server_access_GroupChatAccess_void_sendInGameMessage_String_String_Date_SendInGameMessageCallback"> sendInGameMessage </a>

```
public static void sendInGameMessage(String groupId,  
                                     String text,  
                                     Date createdAt,  
                                     SendInGameMessageCallback callback)
```

Sends an ingame message to a group.

#### Parameters

|Parameter|Description|
|---|---|
|String groupId|ID of the group.|
|String text|Text message.|
|Date createdAt|Date the ingame message was created (optional).|
|[SendInGameMessageCallback](#com.fresvii.server.access.callbacks.groupchat.SendInGameMessageCallback) callback|[Callback](#com.fresvii.server.access.callbacks.groupchat.SendInGameMessageCallback) to be informed about the result of the operation.|



## <a name="com_fresvii_server_access_GroupChatAccess_void_sendTextMessage_String_String_SendTextMessageCallback"> sendTextMessage </a>

```
public static void sendTextMessage(String groupId,  
                                   String text,  
                                   SendTextMessageCallback callback)
```

Sends a text message to a group.

#### Parameters

|Parameter|Description|
|---|---|
|String groupId|ID of the group.|
|String text|Text message.|
|[SendTextMessageCallback](#com.fresvii.server.access.callbacks.groupchat.SendTextMessageCallback) callback|[Callback](#com.fresvii.server.access.callbacks.groupchat.SendTextMessageCallback) to be informed about the result of the operation.|



## <a name="com_fresvii_server_access_GroupChatAccess_void_sendTextMessage_String_String_Date_SendTextMessageCallback"> sendTextMessage </a>

```
public static void sendTextMessage(String groupId,  
                                   String text,  
                                   Date createdAt,  
                                   SendTextMessageCallback callback)
```

Sends a text message to a group.

#### Parameters

|Parameter|Description|
|---|---|
|String groupId|ID of the group.|
|String text|Text message.|
|Date createdAt|Date the text message was created (optional).|
|[SendTextMessageCallback](#com.fresvii.server.access.callbacks.groupchat.SendTextMessageCallback) callback|[Callback](#com.fresvii.server.access.callbacks.groupchat.SendTextMessageCallback) to be informed about the result of the operation.|




---  

## <a name="com.fresvii.components.AppSteroidMessage"> Class AppSteroidMessage </a>

```
public class AppSteroidMessage extends AppSteroidComponent
```

**Hierarchy:**  

```
java.lang.Object  
    com.fresvii.components.AppSteroidComponent  
        com.fresvii.components.AppSteroidMessage
```

**Description:**  
Represents a Fresvii Text Message, Image Message or InGame Message.

**Author:**  
Marcus Froeschl

**Version:**  
1.0

**Since:**  
2014-07-13


### Method Summary

|Method|Description|
|---|---|
|[public Date getCreatedAt()](#com_fresvii_components_AppSteroidMessage_java_util_Date_getCreatedAt_)|Retrieves the date at which the message was created.|
|[public Date getCreatedAtOrDefault()](#com_fresvii_components_AppSteroidMessage_java_util_Date_getCreatedAtOrDefault_)|Retrieves the date at which the message was created, or a default value if the message's createdAt date is null.|
|[public String getGroupId()](#com_fresvii_components_AppSteroidMessage_java_lang_String_getGroupId_)|Retrieves the message's Group ID.|
|[public String getGroupIdOrDefault()](#com_fresvii_components_AppSteroidMessage_java_lang_String_getGroupIdOrDefault_)|Retrieves the message's Group ID, or a default value if the message's Group ID is null.|
|[public String getId()](#com_fresvii_components_AppSteroidMessage_java_lang_String_getId_)|Retrieves the message's ID.|
|[public String getIdOrDefault()](#com_fresvii_components_AppSteroidMessage_java_lang_String_getIdOrDefault_)|Retrieves the message's ID, or a default value if the message's ID is null.|
|[public String getImageThumbnailUrl()](#com_fresvii_components_AppSteroidMessage_java_lang_String_getImageThumbnailUrl_)|Retrieves the message's image thumbnail url.|
|[public String getImageThumbnailUrlOrDefault()](#com_fresvii_components_AppSteroidMessage_java_lang_String_getImageThumbnailUrlOrDefault_)|Retrieves the message's image thumbnail url, or a default value if the message's image thumbnail url is null.|
|[public ExternalBitmapWrapper getImageThumbnailWrapper()](#com_fresvii_components_AppSteroidMessage_com_fresvii_helper_ExternalBitmapWrapper_getImageThumbnailWrapper_)|Retrieves the message's image thumbnail bitmap wrapper class which will load the image in the background.|
|[public String getImageUrl()](#com_fresvii_components_AppSteroidMessage_java_lang_String_getImageUrl_)|Retrieves the message's image url.|
|[public String getImageUrlOrDefault()](#com_fresvii_components_AppSteroidMessage_java_lang_String_getImageUrlOrDefault_)|Retrieves the message's image url, or a default value if the message's image url is null.|
|[public String getText()](#com_fresvii_components_AppSteroidMessage_java_lang_String_getText_)|Retrieves the message's text.|
|[public String getTextOrDefault()](#com_fresvii_components_AppSteroidMessage_java_lang_String_getTextOrDefault_)|Retrieves the message's text, or a default value if the message's text is null.|
|[public Date getUpdatedAt()](#com_fresvii_components_AppSteroidMessage_java_util_Date_getUpdatedAt_)|Retrieves the date at which the message was updated.|
|[public Date getUpdatedAtOrDefault()](#com_fresvii_components_AppSteroidMessage_java_util_Date_getUpdatedAtOrDefault_)|Retrieves the date at which the message was updated, or a default value if the message's updatedAt date is null.|
|[public AppSteroidUser getUser()](#com_fresvii_components_AppSteroidMessage_com_fresvii_components_AppSteroidUser_getUser_)|Retrieves the message's user.|
|[public AppSteroidUser getUserOrDefault()](#com_fresvii_components_AppSteroidMessage_com_fresvii_components_AppSteroidUser_getUserOrDefault_)|Retrieves the message's user, or a default value if the message's user is null.|



### Method Detail
 


## <a name="com_fresvii_components_AppSteroidMessage_java_util_Date_getCreatedAt_"> getCreatedAt </a>

```
public Date getCreatedAt()
```

Retrieves the date at which the message was created.

#### Returns

|Return Type|Description|
|---|---|
|Date|The date at which the message was created.|


## <a name="com_fresvii_components_AppSteroidMessage_java_util_Date_getCreatedAtOrDefault_"> getCreatedAtOrDefault </a>

```
public Date getCreatedAtOrDefault()
```

Retrieves the date at which the message was created, or a default value if the message's createdAt date is null.

#### Returns

|Return Type|Description|
|---|---|
|Date|The date at which the message was created, or a default value.|


## <a name="com_fresvii_components_AppSteroidMessage_java_lang_String_getGroupId_"> getGroupId </a>

```
public String getGroupId()
```

Retrieves the message's Group ID.

#### Returns

|Return Type|Description|
|---|---|
|String|The message's Group ID.|


## <a name="com_fresvii_components_AppSteroidMessage_java_lang_String_getGroupIdOrDefault_"> getGroupIdOrDefault </a>

```
public String getGroupIdOrDefault()
```

Retrieves the message's Group ID, or a default value if the message's Group ID is null.

#### Returns

|Return Type|Description|
|---|---|
|String|The message's Group ID, or a default value.|


## <a name="com_fresvii_components_AppSteroidMessage_java_lang_String_getId_"> getId </a>

```
public String getId()
```

Retrieves the message's ID.

#### Returns

|Return Type|Description|
|---|---|
|String|The message's ID.|


## <a name="com_fresvii_components_AppSteroidMessage_java_lang_String_getIdOrDefault_"> getIdOrDefault </a>

```
public String getIdOrDefault()
```

Retrieves the message's ID, or a default value if the message's ID is null.

#### Returns

|Return Type|Description|
|---|---|
|String|The message's ID, or a default value.|


## <a name="com_fresvii_components_AppSteroidMessage_java_lang_String_getImageThumbnailUrl_"> getImageThumbnailUrl </a>

```
public String getImageThumbnailUrl()
```

Retrieves the message's image thumbnail url.

#### Returns

|Return Type|Description|
|---|---|
|String|The message's image thumbnail url.|


## <a name="com_fresvii_components_AppSteroidMessage_java_lang_String_getImageThumbnailUrlOrDefault_"> getImageThumbnailUrlOrDefault </a>

```
public String getImageThumbnailUrlOrDefault()
```

Retrieves the message's image thumbnail url, or a default value if the message's image thumbnail url is null.

#### Returns

|Return Type|Description|
|---|---|
|String|The message's image thumbnail url, or a default value.|


## <a name="com_fresvii_components_AppSteroidMessage_com_fresvii_helper_ExternalBitmapWrapper_getImageThumbnailWrapper_"> getImageThumbnailWrapper </a>

```
public ExternalBitmapWrapper getImageThumbnailWrapper()
```

Retrieves the message's image thumbnail bitmap wrapper class which will load the image in the background.

#### Returns

|Return Type|Description|
|---|---|
|ExternalBitmapWrapper|Wrapper around the message's image thumbnail bitmap.|


## <a name="com_fresvii_components_AppSteroidMessage_java_lang_String_getImageUrl_"> getImageUrl </a>

```
public String getImageUrl()
```

Retrieves the message's image url.

#### Returns

|Return Type|Description|
|---|---|
|String|The message's image url.|


## <a name="com_fresvii_components_AppSteroidMessage_java_lang_String_getImageUrlOrDefault_"> getImageUrlOrDefault </a>

```
public String getImageUrlOrDefault()
```

Retrieves the message's image url, or a default value if the message's image url is null.

#### Returns

|Return Type|Description|
|---|---|
|String|The message's image url, or a default value.|


## <a name="com_fresvii_components_AppSteroidMessage_java_lang_String_getText_"> getText </a>

```
public String getText()
```

Retrieves the message's text.

#### Returns

|Return Type|Description|
|---|---|
|String|The message's text.|


## <a name="com_fresvii_components_AppSteroidMessage_java_lang_String_getTextOrDefault_"> getTextOrDefault </a>

```
public String getTextOrDefault()
```

Retrieves the message's text, or a default value if the message's text is null.

#### Returns

|Return Type|Description|
|---|---|
|String|The message's text, or a default value.|


## <a name="com_fresvii_components_AppSteroidMessage_java_util_Date_getUpdatedAt_"> getUpdatedAt </a>

```
public Date getUpdatedAt()
```

Retrieves the date at which the message was updated.

#### Returns

|Return Type|Description|
|---|---|
|Date|The date at which the message was updated.|


## <a name="com_fresvii_components_AppSteroidMessage_java_util_Date_getUpdatedAtOrDefault_"> getUpdatedAtOrDefault </a>

```
public Date getUpdatedAtOrDefault()
```

Retrieves the date at which the message was updated, or a default value if the message's updatedAt date is null.

#### Returns

|Return Type|Description|
|---|---|
|Date|The date at which the message was updated, or a default value.|


## <a name="com_fresvii_components_AppSteroidMessage_com_fresvii_components_AppSteroidUser_getUser_"> getUser </a>

```
public AppSteroidUser getUser()
```

Retrieves the message's user.

#### Returns

|Return Type|Description|
|---|---|
|AppSteroidUser|The message's user.|


## <a name="com_fresvii_components_AppSteroidMessage_com_fresvii_components_AppSteroidUser_getUserOrDefault_"> getUserOrDefault </a>

```
public AppSteroidUser getUserOrDefault()
```

Retrieves the message's user, or a default value if the message's user is null.

#### Returns

|Return Type|Description|
|---|---|
|AppSteroidUser|The message's user, or a default value.|



---  

## <a name="com.fresvii.server.access.callbacks.groupchat.SendImageMessageCallback"> Interface SendImageMessageCallback </a>

```
public interface SendImageMessageCallback implements FailureCallback
```

**Hierarchy:**  

```
com.fresvii.server.access.callbacks.groupchat.SendImageMessageCallback
```

**Description:**  
Callback interface to handle [GroupChatAccess.sendImageMessage()](#com_fresvii_server_access_GroupChatAccess_void_sendImageMessage_String_Bitmap_SendImageMessageCallback) results.

**Author:**  
Marcus Froeschl

**Version:**  
1.0




### Method Summary

|Method|Description|
|---|---|
|[public void onSuccess(AppSteroidMessage group)](#com_fresvii_server_access_callbacks_groupchat_SendImageMessageCallback_void_onSuccess_AppSteroidMessage)|Callback invoked when operation succeeds.|



### Method Detail
 


## <a name="com_fresvii_server_access_callbacks_groupchat_SendImageMessageCallback_void_onSuccess_AppSteroidMessage"> onSuccess </a>

```
public void onSuccess(AppSteroidMessage group)
```

Callback invoked when operation succeeds.

#### Parameters

|Parameter|Description|
|---|---|
|[AppSteroidMessage](#com.fresvii.components.AppSteroidMessage) group|The group that was created.|




---  

## <a name="com.fresvii.server.access.callbacks.groupchat.SendInGameMessageCallback"> Interface SendInGameMessageCallback </a>

```
public interface SendInGameMessageCallback implements FailureCallback
```

**Hierarchy:**  

```
com.fresvii.server.access.callbacks.groupchat.SendInGameMessageCallback
```

**Description:**  
Callback interface to handle [GroupChatAccess.sendInGameMessage()](#com_fresvii_server_access_GroupChatAccess_void_sendInGameMessage_String_String_SendInGameMessageCallback) results.

**Author:**  
Marcus Froeschl

**Version:**  
1.0




### Method Summary

|Method|Description|
|---|---|
|[public void onSuccess(AppSteroidMessage message)](#com_fresvii_server_access_callbacks_groupchat_SendInGameMessageCallback_void_onSuccess_AppSteroidMessage)|Callback invoked when operation succeeds.|



### Method Detail
 


## <a name="com_fresvii_server_access_callbacks_groupchat_SendInGameMessageCallback_void_onSuccess_AppSteroidMessage"> onSuccess </a>

```
public void onSuccess(AppSteroidMessage message)
```

Callback invoked when operation succeeds.

#### Parameters

|Parameter|Description|
|---|---|
|[AppSteroidMessage](#com.fresvii.components.AppSteroidMessage) message|The group that was created.|




---  

## <a name="com.fresvii.server.access.callbacks.groupchat.SendTextMessageCallback"> Interface SendTextMessageCallback </a>

```
public interface SendTextMessageCallback implements FailureCallback
```

**Hierarchy:**  

```
com.fresvii.server.access.callbacks.groupchat.SendTextMessageCallback
```

**Description:**  
Callback interface to handle [GroupChatAccess.sendTextMessage()](#com_fresvii_server_access_GroupChatAccess_void_sendTextMessage_String_String_SendTextMessageCallback) results.

**Author:**  
Marcus Froeschl

**Version:**  
1.0




### Method Summary

|Method|Description|
|---|---|
|[public void onSuccess(AppSteroidMessage group)](#com_fresvii_server_access_callbacks_groupchat_SendTextMessageCallback_void_onSuccess_AppSteroidMessage)|Callback invoked when operation succeeds.|



### Method Detail
 


## <a name="com_fresvii_server_access_callbacks_groupchat_SendTextMessageCallback_void_onSuccess_AppSteroidMessage"> onSuccess </a>

```
public void onSuccess(AppSteroidMessage group)
```

Callback invoked when operation succeeds.

#### Parameters

|Parameter|Description|
|---|---|
|[AppSteroidMessage](#com.fresvii.components.AppSteroidMessage) group|The group that was created.|




---  

## <a name="com.fresvii.server.access.callbacks.groupchat.GetGroupMessageCallback"> Interface GetGroupMessageCallback </a>

```
public interface GetGroupMessageCallback implements FailureCallback
```

**Hierarchy:**  

```
com.fresvii.server.access.callbacks.groupchat.GetGroupMessageCallback
```

**Description:**  
Callback interface to handle [GroupChatAccess.getGroupMessage()](#com_fresvii_server_access_GroupChatAccess_void_getGroupMessage_String_String_GetGroupMessageCallback) results.

**Author:**  
Marcus Froeschl

**Version:**  
1.0




### Method Summary

|Method|Description|
|---|---|
|[public void onSuccess(AppSteroidMessage message)](#com_fresvii_server_access_callbacks_groupchat_GetGroupMessageCallback_void_onSuccess_AppSteroidMessage)|Callback invoked when operation succeeds.|



### Method Detail
 


## <a name="com_fresvii_server_access_callbacks_groupchat_GetGroupMessageCallback_void_onSuccess_AppSteroidMessage"> onSuccess </a>

```
public void onSuccess(AppSteroidMessage message)
```

Callback invoked when operation succeeds.

#### Parameters

|Parameter|Description|
|---|---|
|[AppSteroidMessage](#com.fresvii.components.AppSteroidMessage) message|The retrieved message.|




---  

## <a name="com.fresvii.server.access.callbacks.groupchat.GetGroupMessagesCallback"> Interface GetGroupMessagesCallback </a>

```
public interface GetGroupMessagesCallback implements FailureCallback
```

**Hierarchy:**  

```
com.fresvii.server.access.callbacks.groupchat.GetGroupMessagesCallback
```

**Description:**  
Callback interface to handle [GroupChatAccess.getGroupMessages()](#com_fresvii_server_access_GroupChatAccess_void_getGroupMessages_String_int_GetGroupMessagesCallback) results.

**Author:**  
Marcus Froeschl

**Version:**  
1.1




### Method Summary

|Method|Description|
|---|---|
|[public void onSuccess(AppSteroidListMetaInfo metaInfo, List messages)](#com_fresvii_server_access_callbacks_groupchat_GetGroupMessagesCallback_void_onSuccess_AppSteroidListMetaInfo_List)|Callback invoked when operation succeeds.|



### Method Detail
 


## <a name="com_fresvii_server_access_callbacks_groupchat_GetGroupMessagesCallback_void_onSuccess_AppSteroidListMetaInfo_List"> onSuccess </a>

```
public void onSuccess(AppSteroidListMetaInfo metaInfo,  
                      List messages)
```

Callback invoked when operation succeeds.

#### Parameters

|Parameter|Description|
|---|---|
|[AppSteroidListMetaInfo](AndroidSDK.md#com.fresvii.components.AppSteroidListMetaInfo) metaInfo|List meta information.|
|List messages|List of messages retrieved.|




---  

## <a name="com.fresvii.server.access.callbacks.groupchat.GetMessageGroupsCallback"> Interface GetMessageGroupsCallback </a>

```
public interface GetMessageGroupsCallback implements FailureCallback
```

**Hierarchy:**  

```
com.fresvii.server.access.callbacks.groupchat.GetMessageGroupsCallback
```

**Description:**  
Callback interface to handle [GroupChatAccess.getMessageGroups()](#com_fresvii_server_access_GroupChatAccess_void_getMessageGroups_GetMessageGroupsCallback) results.

**Author:**  
Marcus Froeschl

**Version:**  
1.1




### Method Summary

|Method|Description|
|---|---|
|[public void onSuccess(AppSteroidListMetaInfo metaInfo, List groups)](#com_fresvii_server_access_callbacks_groupchat_GetMessageGroupsCallback_void_onSuccess_AppSteroidListMetaInfo_List)|Callback invoked when operation succeeds.|



### Method Detail
 


## <a name="com_fresvii_server_access_callbacks_groupchat_GetMessageGroupsCallback_void_onSuccess_AppSteroidListMetaInfo_List"> onSuccess </a>

```
public void onSuccess(AppSteroidListMetaInfo metaInfo,  
                      List groups)
```

Callback invoked when operation succeeds.

#### Parameters

|Parameter|Description|
|---|---|
|[AppSteroidListMetaInfo](AndroidSDK.md#com.fresvii.components.AppSteroidListMetaInfo) metaInfo|List meta information.|
|List groups|List of groups with messages retrieved.|




---  

## <a name="com.fresvii.server.access.callbacks.groupchat.DeleteGroupMessageCallback"> Interface DeleteGroupMessageCallback </a>

```
public interface DeleteGroupMessageCallback implements FailureCallback
```

**Hierarchy:**  

```
com.fresvii.server.access.callbacks.groupchat.DeleteGroupMessageCallback
```

**Description:**  
Callback interface to handle [GroupChatAccess.deleteGroupMessage()](#com_fresvii_server_access_GroupChatAccess_void_deleteGroupMessage_String_String_DeleteGroupMessageCallback) results.

**Author:**  
Marcus Froeschl

**Version:**  
1.0




### Method Summary

|Method|Description|
|---|---|
|[public void onSuccess()](#com_fresvii_server_access_callbacks_groupchat_DeleteGroupMessageCallback_void_onSuccess_)|Callback invoked when operation succeeds.|



### Method Detail
 


## <a name="com_fresvii_server_access_callbacks_groupchat_DeleteGroupMessageCallback_void_onSuccess_"> onSuccess </a>

```
public void onSuccess()
```

Callback invoked when operation succeeds.


