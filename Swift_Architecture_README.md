# Swift Architecture Concepts 

## Access Token & Refresh Token
- **What:** Access token is a credential to access APIs; Refresh token is used to obtain new access tokens without re-authentication.
- **Why:** Ensures secure, temporary, and continuous access without storing user credentials repeatedly.
- **When:** Use access tokens for API calls and refresh tokens when the access token expires.
- **Where:** Common in authentication flows (OAuth2, Firebase, Google APIs).
- **Who:** Used by client apps, servers, and APIs in secure communication.

## Architecture vs Design Pattern
- **What:** Architecture defines the overall structure (MVC, MVVM), while design patterns solve specific coding problems (Singleton, Observer).
- **Why:** Architecture guides large-scale design; patterns improve code reusability and readability.
- **When:** Architecture is chosen at the start; patterns are applied when solving problems in implementation.
- **Where:** Architecture applies to the whole app; design patterns apply to classes, methods, and components.
- **Who:** Developers and architects use both to maintain scalable software.

## Static vs Dynamic Dispatch
- **What:** Static dispatch decides the method call at compile-time; dynamic dispatch decides at runtime.
- **Why:** Static improves performance; dynamic provides flexibility and polymorphism.
- **When:** Use static for final/private methods; dynamic for overridden methods in inheritance.
- **Where:** Occurs in Swift when calling functions/methods.
- **Who:** Compiler and runtime system handle dispatching.

## Protocol-Oriented Programming
- **What:** Swift emphasizes protocols over inheritance for defining shared behavior.
- **Why:** Improves flexibility, composition, and avoids inheritance complexity.
- **When:** Use when defining shared contracts and default implementations.
- **Where:** Everywhere in Swift (e.g., UITableViewDelegate, Codable).
- **Who:** Apple promoted this with Swift 2.0 to replace class-heavy designs.

## Final Keyword
- **What:** Prevents overriding a method, property, or subclassing a class.
- **Why:** Improves performance (static dispatch) and avoids unintended overrides.
- **When:** Use when designing sealed classes or preventing modifications.
- **Where:** Applied to classes, methods, and properties in Swift.
- **Who:** Developers use it when wanting strict behavior.

## Weak Self vs Unowned Self
- **What:** Weak self is an optional reference that avoids retain cycles; unowned self is non-optional but assumes existence.
- **Why:** To prevent memory leaks with closures capturing self.
- **When:** Use weak if self may become nil; unowned if self always exists during closure lifetime.
- **Where:** Common in closures, delegation, and async callbacks.
- **Who:** Developers use them to manage memory safely.

## Dependency Injection
- **What:** A design pattern where dependencies are passed instead of being created inside a class.
- **Why:** Improves testability, modularity, and flexibility.
- **When:** Use when a class depends on external services or data sources.
- **Where:** Applied in app architecture layers (e.g., injecting services in ViewModels).
- **Who:** Developers use it for decoupled and testable code.

