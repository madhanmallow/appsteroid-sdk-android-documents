
# AppSteroid Group API

Last updated 2014-10-08

-------------------------

## Introduction

AppSteroid Group API can be used to manage AppSteroid groups. You can create groups, add or remove members to/from groups, etc. Groups are the cornerstone for many AppSteroid features. E.g. [Group Chat](GroupChat.md), [VoiceChat](VoiceChat.md) and [Matchmaking](Matchmaking.md) Feature are closely tied to groups. Group creation and management is one of the major tasks your application will have to handle to make full use of these features.


---  

## Classes

|Class|Description|
|---|---|
|[GroupAccess](#com.fresvii.server.access.GroupAccess)|Provides access to Fresvii Server's Group API.|
|[AppSteroidGroup](#com.fresvii.components.AppSteroidGroup)|Represents a Fresvii Group used for text chat, voice chat etc.|
|[CreateMultiGroupCallback](#com.fresvii.server.access.callbacks.group.CreateMultiGroupCallback)|Callback interface to handle [GroupAccess.createMultiGroup()](#com_fresvii_server_access_GroupAccess_void_createMultiGroup_String_List_CreateMultiGroupCallback) results.|
|[CreatePairGroupCallback](#com.fresvii.server.access.callbacks.group.CreatePairGroupCallback)|Callback interface to handle [GroupAccess.createPairGroup()](#com_fresvii_server_access_GroupAccess_void_createPairGroup_String_CreatePairGroupCallback) results.|
|[UpdateMultiGroupCallback](#com.fresvii.server.access.callbacks.group.UpdateMultiGroupCallback)|Callback interface to handle [GroupAccess.updateMultiGroup()](#com_fresvii_server_access_GroupAccess_void_updateMultiGroup_String_String_UpdateMultiGroupCallback) results.|
|[GetGroupsCallback](#com.fresvii.server.access.callbacks.group.GetGroupsCallback)|Callback interface to handle [GroupAccess.getGroups()](#com_fresvii_server_access_GroupAccess_void_getGroups_GetGroupsCallback) results.|
|[DeleteGroupCallback](#com.fresvii.server.access.callbacks.group.DeleteGroupCallback)|Callback interface to handle [GroupAccess.deleteGroup()](#com_fresvii_server_access_GroupAccess_void_deleteGroup_String_DeleteGroupCallback) results.|
|[SubscribeToGroupCallback](#com.fresvii.server.access.callbacks.group.SubscribeToGroupCallback)|Callback interface to handle [GroupAccess.subscribeToGroup()](#com_fresvii_server_access_GroupAccess_void_subscribeToGroup_String_SubscribeToGroupCallback) results.|
|[UnsubscribeFromGroupCallback](#com.fresvii.server.access.callbacks.group.UnsubscribeFromGroupCallback)|Callback interface to handle [GroupAccess.unsubscribeFromGroup()](#com_fresvii_server_access_GroupAccess_void_unsubscribeFromGroup_String_UnsubscribeFromGroupCallback) results.|
|[GetGroupMembersCallback](#com.fresvii.server.access.callbacks.group.GetGroupMembersCallback)|Callback interface to handle [GroupAccess.getGroupMembers()](#com_fresvii_server_access_GroupAccess_void_getGroupMembers_String_int_GetGroupMembersCallback) results.|
|[GetAllGroupMembersCallback](#com.fresvii.server.access.callbacks.group.GetAllGroupMembersCallback)|Callback interface to handle [GroupAccess.getAllGroupMembers()](#com_fresvii_server_access_GroupAccess_void_getAllGroupMembers_String_GetAllGroupMembersCallback) results.|
|[GetAllFriendsInGroupCallback](#com.fresvii.server.access.callbacks.group.GetAllFriendsInGroupCallback)|Callback interface to handle [GroupAccess.getAllFriendsInGroup()](#com_fresvii_server_access_GroupAccess_void_getAllFriendsInGroup_String_GetAllFriendsInGroupCallback) results.|
|[AddMemberToMultiGroupCallback](#com.fresvii.server.access.callbacks.group.AddMemberToMultiGroupCallback)|Callback interface to handle [GroupAccess.addMemberToMultiGroup()](#com_fresvii_server_access_GroupAccess_void_addMemberToMultiGroup_String_String_AddMemberToMultiGroupCallback) results.|
|[DeleteMemberFromMultiGroupCallback](#com.fresvii.server.access.callbacks.group.DeleteMemberFromMultiGroupCallback)|Callback interface to handle [GroupAccess.deleteMemberFromMultiGroup()](#com_fresvii_server_access_GroupAccess_void_deleteMemberFromMultiGroup_String_String_DeleteMemberFromMultiGroupCallback) results.|



---  

## <a name="com.fresvii.server.access.GroupAccess"> Class GroupAccess </a>

```
public class GroupAccess extends Object
```

**Hierarchy:**  

```
java.lang.Object  
    com.fresvii.server.access.GroupAccess
```

**Description:**  
Provides access to Fresvii Server's Group API.  Can be used to create or delete groups, and add or remove members from groups, etc.

**Author:**  
Marcus Froeschl

**Version:**  
1.0

**Since:**  
2014-05-26


### Method Summary

|Method|Description|
|---|---|
|[public static void addMemberToMultiGroup(String groupId, String userId, AddMemberToMultiGroupCallback callback)](#com_fresvii_server_access_GroupAccess_void_addMemberToMultiGroup_String_String_AddMemberToMultiGroupCallback)|Adds a member to a MultiGroup.|
|[public static void createMultiGroup(String name, List invitedUsers, CreateMultiGroupCallback callback)](#com_fresvii_server_access_GroupAccess_void_createMultiGroup_String_List_CreateMultiGroupCallback)|Creates a MultiGroup.|
|[public static void createPairGroup(String userId, CreatePairGroupCallback callback)](#com_fresvii_server_access_GroupAccess_void_createPairGroup_String_CreatePairGroupCallback)|Creates a PairGroup.|
|[public static void deleteGroup(String groupId, DeleteGroupCallback callback)](#com_fresvii_server_access_GroupAccess_void_deleteGroup_String_DeleteGroupCallback)|Deletes a Group (MultiGroup or PairGroup).|
|[public static void deleteMemberFromMultiGroup(String groupId, String userId, DeleteMemberFromMultiGroupCallback callback)](#com_fresvii_server_access_GroupAccess_void_deleteMemberFromMultiGroup_String_String_DeleteMemberFromMultiGroupCallback)|Deletes a member from a MultiGroup.|
|[public static void getAllFriendsInGroup(String groupId, GetAllFriendsInGroupCallback callback)](#com_fresvii_server_access_GroupAccess_void_getAllFriendsInGroup_String_GetAllFriendsInGroupCallback)|Retrieves a list of all friends in a group. This can involve multiple server requests, the caller will only|
|[public static void getAllGroupMembers(String groupId, GetAllGroupMembersCallback callback)](#com_fresvii_server_access_GroupAccess_void_getAllGroupMembers_String_GetAllGroupMembersCallback)|Retrieves a list of all members of a group. This can involve multiple server requests, the caller will only|
|[public static void getAllGroupMembers(String groupId, GetGroupMembersCallback intermediaryCallback, GetAllGroupMembersCallback finalCallback)](#com_fresvii_server_access_GroupAccess_void_getAllGroupMembers_String_GetGroupMembersCallback_GetAllGroupMembersCallback)|Retrieves a list of all members of a group. This can involve multiple server requests, the caller will be informed |
|[public static void getGroup(String groupId, GetGroupCallback callback)](#com_fresvii_server_access_GroupAccess_void_getGroup_String_GetGroupCallback)|Retrieves a Group (MultiGroup or PairGroup).|
|[public static void getGroupMembers(String groupId, GetGroupMembersCallback callback)](#com_fresvii_server_access_GroupAccess_void_getGroupMembers_String_GetGroupMembersCallback)|Retrieves a list of members for a group from the initial page.|
|[public static void getGroupMembers(String groupId, int page, GetGroupMembersCallback callback)](#com_fresvii_server_access_GroupAccess_void_getGroupMembers_String_int_GetGroupMembersCallback)|Retrieves a list of members for a group from the specified page|
|[public static void getGroups(GetGroupsCallback callback)](#com_fresvii_server_access_GroupAccess_void_getGroups_GetGroupsCallback)|Retrieves a list of Groups from the initial page.|
|[public static void getGroups(int page, GetGroupsCallback callback)](#com_fresvii_server_access_GroupAccess_void_getGroups_int_GetGroupsCallback)|Retrieves a list of MultiGroups from the specified page.|
|[public static void subscribeToGroup(String groupId, SubscribeToGroupCallback callback)](#com_fresvii_server_access_GroupAccess_void_subscribeToGroup_String_SubscribeToGroupCallback)|Subscribes to a group (MultiGroup or PairGroup) in order to receive notifications from that group.|
|[public static void unsubscribeFromGroup(String groupId, UnsubscribeFromGroupCallback callback)](#com_fresvii_server_access_GroupAccess_void_unsubscribeFromGroup_String_UnsubscribeFromGroupCallback)|Unsubscribes from a group (MultiGroup or PairGroup) in order to no longer receive notifications from that group.|
|[public static void updateMultiGroup(String groupId, String name, UpdateMultiGroupCallback callback)](#com_fresvii_server_access_GroupAccess_void_updateMultiGroup_String_String_UpdateMultiGroupCallback)|Updates a MultiGroup.|



### Method Detail
 


## <a name="com_fresvii_server_access_GroupAccess_void_addMemberToMultiGroup_String_String_AddMemberToMultiGroupCallback"> addMemberToMultiGroup </a>

```
public static void addMemberToMultiGroup(String groupId,  
                                         String userId,  
                                         AddMemberToMultiGroupCallback callback)
```

Adds a member to a MultiGroup.

#### Parameters

|Parameter|Description|
|---|---|
|String groupId|ID of the group to which the member should be added.|
|String userId|ID of the user to be added.|
|[AddMemberToMultiGroupCallback](#com.fresvii.server.access.callbacks.group.AddMemberToMultiGroupCallback) callback|[Callback](#com.fresvii.server.access.callbacks.group.AddMemberToMultiGroupCallback) to be informed about the result of the operation.|



## <a name="com_fresvii_server_access_GroupAccess_void_createMultiGroup_String_List_CreateMultiGroupCallback"> createMultiGroup </a>

```
public static void createMultiGroup(String name,  
                                    List invitedUsers,  
                                    CreateMultiGroupCallback callback)
```

Creates a MultiGroup.

#### Parameters

|Parameter|Description|
|---|---|
|String name|Optional name for the group.|
|List invitedUsers|[Callback](#com.fresvii.server.access.callbacks.group.CreateMultiGroupCallback) to be informed about the result of the operation.|



## <a name="com_fresvii_server_access_GroupAccess_void_createPairGroup_String_CreatePairGroupCallback"> createPairGroup </a>

```
public static void createPairGroup(String userId,  
                                   CreatePairGroupCallback callback)
```

Creates a PairGroup.

#### Parameters

|Parameter|Description|
|---|---|
|String userId|[Callback](#com.fresvii.server.access.callbacks.group.CreatePairGroupCallback) to be informed about the result of the operation.|



## <a name="com_fresvii_server_access_GroupAccess_void_deleteGroup_String_DeleteGroupCallback"> deleteGroup </a>

```
public static void deleteGroup(String groupId,  
                               DeleteGroupCallback callback)
```

Deletes a Group (MultiGroup or PairGroup).

#### Parameters

|Parameter|Description|
|---|---|
|String groupId|ID of the group to be deleted.|
|[DeleteGroupCallback](#com.fresvii.server.access.callbacks.group.DeleteGroupCallback) callback|[Callback](#com.fresvii.server.access.callbacks.group.DeleteGroupCallback) to be informed about the result of the operation.|



## <a name="com_fresvii_server_access_GroupAccess_void_deleteMemberFromMultiGroup_String_String_DeleteMemberFromMultiGroupCallback"> deleteMemberFromMultiGroup </a>

```
public static void deleteMemberFromMultiGroup(String groupId,  
                                              String userId,  
                                              DeleteMemberFromMultiGroupCallback callback)
```

Deletes a member from a MultiGroup.

#### Parameters

|Parameter|Description|
|---|---|
|String groupId|ID of the group from which the member should be deleted.|
|String userId|ID of the user to be deleted from the group.|
|[DeleteMemberFromMultiGroupCallback](#com.fresvii.server.access.callbacks.group.DeleteMemberFromMultiGroupCallback) callback|[Callback](#com.fresvii.server.access.callbacks.group.DeleteMemberFromMultiGroupCallback) to be informed about the result of the operation.|



## <a name="com_fresvii_server_access_GroupAccess_void_getAllFriendsInGroup_String_GetAllFriendsInGroupCallback"> getAllFriendsInGroup </a>

```
public static void getAllFriendsInGroup(String groupId,  
                                        GetAllFriendsInGroupCallback callback)
```

Retrieves a list of all friends in a group. This can involve multiple server requests, the caller will only  be informed of the final result containing the list of all group members.

#### Parameters

|Parameter|Description|
|---|---|
|String groupId|ID of the group who's members are to be retrieved.|
|[GetAllFriendsInGroupCallback](#com.fresvii.server.access.callbacks.group.GetAllFriendsInGroupCallback) callback|[Callback](#com.fresvii.server.access.callbacks.group.GetAllFriendsInGroupCallback) to be informed about the result of the operation.|



## <a name="com_fresvii_server_access_GroupAccess_void_getAllGroupMembers_String_GetAllGroupMembersCallback"> getAllGroupMembers </a>

```
public static void getAllGroupMembers(String groupId,  
                                      GetAllGroupMembersCallback callback)
```

Retrieves a list of all members of a group. This can involve multiple server requests, the caller will only  be informed of the final result containing the list of all group members.

#### Parameters

|Parameter|Description|
|---|---|
|String groupId|ID of the group who's members are to be retrieved.|
|[GetAllGroupMembersCallback](#com.fresvii.server.access.callbacks.group.GetAllGroupMembersCallback) callback|[Callback](#com.fresvii.server.access.callbacks.group.GetAllGroupMembersCallback) to be informed about the result of the operation.|



## <a name="com_fresvii_server_access_GroupAccess_void_getAllGroupMembers_String_GetGroupMembersCallback_GetAllGroupMembersCallback"> getAllGroupMembers </a>

```
public static void getAllGroupMembers(String groupId,  
                                      GetGroupMembersCallback intermediaryCallback,  
                                      GetAllGroupMembersCallback finalCallback)
```

Retrieves a list of all members of a group. This can involve multiple server requests, the caller will be informed   of intermediary server results and the final server result containing the list of all group members.

#### Parameters

|Parameter|Description|
|---|---|
|String groupId|ID of the group who's members are to be retrieved.|
|[GetGroupMembersCallback](#com.fresvii.server.access.callbacks.group.GetGroupMembersCallback) intermediaryCallback|[Callback](#com.fresvii.server.access.callbacks.group.GetGroupMembersCallback) to be informed about an intermediary |
|[GetAllGroupMembersCallback](#com.fresvii.server.access.callbacks.group.GetAllGroupMembersCallback) finalCallback|[Callback](#com.fresvii.server.access.callbacks.group.GetAllGroupMembersCallback) to be informed about the final result of the |



## <a name="com_fresvii_server_access_GroupAccess_void_getGroup_String_GetGroupCallback"> getGroup </a>

```
public static void getGroup(String groupId,  
                            GetGroupCallback callback)
```

Retrieves a Group (MultiGroup or PairGroup).

#### Parameters

|Parameter|Description|
|---|---|
|String groupId|ID of the group to be retrieved.|
|GetGroupCallback callback|Callback to be informed about the result of the operation.|



## <a name="com_fresvii_server_access_GroupAccess_void_getGroupMembers_String_GetGroupMembersCallback"> getGroupMembers </a>

```
public static void getGroupMembers(String groupId,  
                                   GetGroupMembersCallback callback)
```

Retrieves a list of members for a group from the initial page.

#### Parameters

|Parameter|Description|
|---|---|
|String groupId|ID of the group who's members are to be retrieved.|
|[GetGroupMembersCallback](#com.fresvii.server.access.callbacks.group.GetGroupMembersCallback) callback|[Callback](#com.fresvii.server.access.callbacks.group.GetGroupMembersCallback) to be informed about the result of the operation.|



## <a name="com_fresvii_server_access_GroupAccess_void_getGroupMembers_String_int_GetGroupMembersCallback"> getGroupMembers </a>

```
public static void getGroupMembers(String groupId,  
                                   int page,  
                                   GetGroupMembersCallback callback)
```

Retrieves a list of members for a group from the specified page

#### Parameters

|Parameter|Description|
|---|---|
|String groupId|ID of the group who's members are to be retrieved.|
|int page|Page offset.|
|[GetGroupMembersCallback](#com.fresvii.server.access.callbacks.group.GetGroupMembersCallback) callback|[Callback](#com.fresvii.server.access.callbacks.group.GetGroupMembersCallback) to be informed about the result of the operation.|



## <a name="com_fresvii_server_access_GroupAccess_void_getGroups_GetGroupsCallback"> getGroups </a>

```
public static void getGroups(GetGroupsCallback callback)
```

Retrieves a list of Groups from the initial page.

#### Parameters

|Parameter|Description|
|---|---|
|[GetGroupsCallback](#com.fresvii.server.access.callbacks.group.GetGroupsCallback) callback|[Callback](#com.fresvii.server.access.callbacks.group.GetGroupsCallback) to be informed about the result of the operation.|



## <a name="com_fresvii_server_access_GroupAccess_void_getGroups_int_GetGroupsCallback"> getGroups </a>

```
public static void getGroups(int page,  
                             GetGroupsCallback callback)
```

Retrieves a list of MultiGroups from the specified page.

#### Parameters

|Parameter|Description|
|---|---|
|int page|Page offset.|
|[GetGroupsCallback](#com.fresvii.server.access.callbacks.group.GetGroupsCallback) callback|[Callback](#com.fresvii.server.access.callbacks.group.GetGroupsCallback) to be informed about the result of the operation.|



## <a name="com_fresvii_server_access_GroupAccess_void_subscribeToGroup_String_SubscribeToGroupCallback"> subscribeToGroup </a>

```
public static void subscribeToGroup(String groupId,  
                                    SubscribeToGroupCallback callback)
```

Subscribes to a group (MultiGroup or PairGroup) in order to receive notifications from that group.

#### Parameters

|Parameter|Description|
|---|---|
|String groupId|ID of the group to be subscribed.|
|[SubscribeToGroupCallback](#com.fresvii.server.access.callbacks.group.SubscribeToGroupCallback) callback|[Callback](#com.fresvii.server.access.callbacks.group.SubscribeToGroupCallback) to be informed about the result of the operation.|



## <a name="com_fresvii_server_access_GroupAccess_void_unsubscribeFromGroup_String_UnsubscribeFromGroupCallback"> unsubscribeFromGroup </a>

```
public static void unsubscribeFromGroup(String groupId,  
                                        UnsubscribeFromGroupCallback callback)
```

Unsubscribes from a group (MultiGroup or PairGroup) in order to no longer receive notifications from that group.

#### Parameters

|Parameter|Description|
|---|---|
|String groupId|ID of the group to be unsubscribed.|
|[UnsubscribeFromGroupCallback](#com.fresvii.server.access.callbacks.group.UnsubscribeFromGroupCallback) callback|[Callback](#com.fresvii.server.access.callbacks.group.UnsubscribeFromGroupCallback) to be informed about the result of the operation.|



## <a name="com_fresvii_server_access_GroupAccess_void_updateMultiGroup_String_String_UpdateMultiGroupCallback"> updateMultiGroup </a>

```
public static void updateMultiGroup(String groupId,  
                                    String name,  
                                    UpdateMultiGroupCallback callback)
```

Updates a MultiGroup.

#### Parameters

|Parameter|Description|
|---|---|
|String groupId|ID of the group to be deleted.|
|String name|Optional name for the group.|
|[UpdateMultiGroupCallback](#com.fresvii.server.access.callbacks.group.UpdateMultiGroupCallback) callback|[Callback](#com.fresvii.server.access.callbacks.group.UpdateMultiGroupCallback) to be informed about the result of the operation.|




---  

## <a name="com.fresvii.components.AppSteroidGroup"> Class AppSteroidGroup </a>

```
public class AppSteroidGroup extends AppSteroidComponent
```

**Hierarchy:**  

```
java.lang.Object  
    com.fresvii.components.AppSteroidComponent  
        com.fresvii.components.AppSteroidGroup
```

**Description:**  
Represents a Fresvii Group used for text chat, voice chat etc.

**Author:**  
Marcus Froeschl

**Version:**  
1.0

**Since:**  
2014-05-26


### Method Summary

|Method|Description|
|---|---|
|[public Date getCreatedAt()](#com_fresvii_components_AppSteroidGroup_java_util_Date_getCreatedAt_)|Retrieves the date at which the group was created.|
|[public Date getCreatedAtOrDefault()](#com_fresvii_components_AppSteroidGroup_java_util_Date_getCreatedAtOrDefault_)|Retrieves the date at which the group was created, or a default value if the group's createdAt date is null.|
|[public String getId()](#com_fresvii_components_AppSteroidGroup_java_lang_String_getId_)|Retrieves the group's ID.|
|[public String getIdOrDefault()](#com_fresvii_components_AppSteroidGroup_java_lang_String_getIdOrDefault_)|Retrieves the group's ID, or a default value if the group's ID is null.|
|[public AppSteroidMessage getLatestMessage()](#com_fresvii_components_AppSteroidGroup_com_fresvii_components_AppSteroidMessage_getLatestMessage_)|Retrieves the group's latest message.|
|[public AppSteroidMessage getLatestMessageOrDefault()](#com_fresvii_components_AppSteroidGroup_com_fresvii_components_AppSteroidMessage_getLatestMessageOrDefault_)|Retrieves the group's latest message, or a default value if the group's latest message is null.|
|[public Integer getMemberCount()](#com_fresvii_components_AppSteroidGroup_java_lang_Integer_getMemberCount_)|Retrieves the group's member count.|
|[public int getMemberCountOrDefault()](#com_fresvii_components_AppSteroidGroup_int_getMemberCountOrDefault_)|Retrieves the group's member count, or a default value if the group's member count is null.|
|[public List getMembers()](#com_fresvii_components_AppSteroidGroup_java_util_List_getMembers_)|Retrieves the group's members.|
|[public List getMembersOrDefault()](#com_fresvii_components_AppSteroidGroup_java_util_List_getMembersOrDefault_)|Retrieves the group's member list, or a default value if the group's member list is null.|
|[public List getMessageUsers()](#com_fresvii_components_AppSteroidGroup_java_util_List_getMessageUsers_)|Retrieves the group's message users.|
|[public List getMessageUsersOrDefault()](#com_fresvii_components_AppSteroidGroup_java_util_List_getMessageUsersOrDefault_)|Retrieves the group's message user list, or a default value if the group's message user list is null.|
|[public String getName()](#com_fresvii_components_AppSteroidGroup_java_lang_String_getName_)|Retrieves the group's name.|
|[public String getNameOrDefault()](#com_fresvii_components_AppSteroidGroup_java_lang_String_getNameOrDefault_)|Retrieves the group's name, or a default value if the group's name is null.|
|[public String getRole()](#com_fresvii_components_AppSteroidGroup_java_lang_String_getRole_)|Retrieves the group's role.|
|[public String getRoleOrDefault()](#com_fresvii_components_AppSteroidGroup_java_lang_String_getRoleOrDefault_)|Retrieves the group's role, or a default value if the group's role is null.|
|[public List getSortedMembers()](#com_fresvii_components_AppSteroidGroup_java_util_List_getSortedMembers_)|Retrieves the group's members, sorted alphabetically by member name|
|[public List getSortedMembersOrDefault()](#com_fresvii_components_AppSteroidGroup_java_util_List_getSortedMembersOrDefault_)|Retrieves the group's member list, sorted alphabetically by member name, or a default value if the group's member list is null.|
|[public Date getUpdatedAt()](#com_fresvii_components_AppSteroidGroup_java_util_Date_getUpdatedAt_)|Retrieves the date at which the group was updated.|
|[public Date getUpdatedAtOrDefault()](#com_fresvii_components_AppSteroidGroup_java_util_Date_getUpdatedAtOrDefault_)|Retrieves the date at which the group was updated, or a default value if the group's updatedAt date is null.|
|[public Boolean isCurrentUserSubscribedToGroup()](#com_fresvii_components_AppSteroidGroup_java_lang_Boolean_isCurrentUserSubscribedToGroup_)|Retrieves the group's "subscribed" property.|
|[public boolean isCurrentUserSubscribedToGroupOrDefault()](#com_fresvii_components_AppSteroidGroup_boolean_isCurrentUserSubscribedToGroupOrDefault_)|Retrieves the group's "subscribed" property, or a default value if the group's "subscribed" property is null.|
|[public Boolean isPairGroup()](#com_fresvii_components_AppSteroidGroup_java_lang_Boolean_isPairGroup_)|Retrieves the group's "pair" property.|
|[public boolean isPairGroupOrDefault()](#com_fresvii_components_AppSteroidGroup_boolean_isPairGroupOrDefault_)|Retrieves the group's "pair" property, or a default value if the group's "pair" property is null.|



### Method Detail
 


## <a name="com_fresvii_components_AppSteroidGroup_java_util_Date_getCreatedAt_"> getCreatedAt </a>

```
public Date getCreatedAt()
```

Retrieves the date at which the group was created.

#### Returns

|Return Type|Description|
|---|---|
|Date|The date at which the group was created.|


## <a name="com_fresvii_components_AppSteroidGroup_java_util_Date_getCreatedAtOrDefault_"> getCreatedAtOrDefault </a>

```
public Date getCreatedAtOrDefault()
```

Retrieves the date at which the group was created, or a default value if the group's createdAt date is null.

#### Returns

|Return Type|Description|
|---|---|
|Date|The date at which the group was created, or a default value|


## <a name="com_fresvii_components_AppSteroidGroup_java_lang_String_getId_"> getId </a>

```
public String getId()
```

Retrieves the group's ID.

#### Returns

|Return Type|Description|
|---|---|
|String|The group's ID.|


## <a name="com_fresvii_components_AppSteroidGroup_java_lang_String_getIdOrDefault_"> getIdOrDefault </a>

```
public String getIdOrDefault()
```

Retrieves the group's ID, or a default value if the group's ID is null.

#### Returns

|Return Type|Description|
|---|---|
|String|The group's ID, or a default value|


## <a name="com_fresvii_components_AppSteroidGroup_com_fresvii_components_AppSteroidMessage_getLatestMessage_"> getLatestMessage </a>

```
public AppSteroidMessage getLatestMessage()
```

Retrieves the group's latest message.

#### Returns

|Return Type|Description|
|---|---|
|AppSteroidMessage|The group's latest message.|


## <a name="com_fresvii_components_AppSteroidGroup_com_fresvii_components_AppSteroidMessage_getLatestMessageOrDefault_"> getLatestMessageOrDefault </a>

```
public AppSteroidMessage getLatestMessageOrDefault()
```

Retrieves the group's latest message, or a default value if the group's latest message is null.

#### Returns

|Return Type|Description|
|---|---|
|AppSteroidMessage|The group's latest message, or a default value|


## <a name="com_fresvii_components_AppSteroidGroup_java_lang_Integer_getMemberCount_"> getMemberCount </a>

```
public Integer getMemberCount()
```

Retrieves the group's member count.

#### Returns

|Return Type|Description|
|---|---|
|Integer|The group's member count.|


## <a name="com_fresvii_components_AppSteroidGroup_int_getMemberCountOrDefault_"> getMemberCountOrDefault </a>

```
public int getMemberCountOrDefault()
```

Retrieves the group's member count, or a default value if the group's member count is null.

#### Returns

|Return Type|Description|
|---|---|
|int|The group's member count, or a default value|


## <a name="com_fresvii_components_AppSteroidGroup_java_util_List_getMembers_"> getMembers </a>

```
public List getMembers()
```

Retrieves the group's members.

#### Returns

|Return Type|Description|
|---|---|
|List|The group's members.|


## <a name="com_fresvii_components_AppSteroidGroup_java_util_List_getMembersOrDefault_"> getMembersOrDefault </a>

```
public List getMembersOrDefault()
```

Retrieves the group's member list, or a default value if the group's member list is null.

#### Returns

|Return Type|Description|
|---|---|
|List|The group's member list, or a default value|


## <a name="com_fresvii_components_AppSteroidGroup_java_util_List_getMessageUsers_"> getMessageUsers </a>

```
public List getMessageUsers()
```

Retrieves the group's message users.

#### Returns

|Return Type|Description|
|---|---|
|List|The group's message users.|


## <a name="com_fresvii_components_AppSteroidGroup_java_util_List_getMessageUsersOrDefault_"> getMessageUsersOrDefault </a>

```
public List getMessageUsersOrDefault()
```

Retrieves the group's message user list, or a default value if the group's message user list is null.

#### Returns

|Return Type|Description|
|---|---|
|List|The group's message user list, or a default value|


## <a name="com_fresvii_components_AppSteroidGroup_java_lang_String_getName_"> getName </a>

```
public String getName()
```

Retrieves the group's name.

#### Returns

|Return Type|Description|
|---|---|
|String|The group's name.|


## <a name="com_fresvii_components_AppSteroidGroup_java_lang_String_getNameOrDefault_"> getNameOrDefault </a>

```
public String getNameOrDefault()
```

Retrieves the group's name, or a default value if the group's name is null.

#### Returns

|Return Type|Description|
|---|---|
|String|The group's name, or a default value|


## <a name="com_fresvii_components_AppSteroidGroup_java_lang_String_getRole_"> getRole </a>

```
public String getRole()
```

Retrieves the group's role.

#### Returns

|Return Type|Description|
|---|---|
|String|The group's role.|


## <a name="com_fresvii_components_AppSteroidGroup_java_lang_String_getRoleOrDefault_"> getRoleOrDefault </a>

```
public String getRoleOrDefault()
```

Retrieves the group's role, or a default value if the group's role is null.

#### Returns

|Return Type|Description|
|---|---|
|String|The group's role, or a default value|


## <a name="com_fresvii_components_AppSteroidGroup_java_util_List_getSortedMembers_"> getSortedMembers </a>

```
public List getSortedMembers()
```

Retrieves the group's members, sorted alphabetically by member name

#### Returns

|Return Type|Description|
|---|---|
|List|The group's members.|


## <a name="com_fresvii_components_AppSteroidGroup_java_util_List_getSortedMembersOrDefault_"> getSortedMembersOrDefault </a>

```
public List getSortedMembersOrDefault()
```

Retrieves the group's member list, sorted alphabetically by member name, or a default value if the group's member list is null.

#### Returns

|Return Type|Description|
|---|---|
|List|The group's member list, or a default value|


## <a name="com_fresvii_components_AppSteroidGroup_java_util_Date_getUpdatedAt_"> getUpdatedAt </a>

```
public Date getUpdatedAt()
```

Retrieves the date at which the group was updated.

#### Returns

|Return Type|Description|
|---|---|
|Date|The date at which the group was updated.|


## <a name="com_fresvii_components_AppSteroidGroup_java_util_Date_getUpdatedAtOrDefault_"> getUpdatedAtOrDefault </a>

```
public Date getUpdatedAtOrDefault()
```

Retrieves the date at which the group was updated, or a default value if the group's updatedAt date is null.

#### Returns

|Return Type|Description|
|---|---|
|Date|The date at which the group was updated, or a default value|


## <a name="com_fresvii_components_AppSteroidGroup_java_lang_Boolean_isCurrentUserSubscribedToGroup_"> isCurrentUserSubscribedToGroup </a>

```
public Boolean isCurrentUserSubscribedToGroup()
```

Retrieves the group's "subscribed" property.

#### Returns

|Return Type|Description|
|---|---|
|Boolean|The group's "subscribed" property.|


## <a name="com_fresvii_components_AppSteroidGroup_boolean_isCurrentUserSubscribedToGroupOrDefault_"> isCurrentUserSubscribedToGroupOrDefault </a>

```
public boolean isCurrentUserSubscribedToGroupOrDefault()
```

Retrieves the group's "subscribed" property, or a default value if the group's "subscribed" property is null.

#### Returns

|Return Type|Description|
|---|---|
|boolean|The group's "subscribed" property, or a default value|


## <a name="com_fresvii_components_AppSteroidGroup_java_lang_Boolean_isPairGroup_"> isPairGroup </a>

```
public Boolean isPairGroup()
```

Retrieves the group's "pair" property.

#### Returns

|Return Type|Description|
|---|---|
|Boolean|The group's "pair" property.|


## <a name="com_fresvii_components_AppSteroidGroup_boolean_isPairGroupOrDefault_"> isPairGroupOrDefault </a>

```
public boolean isPairGroupOrDefault()
```

Retrieves the group's "pair" property, or a default value if the group's "pair" property is null.

#### Returns

|Return Type|Description|
|---|---|
|boolean|The group's "pair" property, or a default value|



---  

## <a name="com.fresvii.server.access.callbacks.group.CreateMultiGroupCallback"> Interface CreateMultiGroupCallback </a>

```
public interface CreateMultiGroupCallback implements FailureCallback
```

**Hierarchy:**  

```
com.fresvii.server.access.callbacks.group.CreateMultiGroupCallback
```

**Description:**  
Callback interface to handle [GroupAccess.createMultiGroup()](#com_fresvii_server_access_GroupAccess_void_createMultiGroup_String_List_CreateMultiGroupCallback) results.

**Author:**  
Marcus Froeschl

**Version:**  
1.0




### Method Summary

|Method|Description|
|---|---|
|[public void onSuccess(AppSteroidGroup group)](#com_fresvii_server_access_callbacks_group_CreateMultiGroupCallback_void_onSuccess_AppSteroidGroup)|Callback invoked when operation succeeds.|



### Method Detail
 


## <a name="com_fresvii_server_access_callbacks_group_CreateMultiGroupCallback_void_onSuccess_AppSteroidGroup"> onSuccess </a>

```
public void onSuccess(AppSteroidGroup group)
```

Callback invoked when operation succeeds.

#### Parameters

|Parameter|Description|
|---|---|
|[AppSteroidGroup](#com.fresvii.components.AppSteroidGroup) group|The group that was created.|




---  

## <a name="com.fresvii.server.access.callbacks.group.CreatePairGroupCallback"> Interface CreatePairGroupCallback </a>

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




### Method Summary

|Method|Description|
|---|---|
|[public void onSuccess(AppSteroidGroup group)](#com_fresvii_server_access_callbacks_group_CreatePairGroupCallback_void_onSuccess_AppSteroidGroup)|Callback invoked when operation succeeds.|



### Method Detail
 


## <a name="com_fresvii_server_access_callbacks_group_CreatePairGroupCallback_void_onSuccess_AppSteroidGroup"> onSuccess </a>

```
public void onSuccess(AppSteroidGroup group)
```

Callback invoked when operation succeeds.

#### Parameters

|Parameter|Description|
|---|---|
|[AppSteroidGroup](#com.fresvii.components.AppSteroidGroup) group|The group that was created.|




---  

## <a name="com.fresvii.server.access.callbacks.group.UpdateMultiGroupCallback"> Interface UpdateMultiGroupCallback </a>

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




### Method Summary

|Method|Description|
|---|---|
|[public void onSuccess(AppSteroidGroup group)](#com_fresvii_server_access_callbacks_group_UpdateMultiGroupCallback_void_onSuccess_AppSteroidGroup)|Callback invoked when operation succeeds.|



### Method Detail
 


## <a name="com_fresvii_server_access_callbacks_group_UpdateMultiGroupCallback_void_onSuccess_AppSteroidGroup"> onSuccess </a>

```
public void onSuccess(AppSteroidGroup group)
```

Callback invoked when operation succeeds.

#### Parameters

|Parameter|Description|
|---|---|
|[AppSteroidGroup](#com.fresvii.components.AppSteroidGroup) group|The group that was updated.|




---  

## <a name="com.fresvii.server.access.callbacks.group.GetGroupsCallback"> Interface GetGroupsCallback </a>

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
1.1




### Method Summary

|Method|Description|
|---|---|
|[public void onSuccess(AppSteroidListMetaInfo metaInfo, List groups)](#com_fresvii_server_access_callbacks_group_GetGroupsCallback_void_onSuccess_AppSteroidListMetaInfo_List)|Callback invoked when operation succeeds.|



### Method Detail
 


## <a name="com_fresvii_server_access_callbacks_group_GetGroupsCallback_void_onSuccess_AppSteroidListMetaInfo_List"> onSuccess </a>

```
public void onSuccess(AppSteroidListMetaInfo metaInfo,  
                      List groups)
```

Callback invoked when operation succeeds.

#### Parameters

|Parameter|Description|
|---|---|
|[AppSteroidListMetaInfo](AndroidSDK.md#com.fresvii.components.AppSteroidListMetaInfo) metaInfo|List meta information.|
|List groups|List of groups retrieved.|




---  

## <a name="com.fresvii.server.access.callbacks.group.DeleteGroupCallback"> Interface DeleteGroupCallback </a>

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




### Method Summary

|Method|Description|
|---|---|
|[public void onSuccess()](#com_fresvii_server_access_callbacks_group_DeleteGroupCallback_void_onSuccess_)|Callback invoked when operation succeeds.|



### Method Detail
 


## <a name="com_fresvii_server_access_callbacks_group_DeleteGroupCallback_void_onSuccess_"> onSuccess </a>

```
public void onSuccess()
```

Callback invoked when operation succeeds.



---  

## <a name="com.fresvii.server.access.callbacks.group.SubscribeToGroupCallback"> Interface SubscribeToGroupCallback </a>

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




### Method Summary

|Method|Description|
|---|---|
|[public void onSuccess(AppSteroidGroup group)](#com_fresvii_server_access_callbacks_group_SubscribeToGroupCallback_void_onSuccess_AppSteroidGroup)|Callback invoked when operation succeeds.|



### Method Detail
 


## <a name="com_fresvii_server_access_callbacks_group_SubscribeToGroupCallback_void_onSuccess_AppSteroidGroup"> onSuccess </a>

```
public void onSuccess(AppSteroidGroup group)
```

Callback invoked when operation succeeds.

#### Parameters

|Parameter|Description|
|---|---|
|[AppSteroidGroup](#com.fresvii.components.AppSteroidGroup) group|The group that was subscribed.|




---  

## <a name="com.fresvii.server.access.callbacks.group.UnsubscribeFromGroupCallback"> Interface UnsubscribeFromGroupCallback </a>

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




### Method Summary

|Method|Description|
|---|---|
|[public void onSuccess(AppSteroidGroup group)](#com_fresvii_server_access_callbacks_group_UnsubscribeFromGroupCallback_void_onSuccess_AppSteroidGroup)|Callback invoked when operation succeeds.|



### Method Detail
 


## <a name="com_fresvii_server_access_callbacks_group_UnsubscribeFromGroupCallback_void_onSuccess_AppSteroidGroup"> onSuccess </a>

```
public void onSuccess(AppSteroidGroup group)
```

Callback invoked when operation succeeds.

#### Parameters

|Parameter|Description|
|---|---|
|[AppSteroidGroup](#com.fresvii.components.AppSteroidGroup) group|The group that was unsubscribed.|




---  

## <a name="com.fresvii.server.access.callbacks.group.GetGroupMembersCallback"> Interface GetGroupMembersCallback </a>

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
1.1




### Method Summary

|Method|Description|
|---|---|
|[public void onSuccess(AppSteroidListMetaInfo metaInfo, List members)](#com_fresvii_server_access_callbacks_group_GetGroupMembersCallback_void_onSuccess_AppSteroidListMetaInfo_List)|Callback invoked when operation succeeds.|



### Method Detail
 


## <a name="com_fresvii_server_access_callbacks_group_GetGroupMembersCallback_void_onSuccess_AppSteroidListMetaInfo_List"> onSuccess </a>

```
public void onSuccess(AppSteroidListMetaInfo metaInfo,  
                      List members)
```

Callback invoked when operation succeeds.

#### Parameters

|Parameter|Description|
|---|---|
|[AppSteroidListMetaInfo](AndroidSDK.md#com.fresvii.components.AppSteroidListMetaInfo) metaInfo|List meta information.|
|List members|List of members retrieved.|




---  

## <a name="com.fresvii.server.access.callbacks.group.GetAllGroupMembersCallback"> Interface GetAllGroupMembersCallback </a>

```
public interface GetAllGroupMembersCallback implements FailureCallback
```

**Hierarchy:**  

```
com.fresvii.server.access.callbacks.group.GetAllGroupMembersCallback
```

**Description:**  
Callback interface to handle [GroupAccess.getAllGroupMembers()](#com_fresvii_server_access_GroupAccess_void_getAllGroupMembers_String_GetAllGroupMembersCallback) results.

**Author:**  
Matthias Kollmer

**Version:**  
1.0




### Method Summary

|Method|Description|
|---|---|
|[public void onSuccess(List members)](#com_fresvii_server_access_callbacks_group_GetAllGroupMembersCallback_void_onSuccess_List)|Callback invoked when operation succeeds.|



### Method Detail
 


## <a name="com_fresvii_server_access_callbacks_group_GetAllGroupMembersCallback_void_onSuccess_List"> onSuccess </a>

```
public void onSuccess(List members)
```

Callback invoked when operation succeeds.

#### Parameters

|Parameter|Description|
|---|---|
|List members|List of members retrieved.|




---  

## <a name="com.fresvii.server.access.callbacks.group.GetAllFriendsInGroupCallback"> Interface GetAllFriendsInGroupCallback </a>

```
public interface GetAllFriendsInGroupCallback implements FailureCallback
```

**Hierarchy:**  

```
com.fresvii.server.access.callbacks.group.GetAllFriendsInGroupCallback
```

**Description:**  
Callback interface to handle [GroupAccess.getAllFriendsInGroup()](#com_fresvii_server_access_GroupAccess_void_getAllFriendsInGroup_String_GetAllFriendsInGroupCallback) results.

**Author:**  
Matthias Kollmer

**Version:**  
1.0




### Method Summary

|Method|Description|
|---|---|
|[public void onSuccess(List allMembersInGroup, List allFriends, List friendsInGroup)](#com_fresvii_server_access_callbacks_group_GetAllFriendsInGroupCallback_void_onSuccess_List_List_List)|Callback invoked when operation succeeds.|



### Method Detail
 


## <a name="com_fresvii_server_access_callbacks_group_GetAllFriendsInGroupCallback_void_onSuccess_List_List_List"> onSuccess </a>

```
public void onSuccess(List allMembersInGroup,  
                      List allFriends,  
                      List friendsInGroup)
```

Callback invoked when operation succeeds.

#### Parameters

|Parameter|Description|
|---|---|
|List allMembersInGroup|All members in group retrieved.|
|List allFriends|All friends retrieved.|
|List friendsInGroup|All friends retrieved that are also members of the group.|




---  

## <a name="com.fresvii.server.access.callbacks.group.AddMemberToMultiGroupCallback"> Interface AddMemberToMultiGroupCallback </a>

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




### Method Summary

|Method|Description|
|---|---|
|[public void onSuccess(AppSteroidGroup group)](#com_fresvii_server_access_callbacks_group_AddMemberToMultiGroupCallback_void_onSuccess_AppSteroidGroup)|Callback invoked when operation succeeds.|



### Method Detail
 


## <a name="com_fresvii_server_access_callbacks_group_AddMemberToMultiGroupCallback_void_onSuccess_AppSteroidGroup"> onSuccess </a>

```
public void onSuccess(AppSteroidGroup group)
```

Callback invoked when operation succeeds.

#### Parameters

|Parameter|Description|
|---|---|
|[AppSteroidGroup](#com.fresvii.components.AppSteroidGroup) group|The group the member was added to.|




---  

## <a name="com.fresvii.server.access.callbacks.group.DeleteMemberFromMultiGroupCallback"> Interface DeleteMemberFromMultiGroupCallback </a>

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




### Method Summary

|Method|Description|
|---|---|
|[public void onSuccess()](#com_fresvii_server_access_callbacks_group_DeleteMemberFromMultiGroupCallback_void_onSuccess_)|Callback invoked when operation succeeds.|



### Method Detail
 


## <a name="com_fresvii_server_access_callbacks_group_DeleteMemberFromMultiGroupCallback_void_onSuccess_"> onSuccess </a>

```
public void onSuccess()
```

Callback invoked when operation succeeds.


