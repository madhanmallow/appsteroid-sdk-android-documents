
# AppSteroid Key Value Storage API

Last updated 2014-10-08

-------------------------

## Introduction

AppSteroid Key Value Storage API can be used to store arbitrary user data to the Fresvii Server.


---  

## Classes

|Class|Description|
|---|---|
|[KeyValueStorageAccess](#com.fresvii.server.access.KeyValueStorageAccess)|Provides access to Fresvii Server's Key Value Storage API.|
|[KeyValueStorageAccess.GetAllDataCallback](#com.fresvii.server.access.KeyValueStorageAccess.GetAllDataCallback)|Callback interface to handle [KeyValueStorageAccess.getAllData()](#com_fresvii_server_access_KeyValueStorageAccess_void_getAllData_KeyValueStorageAccess_GetAllDataCallback) results.|
|[KeyValueStorageAccess.GetDataCallback](#com.fresvii.server.access.KeyValueStorageAccess.GetDataCallback)|Callback interface to handle [KeyValueStorageAccess.getData()](#com_fresvii_server_access_KeyValueStorageAccess_void_getData_String_KeyValueStorageAccess_GetDataCallback) results.|
|[KeyValueStorageAccess.GetAllKeysCallback](#com.fresvii.server.access.KeyValueStorageAccess.GetAllKeysCallback)|Callback interface to handle [KeyValueStorageAccess.getAllKeys()](#com_fresvii_server_access_KeyValueStorageAccess_void_getAllKeys_KeyValueStorageAccess_GetAllKeysCallback) results.|
|[KeyValueStorageAccess.AddDataCallback](#com.fresvii.server.access.KeyValueStorageAccess.AddDataCallback)|Callback interface to handle [KeyValueStorageAccess.addData()](#com_fresvii_server_access_KeyValueStorageAccess_void_addData_String_String_KeyValueStorageAccess_AddDataCallback) results.|
|[KeyValueStorageAccess.RemoveDataCallback](#com.fresvii.server.access.KeyValueStorageAccess.RemoveDataCallback)|Callback interface to handle [KeyValueStorageAccess.removeData()](#com_fresvii_server_access_KeyValueStorageAccess_void_removeData_String_KeyValueStorageAccess_RemoveDataCallback) results.|



---  

## <a name="com.fresvii.server.access.KeyValueStorageAccess"> Class KeyValueStorageAccess </a>

```
public class KeyValueStorageAccess extends Object
```

**Hierarchy:**  

```
java.lang.Object  
    com.fresvii.server.access.KeyValueStorageAccess
```

**Description:**  
Provides access to Fresvii Server's Key Value Storage API.  Can be used to store/retrieve arbitrary data to/from the Fresvii server.

**Author:**  
Matthias Kollmer

**Version:**  
1.0

**Since:**  
2014-07-20


### Method Summary

|Method|Description|
|---|---|
|[public static void addData(String keyName, String value, KeyValueStorageAccess.AddDataCallback callback)](#com_fresvii_server_access_KeyValueStorageAccess_void_addData_String_String_KeyValueStorageAccess_AddDataCallback)|Adds a new or replaces an existing piece of data on the server.|
|[public static void addData(Map keyValueData, KeyValueStorageAccess.AddDataCallback callback)](#com_fresvii_server_access_KeyValueStorageAccess_void_addData_Map_KeyValueStorageAccess_AddDataCallback)|Adds or replaces multiple data sets on the server.|
|[public static void getAllData(KeyValueStorageAccess.GetAllDataCallback callback)](#com_fresvii_server_access_KeyValueStorageAccess_void_getAllData_KeyValueStorageAccess_GetAllDataCallback)|Retrieves all data stored previously.|
|[public static void getAllData(String prefix, KeyValueStorageAccess.GetAllDataCallback callback)](#com_fresvii_server_access_KeyValueStorageAccess_void_getAllData_String_KeyValueStorageAccess_GetAllDataCallback)|Retrieves all data where the key begins with the passed prefix.|
|[public static void getAllKeys(KeyValueStorageAccess.GetAllKeysCallback callback)](#com_fresvii_server_access_KeyValueStorageAccess_void_getAllKeys_KeyValueStorageAccess_GetAllKeysCallback)|Retrieves a list of all keys that are currently in use to store data.|
|[public static void getData(String keyName, KeyValueStorageAccess.GetDataCallback callback)](#com_fresvii_server_access_KeyValueStorageAccess_void_getData_String_KeyValueStorageAccess_GetDataCallback)|Retrieves a specific data field stored previously.|
|[public static void removeData(String keyName, KeyValueStorageAccess.RemoveDataCallback callback)](#com_fresvii_server_access_KeyValueStorageAccess_void_removeData_String_KeyValueStorageAccess_RemoveDataCallback)|Removes a single piece of data from the server.|



### Method Detail
 


## <a name="com_fresvii_server_access_KeyValueStorageAccess_void_addData_String_String_KeyValueStorageAccess_AddDataCallback"> addData </a>

```
public static void addData(String keyName,  
                           String value,  
                           KeyValueStorageAccess.AddDataCallback callback)
```

Adds a new or replaces an existing piece of data on the server.

#### Parameters

|Parameter|Description|
|---|---|
|String keyName|The key used to store the data.|
|String value|The data to be stored.|
|[KeyValueStorageAccess.AddDataCallback](#com.fresvii.server.access.KeyValueStorageAccess.AddDataCallback) callback|[Callback](#com.fresvii.server.access.KeyValueStorageAccess.AddDataCallback) to be informed about the result of the operation.|



## <a name="com_fresvii_server_access_KeyValueStorageAccess_void_addData_Map_KeyValueStorageAccess_AddDataCallback"> addData </a>

```
public static void addData(Map keyValueData,  
                           KeyValueStorageAccess.AddDataCallback callback)
```

Adds or replaces multiple data sets on the server.

#### Parameters

|Parameter|Description|
|---|---|
|Map keyValueData|A collection containing key value pairs to be stored on the server.|
|[KeyValueStorageAccess.AddDataCallback](#com.fresvii.server.access.KeyValueStorageAccess.AddDataCallback) callback|[Callback](#com.fresvii.server.access.KeyValueStorageAccess.AddDataCallback) to be informed about the result of the operation.|



## <a name="com_fresvii_server_access_KeyValueStorageAccess_void_getAllData_KeyValueStorageAccess_GetAllDataCallback"> getAllData </a>

```
public static void getAllData(KeyValueStorageAccess.GetAllDataCallback callback)
```

Retrieves all data stored previously.

#### Parameters

|Parameter|Description|
|---|---|
|[KeyValueStorageAccess.GetAllDataCallback](#com.fresvii.server.access.KeyValueStorageAccess.GetAllDataCallback) callback|[Callback](#com.fresvii.server.access.KeyValueStorageAccess.GetAllDataCallback) to be informed about the result of the operation.|



## <a name="com_fresvii_server_access_KeyValueStorageAccess_void_getAllData_String_KeyValueStorageAccess_GetAllDataCallback"> getAllData </a>

```
public static void getAllData(String prefix,  
                              KeyValueStorageAccess.GetAllDataCallback callback)
```

Retrieves all data where the key begins with the passed prefix.

#### Parameters

|Parameter|Description|
|---|---|
|String prefix|The prefix for keys to filter the returned data.|
|[KeyValueStorageAccess.GetAllDataCallback](#com.fresvii.server.access.KeyValueStorageAccess.GetAllDataCallback) callback|[Callback](#com.fresvii.server.access.KeyValueStorageAccess.GetAllDataCallback) to be informed about the result of the operation.|



## <a name="com_fresvii_server_access_KeyValueStorageAccess_void_getAllKeys_KeyValueStorageAccess_GetAllKeysCallback"> getAllKeys </a>

```
public static void getAllKeys(KeyValueStorageAccess.GetAllKeysCallback callback)
```

Retrieves a list of all keys that are currently in use to store data.

#### Parameters

|Parameter|Description|
|---|---|
|[KeyValueStorageAccess.GetAllKeysCallback](#com.fresvii.server.access.KeyValueStorageAccess.GetAllKeysCallback) callback|[Callback](#com.fresvii.server.access.KeyValueStorageAccess.GetAllKeysCallback) to be informed about the result of the operation.|



## <a name="com_fresvii_server_access_KeyValueStorageAccess_void_getData_String_KeyValueStorageAccess_GetDataCallback"> getData </a>

```
public static void getData(String keyName,  
                           KeyValueStorageAccess.GetDataCallback callback)
```

Retrieves a specific data field stored previously.

#### Parameters

|Parameter|Description|
|---|---|
|String keyName|The key for the data to be retrieved.|
|[KeyValueStorageAccess.GetDataCallback](#com.fresvii.server.access.KeyValueStorageAccess.GetDataCallback) callback|[Callback](#com.fresvii.server.access.KeyValueStorageAccess.GetDataCallback) to be informed about the result of the operation.|



## <a name="com_fresvii_server_access_KeyValueStorageAccess_void_removeData_String_KeyValueStorageAccess_RemoveDataCallback"> removeData </a>

```
public static void removeData(String keyName,  
                              KeyValueStorageAccess.RemoveDataCallback callback)
```

Removes a single piece of data from the server.

#### Parameters

|Parameter|Description|
|---|---|
|String keyName|The key name associated with the data to be removed.|
|[KeyValueStorageAccess.RemoveDataCallback](#com.fresvii.server.access.KeyValueStorageAccess.RemoveDataCallback) callback|[Callback](#com.fresvii.server.access.KeyValueStorageAccess.RemoveDataCallback) to be informed about the result of the operation.|




---  

## <a name="com.fresvii.server.access.KeyValueStorageAccess.GetAllDataCallback"> Interface KeyValueStorageAccess.GetAllDataCallback </a>

```
public static interface KeyValueStorageAccess.GetAllDataCallback implements FailureCallback
```

**Hierarchy:**  

```
com.fresvii.server.access.KeyValueStorageAccess.GetAllDataCallback
```

**Description:**  
Callback interface to handle [KeyValueStorageAccess.getAllData()](#com_fresvii_server_access_KeyValueStorageAccess_void_getAllData_KeyValueStorageAccess_GetAllDataCallback) results.









---  

## <a name="com.fresvii.server.access.KeyValueStorageAccess.GetDataCallback"> Interface KeyValueStorageAccess.GetDataCallback </a>

```
public static interface KeyValueStorageAccess.GetDataCallback implements FailureCallback
```

**Hierarchy:**  

```
com.fresvii.server.access.KeyValueStorageAccess.GetDataCallback
```

**Description:**  
Callback interface to handle [KeyValueStorageAccess.getData()](#com_fresvii_server_access_KeyValueStorageAccess_void_getData_String_KeyValueStorageAccess_GetDataCallback) results.









---  

## <a name="com.fresvii.server.access.KeyValueStorageAccess.GetAllKeysCallback"> Interface KeyValueStorageAccess.GetAllKeysCallback </a>

```
public static interface KeyValueStorageAccess.GetAllKeysCallback implements FailureCallback
```

**Hierarchy:**  

```
com.fresvii.server.access.KeyValueStorageAccess.GetAllKeysCallback
```

**Description:**  
Callback interface to handle [KeyValueStorageAccess.getAllKeys()](#com_fresvii_server_access_KeyValueStorageAccess_void_getAllKeys_KeyValueStorageAccess_GetAllKeysCallback) results.









---  

## <a name="com.fresvii.server.access.KeyValueStorageAccess.AddDataCallback"> Interface KeyValueStorageAccess.AddDataCallback </a>

```
public static interface KeyValueStorageAccess.AddDataCallback implements FailureCallback
```

**Hierarchy:**  

```
com.fresvii.server.access.KeyValueStorageAccess.AddDataCallback
```

**Description:**  
Callback interface to handle [KeyValueStorageAccess.addData()](#com_fresvii_server_access_KeyValueStorageAccess_void_addData_String_String_KeyValueStorageAccess_AddDataCallback) results.









---  

## <a name="com.fresvii.server.access.KeyValueStorageAccess.RemoveDataCallback"> Interface KeyValueStorageAccess.RemoveDataCallback </a>

```
public static interface KeyValueStorageAccess.RemoveDataCallback implements FailureCallback
```

**Hierarchy:**  

```
com.fresvii.server.access.KeyValueStorageAccess.RemoveDataCallback
```

**Description:**  
Callback interface to handle [KeyValueStorageAccess.removeData()](#com_fresvii_server_access_KeyValueStorageAccess_void_removeData_String_KeyValueStorageAccess_RemoveDataCallback) results.








