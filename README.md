# React Overview (reactive to every change)

Javascript library used to build **Single Page Application (SPA)** UIs with reuseable components.
It also know as frontend JavaScript framework and toolkit to make declarative smalll pieces of code called components.
It is efficient and fexible javaScript JS Library.

  1. **What is JSX**: Translate tags into react elements.
  2. **React Components**: Small piece of code having UI and its states and related function.
  3. **React Props**: Arguments passed into React components.
  4. **Destructuring in React**: Destructuring makes it easy to extract only what is needed in array or in object.
  5. **React Hooks**: Perform intercepting such call messages or events.
  6. **React Router**: HTTP requests are routed to the code that handles them.
  7. **Redux**

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

Props stand for **"properties"**  immuteable or read only attributes of a components.
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

### React Router

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