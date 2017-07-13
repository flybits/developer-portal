```java
import android.os.Bundle;
import android.support.v7.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        //If your app is supporting FCM (Remember to include your google-services.json)
        PushScope contextScope = new PushScope(MainActivity.this);

        //If your app is supporting GCM
        PushScope contextScope = new PushScope(MainActivity.this, "APP_SENDER_ID"); 
    }
}  
```
