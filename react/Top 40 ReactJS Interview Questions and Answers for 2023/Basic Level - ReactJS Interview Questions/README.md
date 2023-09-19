## Basic Level - ReactJS Interview Questions

#### Table of Contents

- What are the features of React?
- What is JSX?
- Can web browsers read JSX directly?
- What is the virtual DOM?
- Why use React instead of other frameworks, like Angular?
- What is the difference between the ES6 and ES5 standards?
- How do you create a React app?
- What is an event in React?
- How do you create an event in React?
- What are synthetic events in React?
- Explain how lists work in React
- Why is there a need for using keys in Lists?
- What are forms in React?
- How do you create forms in React?
- How do you write comments in React?
- What is an arrow function and how is it used in React?
- How is React different from React Native?

### What are the features of React?

- JSX
- Components
- Virtual DOM
- One-way data-binding
- High performance

#### JSX

JSX is a syntax extension to JavaScript. It is used with React to describe what the user interface shoul
look like. By using JSX, we can write HTML structures in the same file that contains JavaScript code.

#### Components

Components are the building blocks of any React application, and a single app usually consists of
multiple components. It splits the user interface into independent, reusable parts that can be processed
separately.

#### Virtual DOM

React keeps a lightweight representation of the real DOM in the memory, and that is known as the virtual
DOM. When the state of an object changes, virtual DOM changes only that object in the real DOM, rather
than updating all the objects.

#### One-way data-binding

React’s one-way data binding keeps everything modular and fast. A unidirectional data flow means that
when designing a React app, you often nest child components within parent components.

#### High performance

React updates only those components that have changed, rather than updating all the components at once.
This results in much faster web applications.

### What is JSX?

JSX is a syntax extension of JavaScript. It is used with React to describe what the user interface should
look like. By using JSX, we can write HTML structures in the same file that contains JavaScript code.

```js
render() {
    return (
        <div>
            <h1>This is a JSX code</h1>
        </div>
    );
};
```

### Can web browsers read JSX directly?

- Web browsers cannot read JSX directly. This is because they are built to only read regular JS objects
  and JSX is not a regular JavaScript object.
- For a web browser to read a JSX file, the file needs to be transformed into a regular JavaScript
  object. For this, we use Babel.
  ![Babel.js]()

### What is the virtual DOM?

### Why use React instead of other frameworks, like Angular?

### What is the difference between the ES6 and ES5 standards?

### How do you create a React app?

### What is an event in React?

### How do you create an event in React?

### What are synthetic events in React?

### Explain how lists work in React

### Why is there a need for using keys in Lists?

### What are forms in React?

### How do you create forms in React?

### How do you write comments in React?

### What is an arrow function and how is it used in React?

### How is React different from React Native?
