import UIKit
import KernelSDK

@UIApplicationMain
class AppDelegate: UIResponder, UIApplicationDelegate {

    var window: UIWindow?

    func application(_ application: UIApplication, didFinishLaunchingWithOptions launchOptions: [UIApplicationLaunchOptionsKey: Any]?) -> Bool {
        // Override point for customization after application launch.
        
        let kernelScope = KernelScope()
        let scopes : [FlybitsScope] = [kernelScope]
        
        return true
    }
}