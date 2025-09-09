# ✨ Swift Properties ✨

## 1️⃣ Stored Properties

**🔹 What:**
A variable or constant that stores **actual data** as part of a class, struct, or enum instance.

**🔹 Who:**
Used whenever you need to **store data** in an object.

**🔹 When:**
When you want to hold a value that belongs to an instance.

**🔹 Where:**
Inside classes or structs.

**🔹 Why:**
To store state or values for each instance.

**💡 Example:**

```swift
struct Person {
    var name: String
    let age: Int
}

let person = Person(name: "Rasool", age: 25)
print(person.name) // Rasool
```

---

## 2️⃣ Computed Properties

**🔹 What:**
A property that **calculates a value** instead of storing it.

**🔹 Who:**
Used when the value depends on other properties or needs to be calculated dynamically.

**🔹 When:**
When you don’t want to store data but derive it.

**🔹 Where:**
Inside classes, structs, or enums.

**🔹 Why:**
To provide a value dynamically and reduce stored data.

**💡 Example:**

```swift
struct Rectangle {
    var width: Double
    var height: Double
    var area: Double {
        return width * height
    }
}

let rect = Rectangle(width: 5, height: 10)
print(rect.area) // 50
```

---

## 3️⃣ Lazy Properties

**🔹 What:**
A property that is **initialized only when first used**.

**🔹 Who:**
Used for expensive computations or objects you don’t want to create immediately.

**🔹 When:**
When initialization is costly or may not always be needed.

**🔹 Where:**
Inside classes or structs.

**🔹 Why:**
To save memory and improve performance.

**💡 Example:**

```swift
class DataManager {
    lazy var data = loadData()
    func loadData() -> [String] {
        print("Loading data...")
        return ["A", "B", "C"]
    }
}

let manager = DataManager()
print(manager.data) // triggers loadData()
```

---

## 4️⃣ Static vs Class Properties/Methods

**🔹 Static:**

* Belongs to the type, not instance.
* Cannot be overridden.

**💡 Example:**

```swift
struct Math {
    static let pi = 3.14
    static func square(_ x: Int) -> Int { x * x }
}
print(Math.pi)
print(Math.square(5))
```

**🔹 Class:**

* Also belongs to the type.
* **Can be overridden** by subclass.

**💡 Example:**

```swift
class Animal {
    class func sound() { print("Some sound") }
    static func type() { print("Animal type") }
}
class Dog: Animal {
    override class func sound() { print("Bark") }
}
Animal.sound() // Some sound
Dog.sound()    // Bark
Dog.type()     // Animal type
```

---

## 5️⃣ Private Class

**🔹 What:**
A class restricted to **current file or scope**.

**🔹 Who:**
Used to hide implementation details from other files.

**🔹 When:**
When you want encapsulation and limit access.

**🔹 Where:**
Inside the same Swift file.

**🔹 Why:**
To prevent unintended access and maintain clean architecture.

**💡 Example:**

```swift
private class Secret {
    func hello() { print("Hello") }
}

class Normal {
    func test() {
        let s = Secret()
        s.hello() // works inside same file
    }
}
```

---

## ✅ Quick Revision Notes

* **Stored** = stores real value.
* **Computed** = calculates value dynamically.
* **Lazy** = initialized on first use.
* **Static** = type property, not overridable.
* **Class** = type property, overridable.
* **Private Class** = restricted scope to hide implementation.

---
