## Advanced Level TypeScript Interview Questions

#### Table of Contents

- [How to compile Typescript with Visual Studio Code?](#how-to-compile-typescript-with-visual-studio-code)
- [What are the Recent Advancements in TypeScript?](#what-are-the-recent-advancements-in-typescript)
- [Explain the Awaited Type and Promise Improvements](#explain-the-awaited-type-and-promise-improvements)
- [Explain how TypeScript files can be supported from Node Modules](#explain-how-typescript-files-can-be-supported-from-node-modules)
- [What is Type Assertion? Explain its types](#what-is-type-assertion-explain-its-types)
- [What is Recursive Type Aliases?](#what-is-recursive-type-aliases)

### How to compile Typescript with Visual Studio Code?

- Visual Studio Code includes TypeScript language support but does not include
  the TypeScript compiler.
- You need to install the TypeScript compiler either globally or in your
  workspace to transpile TypeScript source code to JavaScript
- The easiest way to install TypeScript is through npm, the Node.js Package
  Manager. If you have npm installed, you can install TypeScript globally (-g)
  on your computer by:

```bash
npm install -g typescript
```

- You can test your install by checking the version or help.

```bash
tsc --version
```

### What are the Recent Advancements in TypeScript?

- TypeScript 4.2 has been released, and it includes more flexible type
  annotations, tougher checks, additional configuration choices, and a few
  breaking changes.
- Rest arguments can now be placed anywhere in a triple type. In type error
  messages, type aliases are no longer enlarged, resulting in a better developer
  experience.
- TypeScript 4.2 brings the language one step closer to its aim of accurately
  typing JavaScript at any size, anywhere JavaScript is used.

### Explain the Awaited Type and Promise Improvements

The Awaited type is a new utility type introduced in TypeScript 4.5. This type
is intended to represent activities such as `await` in `async` functions and the
`.then()` method on Promises - notably, the way they recursively unwrap
Promises.

```js
// A = string

type A = Awaited<Promise<string>>;

// B = number

type B = Awaited<Promise<Promise<number>>>;

// C = boolean | number

type C = Awaited<boolean | Promise<number>>;
```

Existing APIs, such as JavaScript built-ins like `Promise.all`, `Promise.race`,
and others, can benefit from the Awaited type. In fact, some of `Promise.all`'s
inference concerns provided a foundation for Awaited.

`Promise.all` combines certain traits with Awaited to produce far superior
inference results.

### Explain how TypeScript files can be supported from Node Modules

TypeScript includes a series of declaration files to guarantee that TypeScript
and JavaScript support works well right out of the box (`.d.ts` files). The
various APIs in the JavaScript language, as well as the standard browser DOM
APIs, are represented in these declaration files. While there are some fair
defaults based on your target, you can configure the `lib` setting in the
tsconfig.json to specify which declaration files your program uses.

TypeScript has a feature similar to `@types/` support that allows you to
override a specific built-in `lib`. TypeScript will check for a scoped
`@typescript/lib-*` package in node modules when selecting which `lib` files to
include. After that, you can use your package manager to install a specific
package to take over for a particular library.

### What is Type Assertion? Explain its types

You can find yourself in a scenario where you know a type for an entity that is
more specific than its present type.

A type assertion is similar to a type cast in other languages, but it does not
do any additional data verification or restructuring. It has no effect on
runtime and is only used by the compiler. TypeScript expects that you, the
programmer, have completed any necessary specific checks.

There are two types of type assertions.

One is the as-syntax:

```js

let someValue: unknown = "this is a string";

let strLength: number = (someValue as string).length;
```

The other version is the "angle-bracket" syntax:

```js
let someValue: unknown = "this is a string";

let strLength: number = (<string>someValue).length;
```

Both samples are identical. selecting one over the other is basically a matter
of preference; however, only as-style assertions are allowed when combining
TypeScript with JSX.

### What is Recursive Type Aliases?

The ability to "recursively" reference type aliases has always been limited. The
reason for this is because each type alias must be capable of substituting
itself for whatever it aliases. Because this isn't always possible, the compiler
rejects some recursive aliases.

Interfaces can be recursive, but their expressiveness is limited, and type
aliases cannot. That involves combining the two: creating a type alias and
extracting the type's recursive portions into interfaces. It's effective.

```js
type ValueOrArray<T> = T | ArrayOfValueOrArray<T>;

interface ArrayOfValueOrArray<T> extends Array<ValueOrArray<T>> {}
```
