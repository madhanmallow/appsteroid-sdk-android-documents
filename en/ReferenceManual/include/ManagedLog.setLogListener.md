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
