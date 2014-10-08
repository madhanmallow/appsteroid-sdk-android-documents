#### Example

```
// Application may implement the UserAuthEventListener interface
public class MainActivity extends Activity implements UserAuthEventListener {
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        // Application may wish to register a UserAuthEventListener
        // to be notified when a new user is signed up, or the user logs in
        AccountAccess.addUserAuthEventListener(this);
        
        // Start the AppSteroid
        AppSteroid.start(
        	    getApplicationContext(),
        	    MY_APP_ID,
        	    MY_APP_SECRET,
        	    MY_APP_NAME,
        	    MY_GCM_SENDER_ID);
        
        ...
    }

    @Override
    public void onUserAuthEvent(String userId, UserAuthEvent event) {
        switch ( event ) {
            case USER_SIGNED_UP:
                // Add any code you wish to be executed when a new user signed up
                break;
            case USER_LOGGED_IN:
                // Add any code you wish to be executed when the user logs in
                break;
        }
    }
}
```
