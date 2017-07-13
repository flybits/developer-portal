```java
FlybitsManager manager = new FlybitsManager.Builder(context)
  .addScope(Kernel.SCOPE)
  .setAccount(new AnonymousIDP())
  .setDebug()
  .build();

manager.connect();  
```
