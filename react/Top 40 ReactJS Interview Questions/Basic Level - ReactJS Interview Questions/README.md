## Basic Level - ReactJS Interview Questions

#### Table of Contents

- [What are the features of React?](#what-are-the-features-of-react)
- [What is JSX?](#what-is-jsx)
- [Can web browsers read JSX directly?](#can-web-browsers-read-jsx-directly)
- [What is the virtual DOM?](#what-is-the-virtual-dom)
- [Why use React instead of other frameworks, like Angular?](#why-use-react-instead-of-other-frameworks-like-angular)
- [What is the difference between the ES6 and ES5 standards?](#what-is-the-difference-between-the-es6-and-es5-standards)
- [How do you create a React app?](#how-do-you-create-a-react-app)
- [What is an event in React?](#what-is-an-event-in-react)
- [How do you create an event in React?](#how-do-you-create-an-event-in-react)
- [What are synthetic events in React?](#what-are-synthetic-events-in-react)
- [Explain how lists work in React](#explain-how-lists-work-in-react)
- [Why is there a need for using keys in Lists?](#why-is-there-a-need-for-using-keys-in-lists)
- [What are forms in React?](#what-are-forms-in-react)
- [How do you create forms in React?](#how-do-you-create-forms-in-react)
- [How do you write comments in React?](#how-do-you-write-comments-in-react)
- [What is an arrow function and how is it used in React?](#what-is-an-arrow-function-and-how-is-it-used-in-react)
- [How is React different from React Native?](#how-is-react-different-from-react-native)

### What are the features of React?

- JSX
- Components
- Virtual DOM
- One-way data-binding
- High performance

#### JSX

JSX is a syntax extension to JavaScript. It is used with React to describe what
the user interface shoul look like. By using JSX, we can write HTML structures
in the same file that contains JavaScript code.

#### Components

Components are the building blocks of any React application, and a single app
usually consists of multiple components. It splits the user interface into
independent, reusable parts that can be processed separately.

#### Virtual DOM

React keeps a lightweight representation of the real DOM in the memory, and that
is known as the virtual DOM. When the state of an object changes, virtual DOM
changes only that object in the real DOM, rather than updating all the objects.

#### One-way data-binding

React’s one-way data binding keeps everything modular and fast. A unidirectional
data flow means that when designing a React app, you often nest child components
within parent components.

#### High performance

React updates only those components that have changed, rather than updating all
the components at once. This results in much faster web applications.

### What is JSX?

JSX is a syntax extension of JavaScript. It is used with React to describe what
the user interface should look like. By using JSX, we can write HTML structures
in the same file that contains JavaScript code.

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

- Web browsers cannot read JSX directly. This is because they are built to only
  read regular JS objects and JSX is not a regular JavaScript object.
- For a web browser to read a JSX file, the file needs to be transformed into a
  regular JavaScript object. For this, we use Babel.

![Babel](/react/Top%2040%20ReactJS%20Interview%20Questions/Basic%20Level%20-%20ReactJS%20Interview%20Questions/babel.png)

### What is the virtual DOM?

DOM stands for Document Object Model. The DOM represents an HTML document with a
logical tree structure. Each branch of the tree ends in a node, and each node
contains objects.

React keeps a lightweight representation of the real DOM in the memory, and that
is known as the virtual DOM. When the state of an object changes, the virtual
DOM changes only that object in the real DOM, rather than updating all the
objects. The following are some of the most frequently asked react interview
questions.

![DOM](/react/Top%2040%20ReactJS%20Interview%20Questions/Basic%20Level%20-%20ReactJS%20Interview%20Questions/dom.png)

### Why use React instead of other frameworks, like Angular?

- Easy creation of dynamic applications
- Improved performance
- Reusale components
- Unidirectional data flow
- Dedicated tools for easy debugging

#### Easy creation of dynamic applications

React makes it easier to create dynamic web applications because it provides
less coding and provides more functionality, whereas, with JavaScript
applications, code tends to get complex very quickly.

#### Improved performance

React uses virtual DOM, which makes web applications perform faster. Virtual DOM
compares its previous state and updates only those components in the real DOM,
whose states have changed, rather than updating all the components — like
conventional web applications.

#### Reusale components

Components are the building blocks of any React application, and a single app
usually consists of multiple components. These components have their own logic
and controls, and they can be reused through the application, which, in turn,
dramatically reduces the development time of an application.

#### Unidirectional data flow

React follows a unidirectional data flow. This means that when designing a React
app, we often nest child components within parent components. And since the data
flows in a single direction, it becomes easier to debug errors and know where
the problem occurs in an application at the moment.

#### Dedicated tools for easy debugging

Facebook has released a chrome extension that we can use to debug React
applications. This makes the process of debugging React to web applications
faster and easier.

### What is the difference between the ES6 and ES5 standards?

- Components and Function
- `exports` vs `export`
- `require` vs `import`

#### Components and Function

```js
// ES5
var MyComponent = React.createClass({
  render: function () {
    return <h3>Hello World</h3>;
  },
});
// ES6
class MyComponent extends ReactComponent {
  render() {
    return <h3>Hello World</h3>;
  }
}
```

#### require vs import

```js
// ES5
var React = require("react");
// ES6
import React from "react";
```

### How do you create a React app?

- Install `NodeJS` on the computer because we need `npm` to install the React
  library. Npm is the node package manager that contains many JavaScript
  libraries, including React.
- Install the `create-react-app` package using the command prompt or terminal.
- Install a text editor of your choice, like `VS Code` or Sublime Text.

### What is an event in React?

An event is an action that a user or system may trigger, such as pressing a key,
a mouse click, etc.

- React events are named using camelCase, rather than lowercase in HTML.
- With JSX, you pass a function as the event handler, rather than a string in
  HTML.

### How do you create an event in React?

A React event can be created by doing the following code

```js
class HelloWorld extends ReactComponent {
  greeting() {
    aldert("Hello World");
  }
  render() {
    return <button onClick={this.work}></button>;
  }
}
```

### What are synthetic events in React?

- Synthetic events combine the response of different browser's native events
  into one API, ensuring that the events are consistent across different
  browsers.
- The application is consistent regardless of the browser it is running in. For
  example, `preventDefault` is a synthetic event.

```js
function ActionLink() {
  function handleClick(evt) {
    evt.preventDefault();
    console.info("You just clicked a link.");
  }
  return (
    <a href="#" onClick={handleClick}>
      Click Me
    </a>
  );
}
```

### Explain how lists work in React

- We create lists in React as we do in regular JavaScript. Lists display data in
  an ordered format
- The traversal of lists is done using the map() function

```js
const fruits = ["Apple", "Banana", "Orange", "Dart"];
const listOfFruits = () => {
  const listItems = fruits.map((fruit, index) => <li key={index}>{fruit}</li>);
  return <ul>{listItems}</ul>;
};
```

### Why is there a need for using keys in Lists?

- A key is a unique identifier and it is used to identify which items have
  changed, been updated or deleted from the lists.
- It also helps to determine which components need to be re-rendered instead of
  re-rendering all the components every time. Therefore, it increases
  performance, as only the updated components are re-rendered.

### What are forms in React?

- Using forms, users can interact with the application and enter the required
  information whenever needed. Form contain certain elements, such as text
  fields, buttons, checkboxes, radio buttons, etc.
- Forms are used for many different tasks such as user authentication,
  searching, filtering, indexing, etc.

### How do you create forms in React?

We create forms in React by doing the following:

```js
class NameForm extends React.Component {
  this.state = {value: ''};

  handleChange(event) {
    this.setState({value: event.target.value});
  };

  handleSubmit(event) {
    alert('A name was enterd: ' + this.state.value);
    event.preventDefault();
  };

  render() {
    return (
      <form onSubmit={this.handleSubmit.bind(this)}>
        <label>Name:</label>
        <input type='text' value={this.state.value}
          onChange={this.handleChange.bind(this)}/>
        <input type='submit' value="Submit"/>
      </form>
    )
  }
}
```

### How do you write comments in React?

There are basically two ways in which we can write comments:

- Single-line comments `//`
- Multi-line comments `/* */`

### What is an arrow function and how is it used in React?

- An arrow function is a short way of writing a function to React.
- It is unnecessary to bind ‘this’ inside the constructor when using an arrow
  function. This prevents bugs caused by the use of ‘this’ in React callbacks.

#### Without Arrow Function

```js
render() {
  return (
    <MyInput onChange={this.handleChange.bind(this)}/>
  )
}
```

#### With Arrow Function

```js
render() {
  return (
    <MyInput onChange={(e) => this.handleOnChange(e)} />
  )
}
```

### How is React different from React Native?

|               |       **React**       |   **React Native**    |
| :-----------: | :-------------------: | :-------------------: |
|    Release    |         2013          |         2015          |
|   Platform    |          Web          | Mobile - Android, iOS |
|     HTML      |          Yes          |          No           |
|      CSS      |          Yes          |          No           |
| Prerequisites | HTML, CSS, JavaScript |       React.js        |
