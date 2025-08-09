# 📦 Collections in Swift

---

## 📚 Arrays  
**📝 What:** An ordered collection of values of the same type.  

**⏳ When:** When you need to store items in a specific sequence.  

**🎯 Why:** To keep track of elements where order matters and allow duplicates.  

**🌍 Where:** Used for lists, queues, ordered datasets.  

**⚙️ How:** Create with square brackets `[]` and access by index starting from `0`.  

💡 **Real World Example:** A to-do list where tasks are in a specific order.  

```swift
var fruits = ["Apple", "Banana", "Mango"]
fruits.append("Orange")       // Add element
print(fruits[1])               // Access element
fruits.remove(at: 0)           // Remove element
print(fruits)
```

---

## 🪄 Sets  
**📝 What:** An unordered collection of unique values.  

**⏳ When:** When you need to store elements without duplicates.  

**🎯 Why:** To ensure all items are unique and quickly check membership.  

**🌍 Where:** Used for tags, unique IDs, filtering duplicates.  

**⚙️ How:** Create with curly braces `{}` or `Set()` and elements are stored without order.  

💡 **Real World Example:** A collection of unique course codes in a university.  

```swift
var courseCodes: Set = ["CS101", "MATH201", "ENG102"]
courseCodes.insert("BIO301")     // Add element
print(courseCodes.contains("CS101")) // Check existence
courseCodes.remove("ENG102")     // Remove element
print(courseCodes)
```

---

## 🗂️ Dictionaries  
**📝 What:** An unordered collection of key-value pairs.  

**⏳ When:** When you want to associate a value with a unique key.  

**🎯 Why:** To look up data quickly using a key.  

**🌍 Where:** Used for contact lists, settings, key-value databases.  

**⚙️ How:** Create with square brackets `[:]` where each key maps to a value.  

💡 **Real World Example:** A phonebook where names are keys and phone numbers are values.  

```swift
var phoneBook = ["Alice": "123-456-7890", "Bob": "987-654-3210"]
phoneBook["Charlie"] = "555-555-5555"    // Add key-value pair
print(phoneBook["Alice"] ?? "Not Found") // Access by key
phoneBook.removeValue(forKey: "Bob")     // Remove entry
print(phoneBook)
```
