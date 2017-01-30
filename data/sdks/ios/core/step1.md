```java
BroadcastReceiver receiver = new BroadcastReceiver() {
  @Override
  public void onReceive(Context context, Intent intent) {
    Bundle bundle = intent.getExtras();
    if (bundle.containsKey(PushManager.BROADCAST_CONTEXT_TYPE)) {

      //AvailablePlugins.BATTERY.getKey() can be any Context Plugin Identifier
      if (bundle.getString(PushManager.BROADCAST_CONTEXT_TYPE).equals(AvailablePlugins.BATTERY.getKey())) {

        BatteryData data = bundle.getParcelable(PushManager.BROADCAST_CONTEXT_OBJ);

        if (data != null) {
          //Do Something
        }
      }

      else if (bundle.getString(PushManager.BROADCAST_CONTEXT_TYPE).equals(AvailablePlugins.BEACON.getKey())) {

        BeaconActive data   = bundle.getParcelable(PushManager.BROADCAST_CONTEXT_OBJ);
        boolean isInRange   = bundle.getBoolean("inRange");

        if (data != null) {
            //Do Something
        }
      }
    }
  }
};