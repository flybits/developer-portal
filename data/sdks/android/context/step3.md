```java
import android.os.Bundle;
import android.support.v7.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main2);

        ContextScope contextScope 
          = new ContextScope(MainActivity.this, 1, TimeUnit.MINUTES, ContextPriority.HIGH) 
    }
}  
```
