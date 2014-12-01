
# AppSteroid for Android

Last updated 2014-12-01

---

## Introduction

AppSteroid for Android is an integrated backend gaming service for Android.
With AppSteroid, you can easily incorporate various backend services refined to mobile games into your apps for free.


---  

## Document Sections

|Section|Description|
|---|---|
|[AppSteroid Account API](Account.md#Account.md)|AppSteroid Account API can be used to manage AppSteroid user accounts.|
|[AppSteroid Custom Message API](CustomMessage.md#CustomMessage.md)|AppSteroid Custom Message API can be used to send user-defined push notifications (APNS or GCM) to channels of users.|
|[AppSteroid Friend API](Friends.md#Friends.md)|AppSteroid Friend API can be used to manage AppSteroid Friend Relations.|
|[AppSteroid GcmClient API](GcmClient.md#GcmClient.md)|AppSteroid GcmClient API can be used to receive GCM Push notifications of events such as incoming text messages and many more.|
|[AppSteroid Group API](Group.md#Group.md)|AppSteroid Group API can be used to manage AppSteroid groups.|
|[AppSteroid Group Chat API](GroupChat.md#GroupChat.md)|AppSteroid Group Chat API can be used to send and retrieve several types of AppSteroid Chat messages.|
|[AppSteroid Key Value Storage API](KeyValueStorage.md#KeyValueStorage.md)|AppSteroid Key Value Storage API can be used to store arbitrary user data to the AppSteroid Server.|
|[AppSteroid Leaderboards API](Leaderboards.md#Leaderboards.md)|AppSteroid Leaderboards API can be used to manage AppSteroid leaderboards.|
|[AppSteroid Matchmaking API](Matchmaking.md#Matchmaking.md)|AppSteroid Matchmaking API can be used to initiate matchmaking.|
|[AppSteroid SNS Account API](SnsAccount.md#SnsAccount.md)|AppSteroid SNS Account API can be used to transfer user data between authorized devices.|
|[AppSteroid User API](User.md#User.md)|AppSteroid User API can be used to manage AppSteroid users.|
|[AppSteroid VoiceChat API](VoiceChat.md#VoiceChat.md)|AppSteroid VoiceChat API can be used to establish voice calls between AppSteroid Users.|



---  

## Classes

|Class|Description|
|---|---|
|[AppSteroid](#com.fresvii.AppSteroid)|Main entry point for AppSteroid.|
|[LeaderboardReferenceTime](#com.fresvii.LeaderboardReferenceTime)|Reference time that will be used when retrieving leaderboard ranking.|
|[AppSteroidActivity](#com.fresvii.gui.AppSteroidActivity)|Activity class used to display all Fresvii related content within specialized fragments.|
|[ShowTabsCollection](#com.fresvii.gui.ShowTabsCollection)|Class to indicate usage of the tab bar and to specify the tabs to show.|
|[ShowTabsCollection.TabGroup](#com.fresvii.gui.ShowTabsCollection.TabGroup)|Specifies different types of tabs that can be displayed in a tabbed FresviiActivity.|
|[AppSteroidComponent](#com.fresvii.components.AppSteroidComponent)|Represents a Fresvii Component.|
|[AppSteroidListMetaInfo](#com.fresvii.components.AppSteroidListMetaInfo)|Represents meta information on a Fresvii list object.|
|[FailureCallback](#com.fresvii.server.access.callbacks.FailureCallback)|Callback interface to handle operation errors.|
|[ManagedLog](#com.fresvii.helper.ManagedLog)|Implements logging with a log level restriction. |
|[ManagedLog.LogLevel](#com.fresvii.helper.ManagedLog.LogLevel)|Log Level.|
|[ManagedLog.LogListener](#com.fresvii.helper.ManagedLog.LogListener)|Application may implement this interface to manage the log output by itself.|



---  

## <a name="com.fresvii.AppSteroid"> Class AppSteroid </a>

```
public class AppSteroid extends Object
```

**Hierarchy:**  

```
java.lang.Object  
    com.fresvii.AppSteroid
```

**Description:**  
Main entry point for AppSteroid.

**Author:**  
matsushimakatsuhito

**Version:**  
1.0

**Since:**  
2014-02-14


### Method Summary

|Method|Description|
|---|---|
|[public static boolean isStarted()](#com_fresvii_AppSteroid_boolean_isStarted_)|Checks if the AppSteroid has been started.|
|[public static void setDefaultNotificationIcons(int smallIcon, Bitmap largeIcon)](#com_fresvii_AppSteroid_void_setDefaultNotificationIcons_int_Bitmap)|Default GCM notification icon settings.|
|[public static void setLeaderboardReferenceTimeForToday(LeaderboardReferenceTime leaderboardReferenceTimeForToday)](#com_fresvii_AppSteroid_void_setLeaderboardReferenceTimeForToday_LeaderboardReferenceTime)|Sets the LeaderboardReferenceTime for today's highscores.|
|[public static void setLeaderboardReferenceTimeForWeekly(LeaderboardReferenceTime leaderboardReferenceTimeForWeekly)](#com_fresvii_AppSteroid_void_setLeaderboardReferenceTimeForWeekly_LeaderboardReferenceTime)|Sets the LeaderboardReferenceTime for weekly highscores.|
|[public static void setMatchmakingPlayerCount(int playerCount)](#com_fresvii_AppSteroid_void_setMatchmakingPlayerCount_int)|Sets the number of players used for outgoing matchmaking requests.|
|[public static void setTimeout(int timeout)](#com_fresvii_AppSteroid_void_setTimeout_int)|Sets the timeout period for network communications.|
|[public static void start(Context context, String appIdentifier, String appSecretKey, String appName, String gcmSenderId)](#com_fresvii_AppSteroid_void_start_Context_String_String_String_String)|Used to start the AppSteroid.|
|[public static void start(Context context, String appIdentifier, String appSecretKey, String appName)](#com_fresvii_AppSteroid_void_start_Context_String_String_String)|Used to start the AppSteroid (deprecated).|
|[public static void start(Context applicationContext, String appIdentifier, String appSecretKey, String appName, String gcmSenderId, boolean automaticallyLogInUserIfUserExists, boolean automaticallySignUpNewUserIfNoUserExists)](#com_fresvii_AppSteroid_void_start_Context_String_String_String_String_boolean_boolean)|Used to start the AppSteroid.|



### Method Detail
 


## <a name="com_fresvii_AppSteroid_boolean_isStarted_"> isStarted </a>

```
public static boolean isStarted()
```

Checks if the AppSteroid has been started.

#### Returns

|Return Type|Description|
|---|---|
|boolean|true if the AppSteroid has been started, false otherwise.|


## <a name="com_fresvii_AppSteroid_void_setDefaultNotificationIcons_int_Bitmap"> setDefaultNotificationIcons </a>

```
public static void setDefaultNotificationIcons(int smallIcon,  
                                               Bitmap largeIcon)
```

Default GCM notification icon settings.  Please refer to <a href="http://developer.android.com/reference/android/app/Notification.Builder.html">Android official document</a> about small icon and large icon.

#### Parameters

|Parameter|Description|
|---|---|
|int smallIcon|Notification small icon.|
|Bitmap largeIcon|Notification large icon.|



## <a name="com_fresvii_AppSteroid_void_setLeaderboardReferenceTimeForToday_LeaderboardReferenceTime"> setLeaderboardReferenceTimeForToday </a>

```
public static void setLeaderboardReferenceTimeForToday(LeaderboardReferenceTime leaderboardReferenceTimeForToday)
```

Sets the LeaderboardReferenceTime for today's highscores.

#### Parameters

|Parameter|Description|
|---|---|
|[LeaderboardReferenceTime](#com.fresvii.LeaderboardReferenceTime) leaderboardReferenceTimeForToday|LeaderboardReferenceTime for today's highscores.|



## <a name="com_fresvii_AppSteroid_void_setLeaderboardReferenceTimeForWeekly_LeaderboardReferenceTime"> setLeaderboardReferenceTimeForWeekly </a>

```
public static void setLeaderboardReferenceTimeForWeekly(LeaderboardReferenceTime leaderboardReferenceTimeForWeekly)
```

Sets the LeaderboardReferenceTime for weekly highscores.

#### Parameters

|Parameter|Description|
|---|---|
|[LeaderboardReferenceTime](#com.fresvii.LeaderboardReferenceTime) leaderboardReferenceTimeForWeekly|LeaderboardReferenceTime for weekly highscores.|



## <a name="com_fresvii_AppSteroid_void_setMatchmakingPlayerCount_int"> setMatchmakingPlayerCount </a>

```
public static void setMatchmakingPlayerCount(int playerCount)
```

Sets the number of players used for outgoing matchmaking requests.

#### Parameters

|Parameter|Description|
|---|---|
|int playerCount|Player count for matchmaking.|



## <a name="com_fresvii_AppSteroid_void_setTimeout_int"> setTimeout </a>

```
public static void setTimeout(int timeout)
```

Sets the timeout period for network communications.  The default value is 10 seconds.

#### Parameters

|Parameter|Description|
|---|---|
|int timeout|Timeout (in seconds).|



## <a name="com_fresvii_AppSteroid_void_start_Context_String_String_String_String"> start </a>

```
public static void start(Context context,  
                         String appIdentifier,  
                         String appSecretKey,  
                         String appName,  
                         String gcmSenderId)
```

Used to start the AppSteroid.  When you use this method to start the AppSteroid,   a new AppSteroid user will be automatically signed up and logged in if there is no existing user yet.

#### Parameters

|Parameter|Description|
|---|---|
|Context context|Application context.|
|String appIdentifier|AppSteroid Application ID of your application.|
|String appSecretKey|Secret Key of your application.|
|String appName|Name of your application.|
|String gcmSenderId|Optional GCM Sender ID of your application.|



#### Example

    public class MainActivity extends Activity {
        @Override
        protected void onCreate(Bundle savedInstanceState) {
            // Application may call ManagedLog.initLog() before starting the AppSteroid,
            // e.g. for debugging purposes.
            ManagedLog.initLog(MY_APP_NAME, LogLevel.VERBOSE);
            
            // Any application must call AppSteroid.start() in order to work with the AppSteroid
            AppSteroid.start(
            	    getApplicationContext(),
            	    MY_APP_ID,
            	    MY_APP_SECRET,
            	    MY_APP_NAME,
            	    MY_GCM_SENDER_ID);
            
            ...
        }
    }




## <a name="com_fresvii_AppSteroid_void_start_Context_String_String_String"> start </a>

```
public static void start(Context context,  
                         String appIdentifier,  
                         String appSecretKey,  
                         String appName)
```

Used to start the AppSteroid (deprecated).  When you use this method to start the AppSteroid,   a new AppSteroid user will be automatically signed up and logged in if there is no existing user yet.  This method is DEPRECATED. Use [AppSteroid.start()](#com_fresvii_AppSteroid_void_start_Context_String_String_String_String) instead.

#### Parameters

|Parameter|Description|
|---|---|
|Context context|Application context.|
|String appIdentifier|AppSteroid Application ID of your application.|
|String appSecretKey|Secret Key of your application.|
|String appName|Name of your application.|



## <a name="com_fresvii_AppSteroid_void_start_Context_String_String_String_String_boolean_boolean"> start </a>

```
public static void start(Context applicationContext,  
                         String appIdentifier,  
                         String appSecretKey,  
                         String appName,  
                         String gcmSenderId,  
                         boolean automaticallyLogInUserIfUserExists,  
                         boolean automaticallySignUpNewUserIfNoUserExists)
```

Used to start the AppSteroid.  Using this method to start the AppSteroid allows you to specify if the AppSteroid  should automatically sign up and log in a new AppSteroid user if there is no existing user yet,  or if you wish to handle user management manually in your application instead.

#### Parameters

|Parameter|Description|
|---|---|
|Context applicationContext|Application context.|
|String appIdentifier|AppSteroid Application ID of your application.|
|String appSecretKey|Secret Key of your application.|
|String appName|Name of your application.|
|String gcmSenderId|Optional GCM Sender ID of your application.|
|boolean automaticallyLogInUserIfUserExists|Specify if the AppSteroid should automatically log in an existing AppSteroid user.|
|boolean automaticallySignUpNewUserIfNoUserExists|Specify if the AppSteroid should automatically sign up a new AppSteroid user if no user exists yet.|




---  

## <a name="com.fresvii.LeaderboardReferenceTime"> Class LeaderboardReferenceTime </a>

```
public class LeaderboardReferenceTime extends Object
```

**Hierarchy:**  

```
java.lang.Object  
    com.fresvii.LeaderboardReferenceTime
```

**Description:**  
Reference time that will be used when retrieving leaderboard ranking.

**Author:**  
Marcus Froeschl

**Version:**  
1.0

**Since:**  
2014-10-02


### Field Summary

|Field|Description|
|---|---|
|DEFAULT_HOUR|Default Hour. Value: 0|
|DEFAULT_MINUTE|Default Minute. Value: 0|
|DEFAULT_WEEKDAY|Default Weekday. Value: 1 (Sunday)|




---  

## <a name="com.fresvii.gui.AppSteroidActivity"> Class AppSteroidActivity </a>

```
public class AppSteroidActivity extends FragmentActivity implements ActionBar.TabListener
```

**Hierarchy:**  

```
java.lang.Object  
    android.content.Context  
        android.content.ContextWrapper  
            android.view.ContextThemeWrapper  
                android.app.Activity  
                    android.support.v4.app.FragmentActivity  
                        com.fresvii.gui.AppSteroidActivity
```

**Description:**  
Activity class used to display all Fresvii related content within specialized fragments.

**Author:**  
Matthias Kollmer

**Version:**  
1.0

**Since:**  
2014-09-15


### Method Summary

|Method|Description|
|---|---|
|[public static void startActivity(Context context, AppSteroidActivity.FresviiViewType fresviiViewType)](#com_fresvii_gui_AppSteroidActivity_void_startActivity_Context_AppSteroidActivity_FresviiViewType)|Starts an activity showing a specific FresviiViewType.|
|[public static void startAndShowChatList(Context context)](#com_fresvii_gui_AppSteroidActivity_void_startAndShowChatList_Context)|Starts an activity showing the current user's Chat List.|
|[public static void startAndShowEditProfile(Context context)](#com_fresvii_gui_AppSteroidActivity_void_startAndShowEditProfile_Context)|Starts an activity showing the user's EditProfile.|
|[public static void startAndShowForum(Context context)](#com_fresvii_gui_AppSteroidActivity_void_startAndShowForum_Context)|Starts an activity showing the Forum.|
|[public static void startAndShowForumThread(Context context, String threadId)](#com_fresvii_gui_AppSteroidActivity_void_startAndShowForumThread_Context_String)|Starts an activity showing a specific Forum Thread.|
|[public static void startAndShowGroupChat(Context context, String groupId)](#com_fresvii_gui_AppSteroidActivity_void_startAndShowGroupChat_Context_String)|Starts an activity showing a specific group chat.|
|[public static void startAndShowLeaderboard(Context context, String leaderboardId)](#com_fresvii_gui_AppSteroidActivity_void_startAndShowLeaderboard_Context_String)|Starts an activity showing a specific Fresvii leaderboard.|
|[public static void startAndShowMatchmaking(Context context)](#com_fresvii_gui_AppSteroidActivity_void_startAndShowMatchmaking_Context)|Starts an activity showing the Matchmaking.|
|[public static void startAndShowUserProfile(Context context, String userId)](#com_fresvii_gui_AppSteroidActivity_void_startAndShowUserProfile_Context_String)|Starts an activity showing a specific user's profile.|
|[public static void startTabbedActivity(Context context, ShowTabsCollection tabs)](#com_fresvii_gui_AppSteroidActivity_void_startTabbedActivity_Context_ShowTabsCollection)|Starts a tabbed activity showing the specified tabs.|



### Method Detail
 


## <a name="com_fresvii_gui_AppSteroidActivity_void_startActivity_Context_AppSteroidActivity_FresviiViewType"> startActivity </a>

```
public static void startActivity(Context context,  
                                 AppSteroidActivity.FresviiViewType fresviiViewType)
```

Starts an activity showing a specific FresviiViewType.  This method is deprecated. Use specialized methods such as [AppSteroidActivity.startAndShowForum()](#com_fresvii_gui_AppSteroidActivity_void_startAndShowForum_Context) instead.

#### Parameters

|Parameter|Description|
|---|---|
|Context context|Context used to start the activity.|
|AppSteroidActivity.FresviiViewType fresviiViewType|The view to be displayed in the activity.|



## <a name="com_fresvii_gui_AppSteroidActivity_void_startAndShowChatList_Context"> startAndShowChatList </a>

```
public static void startAndShowChatList(Context context)
```

Starts an activity showing the current user's Chat List.

#### Parameters

|Parameter|Description|
|---|---|
|Context context|Context used to start the activity.|



## <a name="com_fresvii_gui_AppSteroidActivity_void_startAndShowEditProfile_Context"> startAndShowEditProfile </a>

```
public static void startAndShowEditProfile(Context context)
```

Starts an activity showing the user's EditProfile.

#### Parameters

|Parameter|Description|
|---|---|
|Context context|Context used to start the activity.|



## <a name="com_fresvii_gui_AppSteroidActivity_void_startAndShowForum_Context"> startAndShowForum </a>

```
public static void startAndShowForum(Context context)
```

Starts an activity showing the Forum.

#### Parameters

|Parameter|Description|
|---|---|
|Context context|Context used to start the activity.|



## <a name="com_fresvii_gui_AppSteroidActivity_void_startAndShowForumThread_Context_String"> startAndShowForumThread </a>

```
public static void startAndShowForumThread(Context context,  
                                           String threadId)
```

Starts an activity showing a specific Forum Thread.

#### Parameters

|Parameter|Description|
|---|---|
|Context context|Context used to start the activity.|
|String threadId|The id of a specific Forum Thread to show.|



## <a name="com_fresvii_gui_AppSteroidActivity_void_startAndShowGroupChat_Context_String"> startAndShowGroupChat </a>

```
public static void startAndShowGroupChat(Context context,  
                                         String groupId)
```

Starts an activity showing a specific group chat.

#### Parameters

|Parameter|Description|
|---|---|
|Context context|Context used to start the activity.|
|String groupId|The id of a specific group to show.|



## <a name="com_fresvii_gui_AppSteroidActivity_void_startAndShowLeaderboard_Context_String"> startAndShowLeaderboard </a>

```
public static void startAndShowLeaderboard(Context context,  
                                           String leaderboardId)
```

Starts an activity showing a specific Fresvii leaderboard.

#### Parameters

|Parameter|Description|
|---|---|
|Context context|Context used to start the activity.|
|String leaderboardId|[optional] The id of a specific leaderboard to show. If not given the first leaderboard|



## <a name="com_fresvii_gui_AppSteroidActivity_void_startAndShowMatchmaking_Context"> startAndShowMatchmaking </a>

```
public static void startAndShowMatchmaking(Context context)
```

Starts an activity showing the Matchmaking.

#### Parameters

|Parameter|Description|
|---|---|
|Context context|Context used to start the activity.|



## <a name="com_fresvii_gui_AppSteroidActivity_void_startAndShowUserProfile_Context_String"> startAndShowUserProfile </a>

```
public static void startAndShowUserProfile(Context context,  
                                           String userId)
```

Starts an activity showing a specific user's profile.

#### Parameters

|Parameter|Description|
|---|---|
|Context context|Context used to start the activity.|
|String userId|The id of a specific user to show.|



## <a name="com_fresvii_gui_AppSteroidActivity_void_startTabbedActivity_Context_ShowTabsCollection"> startTabbedActivity </a>

```
public static void startTabbedActivity(Context context,  
                                       ShowTabsCollection tabs)
```

Starts a tabbed activity showing the specified tabs.

#### Parameters

|Parameter|Description|
|---|---|
|Context context|Context used to start the activity.|
|[ShowTabsCollection](#com.fresvii.gui.ShowTabsCollection) tabs|The tabs to be displayed in the activity. If omitted or empty, all tab groups will be displayed.|



#### Example

Open both the Forum View and the User's Profile View in a Tabbed Activity:

    AppSteroidActivity.startTabbedActivity(
        getApplicationContext(), 
        new ShowTabsCollection(
            TabGroup.FORUM, 
            TabGroup.PROFILE));







---  

## <a name="com.fresvii.gui.ShowTabsCollection"> Class ShowTabsCollection </a>

```
public class ShowTabsCollection extends Object
```

**Hierarchy:**  

```
java.lang.Object  
    com.fresvii.gui.ShowTabsCollection
```

**Description:**  
Class to indicate usage of the tab bar and to specify the tabs to show.

**Author:**  
Matthias Kollmer

**Version:**  
1.0

**Since:**  
2014-09-15



---  

## <a name="com.fresvii.gui.ShowTabsCollection.TabGroup"> Enum ShowTabsCollection.TabGroup </a>

```
public static final class ShowTabsCollection.TabGroup extends Enum
```

**Hierarchy:**  

```
java.lang.Object  
    java.lang.Enum  
        com.fresvii.gui.ShowTabsCollection.TabGroup
```

**Description:**  
Specifies different types of tabs that can be displayed in a tabbed FresviiActivity.








### Field Summary

|Field|Description|
|---|---|
|CHAT|Chat Tab.|
|FORUM|Forum Tab.|
|LEADERBOARD|Leaderboard Tab.|
|MATCHMAKING|Matchmaking Tab.|
|PROFILE|Profile Tab.|




---  

## <a name="com.fresvii.components.AppSteroidComponent"> Class AppSteroidComponent </a>

```
public abstract class AppSteroidComponent extends Object
```

**Hierarchy:**  

```
java.lang.Object  
    com.fresvii.components.AppSteroidComponent
```

**Description:**  
Represents a Fresvii Component.

**Author:**  
Matthias Kollmer

**Version:**  
1.0

**Since:**  
2014-08-19


### Method Summary

|Method|Description|
|---|---|
|[public boolean hasSameId(String id)](#com_fresvii_components_AppSteroidComponent_boolean_hasSameId_String)|Checks if this Fresvii component has the same Fresvii ID.|



### Method Detail
 


## <a name="com_fresvii_components_AppSteroidComponent_boolean_hasSameId_String"> hasSameId </a>

```
public boolean hasSameId(String id)
```

Checks if this Fresvii component has the same Fresvii ID.

#### Parameters

|Parameter|Description|
|---|---|
|String id|Fresvii ID to compare.|


#### Returns

|Return Type|Description|
|---|---|
|boolean|true if the give ID matches the component's ID, false otherwise.|



---  

## <a name="com.fresvii.components.AppSteroidListMetaInfo"> Class AppSteroidListMetaInfo </a>

```
public class AppSteroidListMetaInfo extends Object
```

**Hierarchy:**  

```
java.lang.Object  
    com.fresvii.components.AppSteroidListMetaInfo
```

**Description:**  
Represents meta information on a Fresvii list object.

**Author:**  
Marcus Froeschl

**Version:**  
1.0

**Since:**  
2014-08-07


### Method Summary

|Method|Description|
|---|---|
|[public Integer getCurrentPage()](#com_fresvii_components_AppSteroidListMetaInfo_java_lang_Integer_getCurrentPage_)|Retrieves the list's currentPage.|
|[public int getCurrentPageOrDefault()](#com_fresvii_components_AppSteroidListMetaInfo_int_getCurrentPageOrDefault_)|Retrieves the list's currentPage, or a default value if the list's currentPage is null.|
|[public Integer getNextPage()](#com_fresvii_components_AppSteroidListMetaInfo_java_lang_Integer_getNextPage_)|Retrieves the list's nextPage.|
|[public int getNextPageOrDefault()](#com_fresvii_components_AppSteroidListMetaInfo_int_getNextPageOrDefault_)|Retrieves the list's nextPage, or a default value if the list's nextPage is null.|
|[public Integer getPerPage()](#com_fresvii_components_AppSteroidListMetaInfo_java_lang_Integer_getPerPage_)|Retrieves the list's perPage.|
|[public int getPerPageOrDefault()](#com_fresvii_components_AppSteroidListMetaInfo_int_getPerPageOrDefault_)|Retrieves the list's perPage, or a default value if the list's perPage is null.|
|[public Integer getTotalCount()](#com_fresvii_components_AppSteroidListMetaInfo_java_lang_Integer_getTotalCount_)|Retrieves the list's totalCount.|
|[public int getTotalCountOrDefault()](#com_fresvii_components_AppSteroidListMetaInfo_int_getTotalCountOrDefault_)|Retrieves the list's totalCount, or a default value if the list's totalCount is null.|
|[public Integer getTotalPages()](#com_fresvii_components_AppSteroidListMetaInfo_java_lang_Integer_getTotalPages_)|Retrieves the list's totalPages.|
|[public int getTotalPagesOrDefault()](#com_fresvii_components_AppSteroidListMetaInfo_int_getTotalPagesOrDefault_)|Retrieves the list's totalPages, or a default value if the list's totalPages is null.|



### Method Detail
 


## <a name="com_fresvii_components_AppSteroidListMetaInfo_java_lang_Integer_getCurrentPage_"> getCurrentPage </a>

```
public Integer getCurrentPage()
```

Retrieves the list's currentPage.

#### Returns

|Return Type|Description|
|---|---|
|Integer|The list's currentPage.|


## <a name="com_fresvii_components_AppSteroidListMetaInfo_int_getCurrentPageOrDefault_"> getCurrentPageOrDefault </a>

```
public int getCurrentPageOrDefault()
```

Retrieves the list's currentPage, or a default value if the list's currentPage is null.

#### Returns

|Return Type|Description|
|---|---|
|int|The list's currentPage, or a default value|


## <a name="com_fresvii_components_AppSteroidListMetaInfo_java_lang_Integer_getNextPage_"> getNextPage </a>

```
public Integer getNextPage()
```

Retrieves the list's nextPage.

#### Returns

|Return Type|Description|
|---|---|
|Integer|The list's nextPage.|


## <a name="com_fresvii_components_AppSteroidListMetaInfo_int_getNextPageOrDefault_"> getNextPageOrDefault </a>

```
public int getNextPageOrDefault()
```

Retrieves the list's nextPage, or a default value if the list's nextPage is null.

#### Returns

|Return Type|Description|
|---|---|
|int|The list's nextPage, or a default value|


## <a name="com_fresvii_components_AppSteroidListMetaInfo_java_lang_Integer_getPerPage_"> getPerPage </a>

```
public Integer getPerPage()
```

Retrieves the list's perPage.

#### Returns

|Return Type|Description|
|---|---|
|Integer|The list's perPage.|


## <a name="com_fresvii_components_AppSteroidListMetaInfo_int_getPerPageOrDefault_"> getPerPageOrDefault </a>

```
public int getPerPageOrDefault()
```

Retrieves the list's perPage, or a default value if the list's perPage is null.

#### Returns

|Return Type|Description|
|---|---|
|int|The list's perPage, or a default value|


## <a name="com_fresvii_components_AppSteroidListMetaInfo_java_lang_Integer_getTotalCount_"> getTotalCount </a>

```
public Integer getTotalCount()
```

Retrieves the list's totalCount.

#### Returns

|Return Type|Description|
|---|---|
|Integer|The list's totalCount.|


## <a name="com_fresvii_components_AppSteroidListMetaInfo_int_getTotalCountOrDefault_"> getTotalCountOrDefault </a>

```
public int getTotalCountOrDefault()
```

Retrieves the list's totalCount, or a default value if the list's totalCount is null.

#### Returns

|Return Type|Description|
|---|---|
|int|The list's totalCount, or a default value|


## <a name="com_fresvii_components_AppSteroidListMetaInfo_java_lang_Integer_getTotalPages_"> getTotalPages </a>

```
public Integer getTotalPages()
```

Retrieves the list's totalPages.

#### Returns

|Return Type|Description|
|---|---|
|Integer|The list's totalPages.|


## <a name="com_fresvii_components_AppSteroidListMetaInfo_int_getTotalPagesOrDefault_"> getTotalPagesOrDefault </a>

```
public int getTotalPagesOrDefault()
```

Retrieves the list's totalPages, or a default value if the list's totalPages is null.

#### Returns

|Return Type|Description|
|---|---|
|int|The list's totalPages, or a default value|



---  

## <a name="com.fresvii.server.access.callbacks.FailureCallback"> Interface FailureCallback </a>

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




### Method Summary

|Method|Description|
|---|---|
|[public void onFailure(Throwable error)](#com_fresvii_server_access_callbacks_FailureCallback_void_onFailure_Throwable)|Callback invoked when the associated operation ended with an error.|



### Method Detail
 


## <a name="com_fresvii_server_access_callbacks_FailureCallback_void_onFailure_Throwable"> onFailure </a>

```
public void onFailure(Throwable error)
```

Callback invoked when the associated operation ended with an error.

#### Parameters

|Parameter|Description|
|---|---|
|Throwable error|Error object.|




---  

## <a name="com.fresvii.helper.ManagedLog"> Class ManagedLog </a>

```
public class ManagedLog extends Object
```

**Hierarchy:**  

```
java.lang.Object  
    com.fresvii.helper.ManagedLog
```

**Description:**  
Implements logging with a log level restriction.   Application may change maximum log level, and optionally implement a [LogListener](#com.fresvii.helper.ManagedLog.LogListener).

**Author:**  
Matthias Kollmer, Marcus Froeschl

**Version:**  
1.0

**Since:**  
2014-05-26


### Field Summary

|Field|Description|
|---|---|
|DEFAULT_MAXIMUM_LOG_LEVEL|The default maximum log level (WARNING)|
|DEFAULT_MAXIMUM_LOG_LISTENER_LEVEL|The default maximum log level for the [LogListener](#com.fresvii.helper.ManagedLog.LogListener) (NONE).|



### Method Summary

|Method|Description|
|---|---|
|[public static ManagedLog.LogLevel getMaximumLogLevel()](#com_fresvii_helper_ManagedLog_com_fresvii_helper_ManagedLog_LogLevel_getMaximumLogLevel_)|Retrieves the maximum log level.|
|[public static ManagedLog.LogLevel getMaximumLogListenerLogLevel()](#com_fresvii_helper_ManagedLog_com_fresvii_helper_ManagedLog_LogLevel_getMaximumLogListenerLogLevel_)|Retrieves the maximum log level for the [LogListener](#com.fresvii.helper.ManagedLog.LogListener).|
|[public static void initLog(String logTag, ManagedLog.LogLevel maximumLogLevel)](#com_fresvii_helper_ManagedLog_void_initLog_String_ManagedLog_LogLevel)|Initializes the log.|
|[public static void setLogListener(ManagedLog.LogListener logListener)](#com_fresvii_helper_ManagedLog_void_setLogListener_ManagedLog_LogListener)|Sets the [ManagedLog.LogListener](#com.fresvii.helper.ManagedLog.LogListener) that will receive future log output from this application.|
|[public static void setLogListener(ManagedLog.LogListener logListener, ManagedLog.LogLevel maximumLogLevel)](#com_fresvii_helper_ManagedLog_void_setLogListener_ManagedLog_LogListener_ManagedLog_LogLevel)|Sets the [ManagedLog.LogListener](#com.fresvii.helper.ManagedLog.LogListener) that will receive future log output from this application.|



### Method Detail
 


## <a name="com_fresvii_helper_ManagedLog_com_fresvii_helper_ManagedLog_LogLevel_getMaximumLogLevel_"> getMaximumLogLevel </a>

```
public static ManagedLog.LogLevel getMaximumLogLevel()
```

Retrieves the maximum log level.

#### Returns

|Return Type|Description|
|---|---|
|ManagedLog.LogLevel|The maximum log level.|


## <a name="com_fresvii_helper_ManagedLog_com_fresvii_helper_ManagedLog_LogLevel_getMaximumLogListenerLogLevel_"> getMaximumLogListenerLogLevel </a>

```
public static ManagedLog.LogLevel getMaximumLogListenerLogLevel()
```

Retrieves the maximum log level for the [LogListener](#com.fresvii.helper.ManagedLog.LogListener).

#### Returns

|Return Type|Description|
|---|---|
|ManagedLog.LogLevel|The maximum log level for the {@link LogListener LogListener}.|


## <a name="com_fresvii_helper_ManagedLog_void_initLog_String_ManagedLog_LogLevel"> initLog </a>

```
public static void initLog(String logTag,  
                           ManagedLog.LogLevel maximumLogLevel)
```

Initializes the log.  The application may call this method before calling [AppSteroid.start()](#com_fresvii_AppSteroid_void_start_Context_String_String_String_String)  to apply log settings different from the default values, e.g. for the purpose of debugging.

#### Parameters

|Parameter|Description|
|---|---|
|String logTag|The log tag that will be used for logging.|
|[ManagedLog.LogLevel](#com.fresvii.helper.ManagedLog.LogLevel) maximumLogLevel|The maximum [LogLevel](#com.fresvii.helper.ManagedLog.LogLevel). Any log above this log level will not be printed.|



#### Example

    public class MainActivity extends Activity {
        @Override
        protected void onCreate(Bundle savedInstanceState) {
            // Application may call ManagedLog.initLog() before starting the AppSteroid,
            // e.g. for debugging purposes.
            ManagedLog.initLog(MY_APP_NAME, LogLevel.VERBOSE);
            
            // Any application must call AppSteroid.start() in order to work with the AppSteroid
            AppSteroid.start(
            	    getApplicationContext(),
            	    MY_APP_ID,
            	    MY_APP_SECRET,
            	    MY_APP_NAME,
            	    MY_GCM_SENDER_ID);
            
            ...
        }
    }




## <a name="com_fresvii_helper_ManagedLog_void_setLogListener_ManagedLog_LogListener"> setLogListener </a>

```
public static void setLogListener(ManagedLog.LogListener logListener)
```

Sets the [ManagedLog.LogListener](#com.fresvii.helper.ManagedLog.LogListener) that will receive future log output from this application.  Will use the same maximum LogLevel as the default logging mechanism.  Removes the existing log listener if null is passed.  It is only safe to call this method before before calling [AppSteroid.start()](#com_fresvii_AppSteroid_void_start_Context_String_String_String_String).

#### Parameters

|Parameter|Description|
|---|---|
|[ManagedLog.LogListener](#com.fresvii.helper.ManagedLog.LogListener) logListener|The log listener.|



## <a name="com_fresvii_helper_ManagedLog_void_setLogListener_ManagedLog_LogListener_ManagedLog_LogLevel"> setLogListener </a>

```
public static void setLogListener(ManagedLog.LogListener logListener,  
                                  ManagedLog.LogLevel maximumLogLevel)
```

Sets the [ManagedLog.LogListener](#com.fresvii.helper.ManagedLog.LogListener) that will receive future log output from this application.  Removes the existing log listener if null is passed.  It is only safe to call this method before before calling [AppSteroid.start()](#com_fresvii_AppSteroid_void_start_Context_String_String_String_String).

#### Parameters

|Parameter|Description|
|---|---|
|[ManagedLog.LogListener](#com.fresvii.helper.ManagedLog.LogListener) logListener|The log listener.|
|[ManagedLog.LogLevel](#com.fresvii.helper.ManagedLog.LogLevel) maximumLogLevel|Maximum [LogLevel](#com.fresvii.helper.ManagedLog.LogLevel) for the log listener.|



#### Example

```
// Application may implement the LogListener interface
public class MainActivity extends Activity implements LogListener {
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        // Application may call ManagedLog.initLog(), e.g. to disable the default logging.
        ManagedLog.initLog(MY_APP_NAME, LogLevel.NONE);

        // Application may wish to register its own LogListener before strating the AppSteroid.
        ManagedLog.setLogListener(this, LogLevel.VERBOSE);
        
        // Any application must call AppSteroid.start() in order to work with the AppSteroid
        AppSteroid.start(
        	    getApplicationContext(),
        	    MY_APP_ID,
        	    MY_APP_SECRET,
        	    MY_APP_NAME,
        	    MY_GCM_SENDER_ID);
        
        ...
    }

    @Override
    public void onLogMessage(final LogLevel logLevel, final String module, final String message) {
    	// Application may implement its own logging routine here

    	...
    }
}
```





---  

## <a name="com.fresvii.helper.ManagedLog.LogLevel"> Enum ManagedLog.LogLevel </a>

```
public static final class ManagedLog.LogLevel extends Enum
```

**Hierarchy:**  

```
java.lang.Object  
    java.lang.Enum  
        com.fresvii.helper.ManagedLog.LogLevel
```

**Description:**  
Log Level.








### Field Summary

|Field|Description|
|---|---|
|CRITICAL_ERROR|Critical error.|
|DEBUG|Debug.|
|ERROR|Error.|
|INFO|Info.|
|NONE|No log output.|
|VERBOSE|Verbose.|
|WARNING|Warning.|




---  

## <a name="com.fresvii.helper.ManagedLog.LogListener"> Interface ManagedLog.LogListener </a>

```
public static interface ManagedLog.LogListener
```

**Hierarchy:**  

```
com.fresvii.helper.ManagedLog.LogListener
```

**Description:**  
Application may implement this interface to manage the log output by itself.








### Method Summary

|Method|Description|
|---|---|
|[public void onLogMessage(ManagedLog.LogLevel logLevel, String module, String message)](#com_fresvii_helper_ManagedLog_LogListener_void_onLogMessage_ManagedLog_LogLevel_String_String)|Invoked when a log message should be logged.|



### Method Detail
 


## <a name="com_fresvii_helper_ManagedLog_LogListener_void_onLogMessage_ManagedLog_LogLevel_String_String"> onLogMessage </a>

```
public void onLogMessage(ManagedLog.LogLevel logLevel,  
                         String module,  
                         String message)
```

Invoked when a log message should be logged.

#### Parameters

|Parameter|Description|
|---|---|
|[ManagedLog.LogLevel](#com.fresvii.helper.ManagedLog.LogLevel) logLevel|[LogLevel](#com.fresvii.helper.ManagedLog.LogLevel) of the message.|
|String module|Module where the log message originated.|
|String message|The log message.|



