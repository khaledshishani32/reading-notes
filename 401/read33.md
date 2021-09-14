## Next.js Assets, Metadata & CSS 

### To build a complete web application with React from scratch, there are many important details you need to consider:

- Code has to be bundled using a bundler like webpack and transformed using a compiler like Babel.
- You need to do production optimizations such as code splitting.
- You might want to statically pre-render some pages for performance and SEO. You might also want to use server-side     rendering or client-side rendering.
- You might have to write some server-side code to connect your React app to your data store.


#### Next.js handles static assets such as images and video. Metadata like HTML tag. CSS styling allows you to import css and scss files.

## Assets

#### When we put static files like images and video under top-level ‘public’ folder. Files in the public folder can be referenced by pages.

#### So we can use the picture vercel.svg into our first-post page.
```
<img src="/vercel.svg" alt="Vercel Logo" className="logo" />
```
![](https://wiztone.github.io/2020/06/17/Next-js-Assets-Metadata-CSS/02.png)


## Metadata

#### Metadata like html tag <head> has been instead of <Head> , which is React component in Next.js. We can add <Head> into our first-post.js
![](https://wiztone.github.io/2020/06/17/Next-js-Assets-Metadata-CSS/01.png)

## CSS

- Next.js use styled-jsx which is a CSS in JS, we can write the CSS only for the specific component. Besides, Next.js allows to import .css and .scss files.
- We can also create the _app.js for the global entry point, then import CSS file for the global CSS styling.



### What is React context?

#### React context allows us to pass down and use (consume) data in whatever component we need in our React app without using props.

### When should you use React context?

#### React context is great when you are passing data that can be used in any component in your application.

#### These types of data include:

- Theme data (like dark or light mode)
- User data (the currently authenticated user)
- Location-specific data (like user language or locale)

### How do I use React context?

#### Context is an API that is built into React, starting from React version 16.

#### This means that we can create and use context directly by importing React in any React project.

#### There are four steps to using React context:

- Create context using the createContext method.
- Take your created context and wrap the context provider around your component tree.
- Put any value you like on your context provider using the value prop.
- Read that value within any component by using the context consumer.

### What is the useContext hook?
#### Looking at the example above, the render props pattern for consuming context may look a bit strange to you.

#### Another way of consuming context became available in React 16.8 with the arrival of React hooks. We can now consume context with the useContext hook.

#### Instead of using render props, we can pass the entire context object to React.useContext() to consume context at the top of our component.

#### Here is the example above using the useContext hook:

```
import React from 'react';

export const UserContext = React.createContext();

export default function App() {
  return (
    <UserContext.Provider value="Reed">
      <User />
    </UserContext.Provider>
  )
}

function User() {
  const value = React.useContext(UserContext);  
    
  return <h1>{value}</h1>;
}
```

