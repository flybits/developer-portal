```swift
import UIKit
import PushSDK

@UIApplicationMain
class AppDelegate: UIResponder, UIApplicationDelegate {

    var window: UIWindow?

    func application(_ application: UIApplication, didFinishLaunchingWithOptions launchOptions: [UIApplicationLaunchOptionsKey: Any]?) -> Bool {
        // Override point for customization after application launch.
        
        let pushScope = PushScope()
        let scopes : [FlybitsScope] = [pushScope]
                
        return true
    }
}
```