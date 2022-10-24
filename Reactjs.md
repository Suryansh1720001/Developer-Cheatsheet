
# React-Cheatsheet🚀

ReactJS is an open-source, component based front end library. React d developed by Facebook and it is a JS library. Using this library we can build highly engaging and fast single-page web applications.

# Hello World in React
```sh
// Import React and ReactDOM
import React from 'react'
import ReactDOM from 'react-dom'
// Render component into the DOM - only once per app
ReactDOM.render(
 <h1>Hello, world!</h1>,
 document.getElementById('root')
);
```


## What is React Elements?
This React Elements are the smallest building blocks of React. This element describes what we want to see on the screen of our website.

```sh
<span>Title</span>
<div> lorem.....</div>
<button>button</button>
<h1>Headings</h1>
```
React elements is written by using a method called JSX.
All the single-tag elements should be self-closing and must end with a forward slash `/ ` , `ex- img tag` :

```sh
<br />
<img src="pic.jpeg" />
<hr />
```

## Attributes in React
JSX is totally JavaScript and JS uses a camelcase naming convention.
Attribute example: 
we write `class` attribute as `className` in Reactjs.

```sh
<div className="section"></div>
```

# Styling of elements in react
In react instead of using double quotes (“”), we use two sets of curly braces in case of inline styling.

```sh
<p style={{ fontSize: 34, margin: '0 auto auto 10px', textAlign: 'right', color:'red' }}> Paragraph Content</p>
```

# What is Fragments in React?

We can use fragments in those conditions when we don’t want to wrap  or there is no use to enclose our elements in a container element like a div. Symbol of fragment `<></>`:

```sh

function ComponentName() {
  return (
    <>
      <span>Title</span>
      </p>My paragraph Content</p>
    </>
  );
} 
```
# Components in React

Every application which we will develop in React is made up of pieces that pieces is called components. This make the life of developer easy and also we can easily collaborate on github and divide the tasks in component.

There are 2 types of components currently in React: Class and Functional.

# Class Component
```sh
import React from 'react'
import ReactDOM from 'react-dom'

class ProductCard extends React.Component {
  render() {
    return (
      <div>
        <h2>This is ProductCard </h2>
      </div>
    )
  }
}

ReactDOM.render(<ProductCard />, document.getElementById('root'));
```
# Functional Component
```sh
function Navbar() {
  return (
     <div> Navbar Content</div>
  );
} 

function Footer() {
  return (
     <div> Footer Content</div>
  );
} 
```
# Props in React 
In this code sample we are passing a prop `age ` from App to the Client component.
we passed Props from the parent component to a child component.
```sh
function App() {
  return <Client age="Twenty" />
}

function Client(props) {
  return <h1>John age is {props.age}</h1>; // John age is Twenty
}
```

# Children Props in React 
When we pass Props by placing data between the opening and closing tags of a component then this way passed Props  are placed on the `children` property.

```sh
function App() {
  return (
   <Client>
     <h1>Rohit age is Twenty</h1>
   </Client>
  );
}

function Client({ children }) {
  return children; // Rohit age is Twenty
}
```

# Stateless React Component
```sh
const Headline = () => {
 return <h1>React Cheat Sheet</h1>
}
// Component that receives props
const Greetings = (props) => {
 return <p>You will love it {props.name}.</p>
}
// Component must only return ONE element (eg. DIV)
const Intro = () => {
 return (
 <div>
 <Headline />
 <p>Welcome to the React world!</p>
 <Greetings name=”Petr” />
 </div>
 )
}
ReactDOM.render(
 <Intro />,
 document.getElementById('root')
);
```

# Conditional rendering of elements and CSS class

```sh
render() {
 const {isLoggedIn, username} = this.state;
 return (
 <div className={`login ${isLoggedIn ? 'is-in'
: 'is-out'}`}>
 {
 !!isLoggedIn ?
 <p>Logged in as {username}.</p>
 :
 <p>Logged out.</p>
 }
 </div>
 )
}
```

# Import multiple exports using braces
```sh
import React, {ComponentName} from 'react'
import ReactDOM from 'react-dom'
class Hello extends ComponentName {
  ...
}
```

# Lifecycle Methods in React

```sh
 componentWillMount() {
 // It will fires immediately before the initial render
 }
 componentDidMount() {
 // It will fires immediately after the initial render
 }
 componentWillReceiveProps() {
 // It will fires when component is receiving new props
 }
 shouldComponentUpdate() {
 // It will fires before rendering with new props or state
 }
 componentWillUpdate() {
 // It will fires immediately before rendering with new props or state
 }
 componentDidUpdate() {
 // It will fires immediately after rendering with new props or state
 }
 componentWillUnmount() {
 // It will fires immediately before component is unmounted from DOM (removed)
 }

```
# Follow for more
## Playlist
* [Here](https://www.youtube.com/watch?v=-mJFZp84TIY&list=PLu0W_9lII9agx66oZnT6IyhcMIbUMNMdt)
* [Here](https://www.youtube.com/watch?v=tiLWCNFzThE&list=PLwGdqUZWnOp3aROg4wypcRhZqJG3ajZWJ)
* [Here](https://www.youtube.com/watch?v=QFaFIcGhPoM&list=PLC3y8-rFHvwgg3vaYJgHGnModB54rxOk3)
 
## Tutorial
* [Here](https://www.w3schools.com/REACT/DEFAULT.ASP)
* [Here](https://www.tutorialspoint.com/reactjs/index.htm)


# Thank You!💙
 
 



 
 
 
 
 