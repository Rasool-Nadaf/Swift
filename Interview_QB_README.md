# Swift Interview Preparation Guide

## Part 1 â€” Swift Basics

### Variables (var) & Constants (let)
Q1: What is the difference between `var` and `let`?  
A: `var` is used for mutable variables (values can change). `let` is for constants (values cannot change).

Q2: Why should you prefer `let` over `var`?  
A: Immutability makes code safer, reduces bugs, and improves performance.

Q3: Can a constant (`let`) be changed if itâ€™s a reference type?  
A: You cannot reassign the reference, but the contents of the object (like array elements) can change if itâ€™s a class type.

---

### Data Types (Int, Float, Double, Bool, String, Character)
Q1: What is the difference between Float and Double?  
A: `Float` is 32-bit (less precision), `Double` is 64-bit (higher precision).

Q2: What is the default floating type in Swift?  
A: `Double`.

Q3: What is the difference between Character and String?  
A: `Character` stores a single Unicode symbol, `String` stores a collection of characters.

---

### Type Inference & Type Annotation
Q1: What is type inference?  
A: Swift automatically detects the type based on the initial value.

Q2: What is type annotation?  
A: Explicitly defining a type (e.g., `let age: Int = 25`).

---

### Operators
Q1: What are arithmetic operators in Swift?  
A: `+`, `-`, `*`, `/`, `%`.

Q2: What is the difference between `==` and `===`?  
A: `==` checks value equality, `===` checks reference identity (classes only).

Q3: What is the nil-coalescing operator?  
A: `??` provides a default value if optional is nil.

---

### Optionals (?, !)
Q1: What is an Optional?  
A: A type that may hold a value or nil, written as `?`.

Q2: What is force unwrapping?  
A: Using `!` to access optional value directly (unsafe if nil).

Q3: What is optional binding?  
A: Safely unwrap optionals using `if let` or `guard let`.

Q4: What is optional chaining?  
A: Accessing properties/methods of an optional safely using `?`.

---

### Guard Statement
Q1: What is guard used for?  
A: To exit early if a condition fails, ensuring cleaner code.

Q2: Difference between `if let` and `guard let`?  
A: `if let` unwraps for a limited scope, `guard let` keeps unwrapped values available after the guard block.

---

### Control Flow & Loops
Q1: What loops are available in Swift?  
A: `for-in`, `while`, `repeat-while`.

Q2: What is the difference between break and continue?  
A: `break` exits the loop, `continue` skips the current iteration.

---

### Functions
Q1: What is the syntax of a function?  
A: `func name(parameters) -> ReturnType { }`.

Q2: What are default parameters?  
A: Parameters with default values if not passed.

Q3: What is inout parameter?  
A: Passes variable by reference using `inout`.

---

### Closures & Higher Order Functions
Q1: What is a closure?  
A: A self-contained block of code that can capture values.

Q2: What is trailing closure syntax?  
A: Placing closure outside the function parentheses for readability.

Q3: What is an escaping closure?  
A: A closure that is executed after the function returns.

Q4: What is an autoclosure?  
A: A closure created automatically to wrap an expression.

Q5: Explain map, filter, reduce.  
A: `map` transforms elements, `filter` selects matching elements, `reduce` combines into a single value.

---

### Enumerations
Q1: What are enums?  
A: A type with a group of related values.

Q2: What are raw values in enums?  
A: Predefined constant values (e.g., Int, String).

Q3: What are associated values in enums?  
A: Values attached to specific enum cases.

---

## Part 2 â€” Collections

### Arrays
Q1: What is an array in Swift?  
A: Ordered collection of values.

Q2: Difference between mutable and immutable arrays?  
A: Arrays with `let` are immutable, with `var` are mutable.

---

### Dictionaries
Q1: What is a dictionary?  
A: Key-value pair collection.

Q2: Can dictionary keys be duplicated?  
A: No, keys must be unique.

---

### Sets
Q1: What is a set?  
A: Unordered collection of unique elements.

Q2: Difference between array and set?  
A: Array is ordered and can have duplicates, set is unordered and unique.

---

### Ranges
Q1: What is the difference between `..<` and `...`?  
A: `..<` excludes the upper bound, `...` includes it.

---

### Collection Methods
Q1: Common array methods?  
A: `append`, `remove`, `insert`, `filter`, `map`, `reduce`.

---

## Part 3 â€” Object-Oriented Programming (OOP) in Swift

### Classes & Structs
Q1: Difference between class and struct?  
A: Class is reference type, struct is value type.

Q2: When to use struct vs class?  
A: Use struct for lightweight data, class for inheritance and reference sharing.

---

### Properties
Q1: What are stored and computed properties?  
A: Stored hold data, computed calculate values dynamically.

Q2: What is a lazy property?  
A: Initialized only when first accessed.

Q3: What is a static property?  
A: Belongs to the type, not an instance.

---

### Property Observers
Q1: What are willSet and didSet?  
A: Observers that run before/after a property value changes.

---

### Methods & Initializers
Q1: What are instance and class methods?  
A: Instance methods work on objects, class/static methods work on the type.

Q2: What are designated and convenience initializers?  
A: Designated fully initializes, convenience calls another initializer.

Q3: What is a failable initializer?  
A: Returns nil if initialization fails.

---

### Inheritance & Polymorphism
Q1: What is inheritance?  
A: A class can inherit properties/methods from another.

Q2: What is method overriding?  
A: Subclass provides its own implementation of a parent method.

Q3: What is polymorphism?  
A: One interface, many implementations (e.g., overriding methods).

---

### Encapsulation & Abstraction
Q1: What is encapsulation?  
A: Hiding implementation details and exposing only necessary parts.

Q2: What is abstraction?  
A: Representing essential features without showing background details.

---

### Protocols & Extensions
Q1: What is a protocol?  
A: A contract that defines required methods/properties.

Q2: What are protocol extensions?  
A: Provide default implementation to conforming types.

Q3: What is the difference between protocol and abstract class?  
A: Protocol has no implementation, abstract class can have partial implementation.

---

### Generics
Q1: What are generics?  
A: Write flexible and reusable functions/classes with placeholder types.

---

### Access Control
Q1: Explain access control levels.  
A: `open` (anywhere, subclassable), `public` (anywhere, not subclassable outside module), `internal` (default, within module), `fileprivate` (within file), `private` (within scope).

---

### Error Handling
Q1: How does Swift handle errors?  
A: Using `do-try-catch` blocks.

Q2: Difference between try?, try!, and try?  
A: `try?` returns optional, `try!` crashes on error, `try` requires catch.

---

### Memory Management
Q1: What is ARC?  
A: Automatic Reference Counting, manages memory automatically.

Q2: What are strong, weak, and unowned references?  
A: Strong increases count, weak doesnâ€™t (optional), unowned doesnâ€™t (non-optional).

Q3: What is a retain cycle?  
A: When two objects strongly reference each other, preventing deallocation.

Q4: How do capture lists prevent retain cycles?  
A: By marking captured references as `[weak self]` or `[unowned self]`.

---

### Singleton Pattern
Q1: What is a singleton?  
A: A class with only one instance globally accessible.

Q2: How do you create one in Swift?  
A: `static let shared = MyClass()`.

---

## Part 4 â€” UIKit + Storyboard Concepts

### MVC Design Pattern
Q1: What is MVC?  
A: Model-View-Controller pattern to separate concerns.

---

### UIViewController Lifecycle
Q1: What are main lifecycle methods?  
A: `viewDidLoad`, `viewWillAppear`, `viewDidAppear`, `viewWillDisappear`, `viewDidDisappear`.

---

### IBOutlet, IBAction
Q1: What is IBOutlet?  
A: Connection from storyboard to code for UI elements.

Q2: What is IBAction?  
A: Function triggered by user interactions like button taps.

---

### UITableView & UICollectionView
Q1: Difference between UITableView and UICollectionView?  
A: Table is single column, collection supports grid layouts.

Q2: What protocols are required?  
A: `UITableViewDataSource`, `UITableViewDelegate`.

---

### Delegates & Protocols
Q1: What is a delegate?  
A: A design pattern where one object acts on behalf of another.

---

### Navigation & Tab Bar Controller
Q1: What is UINavigationController?  
A: Manages a stack of view controllers.

Q2: What is UITabBarController?  
A: Provides tab-based navigation.

---

### Segues & Passing Data
Q1: What is a segue?  
A: Transition between two view controllers in storyboard.

Q2: How to pass data between controllers?  
A: Using `prepare(for:sender:)` or delegation.

---

### Auto Layout & Stack Views
Q1: What is Auto Layout?  
A: A constraint-based layout system for adaptive UI.

Q2: What are stack views?  
A: Simplify layout by stacking views horizontally or vertically.

---

### Gesture Recognizers
Q1: What are gesture recognizers?  
A: Objects that detect gestures like taps, swipes, pinches.

---

### WKWebView
Q1: What is WKWebView?  
A: A modern web view for displaying web content.

---

### Alerts & Action Sheets
Q1: How to display alerts?  
A: Using `UIAlertController` with `.alert` or `.actionSheet` style.
