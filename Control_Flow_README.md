
# Swift Control Flow 
  
---

## 🚦 1. if / else

### 🔹 What:
Used to execute code **based on a condition**.

### 🔹 Why:
To handle **decisions** in your app (e.g., pass/fail, login success/failure).

### 🔹 When:
Use when you want to **check a condition** and respond accordingly.

### 🔹 Where:
Inside functions, loops, or anywhere logic needs branching.

### 🔹 Who:
Used by **all types of apps** — from finance to games.

### ✅ Example:
```swift
let marks = 75
if marks >= 35 {
    print("Pass")
} else {
    print("Fail")
}
```
**Real-life example**: Checking if a student has passed an exam.

---

## 🔁 2. for-in loop

### 🔹 What:
Loops over a **collection or range**.

### 🔹 Why:
To perform **repetitive tasks** like printing values or processing arrays.

### 🔹 When:
When you want to repeat something for a known number of times.

### 🔹 Where:
Used in data processing, UI generation, etc.

### 🔹 Who:
Useful for **developers working with lists or ranges**.

### ✅ Example:
```swift
for day in 1...7 {
    print("Day \(day)")
}
```
**Real-life example**: Displaying days of the week in a planner app.

---

## 🔄 3. while loop

### 🔹 What:
Repeats code **while a condition is true**.

### 🔹 Why:
To continue looping until a condition becomes false.

### 🔹 When:
Use when you **don’t know how many times** the loop should run.

### 🔹 Where:
In places like game loops, login retries, etc.

### 🔹 Who:
Game developers, authentication flows, etc.

### ✅ Example:
```swift
var count = 5
while count > 0 {
    print("Countdown: \(count)")
    count -= 1
}
```
**Real-life example**: Countdown timer in an app.

---

## 🔃 4. repeat-while loop

### 🔹 What:
Like a while loop, but **guarantees at least one execution**.

### 🔹 Why:
To ensure the block runs **at least once** even if the condition is false.

### 🔹 When:
Use when the logic must be performed first before checking the condition.

### 🔹 Where:
In form validation, menu selection, etc.

### 🔹 Who:
Useful in input validation or interactive prompts.

### ✅ Example:
```swift
var pin = 0000
repeat {
    print("Enter PIN:")
    pin = 1234  // simulate user input
} while pin != 1234
print("Access Granted")
```
**Real-life example**: Asking for a correct PIN.

---

## 🔀 5. switch statement

### 🔹 What:
Used to match a value against multiple **possible cases**.

### 🔹 Why:
Cleaner and faster than multiple if-else blocks.

### 🔹 When:
When you want to check **multiple possible values** of a variable.

### 🔹 Where:
Used in menu systems, key input handling, enums, etc.

### 🔹 Who:
Developers handling **multiple known values** or actions.

### ✅ Example:
```swift
let grade = "B"
switch grade {
case "A":
    print("Excellent")
case "B":
    print("Good")
case "C":
    print("Average")
default:
    print("Needs Improvement")
}
```
**Real-life example**: Mapping grades to feedback in an education app.

---

## 📌 Summary Table

| Statement     | Use Case                  | Real-Life Example                  |
|---------------|---------------------------|------------------------------------|
| `if / else`   | Conditional execution     | Pass/fail check                    |
| `for-in`      | Loop through collections  | List days of week                  |
| `while`       | Repeat until false        | Countdown timer                    |
| `repeat-while`| At least one repetition   | Ask for valid input                |
| `switch`      | Multiple value match      | Grade to feedback mapping          |

---


