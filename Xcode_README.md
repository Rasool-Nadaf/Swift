
# 📘 iOS & Swift Concepts 

---

## 🖥️ Xcode
- **What**: Apple’s official IDE for macOS used to develop apps for iOS, macOS, watchOS, and tvOS.  
- **When**: Used whenever building, debugging, or testing iOS/macOS apps.  
- **Why**: Provides tools like Interface Builder, Simulator, Debugger in one place.  
- **Where**: Installed from the Mac App Store.  
- **How**: Create a project → Write Swift code → Design UI → Run on simulator/device.  

---

## 🦅 Swift
- **What**: A powerful and intuitive programming language created by Apple.  
- **When**: Used to build modern iOS/macOS apps.  
- **Why**: Safer, faster, and more readable than Objective-C.  
- **Where**: Anywhere Apple ecosystem apps are built.  
- **How**: Write Swift files `.swift` and compile with Xcode.  

---

## 📱 UIKit
- **What**: A framework that provides UI components (buttons, labels, views).  
- **When**: While designing iOS app interfaces.  
- **Why**: Offers pre-built UI elements for faster development.  
- **Where**: Imported with `import UIKit`.  
- **How**: Create UI elements programmatically or via Storyboard.  

---

## 🏛️ Foundation
- **What**: Framework providing base functionalities (data, dates, collections).  
- **When**: Used for non-UI tasks.  
- **Why**: Handles core logic while UIKit handles UI.  
- **Where**: Imported with `import Foundation`.  
- **How**: Use classes like `Date`, `Data`, `URL`, `Notification`.  

---

## 🧩 NSObject
- **What**: Base class for most Objective-C & Swift classes.  
- **When**: When you need access to Objective-C runtime features.  
- **Why**: Provides memory management, KVC, KVO.  
- **Where**: Superclass of many UIKit classes.  
- **How**: Inherit your custom classes from NSObject if needed.  

---

## 📜 Versions of Swift & Xcode
- **Swift**: Started in 2014 (Swift 1.0) → Now at Swift 5.10+ 🚀  
- **Xcode**: Released in 2003 → Now Xcode 15+ supports iOS 18.  
- Each version improves **performance, safety, and developer productivity**.  

---

## 🏷️ Class
- **What**: Blueprint for creating objects.  
- **When**: When defining custom models, UIControllers, etc.  
- **Why**: Organizes code and enables OOP concepts.  
- **Where**: Defined in `.swift` files.  
- **How**:  
  ```swift
  class Animal {
      var name: String
      init(name: String) {
          self.name = name
      }
  }
  ```  

---

## 🧬 Subclass
- **What**: A class derived from another class.  
- **When**: To extend or modify parent class behavior.  
- **Why**: Promotes reusability.  
- **Where**: Common in UIKit (e.g., UIViewController subclasses).  
- **How**:  
  ```swift
  class Dog: Animal {
      func bark() { print("Woof!") }
  }
  ```  

---

## 🔗 Inheritance
- **What**: Mechanism to derive a new class from an existing one.  
- **When**: When reusing logic of another class.  
- **Why**: Avoids code duplication.  
- **Where**: Used in OOP design.  
- **How**: `class Dog: Animal { }`  

---

## 🏛️ Superclass of UIButton & UILabel
- **UIButton** → subclass of **UIControl → UIView → UIResponder → NSObject**  
- **UILabel** → subclass of **UIView → UIResponder → NSObject**  

---

## 🤝 Delegate vs DataSource
- **Delegate**: Handles **behavior & events** (e.g., what happens on tap).  
- **DataSource**: Provides **data to a component** (e.g., table rows).  

📌 Example: `UITableView`  
- **DataSource**: Number of rows, cell content.  
- **Delegate**: Row selection, cell height.  

---

## 🎡 UIPickerViewController – Mandatory Delegate Method
- `func pickerView(_ pickerView: UIPickerView, numberOfRowsInComponent component: Int) -> Int`  
- `func pickerView(_ pickerView: UIPickerView, titleForRow row: Int, forComponent component: Int) -> String?`  

Without these → Picker cannot display data.  

---


