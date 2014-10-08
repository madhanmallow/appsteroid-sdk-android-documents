
# AppSteroid User API

Last updated 2014-10-08

-------------------------

## Introduction

AppSteroid User API can be used to manage AppSteroid users.


---  

## Classes

|Class|Description|
|---|---|
|[UserAccess](#com.fresvii.server.access.UserAccess)|Provides access to Fresvii Server's User API.|
|[AppSteroidUser](#com.fresvii.components.AppSteroidUser)|Represents a Fresvii user.|
|[AppSteroidCurrentUser](#com.fresvii.components.AppSteroidCurrentUser)|Represents the user logged in to Fresvii Server on this device.|
|[GetUserCallback](#com.fresvii.server.access.callbacks.user.GetUserCallback)|Callback interface to handle UserAccess.getUser() results.|
|[GetUsersCallback](#com.fresvii.server.access.callbacks.user.GetUsersCallback)|Callback interface to handle UserAccess.getUser() results.|



---  

## <a name="com.fresvii.server.access.UserAccess"> Class UserAccess </a>

```
public class UserAccess extends Object
```

**Hierarchy:**  

```
java.lang.Object  
    com.fresvii.server.access.UserAccess
```

**Description:**  
Provides access to Fresvii Server's User API.  Can be used to retrieve information on a specific user, or retrieve a list of users matching conditions.

**Author:**  
matsushimakatsuhito

**Version:**  
1.0

**Since:**  
2014-02-18


### Method Summary

|Method|Description|
|---|---|
|[public static void getUser(String userIdOrCode, GetUserCallback callback)](#com_fresvii_server_access_UserAccess_void_getUser_String_GetUserCallback)|Retrieves a specific user.|
|[public static void getUsers(String provider, String uid, GetUsersCallback callback)](#com_fresvii_server_access_UserAccess_void_getUsers_String_String_GetUsersCallback)|Retrieves a list of users that match providers and UID.|



### Method Detail
 


## <a name="com_fresvii_server_access_UserAccess_void_getUser_String_GetUserCallback"> getUser </a>

```
public static void getUser(String userIdOrCode,  
                           GetUserCallback callback)
```

Retrieves a specific user.

#### Parameters

|Parameter|Description|
|---|---|
|String userIdOrCode|User ID or User code of the user to be retrieved.|
|[GetUserCallback](#com.fresvii.server.access.callbacks.user.GetUserCallback) callback|[Callback](#com.fresvii.server.access.callbacks.user.GetUserCallback) to be informed about the result of the operation.|



## <a name="com_fresvii_server_access_UserAccess_void_getUsers_String_String_GetUsersCallback"> getUsers </a>

```
public static void getUsers(String provider,  
                            String uid,  
                            GetUsersCallback callback)
```

Retrieves a list of users that match providers and UID.

#### Parameters

|Parameter|Description|
|---|---|
|String provider|Provider|
|String uid|UID|
|[GetUsersCallback](#com.fresvii.server.access.callbacks.user.GetUsersCallback) callback|[Callback](#com.fresvii.server.access.callbacks.user.GetUsersCallback) to be informed about the result of the operation.|




---  

## <a name="com.fresvii.components.AppSteroidUser"> Class AppSteroidUser </a>

```
public class AppSteroidUser extends AppSteroidComponent
```

**Hierarchy:**  

```
java.lang.Object  
    com.fresvii.components.AppSteroidComponent  
        com.fresvii.components.AppSteroidUser
```

**Description:**  
Represents a Fresvii user.

**Author:**  
matsushimakatsuhito

**Version:**  
1.0

**Since:**  
2014-02-18


### Method Summary

|Method|Description|
|---|---|
|[public String getCode()](#com_fresvii_components_AppSteroidUser_java_lang_String_getCode_)|Retrieves the user's code.|
|[public String getCodeOrDefault()](#com_fresvii_components_AppSteroidUser_java_lang_String_getCodeOrDefault_)|Retrieves the user's code, or a default value if the user's code is null.|
|[public String getDescription()](#com_fresvii_components_AppSteroidUser_java_lang_String_getDescription_)|Retrieves the user's description.|
|[public String getDescriptionOrDefault()](#com_fresvii_components_AppSteroidUser_java_lang_String_getDescriptionOrDefault_)|Retrieves the user's description, or a default value if the user's description is null.|
|[public String getFriendStatus()](#com_fresvii_components_AppSteroidUser_java_lang_String_getFriendStatus_)|Retrieves the user's friend status.|
|[public String getFriendStatusOrDefault()](#com_fresvii_components_AppSteroidUser_java_lang_String_getFriendStatusOrDefault_)|Retrieves the user's friend status, or a default value if the user's friend status is null.|
|[public String getId()](#com_fresvii_components_AppSteroidUser_java_lang_String_getId_)|Retrieves the user's ID.|
|[public String getIdOrDefault()](#com_fresvii_components_AppSteroidUser_java_lang_String_getIdOrDefault_)|Retrieves the user's ID, or a default value if the user's ID is null.|
|[public String getName()](#com_fresvii_components_AppSteroidUser_java_lang_String_getName_)|Retrieves the user's name.|
|[public String getNameOrDefault()](#com_fresvii_components_AppSteroidUser_java_lang_String_getNameOrDefault_)|Retrieves the user's name, or a default value if the user's name is null.|
|[public String getProfileImageUrl()](#com_fresvii_components_AppSteroidUser_java_lang_String_getProfileImageUrl_)|Retrieves the user's profile image URL.|
|[public String getProfileImageUrlOrDefault()](#com_fresvii_components_AppSteroidUser_java_lang_String_getProfileImageUrlOrDefault_)|Retrieves the user's profile image URL, or a default value if the user's profile image URL is null.|
|[public String getToken()](#com_fresvii_components_AppSteroidUser_java_lang_String_getToken_)|Retrieves the user's token.|
|[public String getTokenOrDefault()](#com_fresvii_components_AppSteroidUser_java_lang_String_getTokenOrDefault_)|Retrieves the user's token, or a default value if the user's token is null.|



### Method Detail
 


## <a name="com_fresvii_components_AppSteroidUser_java_lang_String_getCode_"> getCode </a>

```
public String getCode()
```

Retrieves the user's code.

#### Returns

|Return Type|Description|
|---|---|
|String|The user's code.|


## <a name="com_fresvii_components_AppSteroidUser_java_lang_String_getCodeOrDefault_"> getCodeOrDefault </a>

```
public String getCodeOrDefault()
```

Retrieves the user's code, or a default value if the user's code is null.

#### Returns

|Return Type|Description|
|---|---|
|String|The user's code, or a default value|


## <a name="com_fresvii_components_AppSteroidUser_java_lang_String_getDescription_"> getDescription </a>

```
public String getDescription()
```

Retrieves the user's description.

#### Returns

|Return Type|Description|
|---|---|
|String|The user's description.|


## <a name="com_fresvii_components_AppSteroidUser_java_lang_String_getDescriptionOrDefault_"> getDescriptionOrDefault </a>

```
public String getDescriptionOrDefault()
```

Retrieves the user's description, or a default value if the user's description is null.

#### Returns

|Return Type|Description|
|---|---|
|String|The user's description, or a default value|


## <a name="com_fresvii_components_AppSteroidUser_java_lang_String_getFriendStatus_"> getFriendStatus </a>

```
public String getFriendStatus()
```

Retrieves the user's friend status.

#### Returns

|Return Type|Description|
|---|---|
|String|The user's friend status.|


## <a name="com_fresvii_components_AppSteroidUser_java_lang_String_getFriendStatusOrDefault_"> getFriendStatusOrDefault </a>

```
public String getFriendStatusOrDefault()
```

Retrieves the user's friend status, or a default value if the user's friend status is null.

#### Returns

|Return Type|Description|
|---|---|
|String|The user's friend status, or a default value|


## <a name="com_fresvii_components_AppSteroidUser_java_lang_String_getId_"> getId </a>

```
public String getId()
```

Retrieves the user's ID.

#### Returns

|Return Type|Description|
|---|---|
|String|The user's ID.|


## <a name="com_fresvii_components_AppSteroidUser_java_lang_String_getIdOrDefault_"> getIdOrDefault </a>

```
public String getIdOrDefault()
```

Retrieves the user's ID, or a default value if the user's ID is null.

#### Returns

|Return Type|Description|
|---|---|
|String|The user's ID, or a default value|


## <a name="com_fresvii_components_AppSteroidUser_java_lang_String_getName_"> getName </a>

```
public String getName()
```

Retrieves the user's name.

#### Returns

|Return Type|Description|
|---|---|
|String|The user's name.|


## <a name="com_fresvii_components_AppSteroidUser_java_lang_String_getNameOrDefault_"> getNameOrDefault </a>

```
public String getNameOrDefault()
```

Retrieves the user's name, or a default value if the user's name is null.

#### Returns

|Return Type|Description|
|---|---|
|String|The user's name, or a default value|


## <a name="com_fresvii_components_AppSteroidUser_java_lang_String_getProfileImageUrl_"> getProfileImageUrl </a>

```
public String getProfileImageUrl()
```

Retrieves the user's profile image URL.

#### Returns

|Return Type|Description|
|---|---|
|String|The user's profile image URL.|


## <a name="com_fresvii_components_AppSteroidUser_java_lang_String_getProfileImageUrlOrDefault_"> getProfileImageUrlOrDefault </a>

```
public String getProfileImageUrlOrDefault()
```

Retrieves the user's profile image URL, or a default value if the user's profile image URL is null.

#### Returns

|Return Type|Description|
|---|---|
|String|The user's profile image URL, or a default value|


## <a name="com_fresvii_components_AppSteroidUser_java_lang_String_getToken_"> getToken </a>

```
public String getToken()
```

Retrieves the user's token.

#### Returns

|Return Type|Description|
|---|---|
|String|The user's token.|


## <a name="com_fresvii_components_AppSteroidUser_java_lang_String_getTokenOrDefault_"> getTokenOrDefault </a>

```
public String getTokenOrDefault()
```

Retrieves the user's token, or a default value if the user's token is null.

#### Returns

|Return Type|Description|
|---|---|
|String|The user's token, or a default value|



---  

## <a name="com.fresvii.components.AppSteroidCurrentUser"> Class AppSteroidCurrentUser </a>

```
public class AppSteroidCurrentUser extends AppSteroidUser
```

**Hierarchy:**  

```
java.lang.Object  
    com.fresvii.components.AppSteroidComponent  
        com.fresvii.components.AppSteroidUser  
            com.fresvii.components.AppSteroidCurrentUser
```

**Description:**  
Represents the user logged in to Fresvii Server on this device.  This is a subclass of User where login user information is stored.  Login users are always individuals, so this is a singleton object.

**Author:**  
matsushimakatsuhito

**Version:**  
1.0

**Since:**  
2014-04-20


### Method Summary

|Method|Description|
|---|---|
|[public void autoSignUpAndLogin()](#com_fresvii_components_AppSteroidCurrentUser_void_autoSignUpAndLogin_)|Convenience method that will automatically sign up and log in a new user if there currently is no signed up user.|
|[public void clearUpdates()](#com_fresvii_components_AppSteroidCurrentUser_void_clearUpdates_)|Clears all pending changes to the current user's name, description and profile image.|
|[public static AppSteroidCurrentUser getInstance()](#com_fresvii_components_AppSteroidCurrentUser_com_fresvii_components_AppSteroidCurrentUser_getInstance_)|Retrieves the instance of the singleton object. Use this to access the CurrentUser.|
|[public Date getSessionExpirationDate()](#com_fresvii_components_AppSteroidCurrentUser_java_util_Date_getSessionExpirationDate_)|Retrieves the date when the current user's session expires.|
|[public boolean hasUpdates()](#com_fresvii_components_AppSteroidCurrentUser_boolean_hasUpdates_)|Checks if there are any pending updates to the current user's name, description or profile image.|
|[public boolean isCurrentUser(AppSteroidUser user)](#com_fresvii_components_AppSteroidCurrentUser_boolean_isCurrentUser_AppSteroidUser)|Checks if the specified user is the current user.|
|[public boolean isCurrentUser(String userId)](#com_fresvii_components_AppSteroidCurrentUser_boolean_isCurrentUser_String)|Checks if the specified user ID is the user ID of the current user.|
|[public boolean isLoggedIn()](#com_fresvii_components_AppSteroidCurrentUser_boolean_isLoggedIn_)|Checks if the current user is logged in.|
|[public boolean isSessionExpired()](#com_fresvii_components_AppSteroidCurrentUser_boolean_isSessionExpired_)|Checks if the session of the current user has expired.|
|[public boolean isSignedUp()](#com_fresvii_components_AppSteroidCurrentUser_boolean_isSignedUp_)|Checks if there is a signed up current user.|
|[public void refreshSessionIfExpired()](#com_fresvii_components_AppSteroidCurrentUser_void_refreshSessionIfExpired_)|Convenience method that will automatically refresh the current user's session if the session has expired.|
|[public void saveUpdates(UpdateUserCallback callback)](#com_fresvii_components_AppSteroidCurrentUser_void_saveUpdates_UpdateUserCallback)|Stores all any pending updates to the current user's name, description or profile image to the server.|
|[public void setUpdatedDescription(String updatedDescription)](#com_fresvii_components_AppSteroidCurrentUser_void_setUpdatedDescription_String)|Updates the current user's description. |
|[public void setUpdatedName(String updatedName)](#com_fresvii_components_AppSteroidCurrentUser_void_setUpdatedName_String)|Updates the current user's name. |
|[public void setUpdatedProfileImage(Bitmap updatedProfileImage)](#com_fresvii_components_AppSteroidCurrentUser_void_setUpdatedProfileImage_Bitmap)|Updates the current user's profile image. |



### Method Detail
 


## <a name="com_fresvii_components_AppSteroidCurrentUser_void_autoSignUpAndLogin_"> autoSignUpAndLogin </a>

```
public void autoSignUpAndLogin()
```

Convenience method that will automatically sign up and log in a new user if there currently is no signed up user.  If there is a signed up user, the user's session will be automatically refreshed if required.


## <a name="com_fresvii_components_AppSteroidCurrentUser_void_clearUpdates_"> clearUpdates </a>

```
public void clearUpdates()
```

Clears all pending changes to the current user's name, description and profile image.


## <a name="com_fresvii_components_AppSteroidCurrentUser_com_fresvii_components_AppSteroidCurrentUser_getInstance_"> getInstance </a>

```
public static AppSteroidCurrentUser getInstance()
```

Retrieves the instance of the singleton object. Use this to access the CurrentUser.

#### Returns

|Return Type|Description|
|---|---|
|AppSteroidCurrentUser|Instance of the singleton object.|


## <a name="com_fresvii_components_AppSteroidCurrentUser_java_util_Date_getSessionExpirationDate_"> getSessionExpirationDate </a>

```
public Date getSessionExpirationDate()
```

Retrieves the date when the current user's session expires.

#### Returns

|Return Type|Description|
|---|---|
|Date|Date when the current user's session expires|


## <a name="com_fresvii_components_AppSteroidCurrentUser_boolean_hasUpdates_"> hasUpdates </a>

```
public boolean hasUpdates()
```

Checks if there are any pending updates to the current user's name, description or profile image.

#### Returns

|Return Type|Description|
|---|---|
|boolean|true if there are any pending adjustments, false if there are no pending adjustments.|


## <a name="com_fresvii_components_AppSteroidCurrentUser_boolean_isCurrentUser_AppSteroidUser"> isCurrentUser </a>

```
public boolean isCurrentUser(AppSteroidUser user)
```

Checks if the specified user is the current user.

#### Parameters

|Parameter|Description|
|---|---|
|[AppSteroidUser](#com.fresvii.components.AppSteroidUser) user|User to be checked.|


#### Returns

|Return Type|Description|
|---|---|
|boolean|true if the specified user is the current user, false otherwise|


## <a name="com_fresvii_components_AppSteroidCurrentUser_boolean_isCurrentUser_String"> isCurrentUser </a>

```
public boolean isCurrentUser(String userId)
```

Checks if the specified user ID is the user ID of the current user.

#### Parameters

|Parameter|Description|
|---|---|
|String userId|User ID to be checked.|


#### Returns

|Return Type|Description|
|---|---|
|boolean|true if the specified user id is the user ID of the current user, false otherwise|


## <a name="com_fresvii_components_AppSteroidCurrentUser_boolean_isLoggedIn_"> isLoggedIn </a>

```
public boolean isLoggedIn()
```

Checks if the current user is logged in.

#### Returns

|Return Type|Description|
|---|---|
|boolean|true if logged in, false otherwise.|


## <a name="com_fresvii_components_AppSteroidCurrentUser_boolean_isSessionExpired_"> isSessionExpired </a>

```
public boolean isSessionExpired()
```

Checks if the session of the current user has expired.

#### Returns

|Return Type|Description|
|---|---|
|boolean|true if the session has expired, false otherwise.|


## <a name="com_fresvii_components_AppSteroidCurrentUser_boolean_isSignedUp_"> isSignedUp </a>

```
public boolean isSignedUp()
```

Checks if there is a signed up current user.

#### Returns

|Return Type|Description|
|---|---|
|boolean|true if signed up, false otherwise.|


## <a name="com_fresvii_components_AppSteroidCurrentUser_void_refreshSessionIfExpired_"> refreshSessionIfExpired </a>

```
public void refreshSessionIfExpired()
```

Convenience method that will automatically refresh the current user's session if the session has expired.


## <a name="com_fresvii_components_AppSteroidCurrentUser_void_saveUpdates_UpdateUserCallback"> saveUpdates </a>

```
public void saveUpdates(UpdateUserCallback callback)
```

Stores all any pending updates to the current user's name, description or profile image to the server.

#### Parameters

|Parameter|Description|
|---|---|
|[UpdateUserCallback](Account.md#com.fresvii.server.access.callbacks.account.UpdateUserCallback) callback|UpdateUserCallback to be informed about the result of this operation.|



## <a name="com_fresvii_components_AppSteroidCurrentUser_void_setUpdatedDescription_String"> setUpdatedDescription </a>

```
public void setUpdatedDescription(String updatedDescription)
```

Updates the current user's description.   saveAdjustments() will store changes to the server.  To cancel changes, use clearAdjustments().

#### Parameters

|Parameter|Description|
|---|---|
|String updatedDescription|Description name to be used when saving adjustments.|



## <a name="com_fresvii_components_AppSteroidCurrentUser_void_setUpdatedName_String"> setUpdatedName </a>

```
public void setUpdatedName(String updatedName)
```

Updates the current user's name.   saveAdjustments() will store changes to the server.  To cancel changes, use clearAdjustments().

#### Parameters

|Parameter|Description|
|---|---|
|String updatedName|Name to be used when saving adjustments.|



## <a name="com_fresvii_components_AppSteroidCurrentUser_void_setUpdatedProfileImage_Bitmap"> setUpdatedProfileImage </a>

```
public void setUpdatedProfileImage(Bitmap updatedProfileImage)
```

Updates the current user's profile image.   saveAdjustments() will store changes to the server.  To cancel changes, use clearAdjustments().

#### Parameters

|Parameter|Description|
|---|---|
|Bitmap updatedProfileImage|Profile image name to be used when saving adjustments.|




---  

## <a name="com.fresvii.server.access.callbacks.user.GetUserCallback"> Interface GetUserCallback </a>

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




### Method Summary

|Method|Description|
|---|---|
|[public void onSuccess(AppSteroidUser user)](#com_fresvii_server_access_callbacks_user_GetUserCallback_void_onSuccess_AppSteroidUser)|Callback invoked when operation succeeds.|



### Method Detail
 


## <a name="com_fresvii_server_access_callbacks_user_GetUserCallback_void_onSuccess_AppSteroidUser"> onSuccess </a>

```
public void onSuccess(AppSteroidUser user)
```

Callback invoked when operation succeeds.

#### Parameters

|Parameter|Description|
|---|---|
|[AppSteroidUser](#com.fresvii.components.AppSteroidUser) user|The user retrieved.|




---  

## <a name="com.fresvii.server.access.callbacks.user.GetUsersCallback"> Interface GetUsersCallback </a>

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




### Method Summary

|Method|Description|
|---|---|
|[public void onSuccess(List users)](#com_fresvii_server_access_callbacks_user_GetUsersCallback_void_onSuccess_List)|Callback invoked when operation succeeds.|



### Method Detail
 


## <a name="com_fresvii_server_access_callbacks_user_GetUsersCallback_void_onSuccess_List"> onSuccess </a>

```
public void onSuccess(List users)
```

Callback invoked when operation succeeds.

#### Parameters

|Parameter|Description|
|---|---|
|List users|The users retrieved.|



