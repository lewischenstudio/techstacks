## ReactJS Router Questions

#### Table of Contents

- [What is React Router?](#what-is-react-router)
- [Why do we need to React Router?](#why-do-we-need-to-react-router)
- [How is React routing different from conventional routing?](#how-is-react-routing-different-from-conventional-routing)
- [How do you implement React routing?](#how-do-you-implement-react-routing)

### What is React Router?

React Router is a routing library built on top of React, which is used to create routes in a
React application. This is one of the most frequently asked react interview questions.

### Why do we need to React Router?

- It maintains consistent structure and behavior and is used to develop single-page web
  applications.
- Enables multiple views in a single application by defining multiple routes in the React
  application.

### How is React routing different from conventional routing?

| SN  | **React Routing**                                   | **Conventional Routing**                        |
| --- | --------------------------------------------------- | ----------------------------------------------- |
| 1   | Single HTML Page                                    | Each view is a new HTML file                    |
| 2   | The user navigates multiple views in the same file  | The user navigates multiple files for each view |
| 3   | The page does not refresh since it is a single file | The page refreshes every time user navigates    |
| 4   | Improved performance                                | Slower performance                              |
|     |                                                     |                                                 |

### How do you implement React routing?

We can implement routing in our React application using this method:

Considering we have the components `App`, `About`, and `Contact` in our application:

```js
const routing = (
  <Router>
    <div>
      <h1>React Router Example</h1>
      <Route path="/" component={App} />
      <Route path="/about" component={About} />
      <Route path="/contact" component={Contact} />
    </div>
  </Router>
);
```
