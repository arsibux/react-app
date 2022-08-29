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
  3. Statefull Component
  4. Stateless Component


### Function Component
A functional component is just a plain JavaScript pure function that accepts props as an argument and returns a React element(JSX).

```
const train=()=> {
  return <h2>Hi, I am also a Car!</h2>;
}
```

### Class Component
A class component requires you to extend from React. Component and create a render function which returns a React element.
There is no render method used in functional components.


```
class Train extends React.Component {
  render() {
    return <h2>Hi, I am a Car!</h2>;
  }
}
```

### Statefull Component

### Stateless Component