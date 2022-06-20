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

## 2. Type Inference

---

Type inference is a way to automatically assign a type to a variable.

```typescript
let name = "Rasit";
let age = 30;
```

> In this case, the compiler will automatically assign the type of **'name'** as string and the type of **'age'** as number.
