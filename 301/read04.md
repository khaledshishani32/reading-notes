# React and Forms
---

### What is a ‘Controlled Component ?
- A Controlled Component is one that takes its current value through props and notifies changes through callbacks like onChange . A parent component "controls" it by handling the callback and managing its own state and passing the new values as props to the controlled component.

### 2) Should we wait to store the users responses from the form into state when they submit the form OR should we update the state with their responses as soon as they enter them? Why.
- Since the value attribute is set on our form element, the displayed value will always be this.state.value, making the React state the source of truth. Since handleChange runs on every keystroke to update the React state, the displayed value will update as the user types.

### 3) How do we target what the user is entering if we have an event handler on an input field?
- When creating a form with React components, it is common to use an onChange handler to listen for changes to input elements and record their values in state.
    

   

### references :
---
[medium](https://medium.com)
[stackoverflow.](https://stackoverflow.com)
[educative](https://www.educative.io)
[flow.org](https://flow.org/en/docs/react/components/)