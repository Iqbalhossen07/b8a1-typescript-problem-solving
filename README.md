# Level 2 - Assignment 1: Problem Solving with TypeScript & OOP

This repository contains the complete implementation and technical documentation for **Assignment 1 (Batch 8)** of Programming Hero Level 2.

## Project Overview

This assignment demonstrates mastery over core TypeScript concepts, including:
- **Basic & Primitive Types**: Working with strictly typed values, optional parameters, and default values.
- **Type Narrowing**: Utilizing `typeof` guards to safely handle union types.
- **Tuples & Readonly Modifiers**: Creating immutable tuples for coordinate and data pair representations.
- **Generics & Rest Parameters**: Crafting reusable utility functions (`concatenateArrays`, `pluckValues`) using generic type constraints (`keyof`).
- **Interfaces & Pure Functions**: Defining data models and performing non-mutating array filtering.
- **Object-Oriented Programming (OOP)**: Implementing class hierarchies, inheritance, and access modifiers (`protected`, `private`, `public`).
- **Asynchronous TypeScript**: Managing Promises, timed delays (`setTimeout`), and strict error handling with `Promise<string>`.

## File Structure

```text
├── solutions.ts          # All 8 problem-solving solutions
├── type-vs-interface.md  # Blog post 1: Type Aliases vs. Interface
├── type-narrowing.md     # Blog post 2: Type Narrowing in TypeScript
└── README.md             # Project documentation and blog links
```

## Blog Posts

Check out the detailed technical blog posts written as part of this assignment:
1. [Understanding Type Aliases vs. Interfaces in TypeScript](./type-vs-interface.md)
2. [Mastering Type Narrowing in TypeScript](./type-narrowing.md)

## How to Run & Verify

1. Install dependencies:
   ```bash
   npm install
   ```

2. Perform TypeScript type checking:
   ```bash
   npx tsc --noEmit
   ```
