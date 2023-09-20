## ReactJS Interview Questions on Components

#### Table of Contents

- [What are the components in React?](#what-are-the-components-in-react)
- [What is the use of render() in React?](#what-is-the-use-of-render-in-react)
- [What is a state in React?](#what-is-a-state-in-react)
- [How do you implement state in React?](#how-do-you-implement-state-in-react)
- [How do you update the state of a component?](#how-do-you-update-the-state-of-a-component)
- [What are props in React?](#what-are-props-in-react)
- [How do you pass props between components?](#how-do-you-pass-props-between-components)
- [What are the differences between state and props?](#what-are-the-differences-between-state-and-props)
- [What is a higher-order component in React?](#what-is-a-higher-order-component-in-react)
- [How can you embed two or more components into one?](#how-can-you-embed-two-or-more-components-into-one)
- [What are the differences between class and functional components?](#what-are-the-differences-between-class-and-functional-components)

### What are the components in React?

Components are the building blocks of any React application, and a single app usually consists
of multiple components. A component is essentially a piece of the user interface. It splits
the user interface into independent, reusable parts that can be processed separately.

![React Components](/react/Top%2040%20ReactJS%20Interview%20Questions%20and%20Answers%20for%202023/ReactJS%20Interview%20Questions%20on%20Components/components.png)

There are two types of components in React:

#### Functional Components

These types of components have no state of their own and only contain render methods, and
therefore are also called stateless components. They may derive data from other components as
props (properties).

```js
function Greeting(props) {
  return <h1>Welcome to {props.name}</h1>;
}
```

#### Class Components

These types of components can hold and manage their own state and have a separate render
method to return JSX on the screen. They are also called Stateful components as they can have
a state.

```js
class Greeting extends React.Component {
  render() {
    return <h1>Welcome to {this.props.name}</h1>;
  }
}
```

### What is the use of render() in React?

- It is required for each component to have a render() function. This function returns the
  HTML, which is to be displayed in the component.
- If you need to render more than one element, all of the elements must be inside one parent
  tag like `<div>`, `<form>`.

```js
import React from "react";

class App extends React.Component {
  render() {
    return <h1>Hello World!</h1>;
  }
}
```

### What is a state in React?

- The state is a built-in React object that is used to contain data or information about the
  component. The state in a component can change over time, and whenever it changes, the
  component re-renders.
- The change in state can happen as a response to user action or system-generated events. It
  determines the behavior of the component and how it will render.

### How do you implement state in React?

A React state can be implemented by doing the following code

```js
import React from "react";

class App extends React.Component {
  constructor(props) {
    super(props);

    /* State holds the data that a component
       renders on the web app */
    this.state = {
      firstName: "Lewis",
      lastName: "Chen",
    };
  }
  render() {
    return (
      <div>
        {/* This is how we access the state properties */}
        <h1>{this.state.firstName}</h1>
        <h1>{this.state.lastName}</h1>
      </div>
    );
  }
}
```

### How do you update the state of a component?

We can update the state of a component by using the built-in `setState()` method:

```js
class App extends React.Component {
  constructor() {
    super();
    this.state = {
      message: "Welcome to Github",
    };
    this.buttonPress = this.buttonPress.bind(this);
  }
  buttonPress() {
    this.setState({
      message: "The best place to stack up skills",
    });
  }
  render() {
    return (
      <div>
        <h1>{this.state.message}</h1>
        <button onClick={this.buttonPress}>Click</button>
      </div>
    );
  }
}
```

### What are props in React?

- Props are short for Properties. It is a React built-in object that stores the value of
  attributes of a tag and works similarly to HTML attributes.
- Props provide a way to pass data from one component to another component. Props are passed
  to the component in the same way as arguments are passed in a function.

### How do you pass props between components?

Props are passed from the parent component to its children components.
Here we pass two properties `firstName` and `lastName` and their values from the `App`
component to the child component `NameComponent`.

**Parent Component**

```js
import React from "react";
import NameComponent from "./NameComponent";

class App extends React.Component {
  render() {
    return <NameComponent firstName={"Lewis"} lastName={"Chen"} />;
  }
}
```

**Child Component**

```js
import React from "react";

class NameComponent extends React.Component {
  constructor(props) {
    super(props);
  }
  render() {
    return (
      <div>
        <h1>{this.props.firstName}</h1>
        <h1>{this.props.lastName}</h1>
      </div>
    );
  }
}
```

### What are the differences between state and props?

|                      |               **State**                |                                 **Props**                                 |
| :------------------: | :------------------------------------: | :-----------------------------------------------------------------------: |
|         Use          | Holds information about the components | Allows to pass data from one component to other components as an argument |
|      Mutability      |               Is mutable               |                               Are immutable                               |
|      Read-Only       |             Can be changed             |                               Are read-only                               |
|   Child components   |     Child components cannot access     |                        Child component can access                         |
| Stateless components |           Cannot have state            |                              Can have props                               |

### What is a higher-order component in React?

A higher-order component acts as a container for other components. This helps to keep
components simple and enables re-usability. They are generally used when multiple components
have to use a common logic.

### How can you embed two or more components into one?

When we passed props from the parent to child component, we already embedded two components in
the above example. The basic structure of embedding two or more components into one is like
the following.

```js
class App extends React.Component {
  render() {
    return (
      <div>
        <h1>Hello </h1>
        <World />
      </div>
    );
  }
}

class World extends React.Component {
  render() {
    return <h1>World</h1>;
  }
}

ReactDom.render(<App />, document.getElementById("index"));
```

### What are the differences between class and functional components?

|                   | **Class Components**                           | **Functional Components**               |
| ----------------- | ---------------------------------------------- | --------------------------------------- |
| State             | Can hold or manage state                       | Cannot hold or manage state             |
| Simplicity        | Complex as compared to the stateless component | Simple and easy to understand           |
| Lifecycle methods | Can work with all lifecycle methods            | Does not work with any lifecycle method |
| Reusability       | Can be reused                                  | Cannot be reused                        |

#### Class Component

```js
class StatefulComponent extends React.Component {
  render() {
    return <div>{this.props.title}</div>;
  }
}
```

#### Functional Component

```js
const StatelessComponent = (props) => <div>{this.props.title}</div>;
```
