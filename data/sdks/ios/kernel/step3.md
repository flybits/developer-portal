```swift
import UIKit
import KernelSDK

@UIApplicationMain
class AppDelegate: UIResponder, UIApplicationDelegate {

    var window: UIWindow?

    func application(_ application: UIApplication, didFinishLaunchingWithOptions launchOptions: [UIApplicationLaunchOptionsKey: Any]?) -> Bool {
        // Override point for customization after application launch.
        
        let kernelScope = KernelScope()
        let scopes : [FlybitsScope] = [kernelScope]
        
        let anonymousIDP = AnonymousIDP()
        
        let flybitsManager = FlybitsManager(projectID: "my-project-id", idProvider: anonymousIDP, scopes: scopes)

        _ = flybitsManager.connect { (user, error) in
                guard let user = user, error == nil else {
                    print(error as Any)
                    return
                }
                print(user)
        }
        
        return true
    }
}
```