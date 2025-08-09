# Functions in Swift

## Function
**What:** A function is a reusable block of code that performs a specific task.  
**When:** When you need to execute the same set of instructions multiple times.  
**Why:** To improve code reusability, readability, and maintainability.  
**Where:** Used in almost all programming tasks, such as calculations, data processing, etc.  
**How:** By defining it with a name, parameters (optional), and a body, then calling it.  

**Real World Example:** A coffee machine function that takes an order and makes coffee.

**Code Example:**
```swift
func greet(name: String) -> String {
    return "Hello, \(name)!"
}

print(greet(name: "Rasool"))
```

---

## Nested Function
**What:** A function defined inside another function.  
**When:** When a helper function is only needed inside another function.  
**Why:** To encapsulate logic and avoid polluting the global scope.  
**Where:** Used in closures, decorators, and scope management.  
**How:** Define a function within another function and call it inside.  

**Real World Example:** A hotel booking function containing an inner function to calculate discounts.

**Code Example:**
```swift
func outerFunction(name: String) -> String {
    func innerFunction() -> String {
        return "Hello, \(name)!"
    }
    return innerFunction()
}

print(outerFunction(name: "Rasool"))
```

---

## Function Overload
**What:** The ability to define multiple functions with the same name but different parameters.  
**When:** When the same operation is needed for different data types or parameter counts.  
**Why:** To simplify the API and make code more intuitive.  
**Where:** Common in statically typed languages like Swift, C++, and Java.  
**How:** Provide multiple function definitions with different parameter types or counts.

**Real World Example:** A print function that can print strings, numbers, or lists.

**Code Example:**
```swift
func add(a: Int, b: Int) -> Int {
    return a + b
}

func add(a: Int, b: Int, c: Int) -> Int {
    return a + b + c
}

print(add(a: 5, b: 10))
print(add(a: 5, b: 10, c: 15))
```

---

## Recursion
**What:** A function calling itself directly or indirectly.  
**When:** When a problem can be divided into smaller, similar subproblems.  
**Why:** To solve problems like tree traversal, factorial, Fibonacci sequence elegantly.  
**Where:** Used in algorithms, data structures, and problem-solving.  
**How:** Call the same function inside itself with modified parameters, define a base case to stop recursion.

**Real World Example:** A folder explorer that goes through subfolders recursively.

**Code Example:**
```swift
func factorial(_ n: Int) -> Int {
    if n == 0 {
        return 1
    }
    return n * factorial(n - 1)
}

print(factorial(5))
```
