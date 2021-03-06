
# Translation to [STPopup](https://github.com/kevin0571/STPopup)
# Overview
There are two ways to provide,`formSheet`、`bottomSheet`,and you can customize backgroundView.
You just need to touch the bar and then move down to close.

![](https://github.com/huangboju/SwiftySTPopup/blob/master/2017-03-21%2020_24_31.gif)

# Installtion

* Cocoapods

`pod MTPopup`

* Carthage

`github "huangboju/MTPopup"`

# Usage

* **BottomSheet**
```swift
class YourController: UIViewController {

    override func viewDidLoad() {
        super.viewDidLoad()

        contentSizeInPopup = CGSize(width: 300, height: 200)
        landscapeContentSizeInPopup = CGSize(width: 400, height: 200)
    }
}

let popupController = MTPopupController(rootViewController: YourController())
popupController.style = .bottomSheet // Default is formSheet
popupController.present(in: self)
```

* **Custom backgroundView**

```swift
let popupController = MTPopupController(rootViewController: YourController())

let blurEffect = UIBlurEffect(style: .dark)
popupController.backgroundView = UIVisualEffectView(effect: blurEffect)
popupController.backgroundView?.alpha = 0.8
popupController.present(in: self)
```
