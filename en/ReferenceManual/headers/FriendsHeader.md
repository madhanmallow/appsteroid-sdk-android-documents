
# AppSteroid Friend API

Last updated %LAST_UPDATED%

-------------------------

## Introduction

AppSteroid Friend API can be used to manage AppSteroid friend relations. You can send, accept or hide friend requests, retrieve lists of friends, incoming friend requests or outgoing friend requests.

You may also register a [FriendRequestNotificationListener](GcmClient.md#com.fresvii.gcm.FriendRequestNotificationListener) to be informed about new incoming friend requests or updates to outgoing friend requests, but that is optional since the AppSteroid by default will handle these notifications for you.

The easiest way to make use of the Friends feature is via the built in AppSteroid GUI. E.g. you can open the AppSteroid Forum GUI, and befriend a user via his profile.

    AppSteroidActivity.startAndShowForum(getApplicationContext());

Or you can open your own profile, to accept incoming friend requests and see a list of your own friends.

    AppSteroidActivity.startAndShowEditProfile(getApplicationContext());

![](../Images/FriendList.png)
