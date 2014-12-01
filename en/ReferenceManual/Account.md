
# AppSteroid Account API

Last updated 2014-12-01

-------------------------

## Introduction

AppSteroid Account API can be used to manage AppSteroid user accounts.

Normally, the application does not have to deal with account management. It is sufficient to call [AppSteroid.start()](AndroidSDK.md#com_fresvii_AppSteroid_void_start_Context_String_String_String_String), this will automatically create a new user account if no user account exists yet, and automatically log in the user.

The application may register a [AccountAccess.UserAuthEventListener](#com.fresvii.server.access.AccountAccess.UserAuthEventListener) to be notified when a new user is signed up, or the user logs in.


---  

## Classes

|Class|Description|
|---|---|
|[AccountAccess](#com.fresvii.server.access.AccountAccess)|Provides access to Fresvii Server's Account API.|
|[AccountAccess.UserAuthEvent](#com.fresvii.server.access.AccountAccess.UserAuthEvent)|Events that inform about a user's authentication status|
|[AccountAccess.UserAuthEventListener](#com.fresvii.server.access.AccountAccess.UserAuthEventListener)|Interface that application may implement to listen for [UserAuthEvents](#com.fresvii.server.access.AccountAccess.UserAuthEvent).|
|[SignUpUserCallback](#com.fresvii.server.access.callbacks.account.SignUpUserCallback)|Callback interface to handle [AccountAccess.signUpUser()](#com_fresvii_server_access_AccountAccess_void_signUpUser_SignUpUserCallback) results.|
|[UpdateUserCallback](#com.fresvii.server.access.callbacks.account.UpdateUserCallback)|Callback interface to handle [AccountAccess.updateUser()](#com_fresvii_server_access_AccountAccess_void_updateUser_String_String_Bitmap_UpdateUserCallback) results.|
|[LoginUserCallback](#com.fresvii.server.access.callbacks.account.LoginUserCallback)|Callback interface to handle [AccountAccess.loginUser()](#com_fresvii_server_access_AccountAccess_void_loginUser_LoginUserCallback)  results.|



---  

## <a name="com.fresvii.server.access.AccountAccess"> Class AccountAccess </a>

```
public class AccountAccess extends Object
```

**Hierarchy:**  

```
java.lang.Object  
    com.fresvii.server.access.AccountAccess
```

**Description:**  
Provides access to Fresvii Server's Account API.  Can be used to sign up and log in Fresvii users.

**Author:**  
matsushimakatsuhito

**Version:**  
1.0

**Since:**  
2014-02-18


### Method Summary

|Method|Description|
|---|---|
|[public static void addUserAuthEventListener(AccountAccess.UserAuthEventListener userAuthEventListener)](#com_fresvii_server_access_AccountAccess_void_addUserAuthEventListener_AccountAccess_UserAuthEventListener)|Adds a [UserAuthEventListener](#com.fresvii.server.access.AccountAccess.UserAuthEventListener) that will be informed about [UserAuthEvents](#com.fresvii.server.access.AccountAccess.UserAuthEvent).|
|[public static void loginUser(LoginUserCallback callback)](#com_fresvii_server_access_AccountAccess_void_loginUser_LoginUserCallback)|Logs in the current user.|
|[public static void loginUser(int lifetime, LoginUserCallback callback)](#com_fresvii_server_access_AccountAccess_void_loginUser_int_LoginUserCallback)|Logs in the current user.|
|[public static void refreshSession(RefreshSessionCallback callback)](#com_fresvii_server_access_AccountAccess_void_refreshSession_RefreshSessionCallback)|Refreshes the session of the current user.|
|[public static void removeUserAuthEventListener(AccountAccess.UserAuthEventListener userAuthEventListener)](#com_fresvii_server_access_AccountAccess_void_removeUserAuthEventListener_AccountAccess_UserAuthEventListener)|Removes the specified [UserAuthEventListener](#com.fresvii.server.access.AccountAccess.UserAuthEventListener).|
|[public static void signUpUser(SignUpUserCallback callback)](#com_fresvii_server_access_AccountAccess_void_signUpUser_SignUpUserCallback)|Signs up a new Fresvii user.|
|[public static void signUpUser(String userName, SignUpUserCallback callback)](#com_fresvii_server_access_AccountAccess_void_signUpUser_String_SignUpUserCallback)|Signs up a new Fresvii user.|
|[public static void signUpUser(String userName, String description, Bitmap profileImageBitmap, SignUpUserCallback callback)](#com_fresvii_server_access_AccountAccess_void_signUpUser_String_String_Bitmap_SignUpUserCallback)|Signs up a new Fresvii user.|
|[public static void updateUser(String updatedUserName, String updatedDescription, Bitmap updatedProfileImageBitmap, UpdateUserCallback callback)](#com_fresvii_server_access_AccountAccess_void_updateUser_String_String_Bitmap_UpdateUserCallback)|Updates an existing Fresvii user with the specified new values.|



### Method Detail
 


## <a name="com_fresvii_server_access_AccountAccess_void_addUserAuthEventListener_AccountAccess_UserAuthEventListener"> addUserAuthEventListener </a>

```
public static void addUserAuthEventListener(AccountAccess.UserAuthEventListener userAuthEventListener)
```

Adds a [UserAuthEventListener](#com.fresvii.server.access.AccountAccess.UserAuthEventListener) that will be informed about [UserAuthEvents](#com.fresvii.server.access.AccountAccess.UserAuthEvent).

#### Parameters

|Parameter|Description|
|---|---|
|[AccountAccess.UserAuthEventListener](#com.fresvii.server.access.AccountAccess.UserAuthEventListener) userAuthEventListener|The listener to be added.|



#### Example

```
// Application may implement the UserAuthEventListener interface
public class MainActivity extends Activity implements UserAuthEventListener {
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        // Application may wish to register a UserAuthEventListener
        // to be notified when a new user is signed up, or the user logs in
        AccountAccess.addUserAuthEventListener(this);
        
        // Start the AppSteroid
        AppSteroid.start(
        	    getApplicationContext(),
        	    MY_APP_ID,
        	    MY_APP_SECRET,
        	    MY_APP_NAME,
        	    MY_GCM_SENDER_ID);
        
        ...
    }

    @Override
    public void onUserAuthEvent(String userId, UserAuthEvent event) {
        switch ( event ) {
            case USER_SIGNED_UP:
                // Add any code you wish to be executed when a new user signed up
                break;
            case USER_LOGGED_IN:
                // Add any code you wish to be executed when the user logs in
                break;
        }
    }
}
```




## <a name="com_fresvii_server_access_AccountAccess_void_loginUser_LoginUserCallback"> loginUser </a>

```
public static void loginUser(LoginUserCallback callback)
```

Logs in the current user.  Uses the default lifetime (1 day).

#### Parameters

|Parameter|Description|
|---|---|
|[LoginUserCallback](#com.fresvii.server.access.callbacks.account.LoginUserCallback) callback|[Callback](#com.fresvii.server.access.callbacks.account.LoginUserCallback) to be informed about the result of the operation.|



## <a name="com_fresvii_server_access_AccountAccess_void_loginUser_int_LoginUserCallback"> loginUser </a>

```
public static void loginUser(int lifetime,  
                             LoginUserCallback callback)
```

Logs in the current user.

#### Parameters

|Parameter|Description|
|---|---|
|int lifetime|Timespan after which the session expires. Can be set from 10 seconds to 86400 seconds (1 day).|
|[LoginUserCallback](#com.fresvii.server.access.callbacks.account.LoginUserCallback) callback|[Callback](#com.fresvii.server.access.callbacks.account.LoginUserCallback) to be informed about the result of the operation.|



## <a name="com_fresvii_server_access_AccountAccess_void_refreshSession_RefreshSessionCallback"> refreshSession </a>

```
public static void refreshSession(RefreshSessionCallback callback)
```

Refreshes the session of the current user.

#### Parameters

|Parameter|Description|
|---|---|
|RefreshSessionCallback callback|Callback to be informed about the result of the operation.|



## <a name="com_fresvii_server_access_AccountAccess_void_removeUserAuthEventListener_AccountAccess_UserAuthEventListener"> removeUserAuthEventListener </a>

```
public static void removeUserAuthEventListener(AccountAccess.UserAuthEventListener userAuthEventListener)
```

Removes the specified [UserAuthEventListener](#com.fresvii.server.access.AccountAccess.UserAuthEventListener).

#### Parameters

|Parameter|Description|
|---|---|
|[AccountAccess.UserAuthEventListener](#com.fresvii.server.access.AccountAccess.UserAuthEventListener) userAuthEventListener|The listener to be removed.|



## <a name="com_fresvii_server_access_AccountAccess_void_signUpUser_SignUpUserCallback"> signUpUser </a>

```
public static void signUpUser(SignUpUserCallback callback)
```

Signs up a new Fresvii user.  Uses default values for userName, description and profile picture.

#### Parameters

|Parameter|Description|
|---|---|
|[SignUpUserCallback](#com.fresvii.server.access.callbacks.account.SignUpUserCallback) callback|[Callback](#com.fresvii.server.access.callbacks.account.SignUpUserCallback) to be informed about the result of the operation.|



## <a name="com_fresvii_server_access_AccountAccess_void_signUpUser_String_SignUpUserCallback"> signUpUser </a>

```
public static void signUpUser(String userName,  
                              SignUpUserCallback callback)
```

Signs up a new Fresvii user.  Uses default values for description and profile picture.

#### Parameters

|Parameter|Description|
|---|---|
|String userName|Name of the user.|
|[SignUpUserCallback](#com.fresvii.server.access.callbacks.account.SignUpUserCallback) callback|[Callback](#com.fresvii.server.access.callbacks.account.SignUpUserCallback) to be informed about the result of the operation.|



## <a name="com_fresvii_server_access_AccountAccess_void_signUpUser_String_String_Bitmap_SignUpUserCallback"> signUpUser </a>

```
public static void signUpUser(String userName,  
                              String description,  
                              Bitmap profileImageBitmap,  
                              SignUpUserCallback callback)
```

Signs up a new Fresvii user.

#### Parameters

|Parameter|Description|
|---|---|
|String userName|Name of the user.|
|String description|Description of the user.|
|Bitmap profileImageBitmap|Profile picture of the user.|
|[SignUpUserCallback](#com.fresvii.server.access.callbacks.account.SignUpUserCallback) callback|[Callback](#com.fresvii.server.access.callbacks.account.SignUpUserCallback) to be informed about the result of the operation.|



## <a name="com_fresvii_server_access_AccountAccess_void_updateUser_String_String_Bitmap_UpdateUserCallback"> updateUser </a>

```
public static void updateUser(String updatedUserName,  
                              String updatedDescription,  
                              Bitmap updatedProfileImageBitmap,  
                              UpdateUserCallback callback)
```

Updates an existing Fresvii user with the specified new values.

#### Parameters

|Parameter|Description|
|---|---|
|String updatedUserName|Updated name of the user.|
|String updatedDescription|Updated description of the user.|
|Bitmap updatedProfileImageBitmap|Updated profile picture of the user.|
|[UpdateUserCallback](#com.fresvii.server.access.callbacks.account.UpdateUserCallback) callback|[Callback](#com.fresvii.server.access.callbacks.account.UpdateUserCallback) to be informed about the result of the operation.|




---  

## <a name="com.fresvii.server.access.AccountAccess.UserAuthEvent"> Enum AccountAccess.UserAuthEvent </a>

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








### Field Summary

|Field|Description|
|---|---|
|USER_LOGGED_IN|Event fired when user successfully logged in.|
|USER_SIGNED_UP|Event fired when user successfully signed up.|




---  

## <a name="com.fresvii.server.access.AccountAccess.UserAuthEventListener"> Interface AccountAccess.UserAuthEventListener </a>

```
public static interface AccountAccess.UserAuthEventListener
```

**Hierarchy:**  

```
com.fresvii.server.access.AccountAccess.UserAuthEventListener
```

**Description:**  
Interface that application may implement to listen for [UserAuthEvents](#com.fresvii.server.access.AccountAccess.UserAuthEvent).








### Method Summary

|Method|Description|
|---|---|
|[public void onUserAuthEvent(String userId, AccountAccess.UserAuthEvent event)](#com_fresvii_server_access_AccountAccess_UserAuthEventListener_void_onUserAuthEvent_String_AccountAccess_UserAuthEvent)|Called when a UserAuthEvent occurs.|



### Method Detail
 


## <a name="com_fresvii_server_access_AccountAccess_UserAuthEventListener_void_onUserAuthEvent_String_AccountAccess_UserAuthEvent"> onUserAuthEvent </a>

```
public void onUserAuthEvent(String userId,  
                            AccountAccess.UserAuthEvent event)
```

Called when a UserAuthEvent occurs.

#### Parameters

|Parameter|Description|
|---|---|
|String userId|ID of the user associated with the event.|
|[AccountAccess.UserAuthEvent](#com.fresvii.server.access.AccountAccess.UserAuthEvent) event|The event that occurred.|




---  

## <a name="com.fresvii.server.access.callbacks.account.SignUpUserCallback"> Interface SignUpUserCallback </a>

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




### Method Summary

|Method|Description|
|---|---|
|[public void onSuccess(AppSteroidCurrentUser currentUser)](#com_fresvii_server_access_callbacks_account_SignUpUserCallback_void_onSuccess_AppSteroidCurrentUser)|Callback invoked when operation succeeds.|



### Method Detail
 


## <a name="com_fresvii_server_access_callbacks_account_SignUpUserCallback_void_onSuccess_AppSteroidCurrentUser"> onSuccess </a>

```
public void onSuccess(AppSteroidCurrentUser currentUser)
```

Callback invoked when operation succeeds.

#### Parameters

|Parameter|Description|
|---|---|
|[AppSteroidCurrentUser](User.md#com.fresvii.components.AppSteroidCurrentUser) currentUser|The user who was successfully signed in.|




---  

## <a name="com.fresvii.server.access.callbacks.account.UpdateUserCallback"> Interface UpdateUserCallback </a>

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




### Method Summary

|Method|Description|
|---|---|
|[public void onSuccess(AppSteroidCurrentUser currentUser)](#com_fresvii_server_access_callbacks_account_UpdateUserCallback_void_onSuccess_AppSteroidCurrentUser)|Callback invoked when operation succeeds.|



### Method Detail
 


## <a name="com_fresvii_server_access_callbacks_account_UpdateUserCallback_void_onSuccess_AppSteroidCurrentUser"> onSuccess </a>

```
public void onSuccess(AppSteroidCurrentUser currentUser)
```

Callback invoked when operation succeeds.

#### Parameters

|Parameter|Description|
|---|---|
|[AppSteroidCurrentUser](User.md#com.fresvii.components.AppSteroidCurrentUser) currentUser|The user who was successfully updated.|




---  

## <a name="com.fresvii.server.access.callbacks.account.LoginUserCallback"> Interface LoginUserCallback </a>

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




### Method Summary

|Method|Description|
|---|---|
|[public void onSuccess(AppSteroidCurrentUser currentUser)](#com_fresvii_server_access_callbacks_account_LoginUserCallback_void_onSuccess_AppSteroidCurrentUser)|Callback invoked when operation succeeds.|



### Method Detail
 


## <a name="com_fresvii_server_access_callbacks_account_LoginUserCallback_void_onSuccess_AppSteroidCurrentUser"> onSuccess </a>

```
public void onSuccess(AppSteroidCurrentUser currentUser)
```

Callback invoked when operation succeeds.

#### Parameters

|Parameter|Description|
|---|---|
|[AppSteroidCurrentUser](User.md#com.fresvii.components.AppSteroidCurrentUser) currentUser|The user who was successfully logged in.|



