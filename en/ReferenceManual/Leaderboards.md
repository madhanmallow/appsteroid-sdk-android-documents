
# AppSteroid Leaderboards API

Last updated 2014-12-10

-------------------------

## Introduction

AppSteroid Leaderboards API can be used to manage AppSteroid leaderboards.


---  

## Classes

|Class|Description|
|---|---|
|[LeaderboardAccess](#com.fresvii.server.access.LeaderboardAccess)|Provides access to Fresvii Server's Leaderboard API.|
|[AppSteroidLeaderboard](#com.fresvii.components.AppSteroidLeaderboard)|Represents a Fresvii Leaderboard|
|[AppSteroidRank](#com.fresvii.components.AppSteroidRank)|Represents a Fresvii Rank.|
|[AppSteroidScore](#com.fresvii.components.AppSteroidScore)|Represents a Fresvii Score.|
|[AppSteroidScore.ScoreType](#com.fresvii.components.AppSteroidScore.ScoreType)|Score Type.|
|[GetLeaderboardCallback](#com.fresvii.server.access.callbacks.leaderboard.GetLeaderboardCallback)|Callback interface to handle [LeaderboardAccess.getLeaderboard()](#com_fresvii_server_access_LeaderboardAccess_void_getLeaderboard_String_GetLeaderboardCallback) results.|
|[GetLeaderboardsCallback](#com.fresvii.server.access.callbacks.leaderboard.GetLeaderboardsCallback)|Callback interface to handle [LeaderboardAccess.getLeaderboards()](#com_fresvii_server_access_LeaderboardAccess_void_getLeaderboards_GetLeaderboardsCallback) results.|
|[GetRankForUserCallback](#com.fresvii.server.access.callbacks.leaderboard.GetRankForUserCallback)|Callback interface to handle [LeaderboardAccess.getRankForUser()](#com_fresvii_server_access_LeaderboardAccess_void_getRankForUser_String_String_Date_Boolean_GetRankForUserCallback) results.|
|[GetRankingCallback](#com.fresvii.server.access.callbacks.leaderboard.GetRankingCallback)|Callback interface to handle [LeaderboardAccess.getRanking()](#com_fresvii_server_access_LeaderboardAccess_void_getRanking_String_Date_Boolean_GetRankingCallback) results.|
|[GetScoreCallback](#com.fresvii.server.access.callbacks.leaderboard.GetScoreCallback)|Callback interface to handle [LeaderboardAccess.getScore()](#com_fresvii_server_access_LeaderboardAccess_void_getScore_String_String_GetScoreCallback) results.|
|[GetScoresForUserCallback](#com.fresvii.server.access.callbacks.leaderboard.GetScoresForUserCallback)|Callback interface to handle [LeaderboardAccess.getScoresForUser()](#com_fresvii_server_access_LeaderboardAccess_void_getScoresForUser_String_String_Date_AppSteroidScore_ScoreType_GetScoresForUserCallback) results.|
|[PostScoreCallback](#com.fresvii.server.access.callbacks.leaderboard.PostScoreCallback)|Callback interface to handle [LeaderboardAccess.postScore()](#com_fresvii_server_access_LeaderboardAccess_void_postScore_String_Integer_Date_PostScoreCallback) results.|
|[DeleteScoreCallback](#com.fresvii.server.access.callbacks.leaderboard.DeleteScoreCallback)|Callback interface to handle [LeaderboardAccess.deleteScore()](#com_fresvii_server_access_LeaderboardAccess_void_deleteScore_String_String_DeleteScoreCallback) results.|



---  

## <a name="com.fresvii.server.access.LeaderboardAccess"> Class LeaderboardAccess </a>

```
public class LeaderboardAccess extends Object
```

**Hierarchy:**  

```
java.lang.Object  
    com.fresvii.server.access.LeaderboardAccess
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
|[public static void deleteScore(String leaderboardId, String scoreId, DeleteScoreCallback callback)](#com_fresvii_server_access_LeaderboardAccess_void_deleteScore_String_String_DeleteScoreCallback)|Deletes a score from a leaderboard.|
|[public static void getLeaderboard(String leaderboardId, GetLeaderboardCallback callback)](#com_fresvii_server_access_LeaderboardAccess_void_getLeaderboard_String_GetLeaderboardCallback)|Retrieves a leaderboard.|
|[public static void getLeaderboards(GetLeaderboardsCallback callback)](#com_fresvii_server_access_LeaderboardAccess_void_getLeaderboards_GetLeaderboardsCallback)|Retrieves a list of leaderboards from the initial page.|
|[public static void getLeaderboards(int page, GetLeaderboardsCallback callback)](#com_fresvii_server_access_LeaderboardAccess_void_getLeaderboards_int_GetLeaderboardsCallback)|Retrieves a list of leaderboards from the specified page.|
|[public static void getRankForUser(String leaderboardId, String userId, Date startTime, Boolean onlyFriends, GetRankForUserCallback callback)](#com_fresvii_server_access_LeaderboardAccess_void_getRankForUser_String_String_Date_Boolean_GetRankForUserCallback)|Retrieves the rank in a leaderboard for a specific user.|
|[public static void getRanking(String leaderboardId, Date startTime, Boolean onlyFriends, GetRankingCallback callback)](#com_fresvii_server_access_LeaderboardAccess_void_getRanking_String_Date_Boolean_GetRankingCallback)|Retrieves the ranking for a leaderboard from the initial page.|
|[public static void getRanking(int page, String leaderboardId, Date startTime, Boolean onlyFriends, GetRankingCallback callback)](#com_fresvii_server_access_LeaderboardAccess_void_getRanking_int_String_Date_Boolean_GetRankingCallback)|Retrieves the ranking for a leaderboard from the specified page.|
|[public static void getScore(String leaderboardId, String scoreId, GetScoreCallback callback)](#com_fresvii_server_access_LeaderboardAccess_void_getScore_String_String_GetScoreCallback)|Retrieves a score from a leaderboard.|
|[public static void getScoresForUser(String leaderboardId, String userId, Date startTime, AppSteroidScore.ScoreType sortBy, GetScoresForUserCallback callback)](#com_fresvii_server_access_LeaderboardAccess_void_getScoresForUser_String_String_Date_AppSteroidScore_ScoreType_GetScoresForUserCallback)|Retrieves a list of scores for a user from the initial page.|
|[public static void getScoresForUser(int page, String leaderboardId, String userId, Date startTime, AppSteroidScore.ScoreType sortBy, GetScoresForUserCallback callback)](#com_fresvii_server_access_LeaderboardAccess_void_getScoresForUser_int_String_String_Date_AppSteroidScore_ScoreType_GetScoresForUserCallback)|Retrieves a list of scores for a user from the specified page.|
|[public static void postScore(String leaderboardId, Integer value, Date createdAt, PostScoreCallback callback)](#com_fresvii_server_access_LeaderboardAccess_void_postScore_String_Integer_Date_PostScoreCallback)|Posts a score to a leaderboard.|



### Method Detail
 


## <a name="com_fresvii_server_access_LeaderboardAccess_void_deleteScore_String_String_DeleteScoreCallback"> deleteScore </a>

```
public static void deleteScore(String leaderboardId,  
                               String scoreId,  
                               DeleteScoreCallback callback)
```

Deletes a score from a leaderboard.

#### Parameters

|Parameter|Description|
|---|---|
|String leaderboardId|ID of the leaderboard that holds the score.|
|String scoreId|ID of the score to be deleted.|
|[DeleteScoreCallback](#com.fresvii.server.access.callbacks.leaderboard.DeleteScoreCallback) callback|[Callback](#com.fresvii.server.access.callbacks.leaderboard.DeleteScoreCallback) to be informed about the result of the operation.|



## <a name="com_fresvii_server_access_LeaderboardAccess_void_getLeaderboard_String_GetLeaderboardCallback"> getLeaderboard </a>

```
public static void getLeaderboard(String leaderboardId,  
                                  GetLeaderboardCallback callback)
```

Retrieves a leaderboard.

#### Parameters

|Parameter|Description|
|---|---|
|String leaderboardId|ID of the leaderboard to be retrieved.|
|[GetLeaderboardCallback](#com.fresvii.server.access.callbacks.leaderboard.GetLeaderboardCallback) callback|[Callback](#com.fresvii.server.access.callbacks.leaderboard.GetLeaderboardCallback) to be informed about the result of the operation.|



## <a name="com_fresvii_server_access_LeaderboardAccess_void_getLeaderboards_GetLeaderboardsCallback"> getLeaderboards </a>

```
public static void getLeaderboards(GetLeaderboardsCallback callback)
```

Retrieves a list of leaderboards from the initial page.

#### Parameters

|Parameter|Description|
|---|---|
|[GetLeaderboardsCallback](#com.fresvii.server.access.callbacks.leaderboard.GetLeaderboardsCallback) callback|[Callback](#com.fresvii.server.access.callbacks.leaderboard.GetLeaderboardsCallback) to be informed about the result of the operation.|



## <a name="com_fresvii_server_access_LeaderboardAccess_void_getLeaderboards_int_GetLeaderboardsCallback"> getLeaderboards </a>

```
public static void getLeaderboards(int page,  
                                   GetLeaderboardsCallback callback)
```

Retrieves a list of leaderboards from the specified page.

#### Parameters

|Parameter|Description|
|---|---|
|int page|Page offset.|
|[GetLeaderboardsCallback](#com.fresvii.server.access.callbacks.leaderboard.GetLeaderboardsCallback) callback|[Callback](#com.fresvii.server.access.callbacks.leaderboard.GetLeaderboardsCallback) to be informed about the result of the operation.|



## <a name="com_fresvii_server_access_LeaderboardAccess_void_getRankForUser_String_String_Date_Boolean_GetRankForUserCallback"> getRankForUser </a>

```
public static void getRankForUser(String leaderboardId,  
                                  String userId,  
                                  Date startTime,  
                                  Boolean onlyFriends,  
                                  GetRankForUserCallback callback)
```

Retrieves the rank in a leaderboard for a specific user.

#### Parameters

|Parameter|Description|
|---|---|
|String leaderboardId|ID of the leaderboard from which to retrieve the rank.|
|String userId|ID of the user for which to retrieve the rank.|
|Date startTime|[Callback](#com.fresvii.server.access.callbacks.leaderboard.GetRankForUserCallback) to be informed about the result of the operation.|



## <a name="com_fresvii_server_access_LeaderboardAccess_void_getRanking_String_Date_Boolean_GetRankingCallback"> getRanking </a>

```
public static void getRanking(String leaderboardId,  
                              Date startTime,  
                              Boolean onlyFriends,  
                              GetRankingCallback callback)
```

Retrieves the ranking for a leaderboard from the initial page.

#### Parameters

|Parameter|Description|
|---|---|
|String leaderboardId|ID of the leaderboard for which to retrieve the ranking.|
|Date startTime|Optional start Time.|
|Boolean onlyFriends|Optional flag to specify whether to include only friends in the ranking.|
|[GetRankingCallback](#com.fresvii.server.access.callbacks.leaderboard.GetRankingCallback) callback|[Callback](#com.fresvii.server.access.callbacks.leaderboard.GetRankingCallback) to be informed about the result of the operation.|



## <a name="com_fresvii_server_access_LeaderboardAccess_void_getRanking_int_String_Date_Boolean_GetRankingCallback"> getRanking </a>

```
public static void getRanking(int page,  
                              String leaderboardId,  
                              Date startTime,  
                              Boolean onlyFriends,  
                              GetRankingCallback callback)
```

Retrieves the ranking for a leaderboard from the specified page.

#### Parameters

|Parameter|Description|
|---|---|
|int page|Page offset.|
|String leaderboardId|ID of the leaderboard for which to retrieve the ranking.|
|Date startTime|Optional start Time.|
|Boolean onlyFriends|Optional flag to specify whether to include only friends in the ranking.|
|[GetRankingCallback](#com.fresvii.server.access.callbacks.leaderboard.GetRankingCallback) callback|[Callback](#com.fresvii.server.access.callbacks.leaderboard.GetRankingCallback) to be informed about the result of the operation.|



## <a name="com_fresvii_server_access_LeaderboardAccess_void_getScore_String_String_GetScoreCallback"> getScore </a>

```
public static void getScore(String leaderboardId,  
                            String scoreId,  
                            GetScoreCallback callback)
```

Retrieves a score from a leaderboard.

#### Parameters

|Parameter|Description|
|---|---|
|String leaderboardId|ID of the leaderboard that holds the score.|
|String scoreId|ID of the score to be retrieved.|
|[GetScoreCallback](#com.fresvii.server.access.callbacks.leaderboard.GetScoreCallback) callback|[Callback](#com.fresvii.server.access.callbacks.leaderboard.GetScoreCallback) to be informed about the result of the operation.|



## <a name="com_fresvii_server_access_LeaderboardAccess_void_getScoresForUser_String_String_Date_AppSteroidScore_ScoreType_GetScoresForUserCallback"> getScoresForUser </a>

```
public static void getScoresForUser(String leaderboardId,  
                                    String userId,  
                                    Date startTime,  
                                    AppSteroidScore.ScoreType sortBy,  
                                    GetScoresForUserCallback callback)
```

Retrieves a list of scores for a user from the initial page.

#### Parameters

|Parameter|Description|
|---|---|
|String leaderboardId|ID of the leaderboard from which to retrieve the scores.|
|String userId|ID of the user for which to retrieve the scores.|
|Date startTime|Optional start time.|
|[AppSteroidScore.ScoreType](#com.fresvii.components.AppSteroidScore.ScoreType) sortBy|Optional sort order.|
|[GetScoresForUserCallback](#com.fresvii.server.access.callbacks.leaderboard.GetScoresForUserCallback) callback|[Callback](#com.fresvii.server.access.callbacks.leaderboard.GetScoresForUserCallback) to be informed about the result of the operation.|



## <a name="com_fresvii_server_access_LeaderboardAccess_void_getScoresForUser_int_String_String_Date_AppSteroidScore_ScoreType_GetScoresForUserCallback"> getScoresForUser </a>

```
public static void getScoresForUser(int page,  
                                    String leaderboardId,  
                                    String userId,  
                                    Date startTime,  
                                    AppSteroidScore.ScoreType sortBy,  
                                    GetScoresForUserCallback callback)
```

Retrieves a list of scores for a user from the specified page.

#### Parameters

|Parameter|Description|
|---|---|
|int page|Page offset.|
|String leaderboardId|ID of the leaderboard from which to retrieve the scores.|
|String userId|ID of the user for which to retrieve the scores.|
|Date startTime|Optional start time.|
|[AppSteroidScore.ScoreType](#com.fresvii.components.AppSteroidScore.ScoreType) sortBy|Optional sort order.|
|[GetScoresForUserCallback](#com.fresvii.server.access.callbacks.leaderboard.GetScoresForUserCallback) callback|[Callback](#com.fresvii.server.access.callbacks.leaderboard.GetScoresForUserCallback) to be informed about the result of the operation.|



## <a name="com_fresvii_server_access_LeaderboardAccess_void_postScore_String_Integer_Date_PostScoreCallback"> postScore </a>

```
public static void postScore(String leaderboardId,  
                             Integer value,  
                             Date createdAt,  
                             PostScoreCallback callback)
```

Posts a score to a leaderboard.

#### Parameters

|Parameter|Description|
|---|---|
|String leaderboardId|ID of the leaderboard to which the score should be posted.|
|Integer value|Score value.|
|Date createdAt|Optional Date at which the score was achieved.|
|[PostScoreCallback](#com.fresvii.server.access.callbacks.leaderboard.PostScoreCallback) callback|[Callback](#com.fresvii.server.access.callbacks.leaderboard.PostScoreCallback) to be informed about the result of the operation.|




---  

## <a name="com.fresvii.components.AppSteroidLeaderboard"> Class AppSteroidLeaderboard </a>

```
public class AppSteroidLeaderboard extends AppSteroidComponent
```

**Hierarchy:**  

```
java.lang.Object  
    com.fresvii.components.AppSteroidComponent  
        com.fresvii.components.AppSteroidLeaderboard
```

**Description:**  
Represents a Fresvii Leaderboard

**Author:**  
Marcus Froeschl

**Version:**  
1.0

**Since:**  
2014-08-19


### Method Summary

|Method|Description|
|---|---|
|[public Boolean getAscend()](#com_fresvii_components_AppSteroidLeaderboard_java_lang_Boolean_getAscend_)|Retrieves the ascend property.|
|[public boolean getAscendOrDefault()](#com_fresvii_components_AppSteroidLeaderboard_boolean_getAscendOrDefault_)|Retrieves the ascend property, or a default value if the ascend property is null.|
|[public Date getCreatedAt()](#com_fresvii_components_AppSteroidLeaderboard_java_util_Date_getCreatedAt_)|Retrieves the date at which the object was created.|
|[public Date getCreatedAtOrDefault()](#com_fresvii_components_AppSteroidLeaderboard_java_util_Date_getCreatedAtOrDefault_)|Retrieves the date at which the object was created, or a default value if the object's createdAt date is null.|
|[public String getId()](#com_fresvii_components_AppSteroidLeaderboard_java_lang_String_getId_)|Retrieves the ID.|
|[public String getIdOrDefault()](#com_fresvii_components_AppSteroidLeaderboard_java_lang_String_getIdOrDefault_)|Retrieves the ID, or a default value if the ID is null.|
|[public String getName()](#com_fresvii_components_AppSteroidLeaderboard_java_lang_String_getName_)|Retrieves the name.|
|[public String getNameOrDefault()](#com_fresvii_components_AppSteroidLeaderboard_java_lang_String_getNameOrDefault_)|Retrieves the name, or a default value if the name is null.|
|[public AppSteroidScore.ScoreType getScoreType()](#com_fresvii_components_AppSteroidLeaderboard_com_fresvii_components_AppSteroidScore_ScoreType_getScoreType_)|Retrieves the ScoreType.|
|[public AppSteroidScore.ScoreType getScoreTypeOrDefault()](#com_fresvii_components_AppSteroidLeaderboard_com_fresvii_components_AppSteroidScore_ScoreType_getScoreTypeOrDefault_)|Retrieves the ScoreType, or a default value if the object's ScoreType is null.|
|[public Date getUpdatedAt()](#com_fresvii_components_AppSteroidLeaderboard_java_util_Date_getUpdatedAt_)|Retrieves the date at which the object was updated.|
|[public Date getUpdatedAtOrDefault()](#com_fresvii_components_AppSteroidLeaderboard_java_util_Date_getUpdatedAtOrDefault_)|Retrieves the date at which the object was updated, or a default value if the object's updatedAt date is null.|



### Method Detail
 


## <a name="com_fresvii_components_AppSteroidLeaderboard_java_lang_Boolean_getAscend_"> getAscend </a>

```
public Boolean getAscend()
```

Retrieves the ascend property.

#### Returns

|Return Type|Description|
|---|---|
|Boolean|The ascend property.|


## <a name="com_fresvii_components_AppSteroidLeaderboard_boolean_getAscendOrDefault_"> getAscendOrDefault </a>

```
public boolean getAscendOrDefault()
```

Retrieves the ascend property, or a default value if the ascend property is null.

#### Returns

|Return Type|Description|
|---|---|
|boolean|The ascend property, or a default value|


## <a name="com_fresvii_components_AppSteroidLeaderboard_java_util_Date_getCreatedAt_"> getCreatedAt </a>

```
public Date getCreatedAt()
```

Retrieves the date at which the object was created.

#### Returns

|Return Type|Description|
|---|---|
|Date|The date at which the object was created.|


## <a name="com_fresvii_components_AppSteroidLeaderboard_java_util_Date_getCreatedAtOrDefault_"> getCreatedAtOrDefault </a>

```
public Date getCreatedAtOrDefault()
```

Retrieves the date at which the object was created, or a default value if the object's createdAt date is null.

#### Returns

|Return Type|Description|
|---|---|
|Date|The date at which the object was created, or a default value|


## <a name="com_fresvii_components_AppSteroidLeaderboard_java_lang_String_getId_"> getId </a>

```
public String getId()
```

Retrieves the ID.

#### Returns

|Return Type|Description|
|---|---|
|String|The ID.|


## <a name="com_fresvii_components_AppSteroidLeaderboard_java_lang_String_getIdOrDefault_"> getIdOrDefault </a>

```
public String getIdOrDefault()
```

Retrieves the ID, or a default value if the ID is null.

#### Returns

|Return Type|Description|
|---|---|
|String|The ID, or a default value|


## <a name="com_fresvii_components_AppSteroidLeaderboard_java_lang_String_getName_"> getName </a>

```
public String getName()
```

Retrieves the name.

#### Returns

|Return Type|Description|
|---|---|
|String|The name.|


## <a name="com_fresvii_components_AppSteroidLeaderboard_java_lang_String_getNameOrDefault_"> getNameOrDefault </a>

```
public String getNameOrDefault()
```

Retrieves the name, or a default value if the name is null.

#### Returns

|Return Type|Description|
|---|---|
|String|The name, or a default value|


## <a name="com_fresvii_components_AppSteroidLeaderboard_com_fresvii_components_AppSteroidScore_ScoreType_getScoreType_"> getScoreType </a>

```
public AppSteroidScore.ScoreType getScoreType()
```

Retrieves the ScoreType.

#### Returns

|Return Type|Description|
|---|---|
|AppSteroidScore.ScoreType|The ScoreType.|


## <a name="com_fresvii_components_AppSteroidLeaderboard_com_fresvii_components_AppSteroidScore_ScoreType_getScoreTypeOrDefault_"> getScoreTypeOrDefault </a>

```
public AppSteroidScore.ScoreType getScoreTypeOrDefault()
```

Retrieves the ScoreType, or a default value if the object's ScoreType is null.

#### Returns

|Return Type|Description|
|---|---|
|AppSteroidScore.ScoreType|The ScoreType, or a default value|


## <a name="com_fresvii_components_AppSteroidLeaderboard_java_util_Date_getUpdatedAt_"> getUpdatedAt </a>

```
public Date getUpdatedAt()
```

Retrieves the date at which the object was updated.

#### Returns

|Return Type|Description|
|---|---|
|Date|The date at which the object was updated.|


## <a name="com_fresvii_components_AppSteroidLeaderboard_java_util_Date_getUpdatedAtOrDefault_"> getUpdatedAtOrDefault </a>

```
public Date getUpdatedAtOrDefault()
```

Retrieves the date at which the object was updated, or a default value if the object's updatedAt date is null.

#### Returns

|Return Type|Description|
|---|---|
|Date|The date at which the object was updated, or a default value|



---  

## <a name="com.fresvii.components.AppSteroidRank"> Class AppSteroidRank </a>

```
public class AppSteroidRank extends AppSteroidScore
```

**Hierarchy:**  

```
java.lang.Object  
    com.fresvii.components.AppSteroidComponent  
        com.fresvii.components.AppSteroidScore  
            com.fresvii.components.AppSteroidRank
```

**Description:**  
Represents a Fresvii Rank.

**Author:**  
Marcus Froeschl

**Version:**  
1.0

**Since:**  
2014-08-19


### Method Summary

|Method|Description|
|---|---|
|[public Integer getRank()](#com_fresvii_components_AppSteroidRank_java_lang_Integer_getRank_)|Retrieves the rank.|
|[public int getRankOrDefault()](#com_fresvii_components_AppSteroidRank_int_getRankOrDefault_)|Retrieves the rank, or a default value if the rank is null.|
|[public AppSteroidScore getScore()](#com_fresvii_components_AppSteroidRank_com_fresvii_components_AppSteroidScore_getScore_)|Retrieves the score.|
|[public AppSteroidScore getScoreOrDefault()](#com_fresvii_components_AppSteroidRank_com_fresvii_components_AppSteroidScore_getScoreOrDefault_)|Retrieves the score, or a default value if the score is null.|



### Method Detail
 


## <a name="com_fresvii_components_AppSteroidRank_java_lang_Integer_getRank_"> getRank </a>

```
public Integer getRank()
```

Retrieves the rank.

#### Returns

|Return Type|Description|
|---|---|
|Integer|The rank.|


## <a name="com_fresvii_components_AppSteroidRank_int_getRankOrDefault_"> getRankOrDefault </a>

```
public int getRankOrDefault()
```

Retrieves the rank, or a default value if the rank is null.

#### Returns

|Return Type|Description|
|---|---|
|int|The rank, or a default value|


## <a name="com_fresvii_components_AppSteroidRank_com_fresvii_components_AppSteroidScore_getScore_"> getScore </a>

```
public AppSteroidScore getScore()
```

Retrieves the score.

#### Returns

|Return Type|Description|
|---|---|
|AppSteroidScore|The rank.|


## <a name="com_fresvii_components_AppSteroidRank_com_fresvii_components_AppSteroidScore_getScoreOrDefault_"> getScoreOrDefault </a>

```
public AppSteroidScore getScoreOrDefault()
```

Retrieves the score, or a default value if the score is null.

#### Returns

|Return Type|Description|
|---|---|
|AppSteroidScore|The score, or a default value|



---  

## <a name="com.fresvii.components.AppSteroidScore"> Class AppSteroidScore </a>

```
public class AppSteroidScore extends AppSteroidComponent
```

**Hierarchy:**  

```
java.lang.Object  
    com.fresvii.components.AppSteroidComponent  
        com.fresvii.components.AppSteroidScore
```

**Description:**  
Represents a Fresvii Score.

**Author:**  
Marcus Froeschl

**Version:**  
1.0

**Since:**  
2014-08-19


### Method Summary

|Method|Description|
|---|---|
|[public Date getCreatedAt()](#com_fresvii_components_AppSteroidScore_java_util_Date_getCreatedAt_)|Retrieves the date at which the object was created.|
|[public Date getCreatedAtOrDefault()](#com_fresvii_components_AppSteroidScore_java_util_Date_getCreatedAtOrDefault_)|Retrieves the date at which the object was created, or a default value if the object's createdAt date is null.|
|[public String getId()](#com_fresvii_components_AppSteroidScore_java_lang_String_getId_)|Retrieves the ID.|
|[public String getIdOrDefault()](#com_fresvii_components_AppSteroidScore_java_lang_String_getIdOrDefault_)|Retrieves the ID, or a default value if the ID is null.|
|[public AppSteroidLeaderboard getLeaderboard()](#com_fresvii_components_AppSteroidScore_com_fresvii_components_AppSteroidLeaderboard_getLeaderboard_)|Retrieves the leaderboard.|
|[public AppSteroidLeaderboard getLeaderboardOrDefault()](#com_fresvii_components_AppSteroidScore_com_fresvii_components_AppSteroidLeaderboard_getLeaderboardOrDefault_)|Retrieves the leaderboard, or a default value if the leaderboard is null.|
|[public AppSteroidUser getUser()](#com_fresvii_components_AppSteroidScore_com_fresvii_components_AppSteroidUser_getUser_)|Retrieves the user.|
|[public AppSteroidUser getUserOrDefault()](#com_fresvii_components_AppSteroidScore_com_fresvii_components_AppSteroidUser_getUserOrDefault_)|Retrieves the user, or a default value if the user is null.|
|[public Integer getValue()](#com_fresvii_components_AppSteroidScore_java_lang_Integer_getValue_)|Retrieves the value.|
|[public int getValueOrDefault()](#com_fresvii_components_AppSteroidScore_int_getValueOrDefault_)|Retrieves the value, or a default value if the value is null.|



### Method Detail
 


## <a name="com_fresvii_components_AppSteroidScore_java_util_Date_getCreatedAt_"> getCreatedAt </a>

```
public Date getCreatedAt()
```

Retrieves the date at which the object was created.

#### Returns

|Return Type|Description|
|---|---|
|Date|The date at which the object was created.|


## <a name="com_fresvii_components_AppSteroidScore_java_util_Date_getCreatedAtOrDefault_"> getCreatedAtOrDefault </a>

```
public Date getCreatedAtOrDefault()
```

Retrieves the date at which the object was created, or a default value if the object's createdAt date is null.

#### Returns

|Return Type|Description|
|---|---|
|Date|The date at which the object was created, or a default value|


## <a name="com_fresvii_components_AppSteroidScore_java_lang_String_getId_"> getId </a>

```
public String getId()
```

Retrieves the ID.

#### Returns

|Return Type|Description|
|---|---|
|String|The ID.|


## <a name="com_fresvii_components_AppSteroidScore_java_lang_String_getIdOrDefault_"> getIdOrDefault </a>

```
public String getIdOrDefault()
```

Retrieves the ID, or a default value if the ID is null.

#### Returns

|Return Type|Description|
|---|---|
|String|The ID, or a default value|


## <a name="com_fresvii_components_AppSteroidScore_com_fresvii_components_AppSteroidLeaderboard_getLeaderboard_"> getLeaderboard </a>

```
public AppSteroidLeaderboard getLeaderboard()
```

Retrieves the leaderboard.

#### Returns

|Return Type|Description|
|---|---|
|AppSteroidLeaderboard|The leaderboard.|


## <a name="com_fresvii_components_AppSteroidScore_com_fresvii_components_AppSteroidLeaderboard_getLeaderboardOrDefault_"> getLeaderboardOrDefault </a>

```
public AppSteroidLeaderboard getLeaderboardOrDefault()
```

Retrieves the leaderboard, or a default value if the leaderboard is null.

#### Returns

|Return Type|Description|
|---|---|
|AppSteroidLeaderboard|The leaderboard, or a default value|


## <a name="com_fresvii_components_AppSteroidScore_com_fresvii_components_AppSteroidUser_getUser_"> getUser </a>

```
public AppSteroidUser getUser()
```

Retrieves the user.

#### Returns

|Return Type|Description|
|---|---|
|AppSteroidUser|The user.|


## <a name="com_fresvii_components_AppSteroidScore_com_fresvii_components_AppSteroidUser_getUserOrDefault_"> getUserOrDefault </a>

```
public AppSteroidUser getUserOrDefault()
```

Retrieves the user, or a default value if the user is null.

#### Returns

|Return Type|Description|
|---|---|
|AppSteroidUser|The user, or a default value|


## <a name="com_fresvii_components_AppSteroidScore_java_lang_Integer_getValue_"> getValue </a>

```
public Integer getValue()
```

Retrieves the value.

#### Returns

|Return Type|Description|
|---|---|
|Integer|The value.|


## <a name="com_fresvii_components_AppSteroidScore_int_getValueOrDefault_"> getValueOrDefault </a>

```
public int getValueOrDefault()
```

Retrieves the value, or a default value if the value is null.

#### Returns

|Return Type|Description|
|---|---|
|int|The value, or a default value|



---  

## <a name="com.fresvii.components.AppSteroidScore.ScoreType"> Enum AppSteroidScore.ScoreType </a>

```
public static final class AppSteroidScore.ScoreType extends Enum
```

**Hierarchy:**  

```
java.lang.Object  
    java.lang.Enum  
        com.fresvii.components.AppSteroidScore.ScoreType
```

**Description:**  
Score Type.








### Field Summary

|Field|Description|
|---|---|
|BEST_SCORE|Scores are submitted by best score.|
|RECENT_SCORE|Scores are submitted by recent score.|




---  

## <a name="com.fresvii.server.access.callbacks.leaderboard.GetLeaderboardCallback"> Interface GetLeaderboardCallback </a>

```
public interface GetLeaderboardCallback implements FailureCallback
```

**Hierarchy:**  

```
com.fresvii.server.access.callbacks.leaderboard.GetLeaderboardCallback
```

**Description:**  
Callback interface to handle [LeaderboardAccess.getLeaderboard()](#com_fresvii_server_access_LeaderboardAccess_void_getLeaderboard_String_GetLeaderboardCallback) results.

**Author:**  
Marcus Froeschl

**Version:**  
1.0




### Method Summary

|Method|Description|
|---|---|
|[public void onSuccess(AppSteroidLeaderboard leaderboard)](#com_fresvii_server_access_callbacks_leaderboard_GetLeaderboardCallback_void_onSuccess_AppSteroidLeaderboard)|Callback invoked when operation succeeds.|



### Method Detail
 


## <a name="com_fresvii_server_access_callbacks_leaderboard_GetLeaderboardCallback_void_onSuccess_AppSteroidLeaderboard"> onSuccess </a>

```
public void onSuccess(AppSteroidLeaderboard leaderboard)
```

Callback invoked when operation succeeds.

#### Parameters

|Parameter|Description|
|---|---|
|[AppSteroidLeaderboard](#com.fresvii.components.AppSteroidLeaderboard) leaderboard|The leaderboard that was retrieved|




---  

## <a name="com.fresvii.server.access.callbacks.leaderboard.GetLeaderboardsCallback"> Interface GetLeaderboardsCallback </a>

```
public interface GetLeaderboardsCallback implements FailureCallback
```

**Hierarchy:**  

```
com.fresvii.server.access.callbacks.leaderboard.GetLeaderboardsCallback
```

**Description:**  
Callback interface to handle [LeaderboardAccess.getLeaderboards()](#com_fresvii_server_access_LeaderboardAccess_void_getLeaderboards_GetLeaderboardsCallback) results.

**Author:**  
Marcus Froeschl

**Version:**  
1.0




### Method Summary

|Method|Description|
|---|---|
|[public void onSuccess(AppSteroidListMetaInfo metaInfo, List leaderboards)](#com_fresvii_server_access_callbacks_leaderboard_GetLeaderboardsCallback_void_onSuccess_AppSteroidListMetaInfo_List)|Callback invoked when operation succeeds.|



### Method Detail
 


## <a name="com_fresvii_server_access_callbacks_leaderboard_GetLeaderboardsCallback_void_onSuccess_AppSteroidListMetaInfo_List"> onSuccess </a>

```
public void onSuccess(AppSteroidListMetaInfo metaInfo,  
                      List leaderboards)
```

Callback invoked when operation succeeds.

#### Parameters

|Parameter|Description|
|---|---|
|[AppSteroidListMetaInfo](AndroidSDK.md#com.fresvii.components.AppSteroidListMetaInfo) metaInfo|List meta information.|
|List leaderboards|List of leaderboards retrieved.|




---  

## <a name="com.fresvii.server.access.callbacks.leaderboard.GetRankForUserCallback"> Interface GetRankForUserCallback </a>

```
public interface GetRankForUserCallback implements FailureCallback
```

**Hierarchy:**  

```
com.fresvii.server.access.callbacks.leaderboard.GetRankForUserCallback
```

**Description:**  
Callback interface to handle [LeaderboardAccess.getRankForUser()](#com_fresvii_server_access_LeaderboardAccess_void_getRankForUser_String_String_Date_Boolean_GetRankForUserCallback) results.

**Author:**  
Marcus Froeschl

**Version:**  
1.0




### Method Summary

|Method|Description|
|---|---|
|[public void onSuccess(AppSteroidRank rank)](#com_fresvii_server_access_callbacks_leaderboard_GetRankForUserCallback_void_onSuccess_AppSteroidRank)|Callback invoked when operation succeeds.|



### Method Detail
 


## <a name="com_fresvii_server_access_callbacks_leaderboard_GetRankForUserCallback_void_onSuccess_AppSteroidRank"> onSuccess </a>

```
public void onSuccess(AppSteroidRank rank)
```

Callback invoked when operation succeeds.

#### Parameters

|Parameter|Description|
|---|---|
|[AppSteroidRank](#com.fresvii.components.AppSteroidRank) rank|The rank that was retrieved|




---  

## <a name="com.fresvii.server.access.callbacks.leaderboard.GetRankingCallback"> Interface GetRankingCallback </a>

```
public interface GetRankingCallback implements FailureCallback
```

**Hierarchy:**  

```
com.fresvii.server.access.callbacks.leaderboard.GetRankingCallback
```

**Description:**  
Callback interface to handle [LeaderboardAccess.getRanking()](#com_fresvii_server_access_LeaderboardAccess_void_getRanking_String_Date_Boolean_GetRankingCallback) results.

**Author:**  
Marcus Froeschl

**Version:**  
1.0




### Method Summary

|Method|Description|
|---|---|
|[public void onSuccess(AppSteroidListMetaInfo metaInfo, List ranking)](#com_fresvii_server_access_callbacks_leaderboard_GetRankingCallback_void_onSuccess_AppSteroidListMetaInfo_List)|Callback invoked when operation succeeds.|



### Method Detail
 


## <a name="com_fresvii_server_access_callbacks_leaderboard_GetRankingCallback_void_onSuccess_AppSteroidListMetaInfo_List"> onSuccess </a>

```
public void onSuccess(AppSteroidListMetaInfo metaInfo,  
                      List ranking)
```

Callback invoked when operation succeeds.

#### Parameters

|Parameter|Description|
|---|---|
|[AppSteroidListMetaInfo](AndroidSDK.md#com.fresvii.components.AppSteroidListMetaInfo) metaInfo|List meta information.|
|List ranking|The ranking that was retrieved.|




---  

## <a name="com.fresvii.server.access.callbacks.leaderboard.GetScoreCallback"> Interface GetScoreCallback </a>

```
public interface GetScoreCallback implements FailureCallback
```

**Hierarchy:**  

```
com.fresvii.server.access.callbacks.leaderboard.GetScoreCallback
```

**Description:**  
Callback interface to handle [LeaderboardAccess.getScore()](#com_fresvii_server_access_LeaderboardAccess_void_getScore_String_String_GetScoreCallback) results.

**Author:**  
Marcus Froeschl

**Version:**  
1.0




### Method Summary

|Method|Description|
|---|---|
|[public void onSuccess(AppSteroidScore score)](#com_fresvii_server_access_callbacks_leaderboard_GetScoreCallback_void_onSuccess_AppSteroidScore)|Callback invoked when operation succeeds.|



### Method Detail
 


## <a name="com_fresvii_server_access_callbacks_leaderboard_GetScoreCallback_void_onSuccess_AppSteroidScore"> onSuccess </a>

```
public void onSuccess(AppSteroidScore score)
```

Callback invoked when operation succeeds.

#### Parameters

|Parameter|Description|
|---|---|
|[AppSteroidScore](#com.fresvii.components.AppSteroidScore) score|The score that was retrieved|




---  

## <a name="com.fresvii.server.access.callbacks.leaderboard.GetScoresForUserCallback"> Interface GetScoresForUserCallback </a>

```
public interface GetScoresForUserCallback implements FailureCallback
```

**Hierarchy:**  

```
com.fresvii.server.access.callbacks.leaderboard.GetScoresForUserCallback
```

**Description:**  
Callback interface to handle [LeaderboardAccess.getScoresForUser()](#com_fresvii_server_access_LeaderboardAccess_void_getScoresForUser_String_String_Date_AppSteroidScore_ScoreType_GetScoresForUserCallback) results.

**Author:**  
Marcus Froeschl

**Version:**  
1.0




### Method Summary

|Method|Description|
|---|---|
|[public void onSuccess(AppSteroidListMetaInfo metaInfo, List scores)](#com_fresvii_server_access_callbacks_leaderboard_GetScoresForUserCallback_void_onSuccess_AppSteroidListMetaInfo_List)|Callback invoked when operation succeeds.|



### Method Detail
 


## <a name="com_fresvii_server_access_callbacks_leaderboard_GetScoresForUserCallback_void_onSuccess_AppSteroidListMetaInfo_List"> onSuccess </a>

```
public void onSuccess(AppSteroidListMetaInfo metaInfo,  
                      List scores)
```

Callback invoked when operation succeeds.

#### Parameters

|Parameter|Description|
|---|---|
|[AppSteroidListMetaInfo](AndroidSDK.md#com.fresvii.components.AppSteroidListMetaInfo) metaInfo|List meta information.|
|List scores|List of scores retrieved.|




---  

## <a name="com.fresvii.server.access.callbacks.leaderboard.PostScoreCallback"> Interface PostScoreCallback </a>

```
public interface PostScoreCallback implements FailureCallback
```

**Hierarchy:**  

```
com.fresvii.server.access.callbacks.leaderboard.PostScoreCallback
```

**Description:**  
Callback interface to handle [LeaderboardAccess.postScore()](#com_fresvii_server_access_LeaderboardAccess_void_postScore_String_Integer_Date_PostScoreCallback) results.

**Author:**  
Marcus Froeschl

**Version:**  
1.0




### Method Summary

|Method|Description|
|---|---|
|[public void onSuccess(AppSteroidScore score)](#com_fresvii_server_access_callbacks_leaderboard_PostScoreCallback_void_onSuccess_AppSteroidScore)|Callback invoked when operation succeeds.|



### Method Detail
 


## <a name="com_fresvii_server_access_callbacks_leaderboard_PostScoreCallback_void_onSuccess_AppSteroidScore"> onSuccess </a>

```
public void onSuccess(AppSteroidScore score)
```

Callback invoked when operation succeeds.

#### Parameters

|Parameter|Description|
|---|---|
|[AppSteroidScore](#com.fresvii.components.AppSteroidScore) score|The score that was posted.|




---  

## <a name="com.fresvii.server.access.callbacks.leaderboard.DeleteScoreCallback"> Interface DeleteScoreCallback </a>

```
public interface DeleteScoreCallback implements FailureCallback
```

**Hierarchy:**  

```
com.fresvii.server.access.callbacks.leaderboard.DeleteScoreCallback
```

**Description:**  
Callback interface to handle [LeaderboardAccess.deleteScore()](#com_fresvii_server_access_LeaderboardAccess_void_deleteScore_String_String_DeleteScoreCallback) results.

**Author:**  
Marcus Froeschl

**Version:**  
1.0




### Method Summary

|Method|Description|
|---|---|
|[public void onSuccess()](#com_fresvii_server_access_callbacks_leaderboard_DeleteScoreCallback_void_onSuccess_)|Callback invoked when operation succeeds.|



### Method Detail
 


## <a name="com_fresvii_server_access_callbacks_leaderboard_DeleteScoreCallback_void_onSuccess_"> onSuccess </a>

```
public void onSuccess()
```

Callback invoked when operation succeeds.


