# 🔒 Singleton in Swift 🔒

## 1️⃣ Singleton Class

**🔹 What:**
A class that allows only **one instance** to be created and provides a **global point of access**.

**🔹 Who:**
Used by developers when a single shared instance is needed across the app (e.g., shared settings, network manager).

**🔹 When:**
When you want **one shared object** to manage state or resources.

**🔹 Where:**
Inside Swift classes, often as a static property.

**🔹 Why:**
To ensure only one instance exists and to provide global access.

**💡 Example:**

```swift
class NetworkManager {
    static let shared = NetworkManager()
    private init() {}

    func fetchData() {
        print("Fetching data...")
    }
}

NetworkManager.shared.fetchData()
```

---

## 2️⃣ Thread-Safety of Singleton

**🔹 What:**
Singletons are thread-safe if the instance is **created once** and **shared safely across threads**.

**🔹 Who:**
Developers need thread-safe singletons in **multithreaded apps** (network calls, data managers).

**🔹 When:**
When multiple threads may try to access the singleton simultaneously.

**🔹 Where:**
Inside the static property initialization.

**🔹 Why:**
To prevent multiple instances being created accidentally and ensure safe access.

**💡 Example:**

```swift
class Logger {
    static let shared = Logger() // Swift static properties are thread-safe
    private init() {}
    func log(_ message: String) {
        print(message)
    }
}
```

✅ No extra locks needed; Swift ensures thread-safety for static let initialization.

---

## ✅ Quick Revision Notes

* **Singleton** = single instance + global access.
* **Thread-safe** = safe to access from multiple threads.
* Use **private init()** to prevent other instances.
* Access with **ClassName.shared**.

---
