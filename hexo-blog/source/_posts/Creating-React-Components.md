---
title: Creating React Components
date: 2018-06-04 04:38:32
tags:
  - [React, JavaScript, Components]
---
Components are the core of React. There are two ways to create components in React. The first way to use a JavaScript function (`stateless functional component`). A stateless component can receive data and render it, but does not manage or track changes to that data. The second way is by using ES6 class syntax.

### Create a React Functional Component
To create a component this way, write a JavaScript function that returns either JSX or `null`.

**Important:** React requires your function name to begin with a capital letter.
Here is an example of a stateless functional component that assigns an HTML class in JSX:

```jsx
const FunctionalComp = function() {
  return (
    <div className='customClass' />
  );
}
```

After being transpiled, the `<div>` will have a CSS class of 'customClass'.

**Example 2:**

```jsx
const MyComponent = function() {
  return (
    <div>
      <h1>This is a functional component</h1>
    </div>
  );
}
```

### Create a React Component with the ES6 class Syntax
First let's look at an example of creating a React component with the ES6 class syntax:

```jsx
class Dog extends React.Component {
  constructor(props) {
    super(props);
  }

  render() {
    return (
      <h1>Hello World!</h1>
    );
  }
}
```

In the above example, an ES6 class `Dog` extends the `React.Component` class. So the `Dog` class now has access to many useful React features. Local state and lifecycle hooks are two examples of these features.

The `Dog` class has a `constructor` defined within it that calls `super()`. It uses `super()` to call the constructor of the parent class, in this case `React.Component`.
The constructor is a special method used during the initialization of objects that are created with the `class` keyword.

**Example 2:**

```jsx
class MyComponent extends React.Component {
  constructor(props) {
    super(props);
  }
  
  render() {
    return (
      <div>
        <h1>ES6 class component</h1>
      </div>
    );
  }
};
```
