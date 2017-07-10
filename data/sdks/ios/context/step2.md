import UIKit
import ContextSDK

@UIApplicationMain
class AppDelegate: UIResponder, UIApplicationDelegate {

    var window: UIWindow?

    func application(_ application: UIApplication, didFinishLaunchingWithOptions launchOptions: [UIApplicationLaunchOptionsKey: Any]?) -> Bool {
        // Override point for customization after application launch.
        
        let contextScope = ContextScope(timeToUploadContext: 60, timeUnit: .seconds)
        let scopes : [FlybitsScope] = [contextScope]
        
        return true
    }
}