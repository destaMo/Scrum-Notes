+++
aliases = ["typescript"]
title = "TypeScript"
weight = 1
+++

{{%bubble %}}

## Language

**Description:** You can use features of TypeScript required for work with frameworks built on top of it.

**Person who successfully completed a requirement for given block can:**

- **deliver** simple and typical **functionalities** with **little to no additional help**,
- **present** the problem and explored **solutions clearly and in detail** when asking for help,
- **leverage** the most commonly used **standard library**'s capabilities.

**Prerequisites:**

- [JavaScript's basics](../javascript/basics)

{{% /bubble%}}

## Areas

### TypeScript

- Data types,
- Type guards and types assertions,
- Built-in utility types,
- Generics,
- Conditional Types,
- Mapped and Indexed types.

---

## 📦 Data types

Learn about available data types in TypeScript.

### 🎓 Learn

- 📗 [Primitive types](https://www.typescriptlang.org/docs/handbook/2/everyday-types.html#the-primitives-string-number-and-boolean)
- 📗 [Arrays](https://www.typescriptlang.org/docs/handbook/2/everyday-types.html#arrays)
- 📗 Functions
  - [TS Handbook on Functions](https://www.typescriptlang.org/docs/handbook/2/everyday-types.html#functions)
  - [TS Deep Dive on Functions](https://basarat.gitbook.io/typescript/type-system/functions)
  - [TS Deep Dive on Callables](https://basarat.gitbook.io/typescript/type-system/callable)
- 📗 Object types
  - [TS Handbook on Objects](https://www.typescriptlang.org/docs/handbook/2/objects.html)
  - [TS Handbook on Object types](https://www.typescriptlang.org/docs/handbook/2/objects.html)
- 📗 [Type aliases](https://www.typescriptlang.org/docs/handbook/2/everyday-types.html#interfaces)
- 📗 Interfaces
  - [TS Handbook on Interfaces](https://www.typescriptlang.org/docs/handbook/2/everyday-types.html#interfaces)
  - [TS Deep Dive on Interfaces](https://basarat.gitbook.io/typescript/type-system/interfaces)
  - [Declaratios Merging](https://www.typescriptlang.org/docs/handbook/declaration-merging.html)
- 📗 Union Types
  - [TypeScript Handook on Union types](https://www.typescriptlang.org/docs/handbook/2/everyday-types.html#object-types)
  - [TypeScript Deep Dive on Discriminated unions](https://basarat.gitbook.io/typescript/type-system/discriminated-unions)
- 📗 [null and undefined](https://basarat.gitbook.io/typescript/type-system/never)
- 📗 [Never and void](https://basarat.gitbook.io/typescript/type-system/never)

### 🎤 Interview

- What are primitive types?
- How to define an array of types? How is it different with tuple?
- How to access type of array element? How about accessing type of tuple elements?
- What is type alias?
- What is an interface?
- What are the differences between type alias and interface?
- How to define function in an interface?
- How to define function in a type alias?
- What are function overloads? What are they used for? How can we declare these - show three different ways?
- What are literal types and when they are useful?
- What's the difference between `never` and `void`?
- What difference does it make to have `strictNullChecks` option turned on?

---

## 📦 Type Compatibility

Read on compatibility between different types and structures

### 🎓 Learn

- [Type Compatibility](https://basarat.gitbook.io/typescript/type-system/type-compatibility)

## 📦 Type guards

Learn about narrowing down types using various methods.

### 🎓 Learn

- 📗 [Narrowing types](https://www.typescriptlang.org/docs/handbook/2/narrowing.html)
- 📗 [Type guards](https://basarat.gitbook.io/typescript/type-system/typeguard)

### 🎤 Interview

- How can we narrow down different types? Tell me about and give examples on:
  - Truthiness,
  - `typeof` operator,
  - `in` operator,
  - `instanceof` operator,
  - type predicates,
  - discriminated unions.

---

## 📦 Utility types

Get familiar with some of the utility types.

### 🎓 Learn

- 📗 [Utility Types](https://www.typescriptlang.org/docs/handbook/utility-types.html)

### 🎤 Interview

- Tell me about Extract/Exclude and Omit/Pick - how they are different from each other?
- Tell me about Partial/Required - what are they doing? What is their use case?
- How can we access type of parameters in function? How do we extract type of n-th parameter?
- How can we access type of return value in function?
- What other utility types do you know?

---

## 📦 Generics

How to make use of generics (named templates in other languages sometimes).

### 🎓 Learn

- 📗 [TS Handbook on Generics](https://www.typescriptlang.org/docs/handbook/2/generics.html)
- 📗 [TS Deep Dive on Generics](https://basarat.gitbook.io/typescript/type-system/generics)

### 🎤 Interview

- How to define generic type?
- How to define multiple generic types?
- How to define default generic value?
- How to apply constraints on possible generic values?

### 📝 Katas

- Create a class that makes use of a generic. It should accept anything as a constructor and have following methods:
  - `getValue` - its return type should be derived from generic,
  - `setValue` - its argument should be derived from generic.
- Create a function that makes use of a generic. Return type of this function should be derived from generic.
- Create an interface for a function that accepts object as a first argument and second argument MUST be one of the keys in this obejct.

---

## 📦 Conditional types

Get familiar with assigning types conditionally and extract types from function parameters, return types and promise resolve values.

### 🎓 Learn

- 📗 [Conditional Types](https://www.typescriptlang.org/docs/handbook/2/conditional-types.html)

### 🎤 Interview

- How to use conditional types? When they are useful?
- What does `infer` keyword do?

### 📝 Katas

- Create a type conditional where you extract value from given `Promise<Type>` type.

---

## 📦 Mapped and indexed types

Learn how to transform types from one structure to another.

### 🎓 Learn

- 📗 [keyof type operator](https://www.typescriptlang.org/docs/handbook/2/keyof-types.html)
- 📗 [typeof type operator](https://www.typescriptlang.org/docs/handbook/2/typeof-types.html)
- 📗 [Indexed access](https://www.typescriptlang.org/docs/handbook/2/indexed-access-types.html)
- 📗 [Mapped Types](https://www.typescriptlang.org/docs/handbook/2/mapped-types.html)
- 📗 [Template Literal Types](https://www.typescriptlang.org/docs/handbook/2/template-literal-types.html)

### 🎤 Interview

- What does `keyof` operator do? What's use case for it?
- What does `typeof` operator do in TypeScript context? How it is different from JavaScript runtime?
- How to access nested fields in a object type?
- Explain what is mapped type and what it is useful for?

### 📝 Katas

- Create an interface which as a type variable accepts a union and creates properties from elements of this union (property type can be anything, for example `string`)
- Create an interface type which as a type variable accepts an object type where this object values are functions.
  Returned type should have the same keys, but object value should be value of a function provided under that key.
  > Example: `{ foo: () => number }` should transform to `{ foo: number }`
- Create a static object where it's values are different class constructors (e.g. `Dog`, `Cat`, `Bird`).
  Then create a function that accepts one of the keys of this object as an argument and returns instance of class under this key.
- Create a function that
  - accepts two parameters: field name that starts with `email_{AnyNumberHere}` and field value which is any string; **Hint:** use template literals,
  - returns an object where field name is a key and field value is value.,
  - for a harder version of this task you can try restricting negative numbers from `{AnyNumberHere}` placeholder; you can try using [type-fest](https://github.com/sindresorhus/type-fest) library.

---

## 📦 Summary

It is highly recommended that you read whole **TypeScript Handbook** and **TypeScript Deep Dive** (linked below) for a better understanding of TypeScript.

### 🎓 Learn

- 📗 [TypeScript Handbook](https://www.typescriptlang.org/docs/handbook/intro.html)
- 📗 [TypeScript Deep Dive](https://basarat.gitbook.io/typescript/)

### 📝 Katas

- Solve excersises **1-10** (with extras) and **15** (optionally) from [typescript excersises](https://typescript-exercises.github.io/) (you don't need to put it on github or anywhere, solving them on this page only is fine).
