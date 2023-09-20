## ReactJS Redux Interview Questions

#### Table of Contents

- [What is Redux?](#what-is-redux)
- [What are the components of Redux?](#what-are-the-components-of-redux)
- [What is the Flux?](#what-is-the-flux)
- [How is Redux different from Flux?](#how-is-redux-different-from-flux)

### What is Redux?

Redux is an open-source, JavaScript library used to manage the application state. React uses
Redux to build the user interface. It is a predictable state container for JavaScript
applications and is used for the entire application’s state management.

### What are the components of Redux?

- **Store**: Holds the state of the application.
- **Action**: The source information for the store.
- **Reducer**: Specifies how the application's state changes in response to actions sent to
  the store.

![React Components](/react/Top%2040%20ReactJS%20Interview%20Questions%20and%20Answers%20for%202023/ReactJS%20Redux%20Interview%20Questions/redux.png)

### What is the Flux?

- Flux is the application architecture that Facebook uses for building web applications. It is
  a method of handling complex data inside a client-side application and manages how data flows
  in a React application.
- There is a single source of data (the store) and triggering certain actions is the only way
  way to update them.The actions call the dispatcher, and then the store is triggered and
  updated with their own data accordingly.
- When a dispatch has been triggered, and the store updates, it will emit a change event that
  the views can rerender accordingly.

### How is Redux different from Flux?

| SN  | **Redux**                                                                   | **Flux**                                               |
| --- | --------------------------------------------------------------------------- | ------------------------------------------------------ |
| 1   | Redux is an open-source JavaScript library used to manage application State | Flux is an architecture and not a framework or library |
| 2   | Store's state is immutable                                                  | Store's state is mutable                               |
| 3   | Can only have a single-store                                                | Can have multiple stores                               |
| 4   | Uses the concept of reducer                                                 | Uses the concept of the dispatcher                     |
|     |                                                                             |                                                        |
