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
        setContentView(R.layout.activity_main);

        FlybitsManager manager = new FlybitsManager.Builder(MainActivity.this)
            .addScope(Kernel.SCOPE)
            .setAccount(new AnonymousIDP())
            .setDebug()
            .build();

        manager.connect(new ConnectionResultCallback() {
            @Override
            public void onConnected() {
              //Indicates you are connected to Flybits
            }

            @Override
            public void notConnected() {
              //Indicates that you are not connected to Flybits
            }

            @Override
            public void onException(FlybitsException exception) {
              //Indicates that there was an issue when connecting to Flybits
            }
        });  
    }
}
```
