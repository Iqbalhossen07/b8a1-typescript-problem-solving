# Understanding Type Aliases vs. Interfaces in TypeScript

## Introduction
TypeScript offers two primary ways to define custom data shapes: Type Aliases (`type`) and Interfaces (`interface`). While they often seem interchangeable, key structural differences dictate when to choose one over the other.

## Core Differences and Usage

Interfaces are primarily designed for defining object contracts and class implementations. A standout capability of interfaces is declaration merging, where multiple declarations with the same name automatically merge into one. Interfaces also extend other interfaces or classes using the `extends` keyword.

```typescript
interface User {
  id: number;
  name: string;
}

interface User {
  role: string; // Merged with User interface
}
```

Conversely, type aliases are more flexible. They can define not only object shapes but also primitives, unions, intersections, tuples, and mapped types. However, type aliases cannot be reopened to add new properties once defined.

```typescript
type Status = "pending" | "resolved" | "rejected";
type UserProfile = User & { status: Status };
```

When deciding between them, use `interface` when writing object schemas, public APIs, or library definitions that benefit from declaration merging and OOP inheritance. Opt for `type` when you need union types, primitives, complex tuples, or advanced type transformations.

## Conclusion
Both tools are essential in TypeScript. By favoring interfaces for extensible object structures and type aliases for unions and composite types, you ensure a robust, clean, and maintainable codebase.
