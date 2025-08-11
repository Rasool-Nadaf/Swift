
Swift Concepts

---

## 1. Class

**What:**  
A blueprint or template to create objects. It defines properties (data) and methods (functions) that describe an object.

**Why:**  
To organize code and create reusable components with properties and behaviors.

**When:**  
Use when you want to model real-world entities or organize your code with objects.

**Where:**  
In your Swift files, typically to define view controllers, data models, or helpers.

**How:**  
```swift
class Person {
    var name: String
    func sayHello() {
        print("Hello, \(name)")
    }
}
```

---

## 2. Subclass

**What:**  
A class that inherits properties and methods from another class (called superclass), and can add or override functionality.

**Why:**  
To reuse and extend existing code without rewriting it.

**When:**  
Use when you want a specialized version of a class with extra or modified features.

**Where:**  
When creating custom views, view controllers, or models that are based on a generic class.

**How:**  
```swift
class Animal {
    func makeSound() {
        print("Animal sound")
    }
}

class Dog: Animal {
    override func makeSound() {
        print("Bark")
    }
}
```

---

## 3. Method

**What:**  
A function defined inside a class or struct that performs a task related to the object.

**Why:**  
To define behaviors for your objects.

**When:**  
Whenever you want your objects to do something or manipulate their data.

**Where:**  
Inside classes or structs.

**How:**  
```swift
class Car {
    func startEngine() {
        print("Engine started")
    }
}
```

---

## 4. Alert (UIAlertController)

**What:**  
A pop-up message box to show information or get user confirmation/input.

**Why:**  
To notify users about important information or ask for decisions.

**When:**  
Use when you want to show messages, errors, warnings, or ask simple questions.

**Where:**  
Usually in a view controller where user interaction happens.

**How:**  
```swift
let alert = UIAlertController(title: "Alert", message: "This is a message.", preferredStyle: .alert)
alert.addAction(UIAlertAction(title: "OK", style: .default))
present(alert, animated: true)
```

---

## 5. UITextField Delegate Methods

**What:**  
Methods provided by `UITextFieldDelegate` protocol to manage and respond to text field events (like editing start, end, or return key pressed).

**Why:**  
To control behavior when the user interacts with text fields (e.g., validation, keyboard control).

**When:**  
Use when you want to customize text field behavior or respond to user input.

**Where:**  
In your view controller or class that acts as the delegate for the text field.

**How:**  
1. Make your class conform to `UITextFieldDelegate`:
   ```swift
   class ViewController: UIViewController, UITextFieldDelegate {
       ...
   }
   ```
2. Set the delegate:
   ```swift
   myTextField.delegate = self
   ```
3. Implement delegate methods you need, e.g.:
   ```swift
   func textFieldShouldReturn(_ textField: UITextField) -> Bool {
       textField.resignFirstResponder() // hides keyboard
       return true
   }

   func textFieldDidBeginEditing(_ textField: UITextField) {
       print("Started editing")
   }
   ```

---

If you want, I can also provide example code for all combined in one Swift file! Would you like that?
