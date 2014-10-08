
# AppSteroid Matchmaking API

Last updated %LAST_UPDATED%

-------------------------

## Introduction

AppSteroid Matchmaking API can be used to initiate matchmaking. You can create a matchmaking request, accept matchmaking invitations, retrieve lists of matching and ongoing matches etc.

The easiest way to make use of the Matchmaking feature is via the built in AppSteroid GUI. E.g. you can open the AppSteroid Matchmaking GUI, which will also start a [MatchmakingSession](#com.fresvii.helper.MatchmakingSession) that will handle the matchmaking for you.


    AppSteroidActivity.startAndShowMatchmaking(getApplicationContext());

![](../Images/Matchmaking.png)

Use [AppSteroid.setMatchmakingPlayerCount()](AndroidSDK.md#com_fresvii_AppSteroid_void_setMatchmakingPlayerCount_int) to specify how many players you wish to partake in the match:

    AppSteroid.setMatchmakingPlayerCount(4);

The application should register a [MatchmakingSession.MatchmakingSessionListener](#com.fresvii.helper.MatchmakingSession.MatchmakingSessionListener) to be informed when the match is complete. Once the match is complete, you should start your game.

    public class MyGame extends Activity implements MatchmakingSessionListener {
        @Override
        protected void onCreate(Bundle savedInstanceState) {
            // Any application must call AppSteroid.start() in order to work with the AppSteroid Android SDK
            AppSteroid.start(
            	    super.getApplicationContext(),
            	    MY_APP_ID,
            	    MY_APP_SECRET,
            	    MY_APP_NAME,
            	    MY_GCM_SENDER_ID);
    
            ...
        }
    
        // call this method to start the matchmaking
        public void startMatchmaking() {
            // Specify how many players you wish to match (2-16)
            AppSteroid.setMatchmakingPlayerCount(2);
            
            // Add yourself as MatchmakingSessionListener
            MatchmakingSession.addSessionListener(this);
    
            // Start the matchmaking GUI (This will also start the MatchmakingSession)
            AppSteroidActivity.start(getApplicationContext(), AppSteroidViewType.MATCH_MAKING);
        }
        
        @Override
        public void onMatchmakingSessionStarted() {
        }
        
        @Override
        public void onMatchmakingSessionCreationFailed() {
        }
        
        @Override
        public void onMatchmakingSessionCreated(AppSteroidMatchmakingRequest request, AppSteroidMatch match) {
        }
        
        @Override
        public void onMatchmakingSessionUpdated(AppSteroidMatch match) {
        }
        
        @Override
        public void onMatchmakingSessionCanceled() {
        }
        
        @Override
        public void onMatchmakingSessionCompleted(AppSteroidMatch match) {
            // You should start your game here, when the match was completed.
        }
        
        @Override
        public void onMatchmakingSessionStoppedAndListenerRemoved() {
        }
    }

