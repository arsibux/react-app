# React Components
React component is an independent and reusable bits of code (function) that retrun the react elements (UI).
React element is **"DOM->Document Object Model"** object of an element.
It serves as same javascript function but work in isolation with HTML elements.

![react-component](https://github.com/arsibux/react-app/blob/main/docs/img/components.jpg "react-component")


**"The Document Object Model (DOM)"** is an application programming interface (API) for HTML and XML documents.
It defines the logical structure of documents and the way a document is accessed and manipulated.

## Types of Components

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