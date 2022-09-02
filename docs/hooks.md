# Hooks in React

Code(function) that is used to perform intercepting such call messages or events is called a hook.
Hooks are functions that let you “hook into” React state and lifecycle features from function components. Hooks don’t work inside classes — they let you use React without classes.
The purpose of hook to handle reactive data, any data that changes in the application.

  - useState
  - useEffect
  - useReducer
  - useRef
  - useContext
  - useDispatch

## useState

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

## useEffect

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
