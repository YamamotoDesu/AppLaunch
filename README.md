# AppLaunch
iOS Unit Testing by Example - Chapter 4

![image](https://user-images.githubusercontent.com/47273077/178744829-44543765-d038-4d50-938d-7fb790badb98.png)

TestingAppDelegate.swift
```swift
import UIKit

@objc(TestingAppDelegate)
class TestingAppDelegate: UIResponder, UIApplicationDelegate {

    func application(_ application: UIApplication, didFinishLaunchingWithOptions launchOptions: [UIApplication.LaunchOptionsKey: Any]?) -> Bool {
        // Override point for customization after application launch.
        print(">> Launching with testing app delegate")
        return true
    }

}

```

AppDelegate.swift
```swift

// @main 削除する
class AppDelegate: UIResponder, UIApplicationDelegate {

```

main.swift
```swift

import UIKit

let appDelegateClass: AnyClass = NSClassFromString("TestingAppDelegate") ?? AppDelegate.self
UIApplicationMain(
    CommandLine.argc,
    CommandLine.unsafeArgv,
    nil,
    NSStringFromClass(appDelegateClass))

```
