# 📘 UITableView Concepts

## 🔹 1. Mandatory Methods of UITableView

-   **`tableView(_:numberOfRowsInSection:)`** → Tells how many rows
    should be displayed in each section.\
-   **`tableView(_:cellForRowAt:)`** → Provides the cell (content) for
    each row in the table.

👉 Without these methods, the table view cannot show any data.\
Other methods like `numberOfSections(in:)` are optional (default is 1).

------------------------------------------------------------------------

## 🔹 2. Superclass of UITableView

`UITableView` is a subclass of `UIScrollView`, which is itself a
subclass of `UIView`.\


### Hierarchy:

-   NSObject\
    ⬇\
-   UIResponder\
    ⬇\
-   UIView\
    ⬇\
-   UIScrollView\
    ⬇\
-   UITableView

------------------------------------------------------------------------


