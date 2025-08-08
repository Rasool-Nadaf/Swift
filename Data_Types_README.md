
# 📘 Swift Data Types:

---

## 1. `Int` (Integer)
- **What**: Stores whole numbers (positive, negative, or zero).
- **Why**: General-purpose integer storage.
- **When**: When precision matters and you don’t need to limit memory size.
- **Where**: Counting, indexing, IDs.
- **How**: `let age: Int = 25`
- **Range**:
  - `Int32`: -2,147,483,648 to 2,147,483,647
  - `Int64`: -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807
- **Example**: Number of students in a school.

---

## 2. `UInt` (Unsigned Integer)
- **What**: Stores only positive integers.
- **Why**: Saves memory and increases range by excluding negative numbers.
- **When**: When negative values are not required.
- **Where**: Indexes, counters.
- **How**: `let index: UInt = 10`
- **Range**:
  - `UInt32`: 0 to 4,294,967,295
  - `UInt64`: 0 to 18,446,744,073,709,551,615
- **Example**: Total steps walked today.

---

## 3. `Int8` / `UInt8` (Byte)
- **What**: 8-bit signed (`Int8`) or unsigned (`UInt8`) integer.
- **Why**: Use when memory is highly constrained.
- **When**: Low-memory environments like IoT, embedded systems.
- **Where**: RGB color values, status flags.
- **How**: `let red: UInt8 = 255`
- **Range**:
  - `Int8`: -128 to 127
  - `UInt8`: 0 to 255
- **Example**: Number of students in class.

---

## 4. `Int16` / `UInt16` (Short)
- **What**: 16-bit signed (`Int16`) or unsigned (`UInt16`) integer.
- **Why**: Use when a small range is sufficient and memory saving is desired.
- **When**: For storing small values.
- **Where**: Ports, status codes, compact data storage.
- **How**: `let port: UInt16 = 8080`
- **Range**:
  - `Int16`: -32,768 to 32,767
  - `UInt16`: 0 to 65,535
- **Example**: Network port number.

---

## 5. `Float`
- **What**: 32-bit decimal number.
- **Why**: Use when precision isn't critical and memory needs to be conserved.
- **When**: Low-precision scientific values.
- **Where**: Animation speed, temperature.
- **How**: `let temperature: Float = 36.6`
- **Range**: ±1.18 × 10⁻³⁸ to ±3.4 × 10³⁸
- **Example**: Body temperature sensor.

---

## 6. `Double`
- **What**: 64-bit decimal number.
- **Why**: Use for high-precision calculations.
- **When**: Financial, GPS, scientific calculations.
- **Where**: Banking, navigation apps.
- **How**: `let pi: Double = 3.1415926535`
- **Range**: ±2.23 × 10⁻³⁰⁸ to ±1.79 × 10³⁰⁸
- **Example**: Bank interest rate.

---

## 7. `Bool`
- **What**: Stores true or false.
- **Why**: Used for logical decisions.
- **When**: Conditional flows or toggles.
- **Where**: Switches, flags.
- **How**: `let isActive: Bool = true`
- **Example**: Is light on?

---

## 8. `Character`
- **What**: Single Unicode character.
- **Why**: For working with individual letters/symbols.
- **When**: When only one character is needed.
- **Where**: Grades, initials.
- **How**: `let grade: Character = "A"`
- **Example**: Grade in a report card.

---

## 9. `String`
- **What**: Collection of characters.
- **Why**: For working with text.
- **When**: Whenever textual data is handled.
- **Where**: Names, messages, labels.
- **How**: `let name: String = "Alice"`
- **Example**: User's email or bio.

---

## 10. `Array`
- **What**: Ordered collection of similar types.
- **Why**: To manage a list of data.
- **When**: When data needs to be accessed in sequence.
- **Where**: Images in a gallery, tasks.
- **How**: `let cities = ["New York", "Tokyo"]`
- **Example**: List of friends.

---

## 11. `Tuple`
- **What**: Group of multiple values (can be different types).
- **Why**: Useful for returning multiple values from a function.
- **When**: Bundling temporary data.
- **Where**: Coordinates, function outputs.
- **How**: `let person = (name: "Bob", age: 30)`
- **Example**: Person profile summary.

---

## 12. `Optional`
- **What**: A value that may or may not be present.
- **Why**: Prevents crashes due to `nil` values.
- **When**: When values may be missing.
- **Where**: Form fields, optional features.
- **How**: `var nickname: String? = nil`
- **Example**: Middle name in user profile.

---

✅ **Summary – When to Use Which Integer Type:**

| Type     | Size | Signed | Range (approx)                      | Use When                                     |
|----------|------|--------|-------------------------------------|----------------------------------------------|
| `Int8`   | 1B   | Yes    | -128 to 127                         | Color values, small counters                 |
| `UInt8`  | 1B   | No     | 0 to 255                            | Byte-sized data, flags                       |
| `Int16`  | 2B   | Yes    | -32,768 to 32,767                   | Status codes, small integers                 |
| `UInt16` | 2B   | No     | 0 to 65,535                         | Ports, hardware I/O                          |
| `Int`    | 4B/8B| Yes    | Depends on platform                 | General-purpose integers                     |
| `UInt`   | 4B/8B| No     | Positive integers only              | Indexing, memory-safe IDs                    |
| `Float`  | 4B   | -      | ±3.4 × 10^38                        | Low-precision decimal numbers                |
| `Double` | 8B   | -      | ±1.79 × 10^308                      | High-precision decimal numbers               |

---

📌 **Tip**: In Swift, `Int` and `Double` are preferred by default unless optimization is required.
