## ReactJS Styling Questions

#### Table of Contents

- [How do you style React components?](#how-do-you-style-react-components)
- [Explain the use of CSS modules in React.](#explain-the-use-of-css-modules-in-react)

### How do you style React components?

There are several ways in which we can style React components:

- Inline Styling
- JavaScript Object
- CSS Stylesheet

#### Inline Styling

```js
class HelloWorld extends React.Component {
  render() {
    return (
      <div>
        <h1 style={{ color: "blue" }}>Hello World!</h1>
      </div>
    );
  }
}
```

#### JavaScript Object

```js
class HelloWorld extends React.Component {
  render() {
    const simpleStyle = {
      color: "blue",
      backgroundColor: "green",
      margin: "8px",
      fontFamily: "Roboto",
    };
    return (
      <div>
        <h1 style={simpleStyle}>Hello World!</h1>
      </div>
    );
  }
}
```

#### CSS Stylesheet

```css
h1 {
  color: "blue";
  background-color: "green";
  margin: "8px";
  font-family: "Roboto";
}
```

```js
import "./HelloWorld.css";

class HelloWorld extends React.Component {
  render() {
    return (
      <div>
        <h1>Hello World!</h1>
      </div>
    );
  }
}
```

### Explain the use of CSS modules in React.

- The CSS module file is created with the `.module.css` extension
- The CSS inside a module file is available only for the component that imported it, so there
  are no naming conflicts while styling the components.
