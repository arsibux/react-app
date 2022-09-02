# Destructuring in React

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