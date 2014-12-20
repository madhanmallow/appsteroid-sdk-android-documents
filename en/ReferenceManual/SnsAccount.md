
# AppSteroid SNS Account API

Last updated 2014-12-10

-------------------------

## Introduction

AppSteroid SNS Account API can be used to transfer user data between authorized devices.


---  

## Classes

|Class|Description|
|---|---|
|[SnsAccountAccess](#com.fresvii.server.access.SnsAccountAccess)|Provides access to Fresvii Server's SNS API.|
|[AppSteroidSnsAccount](#com.fresvii.components.AppSteroidSnsAccount)|Represents an SNS Account.|
|[AddUserSnsAccountCallback](#com.fresvii.server.access.callbacks.account.AddUserSnsAccountCallback)|Callback interface to handle [SnsAccountAccess.addUserSnsAccount()](#com_fresvii_server_access_SnsAccountAccess_void_addUserSnsAccount_String_String_AddUserSnsAccountCallback) results.|
|[GetUserSnsAccountsCallback](#com.fresvii.server.access.callbacks.account.GetUserSnsAccountsCallback)|Callback interface to handle [SnsAccountAccess.getUserSnsAccounts()](#com_fresvii_server_access_SnsAccountAccess_void_getUserSnsAccounts_GetUserSnsAccountsCallback) results.|
|[DeleteUserSnsAccountCallback](#com.fresvii.server.access.callbacks.account.DeleteUserSnsAccountCallback)|Callback interface to handle [SnsAccountAccess.deleteUserSnsAccount()](#com_fresvii_server_access_SnsAccountAccess_void_deleteUserSnsAccount_String_DeleteUserSnsAccountCallback) results.|



---  

## <a name="com.fresvii.server.access.SnsAccountAccess"> Class SnsAccountAccess </a>

```
public class SnsAccountAccess extends Object
```

**Hierarchy:**  

```
java.lang.Object  
    com.fresvii.server.access.SnsAccountAccess
```

**Description:**  
Provides access to Fresvii Server's SNS API.  Can be used to register, delete, and retrieve login user SNS accounts.

**Author:**  
matsushimakatsuhito

**Version:**  
1.0

**Since:**  
2014-04-20


### Method Summary

|Method|Description|
|---|---|
|[public static void addUserSnsAccount(String provider, String uid, AddUserSnsAccountCallback callback)](#com_fresvii_server_access_SnsAccountAccess_void_addUserSnsAccount_String_String_AddUserSnsAccountCallback)|Adds an SNS account.|
|[public static void deleteUserSnsAccount(String snsAccountId, DeleteUserSnsAccountCallback callback)](#com_fresvii_server_access_SnsAccountAccess_void_deleteUserSnsAccount_String_DeleteUserSnsAccountCallback)|Deletes an SNS account.|
|[public static void getUserSnsAccounts(GetUserSnsAccountsCallback callback)](#com_fresvii_server_access_SnsAccountAccess_void_getUserSnsAccounts_GetUserSnsAccountsCallback)|Retrieves a list of SNS Accounts.|



### Method Detail
 


## <a name="com_fresvii_server_access_SnsAccountAccess_void_addUserSnsAccount_String_String_AddUserSnsAccountCallback"> addUserSnsAccount </a>

```
public static void addUserSnsAccount(String provider,  
                                     String uid,  
                                     AddUserSnsAccountCallback callback)
```

Adds an SNS account.

#### Parameters

|Parameter|Description|
|---|---|
|String provider|Provider|
|String uid|UID|
|[AddUserSnsAccountCallback](#com.fresvii.server.access.callbacks.account.AddUserSnsAccountCallback) callback|[Callback](#com.fresvii.server.access.callbacks.account.AddUserSnsAccountCallback) to be informed about the result of the operation.|



## <a name="com_fresvii_server_access_SnsAccountAccess_void_deleteUserSnsAccount_String_DeleteUserSnsAccountCallback"> deleteUserSnsAccount </a>

```
public static void deleteUserSnsAccount(String snsAccountId,  
                                        DeleteUserSnsAccountCallback callback)
```

Deletes an SNS account.

#### Parameters

|Parameter|Description|
|---|---|
|String snsAccountId|ID of the SNS Account to be deleted.|
|[DeleteUserSnsAccountCallback](#com.fresvii.server.access.callbacks.account.DeleteUserSnsAccountCallback) callback|Callback to be informed about the result of the operation.|



## <a name="com_fresvii_server_access_SnsAccountAccess_void_getUserSnsAccounts_GetUserSnsAccountsCallback"> getUserSnsAccounts </a>

```
public static void getUserSnsAccounts(GetUserSnsAccountsCallback callback)
```

Retrieves a list of SNS Accounts.

#### Parameters

|Parameter|Description|
|---|---|
|[GetUserSnsAccountsCallback](#com.fresvii.server.access.callbacks.account.GetUserSnsAccountsCallback) callback|[Callback](#com.fresvii.server.access.callbacks.account.GetUserSnsAccountsCallback) to be informed about the result of the operation.|




---  

## <a name="com.fresvii.components.AppSteroidSnsAccount"> Class AppSteroidSnsAccount </a>

```
public class AppSteroidSnsAccount extends AppSteroidComponent
```

**Hierarchy:**  

```
java.lang.Object  
    com.fresvii.components.AppSteroidComponent  
        com.fresvii.components.AppSteroidSnsAccount
```

**Description:**  
Represents an SNS Account.

**Author:**  
Matthias Kollmer

**Version:**  
1.0

**Since:**  
2014-06-68


### Method Summary

|Method|Description|
|---|---|
|[public Date getCreatedAt()](#com_fresvii_components_AppSteroidSnsAccount_java_util_Date_getCreatedAt_)|Retrieves the date at which the SNS Account was created.|
|[public Date getCreatedAtOrDefault()](#com_fresvii_components_AppSteroidSnsAccount_java_util_Date_getCreatedAtOrDefault_)|Retrieves the date at which the SNS Account was created, or a default value if the SNS Account's createdAt date is null.|
|[public String getId()](#com_fresvii_components_AppSteroidSnsAccount_java_lang_String_getId_)|Retrieves the SNS account's ID.|
|[public String getIdOrDefault()](#com_fresvii_components_AppSteroidSnsAccount_java_lang_String_getIdOrDefault_)|Retrieves the SNS account's ID, or a default value if the SNS account's ID is null.|
|[public String getProvider()](#com_fresvii_components_AppSteroidSnsAccount_java_lang_String_getProvider_)|Retrieves the SNS account's provider.|
|[public String getProviderOrDefault()](#com_fresvii_components_AppSteroidSnsAccount_java_lang_String_getProviderOrDefault_)|Retrieves the SNS account's provider, or a default value if the SNS account's provider is null.|
|[public String getUid()](#com_fresvii_components_AppSteroidSnsAccount_java_lang_String_getUid_)|Retrieves the SNS account's UID.|
|[public String getUidOrDefault()](#com_fresvii_components_AppSteroidSnsAccount_java_lang_String_getUidOrDefault_)|Retrieves the SNS account's UID, or a default value if the SNS account's UID is null.|
|[public Date getUpdatedAt()](#com_fresvii_components_AppSteroidSnsAccount_java_util_Date_getUpdatedAt_)|Retrieves the date at which the SNS Account was updated.|
|[public Date getUpdatedAtOrDefault()](#com_fresvii_components_AppSteroidSnsAccount_java_util_Date_getUpdatedAtOrDefault_)|Retrieves the date at which the SNS Account was updated, or a default value if the SNS Account's updatedAt date is null.|



### Method Detail
 


## <a name="com_fresvii_components_AppSteroidSnsAccount_java_util_Date_getCreatedAt_"> getCreatedAt </a>

```
public Date getCreatedAt()
```

Retrieves the date at which the SNS Account was created.

#### Returns

|Return Type|Description|
|---|---|
|Date|The date at which the SNS Account was created.|


## <a name="com_fresvii_components_AppSteroidSnsAccount_java_util_Date_getCreatedAtOrDefault_"> getCreatedAtOrDefault </a>

```
public Date getCreatedAtOrDefault()
```

Retrieves the date at which the SNS Account was created, or a default value if the SNS Account's createdAt date is null.

#### Returns

|Return Type|Description|
|---|---|
|Date|The date at which the SNS Account was created, or a default value|


## <a name="com_fresvii_components_AppSteroidSnsAccount_java_lang_String_getId_"> getId </a>

```
public String getId()
```

Retrieves the SNS account's ID.

#### Returns

|Return Type|Description|
|---|---|
|String|The SNS account's ID.|


## <a name="com_fresvii_components_AppSteroidSnsAccount_java_lang_String_getIdOrDefault_"> getIdOrDefault </a>

```
public String getIdOrDefault()
```

Retrieves the SNS account's ID, or a default value if the SNS account's ID is null.

#### Returns

|Return Type|Description|
|---|---|
|String|The SNS account's ID, or a default value|


## <a name="com_fresvii_components_AppSteroidSnsAccount_java_lang_String_getProvider_"> getProvider </a>

```
public String getProvider()
```

Retrieves the SNS account's provider.

#### Returns

|Return Type|Description|
|---|---|
|String|The SNS account's provider.|


## <a name="com_fresvii_components_AppSteroidSnsAccount_java_lang_String_getProviderOrDefault_"> getProviderOrDefault </a>

```
public String getProviderOrDefault()
```

Retrieves the SNS account's provider, or a default value if the SNS account's provider is null.

#### Returns

|Return Type|Description|
|---|---|
|String|The SNS account's provider, or a default value|


## <a name="com_fresvii_components_AppSteroidSnsAccount_java_lang_String_getUid_"> getUid </a>

```
public String getUid()
```

Retrieves the SNS account's UID.

#### Returns

|Return Type|Description|
|---|---|
|String|The SNS account's UID.|


## <a name="com_fresvii_components_AppSteroidSnsAccount_java_lang_String_getUidOrDefault_"> getUidOrDefault </a>

```
public String getUidOrDefault()
```

Retrieves the SNS account's UID, or a default value if the SNS account's UID is null.

#### Returns

|Return Type|Description|
|---|---|
|String|The SNS account's UID, or a default value|


## <a name="com_fresvii_components_AppSteroidSnsAccount_java_util_Date_getUpdatedAt_"> getUpdatedAt </a>

```
public Date getUpdatedAt()
```

Retrieves the date at which the SNS Account was updated.

#### Returns

|Return Type|Description|
|---|---|
|Date|The date at which the SNS Account was updated.|


## <a name="com_fresvii_components_AppSteroidSnsAccount_java_util_Date_getUpdatedAtOrDefault_"> getUpdatedAtOrDefault </a>

```
public Date getUpdatedAtOrDefault()
```

Retrieves the date at which the SNS Account was updated, or a default value if the SNS Account's updatedAt date is null.

#### Returns

|Return Type|Description|
|---|---|
|Date|The date at which the SNS Account was updated, or a default value|



---  

## <a name="com.fresvii.server.access.callbacks.account.AddUserSnsAccountCallback"> Interface AddUserSnsAccountCallback </a>

```
public interface AddUserSnsAccountCallback implements FailureCallback
```

**Hierarchy:**  

```
com.fresvii.server.access.callbacks.account.AddUserSnsAccountCallback
```

**Description:**  
Callback interface to handle [SnsAccountAccess.addUserSnsAccount()](#com_fresvii_server_access_SnsAccountAccess_void_addUserSnsAccount_String_String_AddUserSnsAccountCallback) results.

**Author:**  
Matthias Kollmer

**Version:**  
1.0




### Method Summary

|Method|Description|
|---|---|
|[public void onSuccess(AppSteroidSnsAccount snsAccount)](#com_fresvii_server_access_callbacks_account_AddUserSnsAccountCallback_void_onSuccess_AppSteroidSnsAccount)|Callback invoked when operation succeeds.|



### Method Detail
 


## <a name="com_fresvii_server_access_callbacks_account_AddUserSnsAccountCallback_void_onSuccess_AppSteroidSnsAccount"> onSuccess </a>

```
public void onSuccess(AppSteroidSnsAccount snsAccount)
```

Callback invoked when operation succeeds.



---  

## <a name="com.fresvii.server.access.callbacks.account.GetUserSnsAccountsCallback"> Interface GetUserSnsAccountsCallback </a>

```
public interface GetUserSnsAccountsCallback implements FailureCallback
```

**Hierarchy:**  

```
com.fresvii.server.access.callbacks.account.GetUserSnsAccountsCallback
```

**Description:**  
Callback interface to handle [SnsAccountAccess.getUserSnsAccounts()](#com_fresvii_server_access_SnsAccountAccess_void_getUserSnsAccounts_GetUserSnsAccountsCallback) results.

**Author:**  
Matthias Kollmer

**Version:**  
1.0




### Method Summary

|Method|Description|
|---|---|
|[public void onSuccess(List userSnsAccounts)](#com_fresvii_server_access_callbacks_account_GetUserSnsAccountsCallback_void_onSuccess_List)|Callback invoked when operation succeeds.|



### Method Detail
 


## <a name="com_fresvii_server_access_callbacks_account_GetUserSnsAccountsCallback_void_onSuccess_List"> onSuccess </a>

```
public void onSuccess(List userSnsAccounts)
```

Callback invoked when operation succeeds.



---  

## <a name="com.fresvii.server.access.callbacks.account.DeleteUserSnsAccountCallback"> Interface DeleteUserSnsAccountCallback </a>

```
public interface DeleteUserSnsAccountCallback implements FailureCallback
```

**Hierarchy:**  

```
com.fresvii.server.access.callbacks.account.DeleteUserSnsAccountCallback
```

**Description:**  
Callback interface to handle [SnsAccountAccess.deleteUserSnsAccount()](#com_fresvii_server_access_SnsAccountAccess_void_deleteUserSnsAccount_String_DeleteUserSnsAccountCallback) results.

**Author:**  
Matthias Kollmer

**Version:**  
1.0




### Method Summary

|Method|Description|
|---|---|
|[public void onSuccess()](#com_fresvii_server_access_callbacks_account_DeleteUserSnsAccountCallback_void_onSuccess_)|Callback invoked when operation succeeds.|



### Method Detail
 


## <a name="com_fresvii_server_access_callbacks_account_DeleteUserSnsAccountCallback_void_onSuccess_"> onSuccess </a>

```
public void onSuccess()
```

Callback invoked when operation succeeds.


