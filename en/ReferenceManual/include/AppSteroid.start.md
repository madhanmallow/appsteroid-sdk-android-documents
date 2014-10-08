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
