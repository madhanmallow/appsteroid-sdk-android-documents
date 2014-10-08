
# AppSteroid for Android

## Setting up your application's Manifest

Last updated on 2014.09.19

---

AppSteroid requires several permissions, services and activities to be defined in your application's Manifest. You can either set those permissions with the Manifest Merger, or manually edit your application's manifest.


### <a name="ManifestMerger"> 1. Use the Manifest Merger </a> 

The quickest way to set up the permissions, services and activities required by AppSteroid is to enable the Manifest Merger:

1.1. Add the following line to your *"project.properties"* file within your own project:

    manifestmerger.enabled=true

This will merge the manifest from the library project into your own manifest. Only if you wish to set up Android Backup Service, you will still have to edit your Manifest as described in section [2.4. Set up Android Backup Service](#AndroidBackupService).

Also, if you wish more fine-grained control over the Manifest, read on below.


### 2. Manually prepare your application's Manifest

#### 2.1. Define AppSteroid Activities in the Manifest

The AppSteroid comes with a set of default UIs for features such as Forum, Chat, Leaderbaords... E.g., this is how the default Forum UI looks like:

![](../Images/ForumThread.png)

If you wish to use those default UIs (and normally you do), you will have to define the AppSteroid Activity in your application's Manifest like this:

        <activity
                android:name="com.fresvii.gui.AppSteroidActivity" 
                android:theme="@style/AppSteroidTheme" />

If you use the Manifest Merger, the above activities will be automatically defined and you can skip this step.


#### 2.2. Define AppSteroid Receivers and Services in the Manifest

If you wish to receive GCM Notifications, such as...

- Forum Updates
- Chat messages
- Matchmaking invitations
- VoiceChat invitations
- etc.

...you will have to define the following receivers and services in your application's Manifest:

        <!-- This receiver is required by the AppSteroid to receive GCM Notifications -->
        <receiver
                android:name="com.fresvii.gcm.GcmBroadcastReceiver"
                android:permission="com.google.android.c2dm.permission.SEND" >
            <intent-filter>
                <action android:name="com.google.android.c2dm.intent.RECEIVE" />
                <category android:name="com.example.gcm" />
            </intent-filter>
        </receiver>
        
        <!-- This receiver is required by the AppSteroid to react to user actions, such as accepting VoiceChat etc. -->
        <receiver
                android:permission="com.fresvii.gcm.NotificationActionReceiver.permission.ACTION_RECEIVER"
                android:name="com.fresvii.gcm.NotificationActionReceiver" >
            <intent-filter>
                <action android:name="com.fresvii.gcm.NotificationActionReceiver.intent.ACTION_ACCEPT_FRIEND_REQUEST" />
                <action android:name="com.fresvii.gcm.NotificationActionReceiver.intent.ACTION_HIDE_FRIEND_REQUEST" />
                <action android:name="com.fresvii.gcm.NotificationActionReceiver.intent.ACTION_ACCEPT_VOICE_CHAT" />
                <action android:name="com.fresvii.gcm.NotificationActionReceiver.intent.ACTION_CLEAR_NOTIFICATION" />
                <action android:name="com.fresvii.gcm.NotificationActionReceiver.intent.ACTION_ACCEPT_GAME_INVITATION" />
            </intent-filter>
        </receiver>
        
        <!-- This service is required by the AppSteroid to receive GCM Notifications -->
        <service android:name="com.fresvii.gcm.GcmIntentService" />

Unless you have a very specific reason not to, in general you should set up your application to be able to receive GCM Notifications, as they are critical to AppSteroid core features. A lot of AppSteroid's features directly or indirectly depend on GCM Notifications. While AppSteroid will still run without GCM Notifications, the user experience will be severely diminished.

If you use the Manifest Merger, the above receivers and services will be automatically defined and you can skip this step.


#### 2.3. Define AppSteroid Permissions in the Manifest

To make full use of all the features of the AppSteroid, you will have to define the following permissions in your application's manifest:

        <!-- Define permissions for AppSteroid -->
        <permission
            android:name="com.fresvii.gcm.NotificationActionReceiver.permission.ACTION_RECEIVER"
            android:protectionLevel="signature" />
        <permission
            android:name="com.example.gcm.permission.C2D_MESSAGE"
            android:protectionLevel="signature" />
        
        <!-- Permissions required by the AppSteroid -->
        <uses-permission android:name="android.permission.INTERNET"/>
        <uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE" />
        <uses-permission android:name="android.permission.RECORD_AUDIO" />
        <uses-permission android:name="android.permission.MODIFY_AUDIO_SETTINGS" />
        <uses-permission android:name="android.permission.GET_ACCOUNTS" />
        <uses-permission android:name="android.permission.WAKE_LOCK" />   
        <uses-permission android:name="com.google.android.c2dm.permission.RECEIVE" />
        <uses-permission android:name="com.example.gcm.permission.C2D_MESSAGE" />
        <uses-permission android:name="com.example.gcm.c2dm.permission.RECEIVE" />
        <uses-permission android:name="com.fresvii.gcm.NotificationActionReceiver.permission.ACTION_RECEIVER" />

Please see section [3. Overview of Permissions](#OverviewOfPermissions) for a detailed explanation on each permission.

If you use the Manifest Merger, all of the above receivers and services will be automatically defined and you can skip this step.


#### <a name="AndroidBackupService"> 2.4. Set up Android Backup Service </a> 

AppSteroid offers a BackupAgent that can optionally be used to backup the user's data to the [Android Backup Service](http://developer.android.com/google/backup/index.html). This will help the user to keep his Fresvii User ID even when re-installing the application, or migrating to a different Android device. 


##### 2.4.1. Register your application for Android backup Service
If you wish to use the AppSteroidBackupAgent and the Android Backup Service, first you will have to [register](http://developer.android.com/google/backup/signup.html) your application for the Android Backup Service. You will receive a Backup API key.


##### 2.4.2. Define AppSteroidBackupAgent and your Backup API Key in the Manifest.

    <application
            android:allowBackup="true"
            android:backupAgent="com.fresvii.helper.AppSteroidBackupAgent"
            android:restoreAnyVersion="true"
            android:icon="@drawable/your_app_icon"
            android:label="@string/your_app_name"
            android:theme="@style/AppTheme" >
            
        <meta-data android:name="com.google.android.backup.api_key"
            android:value="YOUR_BACKUP_API_KEY" />

If you wish to use the Android backup Service, you will have to edit your Manifest as described above. Unfortunately, the Manifest Merger cannot do this for you, since we cannot know your Backup API Key. If you do not wish to use the Android Backup Service, you can skip this section.


### <a name="OverviewOfPermissions"> 3. Overview of Permissions </a>

|Permission|Required for|Description|
|---|---|---|
|android.permission.INTERNET|everything|Basic Internet Access. This permission is mandatory. Without this permission, AppSteroid will not work at all.|
|android.permission.WRITE_EXTERNAL_STORAGE|Forum, Chat|When you take a picture with the camera to be shared via AppSteroid's Forum or Chat, the AppSteroid stores this picture in a temporary file. For this purpose, it requires access to the external storage. If you do not wish to take pictures with the camera, this permission may be removed.|
|android.permission.RECORD_AUDIO|VoiceChat|VoiceChat requires this permission to access the device's microphone. If you do not wish to use the VoiceChat feature, this permission may be removed.|
|android.permission.MODIFY_AUDIO_SETTINGS|VoiceChat|VoiceChat requires this permission to switch the device's speaker to inner or outer speaker, respectively. If you do not wish to use the VoiceChat feature, this permission may be removed.|
|android.permission.GET_ACCOUNTS|GCM Notifications (Used by Forum, Chat, Matchmaking, VoiceChat...)|GCM Notifications require this permission to work. If you do not wish to use GCM Notifications, this permission may be removed. Be advised that removing GCM Notifications may severely diminish the user experience.|
|com.google.android.c2dm.permission.RECEIVE|GCM Notifications (Used by Forum, Chat, Matchmaking, VoiceChat...)|GCM Notifications require this permission to work. If you do not wish to use GCM Notifications, this permission may be removed. Be advised that removing GCM Notifications may severely diminish the user experience.|
|com.example.gcm.permission.C2D_MESSAGE|GCM Notifications (Used by Forum, Chat, Matchmaking, VoiceChat...)|GCM Notifications require this permission to work. If you do not wish to use GCM Notifications, this permission may be removed. Be advised that removing GCM Notifications may severely diminish the user experience.|
|com.example.gcm.c2dm.permission.RECEIVE|GCM Notifications (Used by Forum, Chat, Matchmaking, VoiceChat...)|GCM Notifications require this permission to work. If you do not wish to use GCM Notifications, this permission may be removed. Be advised that removing GCM Notifications may severely diminish the user experience.|
|com.fresvii.gcm.NotificationActionReceiver.permission.ACTION_RECEIVER|GCM Notifications (Used by Forum, Chat, Matchmaking, VoiceChat...)|GCM Notifications require this permission to work. If you do not wish to use GCM Notifications, this permission may be removed. Be advised that removing GCM Notifications may severely diminish the user experience.|


### 4. Example Manifest

    <manifest xmlns:android="http://schemas.android.com/apk/res/android"
            package="com.fresvii"
            android:versionCode="5003"
            android:versionName="0.5.0" >
        
        <!-- Minimum SDK version for AppSteroid is 14 -->
        <uses-sdk
                android:minSdkVersion="14"
                android:targetSdkVersion="19" />
                
        <!-- Define permissions for AppSteroid -->
        <permission
                android:name="com.fresvii.gcm.NotificationActionReceiver.permission.ACTION_RECEIVER"
                android:protectionLevel="signature" />
        <permission
            android:name="com.fresvii.gcm.permission.C2D_MESSAGE"
            android:protectionLevel="signature" />
        
        <!-- Permissions required by the AppSteroid -->
        <uses-permission android:name="android.permission.INTERNET"/>
        <uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE" />
        <uses-permission android:name="android.permission.RECORD_AUDIO" />
        <uses-permission android:name="android.permission.MODIFY_AUDIO_SETTINGS" />
        <uses-permission android:name="android.permission.GET_ACCOUNTS" />
        <uses-permission android:name="android.permission.WAKE_LOCK" />   
        <uses-permission android:name="com.google.android.c2dm.permission.RECEIVE" />
        <uses-permission android:name="com.example.gcm.permission.C2D_MESSAGE" />
        <uses-permission android:name="com.example.gcm.c2dm.permission.RECEIVE" />
        <uses-permission android:name="com.fresvii.gcm.NotificationActionReceiver.permission.ACTION_RECEIVER" />
        
        <application
                android:allowBackup="true"
                android:label="@string/appsteroid_app_name" >
                
            <!-- This receiver is required by the AppSteroid to receive GCM Notifications -->
            <receiver
                    android:name="com.fresvii.gcm.GcmBroadcastReceiver"
                    android:permission="com.google.android.c2dm.permission.SEND" >
                <intent-filter>
                    <action android:name="com.google.android.c2dm.intent.RECEIVE" />
                    <category android:name="com.example.gcm" />
                </intent-filter>
            </receiver>
            
            <!-- This receiver is required by the AppSteroid to react to user actions, such as accepting VoiceChat etc. -->
            <receiver
                    android:permission="com.fresvii.gcm.NotificationActionReceiver.permission.ACTION_RECEIVER"
                    android:name="com.fresvii.gcm.NotificationActionReceiver" >
                <intent-filter>
                    <action android:name="com.fresvii.gcm.NotificationActionReceiver.intent.ACTION_ACCEPT_FRIEND_REQUEST" />
                    <action android:name="com.fresvii.gcm.NotificationActionReceiver.intent.ACTION_HIDE_FRIEND_REQUEST" />
                    <action android:name="com.fresvii.gcm.NotificationActionReceiver.intent.ACTION_ACCEPT_VOICE_CHAT" />
                    <action android:name="com.fresvii.gcm.NotificationActionReceiver.intent.ACTION_CLEAR_NOTIFICATION" />
                    <action android:name="com.fresvii.gcm.NotificationActionReceiver.intent.ACTION_ACCEPT_GAME_INVITATION" />
                </intent-filter>
            </receiver>
            
            <!-- This service is required by the AppSteroid to receive GCM Notifications -->
            <service android:name="com.fresvii.gcm.GcmIntentService" />
            
            <!-- AppSteroid Activity -->
            <activity
                    android:name="com.fresvii.gui.AppSteroidActivity" 
                    android:theme="@style/AppSteroidTheme" />
        </application>
        
    </manifest>
