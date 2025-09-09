# ✨ Closures in Swift ✨

## 1️⃣ Closure

**🔹 What:**
A closure is a self-contained block of code that can be passed around and executed later, similar to a function but without a name.

**🔹 Who:**
Swift developers use closures to write reusable, inline code blocks for callbacks, completion handlers, or functional programming.

**🔹 When:**
When you want to pass code as a parameter, store it for later, or execute it dynamically.

**🔹 Where:**
Inside functions, classes, structs, or as standalone variables.

**🔹 Why:**
Closures make code flexible and concise. They can capture values from the surrounding context, enabling dynamic behavior.

**💡 Example:**

```swift
let greet = { print("Hello World") }
greet() // prints Hello World
```

---

## 2️⃣ Closure Capture

**🔹 What:**
A closure can capture variables and constants from the surrounding scope and use them even after the scope ends.

**🔹 Who:**
Used whenever a closure needs to remember variables outside its body.

**🔹 When:**
When a closure uses variables/constants defined outside its own body.

**🔹 Where:**
Anywhere a closure is defined (functions, classes, structs).

**🔹 Why:**
To allow closures to retain access to external variables and update or use them later.

**💡 Example:**

```swift
func makeCounter() -> () -> Int {
    var count = 0
    let counterClosure = { () -> Int in
        count += 1
        return count
    }
    return counterClosure
}

let counter = makeCounter()
print(counter()) // 1
print(counter()) // 2
```

---

## 3️⃣ Escaping Closures

**🔹 What:**
A closure that escapes the function body and runs after the function returns. Marked with `@escaping`.

**🔹 Who:**
Used in asynchronous tasks like network calls or delayed operations.

**🔹 When:**
When the closure is executed later, not immediately.

**🔹 Where:**
Completion handlers, URLSession, background tasks.

**🔹 Why:**
Swift needs to know the closure may be stored and used after the function finishes.

**💡 Example:**

```swift
func doLater(closure: @escaping () -> Void) {
    DispatchQueue.main.asyncAfter(deadline: .now() + 2) {
        closure()
    }
}

doLater {
    print("Runs after 2 seconds")
}
```

---

## 4️⃣ Capture Block `[weak self]`

**🔹 What:**
A syntax to control how variables are captured in closures, mainly to avoid retain cycles.

**🔹 Who:**
Used when closures capture objects like `self` in classes.

**🔹 When:**
When closures reference `self` or other class instances and might be stored.

**🔹 Where:**
Before closure parameters: `[weak self]` or `[unowned self]`.

**🔹 Why:**
To prevent memory leaks caused by strong reference cycles.

**💡 Example:**

```swift
class MyClass {
    var value = 10
    func doSomething() {
        DispatchQueue.main.asyncAfter(deadline: .now() + 1) { [weak self] in
            print(self?.value ?? 0)
        }
    }
}
```

---

## ✅ Quick Revision Notes

* **✨ Closure** = self-contained block of code.
* **💫 Closures capture** variables from surrounding scope.
* **⏳ Escaping closures** run after the function returns.
* **⚠️ Capture block `[weak self]`** avoids retain cycles.
* Use `@escaping` only when closure runs later.
* `[weak self]` is necessary in closures inside classes to prevent memory leaks.

---

