## ES6 Syntax and Feature Overview

### Variable declaration

#### ES6 introduced the let keyword, which allows for block-scoped variables which cannot be hoisted or redeclared.
#### ES5
```
var x = 0
```

#### ES6
```
let x = 0
```

#### Constant declaration

```
const CONST_IDENTIFIER = 0 // constants are uppercase by convention
```

### Arrow functions

#### The arrow function expression syntax is a shorter way of creating a function expression. Arrow functions do not have their own this, do not have prototypes, cannot be used for constructors, and should not be used as object methods.
#### ES5
```
function func(a, b, c) {} // function declaration
var func = function (a, b, c) {} // function expression
```

#### ES6
```
let func = (a) => {} // parentheses optional with one parameter
let func = (a, b, c) => {} // parentheses required with multiple parameters
```

### Default parameters

#### Functions can be initialized with default parameters, which will be used only if an argument is not invoked through the function.
#### ES5
```
var func = function (a, b) {
  b = b === undefined ? 2 : b
  return a + b
}
```
#### ES6
```
let func = (a, b = 2) => {
  return a + b
}
```

## React 

### Introducing JSX
#### Consider this variable declaration:
```
const element = <h1>Hello, world!</h1>;
```
#### It is called JSX, and it is a syntax extension to JavaScript. We recommend using it with React to describe what the UI should look like. JSX may remind you of a template language, but it comes with the full power of JavaScript.

### JSX Represents Objects 
#### Babel compiles JSX down to React.createElement() calls.

#### These two examples are identical:
```
const element = (
  <h1 className="greeting">
    Hello, world!
  </h1>
);
```
```
const element = React.createElement(
  'h1',
  {className: 'greeting'},
  'Hello, world!'
);
```

### Components and Props
#### Components let you split the UI into independent, reusable pieces, and think about each piece in isolation. 

### Function and Class Components 
#### The simplest way to define a component is to write a JavaScript function:
```
function Welcome(props) {
  return <h1>Hello, {props.name}</h1>;
}
```
#### This function is a valid React component because it accepts a single “props” (which stands for properties) object argument with data and returns a React element. 

#### You can also use an ES6 class to define a component:
```
class Welcome extends React.Component {
  render() {
    return <h1>Hello, {this.props.name}</h1>;
  }
}
```
### Composing Components 
#### Components can refer to other components in their output. This lets us use the same component abstraction for any level of detail. A button, a form, a dialog, a screen: in React apps, all those are commonly expressed as components.

#### for example, we can create an App component that renders Welcome many times:
```
function Welcome(props) {
  return <h1>Hello, {props.name}</h1>;
}

function App() {
  return (
    <div>
      <Welcome name="Sara" />      <Welcome name="Cahal" />      <Welcome name="Edite" />    </div>
  );
}

ReactDOM.render(
  <App />,
  document.getElementById('root')
);
```

### State and Lifecycle

#### Consider the ticking clock example from one of the previous sections. In Rendering Elements, we have only learned one way to update the UI. We call ReactDOM.render() to change the rendered output:

```
function tick() {
  const element = (
    <div>
      <h1>Hello, world!</h1>
      <h2>It is {new Date().toLocaleTimeString()}.</h2>
    </div>
  );
  ReactDOM.render(    element,    document.getElementById('root')  );}

setInterval(tick, 1000);
```

### Steps to Converting a Function to a Class :


- Create an ES6 class, with the same name, that extends React.Component.
- Add a single empty method to it called render().
- Move the body of the function into the render() method.
- Replace props with this.props in the render() body.
- Delete the remaining empty function declaration.

### Handling Events 

#### Handling events with React elements is very similar to handling events on DOM elements. There are some syntax differences:

- React events are named using camelCase, rather than lowercase.
- With JSX you pass a function as the event handler, rather than a string.

#### For example, the HTML:
```
<button onclick="activateLasers()">
  Activate Lasers
</button>
```
#### is slightly different in React:
```
<button onClick={activateLasers}>  Activate Lasers
</button>
```

#### Passing Arguments to Event Handlers 

#### Inside a loop, it is common to want to pass an extra parameter to an event handler. For example, if id is the row ID, either of the following would work:
```
<button onClick={(e) => this.deleteRow(id, e)}>Delete Row</button>
<button onClick={this.deleteRow.bind(this, id)}>Delete Row</button>
```

### Utility First CSS

#### Traditionally, whenever you need to style something on the web, you write CSS.

#### With Tailwind, you style elements by applying pre-existing classes directly in your HTML.

```
<div class="p-6 max-w-sm mx-auto bg-white rounded-xl shadow-md flex items-center space-x-4">
  <div class="flex-shrink-0">
    <img class="h-12 w-12" src="/img/logo.svg" alt="ChitChat Logo">
  </div>
  <div>
    <div class="text-xl font-medium text-black">ChitChat</div>
    <p class="text-gray-500">You have a new message!</p>
  </div>
</div>
```
#### In the example above, we’ve used:

- Tailwind’s flexbox and padding utilities (flex, flex-shrink-0, and p-6) to control the overall card layout
- The max-width and margin utilities (max-w-sm and mx-auto) to constrain the card width and center it horizontally
- The background color, border radius, and box-shadow utilities (bg-white, rounded-xl, and shadow-md) to style the card’s appearance
- The width and height utilities (w-12 and h-12) to size the logo image
- The space-between utilities (space-x-4) to handle the spacing between the logo and the text
- The font size, text color, and font-weight utilities (text-xl, text-black, font-medium, etc.) to style the card text

## Learn Next.js

#### To build a complete web application with React from scratch, there are many important details you need to consider:

- Code has to be bundled using a bundler like webpack and transformed using a compiler like Babel.
- You need to do production optimizations such as code splitting.
- You might want to statically pre-render some pages for performance and SEO. You might also want to use server-side rendering or client-side rendering.
- You might have to write some server-side code to connect your React app to your data store.

### Next.js: The React Framework
#### Enter Next.js, the React Framework. Next.js provides a solution to all of the above problems. But more importantly, it puts you and your team in the pit of success when building React applications.

#### Next.js aims to have best-in-class developer experience and many built-in features, such as:

- An intuitive page-based routing system (with support for dynamic routes)
- Pre-rendering, both static generation (SSG) and server-side rendering (SSR) are supported on a per-page basis
- Automatic code splitting for faster page loads
- Client-side routing with optimized prefetching
- Built-in CSS and Sass support, and support for any CSS-in-JS library
- Development environment with Fast Refresh support
- API routes to build API endpoints with Serverless Functions
- Fully extendable