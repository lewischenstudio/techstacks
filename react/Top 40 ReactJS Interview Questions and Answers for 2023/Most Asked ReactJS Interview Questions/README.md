## Most Asked ReactJS Interview Questions

#### Table of Contents

- [What is ReactJS?](#what-is-reactjs)
- [Why ReactJS is Used?](#why-reactjs-is-used)
- [How Does ReactJS work?](#how-does-reactjs-work)
- [What are the features of ReactJS?](#what-are-the-features-of-reactjs)
- [What is JSX?](#what-is-jsx)
- [How to create components in ReactJS?](#how-to-create-components-in-reactjs)
- [What are the advantages of ReactJS?](#what-are-the-advantages-of-reactjs)
- [Differentiate between real DOM and virtual DOM?](#differentiate-between-real-dom-and-virtual-dom)
- [What are forms in ReactJS?](#what-are-forms-in-reactjs)
- [How is React different from React Native?](#how-is-react-different-from-react-native)

### What is ReactJS?

React is a JavaScript-based UI development library. Facebook and an open-source developer community run it. Although React is a library rather than a language, it is widely used in web development. The library first appeared in May 2013 and is now one of the most commonly used frontend libraries for web development.

React offers various extensions for entire application architectural support, such as Flux and React Native, beyond mere UI.

### Why ReactJS is Used?

ReactJS's primary goal is to create User Interfaces (UI) which enhance the speed of programs. It makes use of virtual DOM (JavaScript object), which enhances the app's efficiency. Quicker than the standard DOM is the JavaScript virtual DOM.

React's popularity today has eclipsed that of all other front-end development frameworks. Here is why:

- Easy creation of dynamic applications: React makes it easier to create dynamic web applications because it requires less coding and offers more functionality, as opposed to JavaScript, where coding often gets complex very quickly.
- Improved performance: React uses Virtual DOM, thereby creating web applications faster. Virtual DOM compares the components' previous states and updates only the items in the Real DOM that were changed, instead of updating all of the components again, as conventional web applications do.
- Reusable components: Components are the building blocks of any React application, and a single app usually consists of multiple components. These components have their logic and controls, and they can be reused throughout the application, which in turn dramatically reduces the application's development time.
- Unidirectional data flow: React follows a unidirectional data flow. This means that when designing a React app, developers often nest child components within parent components. Since the data flows in a single direction, it becomes easier to debug errors and know where a problem occurs in an application at the moment in question.
- Small learning curve: React is easy to learn, as it mostly combines basic HTML and JavaScript concepts with some beneficial additions. Still, as is the case with other tools and frameworks, you have to spend some time to get a proper understanding of React's library.
- It can be used for the development of both web and mobile apps: We already know that React is used for the development of web applications, but that's not all it can do. There is a framework called React Native, derived from React itself, that is hugely popular and is used for creating beautiful mobile applications. So, in reality, React can be used for making both web and mobile applications.
- Dedicated tools for easy debugging: Facebook has released a Chrome extension that can be used to debug React applications. This makes the process of debugging React web applications faster and easier.

### How Does ReactJS work?

ReactJS creates basic views for every state in the project. When the data changes, the framework also updates and renders the appropriate component promptly. Things that are used
in React are the following:

- components
- properties
- states

To begin with, we can create either a functional or class component, in which there may or may not have be properties inherited from its parent component. We can define state objects in class components (or functional components with side effects). Using JSX, we can write HTML structures in the React component that contains JavaScript codes. JSX is used to describe (render) what the user interface should look like. As time goes by, the component needs to be re-rendered when its state changes. The component’s state may change owing to user action or system-generated events. These changes affect the component’s behavior.

### What are the features of ReactJS?

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

React's one-way data binding keeps everything modular and fast. A unidirectional data flow means that
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

### How to create components in ReactJS?

There are two types of components in React:

- functional components
- class components

#### Functional Components

These types of components have no state of their own and only contain render methods, and
therefore are also called stateless components. They may derive data from other components as
props (properties). We create a functional component in the following way.

```js
function Greeting(props) {
  return <h1>Welcome to {props.name}</h1>;
}
```

#### Class Components

These types of components can hold and manage their own state and have a separate render
method to return JSX on the screen. They are also called Stateful components as they can have
a state. The following way is how we create a class component.

```js
class Greeting extends React.Component {
  render() {
    return <h1>Welcome to {this.props.name}</h1>;
  }
}
```

### What are the advantages of ReactJS?

- React.js builds a customized virtual DOM. Because the JavaScript virtual DOM is quicker than the conventional DOM, this will enhance the performance of apps.
- ReactJS makes an amazing UI possible.
- Search - engine friendly ReactJS.
- Modules and valid data make larger apps easier to manage by increasing readability.
- React integrates various architectures.
- React makes the entire scripting environment process simpler.
- It makes advanced maintenance easier and boosts output.
- Guarantees quicker rendering
- The availability of a script for developing mobile apps is the best feature of React.
- ReactJS is supported by a large community.

#### Advantages and Limitations (Pros and Cons)

**Advantages**

- Makes use of the JavaScript structure known as virtual DOM. Since JavaScript's virtual DOM is quicker than the conventional DOM, this will boost the speed of programs.
- Can be used with various systems and on both client and server sides is commendable.
- Components and identify trends make larger apps easier to manage by increasing clarity.

**Limitations**

- Only addresses the app's angle and distance; as a result, additional techniques must be selected if you want a full collection of development tools.
- Employs inline scripting and JSX, which some programmers might find uncomfortable.

### Differentiate between real DOM and virtual DOM?

The Virtual DOM is React's lightweight version of the Real DOM. Real DOM manipulation is substantially slower than virtual DOM manipulation. When an object's state changes, Virtual DOM updates only that object in the real DOM rather than all of them.

DOM (Document Object Model) treats an XML or HTML document as a tree structure in which each node is an object representing a part of the document.

When the state of an object changes in a React application, VDOM gets updated. It then compares its previous state and then updates only those objects in the real DOM instead of updating all of the objects. This makes things move fast, especially when compared to other front-end technologies that have to update each object even if only a single object changes in the web application.

|        |        **VDOM**        |      **RDOM**      |
| ------ | :--------------------: | :----------------: |
| speed  |          fast          |        slow        |
| upadte | only an object's state | all of the objects |

### What are forms in ReactJS?

- Using forms, users can interact with the application and enter the required information
  whenever needed. Form contain certain elements, such as text fields, buttons, checkboxes,
  radio buttons, etc.
- Forms are used for many different tasks such as user authentication, searching, filtering,
  indexing, etc.

### How is React different from React Native?

|               |       **React**       |   **React Native**    |
| :-----------: | :-------------------: | :-------------------: |
|    Release    |         2013          |         2015          |
|   Platform    |          Web          | Mobile - Android, iOS |
|     HTML      |          Yes          |          No           |
|      CSS      |          Yes          |          No           |
| Prerequisites | HTML, CSS, JavaScript |       React.js        |
