## Intermediate Level TypeScript Interview Questions

#### Table of Contents

- [What is Anonymous Function in TypeScript?](#what-is-anonymous-function-in-typescript)
- [How to Install Typescript?](#how-to-install-typescript)
- [What are Decorators?](#what-are-decorators)
- [What are Mixins?](#what-are-mixins)
- [Explain Classes in TypeScript](#explain-classes-in-typescript)
- [What is Namespace and how to declare it?](#what-is-namespace-and-how-to-declare-it)
- [What are Rest Parameters in Typescript?](#what-are-rest-parameters-in-typescript)
- [What are Objects in TypeScript?](#what-are-objects-in-typescript)
- [Explain Type Aliases](#explain-type-aliases)
- [Explain Modules in TypeScript](#explain-modules-in-typescript)
- [What are Mapped Types ?](#what-are-mapped-types)
- [What are Conditional Types in TypeScript ?](#what-are-conditional-types-in-typescript)
- [What are Distributive Conditional Types?](#what-are-distributive-conditional-types)
- [Explain how TypeScript files can be supported from Node Modules](#explain-how-typescript-files-can-be-supported-from-node-modules)
- [Explain the Components of Typescript](#explain-the-components-of-typescript)
- [What are Object-Oriented Principles supported by TypeScript?](#what-are-object-oriented-principles-supported-by-typescript)
- [Explain the Drawbacks of using Declaration Files with Typescript](#explain-the-drawbacks-of-using-declaration-files-with-typescript)

### What is Anonymous Function in TypeScript?

Anonymous functions are those that have no identifier (function name) attached
to them. At runtime, these functions are dynamically declared. Anonymous
functions, like normal functions, can accept inputs and return outputs. After
its initial creation, an anonymous function is normally inaccessible. An
anonymous function can be assigned to variables.

Syntax:

```js
var res = function( [arguments] ) { ... }
```

Example:

```js
var msg = function () {
  return "hello world";
};
console.log(msg());
```

### How to Install Typescript?

TypeScript is a JavaScript programming language for use in applications.
TypeScript extends JavaScript with optional types that support tools for
large-scale JavaScript applications in any browser, on any host, and on any
operating system. TypeScript compiles to legible JavaScript that adheres to
industry standards.

You can install TypeScript globally with npm, which means you can run the tsc
command from anywhere in your terminal.

For the latest stable version:

```bash
npm install -g typescript
```

### What are Decorators?

The Decorator is a type of declaration that is used to decorate a class
declaration, method, accessor, property, or argument. Decorators take the form
`@expression`, where expression must evaluate to a function that will be called
with information about the decorated declaration when it is called at runtime.

Example:

```js
function color(value: string) {
  // this is the decorator factory, it sets up
  // the returned decorator function
  return function (target) {
    // this is the decorator
    // do something with 'target' and 'value'...
  };
}
```

### What are Mixins?

Combining simpler partial classes is a popular approach of constructing classes
from reusable components. For languages like Scala, you may be familiar with the
concept of mixins or characteristics.

To extend a base class, the design relies on generics and class inheritance. The
finest mixin support in TypeScript is provided through the class expression
pattern.

We have a class where mixins are applied on top of it.

```js
class Sprite {
  name = "";
  x = 0;
  y = 0;
  constructor(name: string) {
    this.name = name;
  }
}
```

### Explain Classes in TypeScript

In terms of OOPs, a class is a template for producing objects. Object-oriented
programming elements like as classes, interfaces, polymorphism, and data binding
are all supported by TypeScript. The term "object" refers to a physical entity.
Classes were not supported in JavaScript ES5 or earlier. This is a feature that
Typescript inherits from ES6.

A class is a collection of items with similar characteristics. Fields, methods,
constructors, Blocks, Nested classes, and interfaces are all included in the
class.

Syntax to declare a class:

```js
class class_Name {
  field;
  method;
}
```

### What is Namespace and how to declare it?

The namespace is used to group functionalities logically. To enable a single or
a group of linked functionalities, a namespace can include interfaces, classes,
functions, and variables.

The namespace keyword, followed by the namespace name, can be used to construct
a namespace. Curly brackets can be used to define all interfaces, classes, and
other objects.

Syntax:

```js
namespace <name>{ ... }
```

### What are Rest Parameters in Typescript?

When the number of parameters that a function will receive is not known or can
vary, we can use rest parameters. In JavaScript, this is achieved with the
"arguments" variable. However, with TypeScript, we can use the rest parameter
denoted by ellipsis `...`.v

- You can use rest parameters when the number of parameters that a function will
  get is unknown or varies.
- The rest parameter can take zero or more parameters. The compiler will
  generate an array of arguments containing the name of the rest parameter.

```js
let Greet = (greeting: string, ...names: string[]) => {
  return greeting + " " + names.join(", ") + "!";
};
Greet("Hi!", "John", "Sam"); // returns "Hi John, Sam"
Greet("Hi!"); // returns "Hi !
```

### What are Objects in TypeScript?

An object is a type of instance that consists of a collection of key-value
pairs. Scalar values, functions, and even arrays of other objects can be used as
values.

Syntax:

```js
var object_name = {
  key1: "value", //scalar value
  key2: "value",
  key3: function () {
    //functions
  },
  key4: ["contentA", "contentB"], //collection
};
```

### Explain Type Aliases

Type aliases give a type a new name. Type aliases are similar to interfaces in
that they can be used to name primitives, unions, tuples, and any other kinds
that you'd have to define by hand otherwise.

Aliasing doesn't truly create a new type; instead, it gives that type a new
name. Aliasing a primitive isn't very useful, however it can be used for
documentation purposes.

Type aliases, like interfaces, can be general; all you have to do is add type
parameters and utilise them on the right side of the alias declaration.

```js
type Container<T> = { value: T };
```

### Explain Modules in TypeScript

A module is created with the intention of organizing TypeScript code. Modules
are classified as follows:

Internal Modules: Internal Modules were previously used to logically group
classes, interfaces, and functions into a single unit that could then be
exported into a different module. In the most recent version of TypeScript, this
logical grouping is referred to as namespace.

External Modules: External modules allow you to describe and load dependencies
between many external js files in TypeScript.

### What are Mapped Types ?

Taking an existing type and making each of its properties optional is a typical
undertaking.

Because this happens frequently enough in JavaScript, TypeScript has a feature
called mapped types that allows you to define new types based on existing ones.
The new type turns each property in the old type in the same way into a mapped
type. You can, for example, make all properties optional or of the readonly
type.

It's important to note that this syntax refers to a type rather than a member.
You can use an intersection type to add more members:

Now, take a look at the simple mapped type and its parts:

```js
type Keys = "option1" | "option2";

type Flags = { [K in Keys]: boolean };
```

The syntax is similar to that of index signatures with a for.. in the middle.
There are three sections in total:

- The type variable K is assigned to each property one by one.
- The literal union of strings The names of the properties to iterate over are
  stored in keys.
- The property's type as a result.

### What are Conditional Types in TypeScript ?

Based on a condition given as a type relationship test, a conditional type
chooses one of two alternative types:

`T extends U ? X : Y`

When T can be assigned to U, the type is X, and when it can't, the type is Y.

Because the condition depends on one or more type variables, a conditional type
`T extends U? X: Y` and is either resolved to X or Y or delayed. Whether to
resolve to X or Y, or to defer, when T or U contains type variables is
determined by whether the type system has enough information to conclude that T
is always assignable to U.

### What are Distributive Conditional Types?

Distributive conditional types are conditional types in which the checked type
is a bare type parameter. During instantiation, distributive conditional types
are automatically distributed over union types.

For example, an instantiation of T extends U ? X : Y with the type argument
`A | B | C for T` is resolved as
`(A extends U ? X : Y) | (B extends U ? X : Y) | (C extends U ? X : Y)`.

### Explain how TypeScript files can be supported from Node Modules

TypeScript includes a series of declaration files to guarantee that TypeScript
and JavaScript support works well right out of the box (`.d.ts` files). The
various APIs in the JavaScript language, as well as the standard browser DOM
APIs, are represented in these declaration files. While there are some fair
defaults based on your target, you can configure the `lib` setting in the
`tsconfig.json` to specify which declaration files your program uses.

TypeScript has a feature similar to @types/ support that allows you to override
a specific built-in `lib`. TypeScript will check for a scoped
`@typescript/lib-*` package in node modules when selecting which `lib` files to
include. After that, you can use your package manager to install a specific
package to take over for a particular library.

### Explain the Components of Typescript

Internally, the TypeScript language is separated into three layers. Each of
these layers is further subdivided into components. These layers are as follows:

- Language
- The TypeScript Compiler
- Language Services for TypeScript

_Language_: It is written in TypeScript and includes TypeScript language
components. It includes syntax, keywords, and type annotations.

_TypeScript Compiler (TSC)_: It converts TypeScript programs into JavaScript
code. It also converts your TypeScript code to JavaScript code, parsing and
type-checking it.

_The TypeScript Language Services_: Provides information that allows editors and
other tools to deliver greater assistance capabilities like automated
refactoring and IntelliSense. It adds a layer of abstraction to the
core-compiler pipeline. It allows you to do things like code formatting and
outlining, colorization, statement completion, signature help, and so on.

### What are Object-Oriented Principles supported by TypeScript?

The object-oriented principles supported by TypeScript are

- **Encapsulation**,
- **Inheritance**,
- **Polymorphism** and
- **Abstraction**

#### Encapsulation

Encapsulation is a major component of Object Oriented Programming, and it is a
method of structuring code so that each block of code has its own set of access
points for external code.

#### Inheritance

TypeScript makes creating an object model and inheritance chain a breeze. To
construct classes, simply use the standard class keyword. The extended keyword
causes the stated base class to be inherited by the child class.

#### Polymorphism

Polymorphism occurs when many classes inherit from the same parent and override
the same functionality. Each of those kid classes is now responsible for
implementing a property or method, but they may do so in their own unique way.

#### Abstraction

Abstraction is a method of modelling objects in a system that separates the
responsibilities of the class or type from the code that inherits it.

### Explain the Drawbacks of using Declaration Files with Typescript

There are two drawbacks to using these declaration files with TypeScript:

Since you upgrade TypeScript, you must also deal with changes to TypeScript's
built-in declaration files, which can be difficult when the DOM APIs change so
regularly.

Customizing these files to meet your needs and the demands of your project's
dependencies is difficult (e.g. if your dependencies declare that they use the
DOM APIs, you might also be forced into using the DOM APIs).
