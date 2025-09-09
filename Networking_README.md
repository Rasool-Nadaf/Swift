# 🌐 Networking in Swift 🌐

## 1️⃣ NSURLSession vs NSURLConnection

**🔹 What:**

* `NSURLConnection` = older API for network requests.
* `NSURLSession` = modern, flexible API with more control over configuration and tasks.

**🔹 Who:**
Used by developers to fetch data, download files, or upload content.

**🔹 When:**

* `NSURLConnection` = older projects, deprecated.
* `NSURLSession` = current projects, supports background tasks.

**🔹 Where:**
Inside Swift/iOS apps where networking is required.

**🔹 Why:**

* `NSURLSession` allows better customization, background downloads, and better performance.

**💡 Example:**

```swift
let url = URL(string: "https://api.github.com")!
let task = URLSession.shared.dataTask(with: url) { data, response, error in
    if let data = data {
        print(String(data: data, encoding: .utf8)!)
    }
}
task.resume()
```

---

## 2️⃣ URLSession Tasks

### a) Data Task

**What:** Fetch small data like JSON or HTML.

```swift
let task = URLSession.shared.dataTask(with: url) { data, response, error in
    // handle data
}
task.resume()
```

### b) Download Task

**What:** Download files to temporary location.

```swift
let task = URLSession.shared.downloadTask(with: url) { tempURL, response, error in
    // handle file
}
task.resume()
```

### c) Upload Task

**What:** Upload files or data to server.

```swift
let task = URLSession.shared.uploadTask(with: request, fromFile: fileURL) { data, response, error in
    // handle response
}
task.resume()
```

### d) Stream Task

**What:** Continuous data streams like sockets.

```swift
// less common, used for TCP connections
```

---

## 3️⃣ Alamofire vs NSURLSession

**🔹 What:**

* `Alamofire` = third-party networking library built on NSURLSession.

**🔹 Who:**
Developers who want simplified syntax, chaining, and built-in JSON handling.

**🔹 When:**
When you want cleaner code, built-in response handling, and less boilerplate.

**🔹 Where:**
In Swift projects using CocoaPods, SwiftPM, or Carthage.

**🔹 Why:**

* Easier syntax
* Automatic JSON serialization
* Request chaining
* Built-in response validation

**💡 Example:**

```swift
Alamofire.request("https://api.github.com").responseJSON { response in
    print(response.value)
}
```

---

## ✅ Quick Revision Notes

* **NSURLSession** = modern, flexible networking.
* **DataTask** = small data fetch.
* **DownloadTask** = files.
* **UploadTask** = upload files/data.
* **StreamTask** = sockets/continuous stream.
* **Alamofire** = simplifies NSURLSession with cleaner syntax and utilities.

---
