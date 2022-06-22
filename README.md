# learning-typescript

## What is TypeScript?

TypeScript is a superset of JavaScript that compiles to plain JavaScript. It is a superset of JavaScript, but not a drop-in replacement. It gives you the power of JavaScript, but with the syntax that makes it more convenient to use. It is fast and efficient, and it is a good choice for large applications.

Video Resource: [Yeni Başlayanlar İçin Typescript](https://youtu.be/1d92ipW7Mx8)

## Install TypeScript

```bash
npm i -g typescript
```

-> If you can get any permission problem, you can use the following command.

```bash
sudo npm i -g typescript
```

## Compiling a TypeScript File

```bash
tsc filename.ts
```

-> The command will compile the file to JavaScript as **'filename.js'**.

<br>

# 1. Type Notations

---

> It is a way to define the type of a variable in JavaScript.

```javascript
// let variableName = value;
let name = "Rasit";
```

> And in TypeScript.

```typescript
// let variableName: type = value;
let name: string = "Rasit";
```

_As you can see, the difference between JavaScript and TypeScript is, in TypeScript, you can define the type of a variable_.
<br>
<br>
Also you can use the properties of the type. For example, if you want to define a type of string, you can use **_includes, startsWith, endsWith_**, etc.
<br>
<br>
When you want to change the value of the variable **name** as number, the compiler will give you an error below.

```typescript
let name: string = "Rasit";
name = 1;
// Error: Type number is not assignable to type 'string'.
```

> Additionally, when you want to compile the file, it will give the same error.

### 1.1. String Type

---

The type of a string is **string**. You can assign a string to a variable.

```typescript
let name: string = "Rasit";
let surname = "Colakel";
```

### 1.3. Boolean Type

---

The type of a boolean variable is **boolean**. And it takes only two values, **true** or **false**. You can not assign _**0 or -1**_ to a boolean variable.

```typescript
let isDone: boolean = false;
let isLoading = true;
// the variables below are types of boolean variable.
```

### 1.4 Arrays

To define an array, you can use the _**string[], number[], any[]**_ type.

```typescript
let names: string[] = ["Rasit", "Colakel"];
let numbers: number[] = [0, 1, 2];
let numbers: any[] = [0, "Rasit"];
```

### 1.5 Enums

Enums are a way to define a set of named constants.

```typescript
enum Color {
  Red,
  Green,
  Blue,
}
```

### 1.6 Tuples

Tuples are a way to define an array where the type of the elements is known, but the number of elements is not.

```typescript
let tuple: [string, number] = ["Rasit", 1];
```

### 1.7 Unknown Type

Unknown type is a type that is used when the type of a variable is not known. But it is different from the _**any**_ type.

```typescript
let a: unknown;
let b: string = a;
// Error: Type 'unknown' is not assignable to type 'string'.
```

The difference between unknown and any is, you can assign an any type to a variable. But, you can not assign an unknown type to a variable.

```typescript
let a: any;
let b: string = a;
// Error: Type 'unknown' is not assignable to type 'string'.
```

## 2. Type Inference

---

Type inference is a way to automatically assign a type to a variable.

```typescript
let name = "Rasit";
let age = 30;
```

> In this case, the compiler will automatically assign the type of **'name'** as string and the type of **'age'** as number.

## 3. Type Assertions

```typescript
let name = "Rasit";
let lowerCaseName = (<string>name).toLowerCase();
```
