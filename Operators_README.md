# Swift Operators

An operator is a symbol that tells the compiler to perform specific mathematical or logical operations. 
---

## 🔢 1. Arithmetic Operators

Used for mathematical calculations.

| Operator | Description     | Example       |
|----------|-----------------|---------------|
| `+`      | Addition         | `a + b`       |
| `-`      | Subtraction      | `a - b`       |
| `*`      | Multiplication   | `a * b`       |
| `/`      | Division         | `a / b`       |
| `%`      | Remainder        | `a % b`       |

```swift
let sum = 5 + 3
let product = 4 * 2
```

---

## 🟰 2. Assignment Operator

Used to assign values.

```swift
var a = 10
a += 5  // Equivalent to a = a + 5
```

---

## 🔁 3. Comparison Operators

Used to compare two values.

| Operator | Description         | Example     |
|----------|---------------------|-------------|
| `==`     | Equal to             | `a == b`    |
| `!=`     | Not equal to         | `a != b`    |
| `>`      | Greater than         | `a > b`     |
| `<`      | Less than            | `a < b`     |
| `>=`     | Greater than or equal| `a >= b`    |
| `<=`     | Less than or equal   | `a <= b`    |

```swift
if age >= 18 {
    print("Adult")
}
```

---

## 🔀 4. Logical Operators

Used to combine multiple conditions.

| Operator | Description   | Example             |
|----------|---------------|---------------------|
| `&&`     | Logical AND    | `a > 0 && b > 0`    |
| `||`     | Logical OR     | `a > 0 || b > 0`    |
| `!`      | Logical NOT    | `!(a > 0)`          |

```swift
if isLoggedIn && hasPermission {
    print("Access granted")
}
```

---

## 🧮 5. Unary Operators

Operate on a single value.

| Operator | Description        |
|----------|--------------------|
| `-`      | Unary minus         |
| `!`      | Logical NOT         |

```swift
let isFalse = !true
```

---

## ➕➖ 6. Increment & Decrement

```swift
var x = 10
x += 1  // Increment
x -= 1  // Decrement
```

---

## 📦 7. Range Operators

Used for creating ranges.

| Operator | Description         | Example     |
|----------|---------------------|-------------|
| `...`    | Closed range         | `1...5`     |
| `..<`    | Half-open range      | `1..<5`     |

```swift
for i in 1...3 {
    print(i)
}
```
