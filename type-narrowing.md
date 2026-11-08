# Mastering Type Narrowing in TypeScript

## Introduction
Type Narrowing is the mechanism TypeScript uses to refine a broad type, such as a union type, into a more specific, concrete type within a conditional execution branch. This guarantees type safety without resorting to unsafe type assertions.

## Practical Narrowing Techniques

TypeScript provides several built-in operators to narrow down types effectively.

First, the `typeof` operator inspects primitive values such as strings, numbers, and booleans at runtime.

```typescript
function printValue(input: string | number): void {
  if (typeof input === "string") {
    console.log(input.toUpperCase());
  } else {
    console.log(input.toFixed(2));
  }
}
```

Second, the `instanceof` operator narrows object instances created from classes or constructor functions by checking their prototype chain.

```typescript
class Dog { bark(): void {} }
class Cat { meow(): void {} }

function handlePet(pet: Dog | Cat): void {
  if (pet instanceof Dog) {
    pet.bark();
  } else {
    pet.meow();
  }
}
```

Third, the `in` operator checks if a specific property exists on an object, which is useful when dealing with distinct object shapes without common constructors.

```typescript
type Admin = { name: string; privileges: string[] };
type Guest = { name: string };

function verifyUser(user: Admin | Guest): boolean {
  return "privileges" in user;
}
```

## Conclusion
Type narrowing transforms uncertain types into concrete, predictable contracts. By leveraging `typeof`, `instanceof`, and the `in` operator, developers can write secure, error-free TypeScript code that runtime logic safely supports.
