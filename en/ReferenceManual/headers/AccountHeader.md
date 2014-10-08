
# AppSteroid Account API

Last updated %LAST_UPDATED%

-------------------------

## Introduction

AppSteroid Account API can be used to manage AppSteroid user accounts.

Normally, the application does not have to deal with account management. It is sufficient to call [AppSteroid.start()](AndroidSDK.md#com_fresvii_AppSteroid_void_start_Context_String_String_String_String), this will automatically create a new user account if no user account exists yet, and automatically log in the user.

The application may register a [AccountAccess.UserAuthEventListener](#com.fresvii.server.access.AccountAccess.UserAuthEventListener) to be notified when a new user is signed up, or the user logs in.
