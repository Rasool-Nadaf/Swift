# iOS Development Concepts

## 1. Cocoa

**What:** A collection of frameworks for macOS development.\
**Why:** Provides APIs for building macOS applications.\
**When:** Used when building apps for macOS.\
**Where:** Includes frameworks like Foundation and AppKit.\
**How:** Developers use Objective-C or Swift with Cocoa frameworks.

------------------------------------------------------------------------

## 2. Cocoa Touch

**What:** A UI framework for building iOS, iPadOS, watchOS, and tvOS
apps.\
**Why:** Provides essential UI components and controls.\
**When:** Used when building iOS-based apps.\
**Where:** Includes UIKit, MapKit, AVKit, etc.\
**How:** Developers use Swift/Objective-C with Cocoa Touch frameworks.

------------------------------------------------------------------------

## 3. View Controller Life Cycle Methods

### Methods:

1.  **`loadView()`**
    -   Called when the controller's view is created programmatically.\
2.  **`viewDidLoad()`**
    -   Called after the view is loaded into memory.\
3.  **`viewWillAppear(_:)`**
    -   Called just before the view appears on screen.\
4.  **`viewDidAppear(_:)`**
    -   Called right after the view is shown.\
5.  **`viewWillDisappear(_:)`**
    -   Called before the view is removed.\
6.  **`viewDidDisappear(_:)`**
    -   Called when the view has disappeared.\
7.  **`didReceiveMemoryWarning()`** *(iOS \< 13)*
    -   Called when system is low on memory.\

------------------------------------------------------------------------

## 4. Object Life Cycle

**Phases:** 1. **Initialization**\
- Objects created with `init()` method.\
- Example: `let obj = MyClass()`

2.  **Usage**
    -   The object performs tasks until it's no longer needed.
3.  **Deallocation**
    -   ARC automatically frees memory when reference count = 0.

------------------------------------------------------------------------

## 5. ARC (Automatic Reference Counting)

**What:** A memory management system in Swift/Objective-C.\
**Why:** Prevents memory leaks by managing object references
automatically.\
**When:** Always active in Swift.\
**Where:** Works for both classes and objects.\
**How:**\
- Strong Reference: Keeps object alive.\
- Weak Reference: Does not increase count, can become `nil`.\
- Unowned Reference: Non-optional, must always have a value.

------------------------------------------------------------------------

## 6. Storyboard

**What:** A visual interface builder file in Xcode.\
**Why:** Helps design multiple screens and navigation flow in one
place.\
**When:** Used to build apps with multiple connected views.\
**Where:** Found in `.storyboard` files.\
**How:** Drag & drop UI components, connect using segues.

------------------------------------------------------------------------

## 7. XIB (Interface Builder File)

**What:** A file containing a single screen's UI.\
**Why:** Good for reusable/custom UI components.\
**When:** Used when designing a single screen independently.\
**Where:** Found in `.xib` files.\
**How:** Loaded programmatically using `Bundle.main.loadNibNamed`.

------------------------------------------------------------------------

## Summary

-   **Cocoa** = macOS frameworks.\
-   **Cocoa Touch** = iOS frameworks.\
-   **View Controller Life Cycle** = Methods from loading → appearing →
    disappearing.\
-   **Object Life Cycle** = Init → Use → Deallocation (handled by ARC).\
-   **ARC** = Automatic memory management.\
-   **Storyboard** = Visual flow of multiple screens.\
-   **XIB** = UI for a single reusable screen.
