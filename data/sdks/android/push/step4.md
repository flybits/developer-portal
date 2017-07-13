```java
import android.os.Bundle;
import android.support.v7.app.AppCompatActivity;

import com.flybits.commons.library.api.FlybitsManager;
import com.flybits.commons.library.api.idps.AnonymousIDP;
import com.flybits.android.push.api.PushScope;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        PushScope pushScope = new PushScope(MainActivity.this);

        FlybitsManager manager = new FlybitsManager.Builder(MainActivity.this)
            .addScope(pushScope)
            .setAccount(new AnonymousIDP())
            .setDebug()
            .build();

        manager.connect();    
    }
}
```
