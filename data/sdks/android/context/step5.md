```java
FlybitsContextPlugin plugin = new FlybitsContextPlugin.Builder()
  .setPluginIdentifier(AvailableContextPlugin.BATTERY)
  .setRefreshTime(1, 1, TimeUnit.MINUTES)
  .build();
  
plugin.register(MainActivity.this);
```
        
