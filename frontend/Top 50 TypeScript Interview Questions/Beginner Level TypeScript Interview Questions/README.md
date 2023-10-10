## Beginner Level TypeScript Interview Questions

#### Table of Contents

- [What is TypeScript?](#what-is-typescript)
- [Explain Arrays in TypeScript](#explain-arrays-in-typescript)
- [List the Applications of TypeScript](#list-the-applications-of-typescript)
- [List the Advantages of TypeScript](#list-the-advantages-of-typescript)
- [List the disadvantages of TypeScript](#list-the-disadvantages-of-typescript)
- [Explain the features of Arrays in TypeScript](#explain-the-features-of-arrays-in-typescript)
- [How to declare a variable in TypeScript?](#how-to-declare-a-variable-in-typescript)
- [Name the access modifiers supported in TypeScript](#name-the-access-modifiers-supported-in-typescript)
- [Explain Loops in Typescript](#explain-loops-in-typescript)
- [What is the use of the tsconfig.json file?](#what-is-the-use-of-the-tsconfigjson-file)
- [How to convert a string to a number in TypeScript?](#how-to-convert-a-string-to-a-number-in-typescript)
- [What is meant by contextual typing?](#what-is-meant-by-contextual-typing)
- [What is JSX?](#what-is-jsx)
- [Define static typing](#define-static-typing)
- [What are import and export keywords in TypeScript?](#what-are-import-and-export-keywords-in-typescript)
- [Can TypeScript be used for the backend?](#can-typescript-be-used-for-the-backend)
- [How will you check if a variable is null or undefined in TypeScript?](#how-will-you-check-if-a-variable-is-null-or-undefined-in-typescript)
- [What are getters/setters?](#what-are-getterssetters)
- [How can a class constant be implemented in TypeScript?](#how-can-a-class-constant-be-implemented-in-typescript)
- [What is the Declare Keyword in TypeScript?](#what-is-the-declare-keyword-in-typescript)
- [What is an Interface with reference to TypeScript?](#what-is-an-interface-with-reference-to-typescript)
- [Describe 'as' syntax in TypeScript](#describe-as-syntax-in-typescript)
- [Define Lambda function](#define-lambda-function)
- [How to create objects in Typescript?](#how-to-create-objects-in-typescript)
- [Explain Different Data Types in Typescript?](#explain-different-data-types-in-typescript)
- [What is meant by Type Inference?](#what-is-meant-by-type-inference)
- [Explain Tuples in Typescript With Example](#explain-tuples-in-typescript-with-example)

### What is TypeScript?

- TypeScript is a superset of JavaScript. It is an object-oriented and tightly
  typed programming language. TypeScript code is transformed to JavaScript,
  which may be used in any environment that supports JavaScript, including
  browsers, Node.js, and your own applications.
- Anders Hejlsberg of MICROSOFT created TypeScript. TypeScript was created in
  response to the limitations of JavaScript for constructing large-scale
  applications within Microsoft and among its external customers. There was a
  demand for bespoke tooling to make developing JavaScript components easier due
  to the complexity of working with complicated JavaScript code.
- TypeScript is a variant of JavaScript with a few more features. TypeScript
  extends JavaScript with extra syntax to provide a more robust interface with
  your editor. TypeScript is a scripting language that is compatible with
  JavaScript and relies on type inference to deliver advanced functionality
  without the need for additional code.

### Explain Arrays in TypeScript

A collection of values of the same data type is called an array. It's a kind
that's been defined by the user. To store values of the same kind, you use
arrays. Arrays are collections of values that are ordered and indexed. The
indexing begins at zero, with the first element having index 0, the second
having index 1, and so on.

Syntax

```js
var array_name[:datatype];        //declaration

array_name = [val1,val2,valn..]   //initialization
```

Example

```js
let values: number[] = [];
values[0] = 10;
values[1] = 20;
values[2] = 30;
```

### List the Applications of TypeScript

- Both client-side and server-side JavaScript applications can be built with
  TypeScript.
- TypeScript is used to create both client-side and server-side JavaScript
  applications.
- Because TypeScript adds more functionality and provides errors directly in the
  code, it can be used instead of JavaScript.
- TypeScript is a programming language that is used to create large-scale
  enterprise systems.

### List the Advantages of TypeScript

- Problems are highlighted throughout development and at compilation time.
- Typescript can be run in any browser or JavaScript engine.
- A namespace notion is created by declaring a module.
- IntelliSense is a TypeScript feature that provides active hints as you type.
- Strongly typed or static typing is supported. The advantage of TypeScript is
  that it is strictly typed or allows for static typing. Because of static
  typing, it may confirm type correctness at compilation time.

### List the disadvantages of TypeScript

- It takes a long time to compile TypeScript code.
- Abstract classes are not supported in TypeScript.
- Converting TypeScript to JavaScript requires an additional compilation step.
- Its type scheme is extremely complicated.

### Explain the features of Arrays in TypeScript

- An array declaration allocates memory blocks in a sequential order.
- Arrays are immutable. This means that once an array is created, it cannot be
  resized.
- An array element is represented by each memory block.
- The subscript/index of an array element is a unique number that identifies the
  element.
- Arrays, like variables, should be declared before being used. Declare an array
  with the var keyword.
- The term "array initialization" refers to the process of filling an array with
  elements.
- The values of array elements can be updated or modified, but they cannot be
  erased.

### How to declare a variable in TypeScript?

- Let and const are the two methods to declare variables.
- Alphabets and numeric digits can both be used in variable names.
- Except for the underscore (\_) and the dollar ($) sign, they cannot contain
  spaces or special characters.
- A digit can't be the first character in a variable name.

### Name the access modifiers supported in TypeScript

The access modifiers supported by TypeScript are:

- Protected- All child classes and members have access to them, but the instance
  does not.
- Private- Only members have access
- Public- Members, child classes, and instances of the class have access to the
  public modifier.

### Explain Loops in Typescript

A loop statement allows to repeat the execution of a statement or a series of
statements. To handle looping requirements, TypeScript provides a variety of
loops.

- For Loop

  The for loop is a definite loop implementation. A definite loop is defined as
  a loop with a fixed number of iterations.

- While Loop

  When the condition supplied evaluates to true, the while loop executes the
  instructions.

- Do..While Loop

  The do...while loop is identical to the while loop, except that the condition
  isn't evaluated the first time the loop runs.

### What is the use of the tsconfig.json file?

The `tsconfig.json` file is a JSON format file where you may specify several
options to inform the compiler how to compile a project. The presence of this
file in the directory implies that it is the TypeScript project root.

### How to convert a string to a number in TypeScript?

You can convert a string to a number by using `parseInt()`, `parseFloat()` and
`Number('')` Method.

| <center>Code</center> | <center>Example</center>                            |
| --------------------- | --------------------------------------------------- |
| `parseInt()`          | `parseInt(string_to_be_converted_to_number, radix)` |
| `parseFloat()`        | `parseFloat(string_to_be_converted_number)`         |
| `Number('')`          | `Number(string_to_be_converted_to_number)`          |

### What is meant by contextual typing?

When one side of the equation has type but the other does not, the TypeScript
compiler determines the form. You can skip typing on the right side because
TypeScript will figure it out for you. This reduces the amount of time spent
typing code.

### What is JSX?

It's a syntax that's similar to XML and can be embedded. It must be converted
into TypeScript that is valid. The JSX file with the `.tsx` extension is used.

JSX has an XML-like syntax that can be embedded. It is intended to be turned
into legitimate JavaScript, though the semantics of that transformation will
vary depending on the implementation. TypeScript allows you to embed JSX, type
verify it, and compile it to JavaScript immediately.

### Define static typing

Static typing refers to a compiler that has recognisable variables, arguments,
and object members at compile time. This aids in the early detection of faults.

### What are import and export keywords in TypeScript?

- Import keyword is used to export declaration. Example: export \* from module
- Any variable, function, or type alias can be exported with the export keyword

### Can TypeScript be used for the backend?

By combining TypeScript with Node.js, backend applications can benefit from the
added security that the language provides.

### How will you check if a variable is null or undefined in TypeScript?

if(value) return true if value is not null, undefined, empty, false, 0 or NaN.

### What are getters/setters?

```js
class Person {
  private _age: number;
  private _firstName: string;
  private _lastName: string;

  public get age() {
    return this._age;
  }

  public set age(theAge: number) {
    if (theAge <= 0 || theAge >= 200) {
      throw new Error("The age is invalid");
    }
    this._age = theAge;
  }
}
```

Getters and setters prevent access to an object's members.They allow you to have
more precise control over how a member interacts with each object. A getter
method starts with keyword 'get' and setter method starts with keyword 'set'

### How can a class constant be implemented in TypeScript?

Class properties cannot be declared with the `const` keyword. The keyword
`const` cannot be used in a class member.

### What is the Declare Keyword in TypeScript?

Since JavaScript lacks a TypeScript declaration, the declare keyword is used to
include it in a TypeScript file without causing a compilation issue. Ambient
methods and declarations use the term to define a variable that already exists.

### What is an Interface with reference to TypeScript?

The interface specifies the syntax that classes must use. All of the members of
an interface are implemented by a class that implements it. It's possible to
refer to it, but not to use it. A type-checking interface is used by the
TypeScript compiler.

### Describe 'as' syntax in TypeScript

In TypeScript, the 'as' syntax is used for Type assertion. It was created
because the original syntax was incompatible with JSX. Only as-style assertions
can be used with JSX and TypeScript.

Example:

```js
let stdid: any = 007;

let stdid = id as number;
```

### Define Lambda function

For defining function expressions, TypeScript provides a shortcut syntax. A
lambda function is an unnamed anonymous function.

Example:

```js
let sum = (a: num, b: num): num => {
  return a + b;
};

console.log(sum(5, 10)); //returns 15
```

Here, `?=>?` is a lambda operator.

### How to create objects in Typescript?

Objects are collections of keys and values that resemble a dictionary. The keys
must be one-of-a-kind. They resemble arrays and are sometimes referred to as
associative arrays. An array, on the other hand, employs numbers to index the
values, whereas an object lets you use any type as the key.

An Object type in TypeScript refers to any value with properties. It can be
defined simply by specifying the properties and the kinds of those properties.
As an example,

```js
let pt: { x: number, y: number } = {
  x: 10,
  y: 20,
};
```

### Explain Different Data Types in Typescript?

| Data Type |  Keyword  |                                     Description                                      |
| :-------: | :-------: | :----------------------------------------------------------------------------------: |
|  Number   |  Number   |            Both Integer and Floating-Point numbers are represented by it             |
|  Boolean  |  Boolean  |                        True and false values are represented                         |
|  String   |  String   |                      It's used to denote a string of characters                      |
|   Void    |   Void    |                       Usually applied to function return types                       |
|   Null    |   Null    |                    It's used when an object isn't worth anything                     |
| Undefined | Undefined |              Indicates the value assigned to an uninitialized variable               |
|    Any    |    Any    | Any type of value can be assigned to a variable if it is declared with any data-type |

### What is meant by Type Inference?

When you don't specify an explicit type for a variable, TypeScript can infer it.
Type inference is the term for this. This is normally done during the
declaration, when the variables or parameters are initialized.

TypeScript recognises that the variable koo is a string, even if you don't
mention string as a type.

```js
let koo = "Hello world";

console.log(typeof koo); // "string"
```

### Explain Tuples in Typescript With Example

Tuples are a collection of values that are diverse. It allows for the storage of
many fields of various sorts. Tuples can also be used as function parameters.

There are instances when it is necessary to save a collection of values of
various types. Arrays will not suffice in this situation. TypeScript provides a
data type called tuple that aids in this endeavor.

Syntax:

```js
var tuple_name = [value c,value b,value c,…value n]
```

For Example:

```js
var yourtuple = [12, "Hi"];
```
