# TypeScript cheat-sheet

<p align="left">
  <img width="80" height="80" src="https://raw.githubusercontent.com/rmolinamir/typescript-cheatsheet/master/TypeScript.png">
</p>

## What is TypeScript ?

TypeScript (TS) is a programming language. We use this programming language for large-scale JavaScript application development. We can refer to it as a typed superset of JavaScript.

🔗 [https://www.typescriptlang.org/](https://www.typescriptlang.org/)

## How TypeScript work?

TypeScript language needs a compiler that can convert TypeScript syntax into standard JavaScript, this compiler is called a transpiler.
Transpiler is designed to convert one programming language into another one.

TypeScript files come with `.ts` extension. Once transpiler compiles the `.ts` files, you will get .js files as output.

## Cheat Sheets

## Contents

- [Type](#-type)
- [Type vs Interface](#type-vs-interface)
- [Object Literal Syntax](#object-literal-syntax)
- [Interface](#-interface)
- [Common Syntax](#common-syntax)
- [Generics](#generics)



## 📄 Type

### Type vs Interface

- Interfaces can only describe object shapes.
- Interfaces can be extended by declaring it multiple times.
- In performance, Types can be faster.

### Object Literal Syntax

```typescript
type JSONResponse = {
  version: number; // Field
  payloadSize: number; // In bytes
  outOfStock?: boolean; // Optional
  update: (retryTimes: number) => void; // Arrow func field
  update(retryTimes: number): void; // Function
  (): JSONResponse; // Type is callable
  [key: string]: number; // Accepts any index
  new (s: string): JSONResponse; // Newable
  readonly body: string; // Readonly property
};
```

## 📄 Interface

Used to describe the shape of objects, and can be extended by others.

### Common Syntax

```typescript
interface JSONResponse extends Response, HTTPAble = {
  version: number;
  payloadSize: number; // In bytes
  outOfStock?: boolean; // Optional
  ...
};
```

> `extends Response, HTTPAble` Optionally take properties from existing interfaces or types.

### Generics

Declare a type which can change according to your interface

```typescript
interface APICall<Response> = {
  data: Response;
};
```
