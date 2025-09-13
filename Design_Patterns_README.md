
# Design Patterns 


---

## 🔹 KVC (Key-Value Coding)
- **What**: A way to access object properties indirectly using string keys.
- **Why**: Provides flexibility when property names are unknown at compile time.
- **When**: When dealing with dynamic data like JSON or reflection.
- **Where**: Common in Swift/Objective-C applications.
- **Who**: Developers needing dynamic property access.
- **Real-Life Example**: Like a **dictionary** in a library – you don’t know the exact page but you look up information using a keyword (key).

---

## 🔹 KVO (Key-Value Observing)
- **What**: A mechanism to observe property value changes.
- **Why**: Helps UI update automatically when data changes.
- **When**: Reactive programming, UI bindings.
- **Where**: iOS/macOS apps observing model changes.
- **Who**: Developers building event-driven apps.
- **Real-Life Example**: A **CCTV camera** observing a door – whenever someone enters, you are notified.

---

## 🔹 Facade Pattern
- **What**: Simplifies a complex system by providing a unified interface.
- **Why**: Hides complexity from the user.
- **When**: When dealing with complex subsystems.
- **Where**: API wrappers, system utilities.
- **Who**: Developers providing easy-to-use libraries.
- **Real-Life Example**: A **TV remote** – hides the complexity of circuits, giving you simple buttons like Power, Volume, and Channel.

---

## 🔹 Adapter Pattern
- **What**: Converts one interface into another.
- **Why**: Makes incompatible classes work together.
- **When**: Integrating legacy code with new systems.
- **Where**: Plug adapters, payment gateways.
- **Who**: Developers connecting different modules.
- **Real-Life Example**: A **mobile charger adapter** – converts wall socket electricity into a format your phone understands.

---

## 🔹 Builder Pattern
- **What**: Step-by-step construction of complex objects.
- **Why**: Avoids complex constructors with many parameters.
- **When**: When creating customizable/complex objects.
- **Where**: Pizza builder, UI builders.
- **Who**: Developers designing configurable products.
- **Real-Life Example**: **Pizza shop** – dough → sauce → cheese → toppings → bake (build step by step).

---

## 🔹 Strategy Pattern
- **What**: Defines interchangeable algorithms.
- **Why**: To choose behavior at runtime.
- **When**: When multiple solutions exist for a problem.
- **Where**: Payment methods, sorting strategies.
- **Who**: Developers building flexible systems.
- **Real-Life Example**: **Google Maps navigation** – you can switch between "fastest route", "shortest route", or "avoid tolls".

---

## 🔹 Factory Pattern
- **What**: Centralized object creation without exposing logic.
- **Why**: Decouples object creation from usage.
- **When**: When you need flexibility in object creation.
- **Where**: Shape factory, car factory.
- **Who**: Developers needing scalable object creation.
- **Real-Life Example**: **Car factory** – you request a Sedan or SUV, factory knows how to build it without you worrying about the process.

---

## 🔹 Command Pattern
- **What**: Encapsulates requests as objects.
- **Why**: Enables undo/redo and decoupling of sender-receiver.
- **When**: When actions should be parameterized or queued.
- **Where**: Remote controls, task schedulers.
- **Who**: Developers implementing event-driven commands.
- **Real-Life Example**: **TV remote buttons** – pressing "Volume Up" sends a command object to the TV.

---

## 🔹 Composite Pattern
- **What**: Composes objects into tree structures.
- **Why**: Treats individual and composite objects uniformly.
- **When**: When dealing with hierarchical structures.
- **Where**: File systems, organization hierarchies.
- **Who**: Developers designing recursive structures.
- **Real-Life Example**: **Company hierarchy** – an employee (leaf) or department (composite) both implement the same behavior like "show details".

---

## 🔹 Template Method Pattern
- **What**: Defines algorithm skeleton, letting subclasses override steps.
- **Why**: Promotes code reuse with flexibility.
- **When**: When algorithms have fixed structure but customizable steps.
- **Where**: Cooking recipes, games.
- **Who**: Developers enforcing a common algorithm structure.
- **Real-Life Example**: **Cooking recipe** – boil water, add ingredients, cook – the skeleton is fixed, but ingredients differ per recipe.

---

## ✅ Quick Real-Life Summary
- **KVC/KVO** → Dictionary lookup & CCTV monitoring.  
- **Facade** → TV remote.  
- **Adapter** → Mobile charger adapter.  
- **Builder** → Pizza shop.  
- **Strategy** → Google Maps routes.  
- **Factory** → Car factory.  
- **Command** → TV remote buttons.  
- **Composite** → Company hierarchy.  
- **Template** → Cooking recipe.  

---
