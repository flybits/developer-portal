```java
import android.os.Bundle;
import android.support.v7.app.AppCompatActivity;

import com.flybits.commons.library.api.FlybitsManager;
import com.flybits.commons.library.api.idps.AnonymousIDP;
import com.flybits.context.ContextScope;
import com.flybits.context.models.ContextPriority;

import java.util.concurrent.TimeUnit;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main2);

        ContextScope contextScope 
            = new ContextScope(MainActivity.this, 1, TimeUnit.MINUTES, ContextPriority.HIGH);
        
        FlybitsManager manager = new FlybitsManager.Builder(MainActivity.this)
            .addScope(contextScope)
            .setDebug()
            .setAccount(new AnonymousIDP())
            .addProjectID(BuildConfig.FLYBITS_PROJECT_ID)
            .build();
    }
}
```
