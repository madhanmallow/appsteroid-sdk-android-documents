
# AppSteroid VoiceChat API

Last updated 2014-12-10

-------------------------

## Introduction

AppSteroid VoiceChat API can be used to establish voice calls between up to 4 AppSteroid Users. You should start by reading the [VoiceChat Get Started](../GetStarted/VoiceChatGetStarted.md).



---  

## Classes

|Class|Description|
|---|---|
|[VoiceChatConfig](#com.fresvii.voicechat.VoiceChatConfig)|Configuration for VoiceChat.|
|[VoiceChatConfig.IncomingVoiceChatBehavior](#com.fresvii.voicechat.VoiceChatConfig.IncomingVoiceChatBehavior)|Specifies the behavior when receiving an incoming VoiceChat invitation.|
|[VoiceChatConfig.SpeakerRouteDuringVoiceChat](#com.fresvii.voicechat.VoiceChatConfig.SpeakerRouteDuringVoiceChat)|Specifies which speaker route to set during VoiceChat.|
|[VoiceChatConfig.AudioModeDuringVoiceChat](#com.fresvii.voicechat.VoiceChatConfig.AudioModeDuringVoiceChat)|Specifies which audio mode to set during VoiceChat.|
|[VoiceChatConfig.VoiceChatProfile](#com.fresvii.voicechat.VoiceChatConfig.VoiceChatProfile)|Profiles for VoiceChat that influence VoiceChat behavior such as which code to use and jitter buffer size.|
|[VoiceChatConference](#com.fresvii.voicechat.VoiceChatConference)|Class used to manage a VoiceChat conference.|
|[VoiceChatConference.CallState](#com.fresvii.voicechat.VoiceChatConference.CallState)|Represents the state of a call in the conference.|
|[VoiceChatConference.ConferenceState](#com.fresvii.voicechat.VoiceChatConference.ConferenceState)|Represents the state of the conference.|
|[VoiceChatConference.ConferenceRole](#com.fresvii.voicechat.VoiceChatConference.ConferenceRole)|Represents the conference role.|
|[VoiceChatConferenceCallback](#com.fresvii.voicechat.VoiceChatConferenceCallback)|Callback interface to handle several [VoiceChatConference](#com.fresvii.voicechat.VoiceChatConference) results.|
|[VoiceChatConferenceListener](#com.fresvii.voicechat.VoiceChatConferenceListener)|Application may implement this interface to handle [VoiceChatConference](#com.fresvii.voicechat.VoiceChatConference) events.|



---  

## <a name="com.fresvii.voicechat.VoiceChatConfig"> Class VoiceChatConfig </a>

```
public class VoiceChatConfig extends Object
```

**Hierarchy:**  

```
java.lang.Object  
    com.fresvii.voicechat.VoiceChatConfig
```

**Description:**  
Configuration for VoiceChat.

**Author:**  
Marcus Froeschl

**Version:**  
1.0

**Since:**  
2014-09-15


### Method Summary

|Method|Description|
|---|---|
|[public VoiceChatConfig.AudioModeDuringVoiceChat getAudioModeDuringVoiceChat()](#com_fresvii_voicechat_VoiceChatConfig_com_fresvii_voicechat_VoiceChatConfig_AudioModeDuringVoiceChat_getAudioModeDuringVoiceChat_)|Retrieves the audio mode that will be set during VoiceChat.|
|[public VoiceChatConfig.IncomingVoiceChatBehavior getIncomingVoiceChatBehavior()](#com_fresvii_voicechat_VoiceChatConfig_com_fresvii_voicechat_VoiceChatConfig_IncomingVoiceChatBehavior_getIncomingVoiceChatBehavior_)|Retrieves the default behavior in case of incoming VoiceChat invitation.|
|[public static VoiceChatConfig getInstance()](#com_fresvii_voicechat_VoiceChatConfig_com_fresvii_voicechat_VoiceChatConfig_getInstance_)|Returns The instance of the VoiceChatConfig singleton object.|
|[public boolean getShouldSetStreamSolo()](#com_fresvii_voicechat_VoiceChatConfig_boolean_getShouldSetStreamSolo_)|Retrieves if STREAM_VOICE_CALL should be set as solo stream during VoiceChat.|
|[public VoiceChatConfig.SpeakerRouteDuringVoiceChat getSpeakerRouteDuringVoiceChat()](#com_fresvii_voicechat_VoiceChatConfig_com_fresvii_voicechat_VoiceChatConfig_SpeakerRouteDuringVoiceChat_getSpeakerRouteDuringVoiceChat_)|Retrieves the default speaker route that will be set during VoiceChat.|
|[public VoiceChatConfig.VoiceChatProfile getVoiceChatProfile()](#com_fresvii_voicechat_VoiceChatConfig_com_fresvii_voicechat_VoiceChatConfig_VoiceChatProfile_getVoiceChatProfile_)|Retrieves the VoiceChatProfile that will be used during VoiceChat.|
|[public void setAudioModeDuringVoiceChat(VoiceChatConfig.AudioModeDuringVoiceChat mode)](#com_fresvii_voicechat_VoiceChatConfig_void_setAudioModeDuringVoiceChat_VoiceChatConfig_AudioModeDuringVoiceChat)|Specifies which audio mode to set during VoiceChat.|
|[public void setIncomingVoiceChatBehavior(VoiceChatConfig.IncomingVoiceChatBehavior incomingVoiceChatBehavior)](#com_fresvii_voicechat_VoiceChatConfig_void_setIncomingVoiceChatBehavior_VoiceChatConfig_IncomingVoiceChatBehavior)|Sets the default behavior in case of incoming VoiceChat invitation.|
|[public void setShouldSetStreamSolo(boolean shouldSetStreamSolo)](#com_fresvii_voicechat_VoiceChatConfig_void_setShouldSetStreamSolo_boolean)|Specifies if STREAM_VOICE_CALL should be set as solo stream during VoiceChat.|
|[public void setSpeakerRouteDuringVoiceChat(VoiceChatConfig.SpeakerRouteDuringVoiceChat route)](#com_fresvii_voicechat_VoiceChatConfig_void_setSpeakerRouteDuringVoiceChat_VoiceChatConfig_SpeakerRouteDuringVoiceChat)|Specifies which speaker route to set during VoiceChat.|
|[public void setVoiceChatProfile(VoiceChatConfig.VoiceChatProfile voiceChatProfile)](#com_fresvii_voicechat_VoiceChatConfig_void_setVoiceChatProfile_VoiceChatConfig_VoiceChatProfile)|Specifies which VoiceChatProfile will be used during VoiceChat.|



### Method Detail
 


## <a name="com_fresvii_voicechat_VoiceChatConfig_com_fresvii_voicechat_VoiceChatConfig_AudioModeDuringVoiceChat_getAudioModeDuringVoiceChat_"> getAudioModeDuringVoiceChat </a>

```
public VoiceChatConfig.AudioModeDuringVoiceChat getAudioModeDuringVoiceChat()
```

Retrieves the audio mode that will be set during VoiceChat.

#### Returns

|Return Type|Description|
|---|---|
|VoiceChatConfig.AudioModeDuringVoiceChat|The audio mode that will be set during VoiceChat.|


## <a name="com_fresvii_voicechat_VoiceChatConfig_com_fresvii_voicechat_VoiceChatConfig_IncomingVoiceChatBehavior_getIncomingVoiceChatBehavior_"> getIncomingVoiceChatBehavior </a>

```
public VoiceChatConfig.IncomingVoiceChatBehavior getIncomingVoiceChatBehavior()
```

Retrieves the default behavior in case of incoming VoiceChat invitation.

#### Returns

|Return Type|Description|
|---|---|
|VoiceChatConfig.IncomingVoiceChatBehavior|The default behavior in case of incoming VoiceChat invitation.|


## <a name="com_fresvii_voicechat_VoiceChatConfig_com_fresvii_voicechat_VoiceChatConfig_getInstance_"> getInstance </a>

```
public static VoiceChatConfig getInstance()
```

Returns The instance of the VoiceChatConfig singleton object.

#### Returns

|Return Type|Description|
|---|---|
|VoiceChatConfig|The instance of the VoiceChatConfig singleton object.|


## <a name="com_fresvii_voicechat_VoiceChatConfig_boolean_getShouldSetStreamSolo_"> getShouldSetStreamSolo </a>

```
public boolean getShouldSetStreamSolo()
```

Retrieves if STREAM_VOICE_CALL should be set as solo stream during VoiceChat.

#### Returns

|Return Type|Description|
|---|---|
|boolean|If STREAM_VOICE_CALL should be set as solo stream during VoiceChat.|


## <a name="com_fresvii_voicechat_VoiceChatConfig_com_fresvii_voicechat_VoiceChatConfig_SpeakerRouteDuringVoiceChat_getSpeakerRouteDuringVoiceChat_"> getSpeakerRouteDuringVoiceChat </a>

```
public VoiceChatConfig.SpeakerRouteDuringVoiceChat getSpeakerRouteDuringVoiceChat()
```

Retrieves the default speaker route that will be set during VoiceChat.

#### Returns

|Return Type|Description|
|---|---|
|VoiceChatConfig.SpeakerRouteDuringVoiceChat|The default speaker route that will be set during VoiceChat.|


## <a name="com_fresvii_voicechat_VoiceChatConfig_com_fresvii_voicechat_VoiceChatConfig_VoiceChatProfile_getVoiceChatProfile_"> getVoiceChatProfile </a>

```
public VoiceChatConfig.VoiceChatProfile getVoiceChatProfile()
```

Retrieves the VoiceChatProfile that will be used during VoiceChat.

#### Returns

|Return Type|Description|
|---|---|
|VoiceChatConfig.VoiceChatProfile|The VoiceChatProfile that will be used during VoiceChat.|


## <a name="com_fresvii_voicechat_VoiceChatConfig_void_setAudioModeDuringVoiceChat_VoiceChatConfig_AudioModeDuringVoiceChat"> setAudioModeDuringVoiceChat </a>

```
public void setAudioModeDuringVoiceChat(VoiceChatConfig.AudioModeDuringVoiceChat mode)
```

Specifies which audio mode to set during VoiceChat.  The default behavior is to use MODE_IN_COMMUNICATION.

#### Parameters

|Parameter|Description|
|---|---|
|[VoiceChatConfig.AudioModeDuringVoiceChat](#com.fresvii.voicechat.VoiceChatConfig.AudioModeDuringVoiceChat) mode|The desired audio mode to set during VoiceChat.|



## <a name="com_fresvii_voicechat_VoiceChatConfig_void_setIncomingVoiceChatBehavior_VoiceChatConfig_IncomingVoiceChatBehavior"> setIncomingVoiceChatBehavior </a>

```
public void setIncomingVoiceChatBehavior(VoiceChatConfig.IncomingVoiceChatBehavior incomingVoiceChatBehavior)
```

Sets the default behavior in case of incoming VoiceChat invitation.  E.g., should the VoiceChat be auto-connected, or should the user be asked?  The default behavior is to ask the user.

#### Parameters

|Parameter|Description|
|---|---|
|[VoiceChatConfig.IncomingVoiceChatBehavior](#com.fresvii.voicechat.VoiceChatConfig.IncomingVoiceChatBehavior) incomingVoiceChatBehavior|The desired default behavior in case of incoming VoiceChat invitation.|



## <a name="com_fresvii_voicechat_VoiceChatConfig_void_setShouldSetStreamSolo_boolean"> setShouldSetStreamSolo </a>

```
public void setShouldSetStreamSolo(boolean shouldSetStreamSolo)
```

Specifies if STREAM_VOICE_CALL should be set as solo stream during VoiceChat.  The default behavior is true.

#### Parameters

|Parameter|Description|
|---|---|
|boolean shouldSetStreamSolo|If STREAM_VOICE_CALL should be set as solo stream during VoiceChat.|



## <a name="com_fresvii_voicechat_VoiceChatConfig_void_setSpeakerRouteDuringVoiceChat_VoiceChatConfig_SpeakerRouteDuringVoiceChat"> setSpeakerRouteDuringVoiceChat </a>

```
public void setSpeakerRouteDuringVoiceChat(VoiceChatConfig.SpeakerRouteDuringVoiceChat route)
```

Specifies which speaker route to set during VoiceChat.  The default behavior is to use the internal speaker.

#### Parameters

|Parameter|Description|
|---|---|
|[VoiceChatConfig.SpeakerRouteDuringVoiceChat](#com.fresvii.voicechat.VoiceChatConfig.SpeakerRouteDuringVoiceChat) route|The speaker route to set during VoiceChat.|



## <a name="com_fresvii_voicechat_VoiceChatConfig_void_setVoiceChatProfile_VoiceChatConfig_VoiceChatProfile"> setVoiceChatProfile </a>

```
public void setVoiceChatProfile(VoiceChatConfig.VoiceChatProfile voiceChatProfile)
```

Specifies which VoiceChatProfile will be used during VoiceChat.  The default behavior is to use LOW_BANDWIDTH.

#### Parameters

|Parameter|Description|
|---|---|
|[VoiceChatConfig.VoiceChatProfile](#com.fresvii.voicechat.VoiceChatConfig.VoiceChatProfile) voiceChatProfile|The desired VoiceChatProfile that will be used during VoiceChat.|




---  

## <a name="com.fresvii.voicechat.VoiceChatConfig.IncomingVoiceChatBehavior"> Enum VoiceChatConfig.IncomingVoiceChatBehavior </a>

```
public static final class VoiceChatConfig.IncomingVoiceChatBehavior extends Enum
```

**Hierarchy:**  

```
java.lang.Object  
    java.lang.Enum  
        com.fresvii.voicechat.VoiceChatConfig.IncomingVoiceChatBehavior
```

**Description:**  
Specifies the behavior when receiving an incoming VoiceChat invitation.








### Field Summary

|Field|Description|
|---|---|
|ASK|Display a notification and ask the user if to accept the VoiceChat invitation.|
|AUTO_ACCEPT|Automatically accept the VoiceChat invitation.|
|DO_NOTHING|Do nothing. Select this if you wish to ignore incoming VoiceChat invitations,|




---  

## <a name="com.fresvii.voicechat.VoiceChatConfig.SpeakerRouteDuringVoiceChat"> Enum VoiceChatConfig.SpeakerRouteDuringVoiceChat </a>

```
public static final class VoiceChatConfig.SpeakerRouteDuringVoiceChat extends Enum
```

**Hierarchy:**  

```
java.lang.Object  
    java.lang.Enum  
        com.fresvii.voicechat.VoiceChatConfig.SpeakerRouteDuringVoiceChat
```

**Description:**  
Specifies which speaker route to set during VoiceChat.








### Field Summary

|Field|Description|
|---|---|
|EXTERNAL|Set to external speaker.|
|INTERNAL|Set to internal speaker.|
|KEEP_CURRENT|Do not set the speaker route at all. Keep the current speaker route.|




---  

## <a name="com.fresvii.voicechat.VoiceChatConfig.AudioModeDuringVoiceChat"> Enum VoiceChatConfig.AudioModeDuringVoiceChat </a>

```
public static final class VoiceChatConfig.AudioModeDuringVoiceChat extends Enum
```

**Hierarchy:**  

```
java.lang.Object  
    java.lang.Enum  
        com.fresvii.voicechat.VoiceChatConfig.AudioModeDuringVoiceChat
```

**Description:**  
Specifies which audio mode to set during VoiceChat.








### Field Summary

|Field|Description|
|---|---|
|KEEP_CURRENT|Do not set the audio mode at all. Keep the current audio mode.|
|MODE_IN_COMMUNICATION|Set to MODE_IN_COMMUNICATION.|
|MODE_NORMAL|Set to MODE_NORMAL.|




---  

## <a name="com.fresvii.voicechat.VoiceChatConfig.VoiceChatProfile"> Enum VoiceChatConfig.VoiceChatProfile </a>

```
public static final class VoiceChatConfig.VoiceChatProfile extends Enum
```

**Hierarchy:**  

```
java.lang.Object  
    java.lang.Enum  
        com.fresvii.voicechat.VoiceChatConfig.VoiceChatProfile
```

**Description:**  
Profiles for VoiceChat that influence VoiceChat behavior such as which code to use and jitter buffer size.








### Field Summary

|Field|Description|
|---|---|
|HIGH_BANDWIDTH|Profile for use in a high bandwidth environment.|
|LOW_BANDWIDTH|Profile for use in a low bandwidth environment.|




---  

## <a name="com.fresvii.voicechat.VoiceChatConference"> Class VoiceChatConference </a>

```
public class VoiceChatConference extends Object
```

**Hierarchy:**  

```
java.lang.Object  
    com.fresvii.voicechat.VoiceChatConference
```

**Description:**  
Class used to manage a VoiceChat conference.  There can be only 1 conference at a time.

**Author:**  
Marcus Froeschl

**Version:**  
1.0

**Since:**  
2014-05-20


### Method Summary

|Method|Description|
|---|---|
|[public void addGuest(String guestId, VoiceChatConferenceCallback addGuestCallback)](#com_fresvii_voicechat_VoiceChatConference_void_addGuest_String_VoiceChatConferenceCallback)|Adds a guest to the conference.|
|[public void addVoiceChatConferenceListener(VoiceChatConferenceListener listener)](#com_fresvii_voicechat_VoiceChatConference_void_addVoiceChatConferenceListener_VoiceChatConferenceListener)|Application can add a [VoiceChatConferenceListener](#com.fresvii.voicechat.VoiceChatConferenceListener) to be informed about VoiceChatConference events|
|[public void doesConferenceExistOnServer(String groupId, DoesConferenceExistCallback callback)](#com_fresvii_voicechat_VoiceChatConference_void_doesConferenceExistOnServer_String_DoesConferenceExistCallback)|Checks if a conference for this group already exists on the Fresvii server|
|[public VoiceChatConference.ConferenceState getConferenceState()](#com_fresvii_voicechat_VoiceChatConference_com_fresvii_voicechat_VoiceChatConference_ConferenceState_getConferenceState_)|Retrieves the current ConferenceState of the VoiceChatConference.|
|[public long getElapsedTime()](#com_fresvii_voicechat_VoiceChatConference_long_getElapsedTime_)|Retrieves the elapsed time of the conference.|
|[public String getGroupId()](#com_fresvii_voicechat_VoiceChatConference_java_lang_String_getGroupId_)|Retrieves the group ID of the VoiceChatConference.|
|[public static VoiceChatConference getInstance()](#com_fresvii_voicechat_VoiceChatConference_com_fresvii_voicechat_VoiceChatConference_getInstance_)|Retrieves the instance of the singleton object. Use this to access the VoiceChatConference.|
|[public VoiceChatConference.ConferenceRole getRole()](#com_fresvii_voicechat_VoiceChatConference_com_fresvii_voicechat_VoiceChatConference_ConferenceRole_getRole_)|Retrieves the role of the VoiceChatConference.|
|[public Date getStartTimestamp()](#com_fresvii_voicechat_VoiceChatConference_java_util_Date_getStartTimestamp_)|Retrieves the timestamp at which the conference started.|
|[public void host(String groupId, VoiceChatConferenceCallback hostCallback)](#com_fresvii_voicechat_VoiceChatConference_void_host_String_VoiceChatConferenceCallback)|Hosts a conference.|
|[public boolean isCurrentlyParticipatingInConference()](#com_fresvii_voicechat_VoiceChatConference_boolean_isCurrentlyParticipatingInConference_)|Checks if a voice chat conference is currently active.|
|[public boolean isMute()](#com_fresvii_voicechat_VoiceChatConference_boolean_isMute_)|Retrieves if the microphone for the conference is mute.|
|[public void join(String groupId, String hostId, VoiceChatConferenceCallback joinCallback)](#com_fresvii_voicechat_VoiceChatConference_void_join_String_String_VoiceChatConferenceCallback)|Joins a conference.|
|[public void leave(VoiceChatConferenceCallback leaveCallback)](#com_fresvii_voicechat_VoiceChatConference_void_leave_VoiceChatConferenceCallback)|Leaves the voicechat conference.|
|[public void mute(VoiceChatConferenceCallback muteCallback)](#com_fresvii_voicechat_VoiceChatConference_void_mute_VoiceChatConferenceCallback)|Mutes the conference.|
|[public void removeGuest(String guestId, VoiceChatConferenceCallback removeGuestCallback)](#com_fresvii_voicechat_VoiceChatConference_void_removeGuest_String_VoiceChatConferenceCallback)|Removes a guest from the conference.|
|[public void removeVoiceChatConferenceListener(VoiceChatConferenceListener listener)](#com_fresvii_voicechat_VoiceChatConference_void_removeVoiceChatConferenceListener_VoiceChatConferenceListener)|Removes a [VoiceChatConferenceListener](#com.fresvii.voicechat.VoiceChatConferenceListener).|
|[public void setVolume(float microphoneVolume, float speakerVolume, VoiceChatConferenceCallback setVolumeCallback)](#com_fresvii_voicechat_VoiceChatConference_void_setVolume_float_float_VoiceChatConferenceCallback)|Sets the volume of the conference.|
|[public void unmute(VoiceChatConferenceCallback unmuteCallback)](#com_fresvii_voicechat_VoiceChatConference_void_unmute_VoiceChatConferenceCallback)|Unmutes the conference.|



### Method Detail
 


## <a name="com_fresvii_voicechat_VoiceChatConference_void_addGuest_String_VoiceChatConferenceCallback"> addGuest </a>

```
public void addGuest(String guestId,  
                     VoiceChatConferenceCallback addGuestCallback)
```

Adds a guest to the conference.  Only works if we did host the conference.

#### Parameters

|Parameter|Description|
|---|---|
|String guestId|Fresvii guestId|
|[VoiceChatConferenceCallback](#com.fresvii.voicechat.VoiceChatConferenceCallback) addGuestCallback|Callback to be informed about the result of the operation.|



## <a name="com_fresvii_voicechat_VoiceChatConference_void_addVoiceChatConferenceListener_VoiceChatConferenceListener"> addVoiceChatConferenceListener </a>

```
public void addVoiceChatConferenceListener(VoiceChatConferenceListener listener)
```

Application can add a [VoiceChatConferenceListener](#com.fresvii.voicechat.VoiceChatConferenceListener) to be informed about VoiceChatConference events

#### Parameters

|Parameter|Description|
|---|---|
|[VoiceChatConferenceListener](#com.fresvii.voicechat.VoiceChatConferenceListener) listener|[VoiceChatConferenceListener](#com.fresvii.voicechat.VoiceChatConferenceListener) to be informed about VoiceChatConference events.|



## <a name="com_fresvii_voicechat_VoiceChatConference_void_doesConferenceExistOnServer_String_DoesConferenceExistCallback"> doesConferenceExistOnServer </a>

```
public void doesConferenceExistOnServer(String groupId,  
                                        DoesConferenceExistCallback callback)
```

Checks if a conference for this group already exists on the Fresvii server

#### Parameters

|Parameter|Description|
|---|---|
|String groupId|Fresvii groupId|
|DoesConferenceExistCallback callback|Callback to be informed about the result of the operation.|



## <a name="com_fresvii_voicechat_VoiceChatConference_com_fresvii_voicechat_VoiceChatConference_ConferenceState_getConferenceState_"> getConferenceState </a>

```
public VoiceChatConference.ConferenceState getConferenceState()
```

Retrieves the current ConferenceState of the VoiceChatConference.

#### Returns

|Return Type|Description|
|---|---|
|VoiceChatConference.ConferenceState|The current ConferenceState.|


## <a name="com_fresvii_voicechat_VoiceChatConference_long_getElapsedTime_"> getElapsedTime </a>

```
public long getElapsedTime()
```

Retrieves the elapsed time of the conference.

#### Returns

|Return Type|Description|
|---|---|
|long|The elapsed time of the conference. 0 if there is no conference.|


## <a name="com_fresvii_voicechat_VoiceChatConference_java_lang_String_getGroupId_"> getGroupId </a>

```
public String getGroupId()
```

Retrieves the group ID of the VoiceChatConference.

#### Returns

|Return Type|Description|
|---|---|
|String|The current group ID. Empty String if there is no conference.|


## <a name="com_fresvii_voicechat_VoiceChatConference_com_fresvii_voicechat_VoiceChatConference_getInstance_"> getInstance </a>

```
public static VoiceChatConference getInstance()
```

Retrieves the instance of the singleton object. Use this to access the VoiceChatConference.

#### Returns

|Return Type|Description|
|---|---|
|VoiceChatConference|Instance of the singleton object.|


## <a name="com_fresvii_voicechat_VoiceChatConference_com_fresvii_voicechat_VoiceChatConference_ConferenceRole_getRole_"> getRole </a>

```
public VoiceChatConference.ConferenceRole getRole()
```

Retrieves the role of the VoiceChatConference.

#### Returns

|Return Type|Description|
|---|---|
|VoiceChatConference.ConferenceRole|The role of the VoiceChatConference. NONE if there is no conference.|


## <a name="com_fresvii_voicechat_VoiceChatConference_java_util_Date_getStartTimestamp_"> getStartTimestamp </a>

```
public Date getStartTimestamp()
```

Retrieves the timestamp at which the conference started.

#### Returns

|Return Type|Description|
|---|---|
|Date|The timestamp at which the conference started.|


## <a name="com_fresvii_voicechat_VoiceChatConference_void_host_String_VoiceChatConferenceCallback"> host </a>

```
public void host(String groupId,  
                 VoiceChatConferenceCallback hostCallback)
```

Hosts a conference.

#### Parameters

|Parameter|Description|
|---|---|
|String groupId|Fresvii groupId|
|[VoiceChatConferenceCallback](#com.fresvii.voicechat.VoiceChatConferenceCallback) hostCallback|Callback to be informed about the result of the operation.|



## <a name="com_fresvii_voicechat_VoiceChatConference_boolean_isCurrentlyParticipatingInConference_"> isCurrentlyParticipatingInConference </a>

```
public boolean isCurrentlyParticipatingInConference()
```

Checks if a voice chat conference is currently active.

#### Returns

|Return Type|Description|
|---|---|
|boolean|True if a voice chat conference is currently active.|


## <a name="com_fresvii_voicechat_VoiceChatConference_boolean_isMute_"> isMute </a>

```
public boolean isMute()
```

Retrieves if the microphone for the conference is mute.

#### Returns

|Return Type|Description|
|---|---|
|boolean|true if the microphone for the conference is mute, false otherwise.|


## <a name="com_fresvii_voicechat_VoiceChatConference_void_join_String_String_VoiceChatConferenceCallback"> join </a>

```
public void join(String groupId,  
                 String hostId,  
                 VoiceChatConferenceCallback joinCallback)
```

Joins a conference.

#### Parameters

|Parameter|Description|
|---|---|
|String groupId|Fresvii groupId.|
|String hostId|Fresvii user ID of the conference host.|
|[VoiceChatConferenceCallback](#com.fresvii.voicechat.VoiceChatConferenceCallback) joinCallback|Callback to be informed about the result of the operation.|



## <a name="com_fresvii_voicechat_VoiceChatConference_void_leave_VoiceChatConferenceCallback"> leave </a>

```
public void leave(VoiceChatConferenceCallback leaveCallback)
```

Leaves the voicechat conference.

#### Parameters

|Parameter|Description|
|---|---|
|[VoiceChatConferenceCallback](#com.fresvii.voicechat.VoiceChatConferenceCallback) leaveCallback|Callback to be informed about the result of the operation.|



## <a name="com_fresvii_voicechat_VoiceChatConference_void_mute_VoiceChatConferenceCallback"> mute </a>

```
public void mute(VoiceChatConferenceCallback muteCallback)
```

Mutes the conference.

#### Parameters

|Parameter|Description|
|---|---|
|[VoiceChatConferenceCallback](#com.fresvii.voicechat.VoiceChatConferenceCallback) muteCallback|Callback to be informed about the result of the operation.|



## <a name="com_fresvii_voicechat_VoiceChatConference_void_removeGuest_String_VoiceChatConferenceCallback"> removeGuest </a>

```
public void removeGuest(String guestId,  
                        VoiceChatConferenceCallback removeGuestCallback)
```

Removes a guest from the conference.  Only works if we did host the conference.

#### Parameters

|Parameter|Description|
|---|---|
|String guestId|Fresvii guestId|
|[VoiceChatConferenceCallback](#com.fresvii.voicechat.VoiceChatConferenceCallback) removeGuestCallback|Callback to be informed about the result of the operation.|



## <a name="com_fresvii_voicechat_VoiceChatConference_void_removeVoiceChatConferenceListener_VoiceChatConferenceListener"> removeVoiceChatConferenceListener </a>

```
public void removeVoiceChatConferenceListener(VoiceChatConferenceListener listener)
```

Removes a [VoiceChatConferenceListener](#com.fresvii.voicechat.VoiceChatConferenceListener).

#### Parameters

|Parameter|Description|
|---|---|
|[VoiceChatConferenceListener](#com.fresvii.voicechat.VoiceChatConferenceListener) listener|[VoiceChatConferenceListener](#com.fresvii.voicechat.VoiceChatConferenceListener) to be removed.|



## <a name="com_fresvii_voicechat_VoiceChatConference_void_setVolume_float_float_VoiceChatConferenceCallback"> setVolume </a>

```
public void setVolume(float microphoneVolume,  
                      float speakerVolume,  
                      VoiceChatConferenceCallback setVolumeCallback)
```

Sets the volume of the conference.

#### Parameters

|Parameter|Description|
|---|---|
|float microphoneVolume|Microphone volume.|
|float speakerVolume|Speaker volume.|
|[VoiceChatConferenceCallback](#com.fresvii.voicechat.VoiceChatConferenceCallback) setVolumeCallback|Callback to be informed about the result of the operation.|



## <a name="com_fresvii_voicechat_VoiceChatConference_void_unmute_VoiceChatConferenceCallback"> unmute </a>

```
public void unmute(VoiceChatConferenceCallback unmuteCallback)
```

Unmutes the conference.

#### Parameters

|Parameter|Description|
|---|---|
|[VoiceChatConferenceCallback](#com.fresvii.voicechat.VoiceChatConferenceCallback) unmuteCallback|Callback to be informed about the result of the operation.|




---  

## <a name="com.fresvii.voicechat.VoiceChatConference.CallState"> Enum VoiceChatConference.CallState </a>

```
public static final class VoiceChatConference.CallState extends Enum
```

**Hierarchy:**  

```
java.lang.Object  
    java.lang.Enum  
        com.fresvii.voicechat.VoiceChatConference.CallState
```

**Description:**  
Represents the state of a call in the conference.








### Field Summary

|Field|Description|
|---|---|
|CONNECTED|The call is connected.|
|IDLE|The call is idle.|
|PROGRESSING|The call is progressing, i.e. dialing or ringing.|




---  

## <a name="com.fresvii.voicechat.VoiceChatConference.ConferenceState"> Enum VoiceChatConference.ConferenceState </a>

```
public static final class VoiceChatConference.ConferenceState extends Enum
```

**Hierarchy:**  

```
java.lang.Object  
    java.lang.Enum  
        com.fresvii.voicechat.VoiceChatConference.ConferenceState
```

**Description:**  
Represents the state of the conference.








### Field Summary

|Field|Description|
|---|---|
|CREATED|The conference is created.|
|DESTROYED|The conference is destroyed.|




---  

## <a name="com.fresvii.voicechat.VoiceChatConference.ConferenceRole"> Enum VoiceChatConference.ConferenceRole </a>

```
public static final class VoiceChatConference.ConferenceRole extends Enum
```

**Hierarchy:**  

```
java.lang.Object  
    java.lang.Enum  
        com.fresvii.voicechat.VoiceChatConference.ConferenceRole
```

**Description:**  
Represents the conference role.








### Field Summary

|Field|Description|
|---|---|
|GUEST|We are a guest in the current conference.|
|HOST|We are the host of the current conference.|
|NONE|There currently is no conference.|




---  

## <a name="com.fresvii.voicechat.VoiceChatConferenceCallback"> Interface VoiceChatConferenceCallback </a>

```
public interface VoiceChatConferenceCallback implements FailureCallback
```

**Hierarchy:**  

```
com.fresvii.voicechat.VoiceChatConferenceCallback
```

**Description:**  
Callback interface to handle several [VoiceChatConference](#com.fresvii.voicechat.VoiceChatConference) results.

**Author:**  
Marcus Froeschl

**Version:**  
1.0




### Method Summary

|Method|Description|
|---|---|
|[public void onSuccess()](#com_fresvii_voicechat_VoiceChatConferenceCallback_void_onSuccess_)|Callback invoked when operation succeeds.|



### Method Detail
 


## <a name="com_fresvii_voicechat_VoiceChatConferenceCallback_void_onSuccess_"> onSuccess </a>

```
public void onSuccess()
```

Callback invoked when operation succeeds.



---  

## <a name="com.fresvii.voicechat.VoiceChatConferenceListener"> Interface VoiceChatConferenceListener </a>

```
public interface VoiceChatConferenceListener
```

**Hierarchy:**  

```
com.fresvii.voicechat.VoiceChatConferenceListener
```

**Description:**  
Application may implement this interface to handle [VoiceChatConference](#com.fresvii.voicechat.VoiceChatConference) events.

**Author:**  
Marcus Froeschl

**Version:**  
1.0

**Since:**  
2014-06-02


### Method Summary

|Method|Description|
|---|---|
|[public void onCallStateChanged(String groupId, String partnerId, VoiceChatConference.CallState callState)](#com_fresvii_voicechat_VoiceChatConferenceListener_void_onCallStateChanged_String_String_VoiceChatConference_CallState)|Called when the state of a call in the VoiceChat conference changes.|
|[public void onConferenceStateChanged(VoiceChatConference.ConferenceState conferenceState, VoiceChatConference.ConferenceRole conferenceRole, String log)](#com_fresvii_voicechat_VoiceChatConferenceListener_void_onConferenceStateChanged_VoiceChatConference_ConferenceState_VoiceChatConference_ConferenceRole_String)|Called when the state of the conference changes.|
|[public void onError(Throwable error)](#com_fresvii_voicechat_VoiceChatConferenceListener_void_onError_Throwable)|Called when an error occurred during the conference.|



### Method Detail
 


## <a name="com_fresvii_voicechat_VoiceChatConferenceListener_void_onCallStateChanged_String_String_VoiceChatConference_CallState"> onCallStateChanged </a>

```
public void onCallStateChanged(String groupId,  
                               String partnerId,  
                               VoiceChatConference.CallState callState)
```

Called when the state of a call in the VoiceChat conference changes.

#### Parameters

|Parameter|Description|
|---|---|
|String groupId|The Fresvii group ID of the associated group.|
|String partnerId|The Fresvii user ID of the associated call partner.|
|[VoiceChatConference.CallState](#com.fresvii.voicechat.VoiceChatConference.CallState) callState|The state of the call.|



## <a name="com_fresvii_voicechat_VoiceChatConferenceListener_void_onConferenceStateChanged_VoiceChatConference_ConferenceState_VoiceChatConference_ConferenceRole_String"> onConferenceStateChanged </a>

```
public void onConferenceStateChanged(VoiceChatConference.ConferenceState conferenceState,  
                                     VoiceChatConference.ConferenceRole conferenceRole,  
                                     String log)
```

Called when the state of the conference changes.

#### Parameters

|Parameter|Description|
|---|---|
|[VoiceChatConference.ConferenceState](#com.fresvii.voicechat.VoiceChatConference.ConferenceState) conferenceState|The state of the conference.|
|[VoiceChatConference.ConferenceRole](#com.fresvii.voicechat.VoiceChatConference.ConferenceRole) conferenceRole|Our role in the conference when it was created / before it was destroyed.|



## <a name="com_fresvii_voicechat_VoiceChatConferenceListener_void_onError_Throwable"> onError </a>

```
public void onError(Throwable error)
```

Called when an error occurred during the conference.

#### Parameters

|Parameter|Description|
|---|---|
|Throwable error|The error that occurred.|



