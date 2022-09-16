# ReactJS - Overview (reactive to every change)

Javascript library used to build **Single Page Application (SPA)** UIs with reuseable components.
It also know as frontend JavaScript framework and toolkit to make declarative smalll pieces of code called components.
It is efficient and fexible javaScript JS Library.
It creates **Virtual Document Object Model** in memory and all manipulation of data occurs in virtual DOM before the browser DOM.

  1. **What is JSX**: Translate tags into react elements.
  2. **State**: Data that may change in application.
  3. **React Components**: Small piece of code having UI and its states and related function.
  4. **React Props**: Arguments passed into React components.
  5. **Destructuring in React**: Destructuring makes it easy to extract only what is needed in array or in object.
  6. **React Hooks**: Perform intercepting such call messages or events.
  7. **React Router**: HTTP requests are routed to the code that handles them.
  8. **Redux**: State management library.

## What is JSX ?

Stands for JavaScript XML. JSX allows us to write HTML in React. JSX makes it easier to write and add HTML in React.

![jsx](https://github.com/arsibux/react-app/blob/main/docs/img/jsx.jpg)

## React Components

React component is an independent and reusable bits of code (function) that retrun the react elements (UI).
React element is **"DOM->Document Object Model"** object of an element.
It serves as same javascript function but work in isolation with HTML elements.

![react-component](https://github.com/arsibux/react-app/blob/main/docs/img/components.jpg "react-component")


**"The Document Object Model (DOM)"** is an application programming interface (API) for HTML and XML documents.
It defines the logical structure of documents and the way a document is accessed and manipulated.

### Types of Components

  1. Function Component
  2. Classes Component

### Function Component
A functional component is just a plain JavaScript pure function that accepts props as an argument and returns a React element(JSX).
There is no render method used in functional components.

```
const train=()=> {
  return <h2>Hi, I am also a Train!</h2>;
}
```

### Class Component
A class component requires you to extend from React. Component and create a render function which returns a React element.
This is the bread and butter of most modern web apps built in ReactJS. These components are simple classes (made up of multiple functions that add functionality to the application).

```
class Train extends React.Component {
  render() {
    return <h2>Hi, I am a Train!</h2>;
  }
}
```

### Stateful and Stateless Components

Stateful and stateless components have many different names.

They are also known as:
– Container vs Presentational components
– Smart vs Dumb components

The literal difference is that one has state, and the other doesn’t. That means the stateful components are keeping track of changing data, while stateless components print out what is given to them via props, or they always render the same thing.

Stateful/Container/Smart component:

```
class Main extends Component {
  constructor() {
    super()
    this.state = {
      books: []
    }
  }
  render() {
    return <BooksList books={this.state.books} />;
  }
}
```

Stateless/Presentational/Dumb component:

```
const BooksList = ({books}) => {
  return (
    <ul>
      {books.map(book => {
        return <li>book</li>
      })}
    </ul>
  )
}
```

Notice the stateless component is written as a function. As cool as state is, you should always aim to make your components as simple and stateless as possible, so different components can be reused like Lego pieces, even if you don’t have immediate plans to reuse a component. The stateful ones should feel lucky to be so

## React props

Props stand for **"properties"**  immuteable or read only attributes(arguments) of a components.
It stores the values of attributes of a tag `<Components name="Ali"  age="25" hieght="5.8"/>`.

![component props](https://github.com/arsibux/react-app-overview/blob/main/docs/img/props.jpg "component props")

```
function Student(props){
  return (
    <>
      <div className="student-profile-container">
        <div className="name">{prop.name}</div>
        <div className="name">{prop.age}</div>
        <div className="name">{prop.height}</div>
      </div>
    </>
  );
}
```

## Destructuring in React

Make available only required individual item, element, or properties of an array or object.
We may have an array or object that we are working with, but we only need some of the items contained in these.

![destructuring](https://github.com/arsibux/react-app-overview/blob/main/docs/img/dest.jpg "destructuring")

```
const student=['Ali', '25', '5.8'];
const height = studuent[2]; // without destructuring

const [name, age, height]= student;

// now value of age is Ali
// value of age  is 25
// value of height is 5.8

<Component name={name} age={age} height={height} /> // using destructuring
```
## State Management

**"State"**: State is data that may change in applicatiion. State is data storage to the component only.
React manages the data(State) by following ways.

  1. URLs
  2. Web Storage  (persist data [cookies, localStorage, indexedDB])
  3. Local Storage (locate state in components)
  4. Lifted State (FormData, Toggles, LocalLists)
  5. Derived State (derived from existing state)
  6. Refs (DOM References)
  7. Context (Loggedin user, Authorizations Settings, Theming, Internationalization Settings)
  8. Third Party Lib (Redux, Mobx, Recoil) remote state (reac-query, Swr, Relay, Appolo)

### Props Drilling

  Passing data through nest component and make available data(state) to child components.

  ![props drilling](https://github.com/arsibux/react-app-overview/blob/main/docs/img/drilling.jpg "drilling")

### Lifting State up

Make available **STATE**(updated data) of child component to its ancestor components or any other component that needs the data.

![lifting up](https://github.com/arsibux/react-app-overview/blob/main/docs/img/liftingup.jpg "lifting")

### Global State

 Single centrilized shared and unrestricted globally accessible state for all application components.
 **Note**:On update state all components shares the same state.

 ![global](https://github.com/arsibux/react-app-overview/blob/main/docs/img/global.jpg "global")


## React Ecosystems
Javascript libraries that helps the react development.

### React Router

ReactJS Router is seperate JS library for navigation among the pages and views of the components in react application.
Router keeps UI (components) sync to URLs and used to creating routing the react application.

![router](https://github.com/arsibux/react-app-overview/blob/main/docs/img/router.jpg "router")

### React Redux

Javascript Library is used to managing the states (Data) of react application. State management pattern with the help of **Events** called **actions**.
It provides shared state management with restrictions and rules, state can be accessed across the different components.

![redux](https://github.com/arsibux/react-app-overview/blob/main/docs/img/redux.jpg "redux")

**Redux Store**: Global Store with big JSON Data.It is **Data Store** for server or internal application DATA(State) that needs to be tracked.

![redux store](https://github.com/arsibux/react-app-overview/blob/main/docs/img/reduxstore.jpg "redux store")

#### Redux Actions
#### Redux Reducers

## React Hooks

Code(function) that is used to perform intercepting such call messages or events is called a hook.
Hooks are functions that let you “hook into” React state and lifecycle features from function components. Hooks don’t work inside classes — they let you use React without classes.
The purpose of hook to handle reactive data, any data that changes in the application.

  - useState
  - useEffect
  - useReducer
  - useRef
  - useContext
  - useDispatch

### useState

  Provides reative values(states) with updater function that can change the value(state) of variable.
  useState allows us to track state(data or value) in a function component.

  ```
  function Name(){

    // Initial state or value of name variable is Ali;
    // setName is function that helps to change the state of variable.
    const [name , setName] = useState("Ali");

    return (
      <>
        <span>{name}</span>
        // updater function update the state of variable <name>.
        <button type="button" onClick={setName('Amin')}>update name</button>
      </>
    );

  }
  ```

  ### useEffect

  In this hook a function is triggered when state of variable changes. It consists of two parts.
  **"useEffect(<function>, <dependency>)"** useEffect accepts two arguments. The second argument is optional.

  ```
  function Counter(){
    const [count, setCount] = useState(0);
    const [cal, setCal] = useState(0);

    useEffect(()=>{
      // function dependent on count value update as state changes this function will triggered.
      setCal(()=>{
          count*2;
      })
    }, count);

    return (
      <>
      <button type="button" onClick={()=>setCount((c)=>c+1;)></button>
      </>
    );
  }
  ```

  ### useContext

  Make the state available globally. It accepts the context object of application and
  add the state to context object and make available it globally.

  ```
  import { useState, createContext, useContext } from "react";
  import ReactDOM from "react-dom/client";

  const UserContext =  createContext(UserContext);

  // Now adding state to context object in one component.
  function  Com1(){
    const [user, setUser] = useState('Ali');
    return(
        // making user state available  globally.
        <UserContext.Provider value={user}>
        <h1>Hello, {user}</h1>
        </UserContext.Provider>
    );
  }

  // Getting the value of user cross Components
  function Com2(){
    const user = useContext(UserContext);
      return(
        <>
          <h2>Hi, {user}</h2>
        </>
      );
  }
  ```

  ### useReducer
  useState with initial state and action. State will update accordingly action.

  ```
  function Student(){
    const initialState = {
      name: "Ali",
      age: 25,
      height: "5.8"
    };

    function reducer(state, action) {
      switch (action.type) {
        case "name":
          return {
            name: "Aslam",
            height: "5.8",
            age: 25
          };
        case "age":
          return {
            name: "Ali",
            height: "5.8",
            age: 35
          };
        case "height":
          return {
            name: "Ali",
            height: "5.8",
            age: 25
          };
        default:
          return {};
      }
    }
    const [student, dispatch] = useReducer(reducer, initialState);
    return (
      <>
        <div className="student-profile-container">
          <div className="name">{student.name}</div>
          <div className="name">{student.age}</div>
          <div className="name">{student.height}</div>
        </div>
        <button onClick={() => dispatch({ type: "name" })}>Name</button>
        <button onClick={() => dispatch({ type: "age" })}>Age</button>
        <button onClick={() => dispatch({ type: "height" })}>Height</button>
      </>
    );
  }
  ```

  ### useRef
  Hook which reach out to the components value.

  ```
  const sound = useRef();
  const color = useRef();
  const submit = (e) => {
    e.preventDefault();
    const soundVal = sound.current.value;
    const colorVal = color.current.value;
    alert(`${soundVal} sounds liek ${colorVal}`);
  };
  return (
    <>
      <form onSubmit={submit}>
        <input ref={sound} type="text" />
        <input ref={color} type="color" />
        <button>add</button>
      </form>
    </>
  );

  ```
## React Terms

|  Sr  |     Title     | Description                                           |
| :-:  | :-----------: | --------------------------------------------------- |
|  1   | Node Js | Javascript open source server environment runs on various plateforms. |
|  2   | npm | Node Package(dependency) Manager. |
|  3   | npx | Node Package Execute(Runner) comes with npm. |
|  4   | yarn | Package Manager like npm. |
|  5   | SPA | Single Page Application. |
|  6   | Compiler | Takes the JS code and transform into different formats. Babel is the most commonly used compiler in react. |
|  7   | Events | is an action that takes place when user interacts with program.
|  8   | Action | is set instructions as a function that required to run.
|  9   | Event Handler | is callback function run asynchronously once at certain event.
|  10  | Callback fn | function runs in sequence as first finished.


## Toolkit

  - [Chrome dev tools for react](https://chrome.google.com/webstore/detail/react-developer-tools/fmkadmapgofadopljbjfkapdkoienihi?hl=en) development tool to inspect react components.
  - [Firefox dev tools for react](https://addons.mozilla.org/en-GB/firefox/addon/react-devtools/) development tool to inspect react components.
  - [VScode](https://code.visualstudio.com/download) Code editor
  - [Code sandbox for react](https://codesandbox.io/s/new?utm_source=dotnew) provide plateform for react developmentand testing.
  - [Codepen](https://codepen.io/) provide plateform for coding and testing.
  - [Glitch](https://glitch.com/) provide plateform for coding and testing.
  - [Bibel JS](https://babeljs.io/repl/) convert html tags to javascript elements object.
  - [Jest Js](https://jestjs.io) provide matcher.
  - [Netlify](https://www.netlify.com/) Build, deployment application. (custom domain, https support.)
  - [What is Redux](https://redux.js.org/tutorials/essentials/part-1-overview-concepts)
  - [Redux DevTools for chrome](https://chrome.google.com/webstore/detail/redux-devtools/lmhkpmbekcpmknklioeibfkpmmfibljd?hl=en)
  - [Redux DevTools for firefox](https://addons.mozilla.org/en-US/firefox/addon/reduxdevtools/)

## Resources

  1. [React](https://reactjs.org/docs/getting-started.html)
  2. [JSX in React](https://www.w3schools.com/react/react_jsx.asp).
  3. [Stateful and Stateless](https://programmingwithmosh.com/javascript/stateful-stateless-components-react/)

## Changelog

- 2020-08-29
  - ADDED: Installation of react-application via npx.
  - ADDED: Documentation with images.
- 2020-08-31
  - ADDED: [Components](https://github.com/arsibux/react-app/blob/main/docs/components.md) documentation.
- 2020-09-02
  - ADDED: [Props](https://github.com/arsibux/react-app/blob/main/docs/props.md), [destructuring](https://github.com/arsibux/react-app/blob/main/docs/dest.md) and [hooks](https://github.com/arsibux/react-app/blob/main/docs/hooks.md) documentation.
- 2020-09-03
  - ADDED: [Types of hooks](https://github.com/arsibux/react-app/blob/main/docs/hooks.md)
  - ADDED: State Management
- 2020-09-05
  - ADDED: Router
  - ADDED: Redux and State Management.
- 2020-09-16
  - ADDED: Props Drilling
  - ADDED: Lifting State up
  - ADDED: Global state
  - UPDATE: Redux and State Management.
