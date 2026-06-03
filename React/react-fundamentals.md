# 🧠 React Fundamentals – Answers & Explanations

## 1. What is React and why is it used?

**Answer:**
React is a JavaScript library used to build user interfaces, especially single-page applications.

**Explanation:**
It helps developers create reusable UI components and efficiently update the UI using a virtual DOM, which improves performance.

---

## 2. What is JSX?

**Answer:**
JSX stands for JavaScript XML. It allows us to write HTML-like code inside JavaScript.

**Explanation:**
Browsers don’t understand JSX directly, so it gets converted into regular JavaScript (using tools like Babel). It makes UI code easier to read and write.

---

## 3. Functional vs Class Components

**Answer:**

* Functional components are simple JavaScript functions.
* Class components use ES6 classes and have lifecycle methods.

**Explanation:**
Modern React mainly uses functional components with hooks because they are simpler and cleaner.

---

## 4. What are props?

**Answer:**
Props are inputs passed from a parent component to a child component.

**Explanation:**
They help make components reusable by allowing dynamic data to be passed.

---

## 5. Difference between state and props

**Answer:**

* Props are read-only and passed from parent
* State is managed inside the component and can change

**Explanation:**
State controls dynamic behavior, while props are used for communication between components.

---

## 6. Can props be modified?

**Answer:**
No, props are immutable (read-only).

**Explanation:**
Only the parent component can change props. This keeps data flow predictable.

---

## 7. What is `useState`?

**Answer:**
`useState` is a hook used to add state in functional components.

**Explanation:**
It returns a state variable and a function to update it. Updating state triggers re-render.

---

## 8. What is `useEffect`?

**Answer:**
`useEffect` is used to perform side effects in a component.

**Explanation:**
Examples of side effects:

* API calls
* Event listeners
* Timers

It runs after rendering.

---

## 9. useEffect vs lifecycle methods

**Answer:**
`useEffect` replaces lifecycle methods like:

* componentDidMount
* componentDidUpdate
* componentWillUnmount

**Explanation:**
Instead of multiple methods, `useEffect` handles everything in one place.

---

## 10. What is re-rendering?

**Answer:**
Re-rendering is when a component updates and displays new data.

**Explanation:**
It happens when:

* State changes
* Props change

React updates only the necessary parts using virtual DOM.

---

## 11. What is conditional rendering?

**Answer:**
Showing different UI based on conditions.

**Explanation:**
Example:

* Show login button if user is logged out
* Show dashboard if logged in

---

## 12. What are keys in React lists?

**Answer:**
Keys are unique identifiers used when rendering lists.

**Explanation:**
They help React identify which items changed, improving performance.

---

## 13. What is destructuring?

**Answer:**
Destructuring extracts values from objects or arrays.

**Explanation:**
Example:

```js
const { name } = props;
```

Makes code shorter and cleaner.

---

## 14. What are arrow functions?

**Answer:**
A shorter way to write functions in JavaScript.

**Explanation:**
Example:

```js
const add = (a, b) => a + b;
```

They don’t have their own `this`, which is useful in React.

---

## 15. Event handling in React

**Answer:**
Handling user actions like clicks, input, etc.

**Explanation:**
Example:

```js
<button onClick={handleClick}>Click</button>
```



## 16. What is Virtual DOM?

**Answer:**
Virtual DOM is a lightweight copy of the real DOM.

**Explanation:**
React updates the virtual DOM first, compares changes (diffing), and then updates only the necessary parts in the real DOM → faster performance.

---

## 17. What is a React Fragment?

**Answer:**
A wrapper that doesn’t add extra nodes to the DOM.

**Explanation:**
Example:

```jsx
<>
  <h1>Hello</h1>
  <p>World</p>
</>
```

Avoids unnecessary `<div>`.

---

## 18. What is lifting state up?

**Answer:**
Moving state to a common parent component.

**Explanation:**
Used when multiple child components need the same data.

---

## 19. What is controlled component?

**Answer:**
Form input controlled by React state.

**Explanation:**
React manages input value using `useState`.

---

## 20. What is uncontrolled component?

**Answer:**
Form input managed by the DOM itself.

**Explanation:**
Uses `ref` instead of state.

---

## 21. What is `useRef`?

**Answer:**
A hook to access DOM elements or persist values.

**Explanation:**
It doesn’t trigger re-render when value changes.

---

## 22. What is prop drilling?

**Answer:**
Passing props through multiple levels of components.

**Explanation:**
Becomes messy → solved using Context API.

---

## 23. What is Context API?

**Answer:**
A way to share data globally without prop drilling.

**Explanation:**
Useful for themes, auth, user data.

---

## 24. What is React Router?

**Answer:**
A library for navigation in React apps.

**Explanation:**
Used to create multiple pages without reloading.

---

## 25. What is SPA (Single Page Application)?

**Answer:**
A web app that loads one HTML page and updates dynamically.

**Explanation:**
React apps are typically SPAs.

---

## 26. What is a key difference between `==` and `===`?

**Answer:**

* `==` checks value only
* `===` checks value + type

**Explanation:**
Always prefer `===` in React.

---

## 27. What is map() in React?

**Answer:**
Used to render lists of elements.

**Explanation:**
Example:

```jsx
items.map(item => <li key={item.id}>{item.name}</li>)
```

---

## 28. What is default export vs named export?

**Answer:**

* Default export → one per file
* Named export → multiple per file

**Explanation:**
Import syntax differs.

---

## 29. What is event.preventDefault()?

**Answer:**
Stops default browser behavior.

**Explanation:**
Used in forms to prevent page reload.

---

## 30. What is React Strict Mode?

**Answer:**
A tool for highlighting potential problems.

**Explanation:**
It doesn’t affect production, only helps during development.

--


## 31. What is reconciliation in React?

**Answer:**
Reconciliation is the process React uses to update the DOM efficiently.

**Explanation:**
React compares the previous virtual DOM with the new one (diffing) and updates only changed elements instead of reloading everything.

---

## 32. What is the difference between `useEffect` and `useLayoutEffect`?

**Answer:**

* `useEffect` runs after the browser paints
* `useLayoutEffect` runs before the paint

**Explanation:**
`useLayoutEffect` is used when you need to measure or modify the DOM before the user sees it.

---

## 33. What is memoization in React?

**Answer:**
Memoization is an optimization technique to avoid unnecessary re-renders.

**Explanation:**
React provides:

* `React.memo` → for components
* `useMemo` → for values
* `useCallback` → for functions

---

## 34. What is `React.memo`?

**Answer:**
A higher-order component that prevents re-render if props don’t change.

**Explanation:**
Useful for performance optimization in large apps.

---

## 35. What is `useCallback`?

**Answer:**
A hook that returns a memoized function.

**Explanation:**
Prevents function re-creation on every render, especially useful when passing functions to child components.

---

## 36. What is `useMemo`?

**Answer:**
A hook that memoizes computed values.

**Explanation:**
Used when calculations are expensive.

---

## 37. What is lazy loading in React?

**Answer:**
Loading components only when needed.

**Explanation:**
Improves performance by reducing initial load time.

---

## 38. What is Suspense?

**Answer:**
A component used to handle lazy loading.

**Explanation:**
Shows fallback UI (like loader) while component loads.

---

## 39. What are higher-order components (HOC)?

**Answer:**
Functions that take a component and return a new component.

**Explanation:**
Used for reusing logic (e.g., authentication, logging).

---

## 40. What is error boundary?

**Answer:**
A component that catches JavaScript errors in child components.

**Explanation:**
Prevents the whole app from crashing.

---

## 41. What is the difference between `useState` and `useReducer`?

**Answer:**

* `useState` → simple state
* `useReducer` → complex state logic

**Explanation:**
`useReducer` is better when state depends on previous state or multiple actions.

---

## 42. What is batching in React?

**Answer:**
React groups multiple state updates into one render.

**Explanation:**
Improves performance by reducing unnecessary renders.

---

## 43. What is synthetic event in React?

**Answer:**
A wrapper around native browser events.

**Explanation:**
Provides consistent behavior across browsers.

---

## 44. What is the difference between `key` and `id`?

**Answer:**

* `key` → used by React internally
* `id` → used in HTML/DOM

**Explanation:**
`key` is not accessible in props.

---

## 45. What causes unnecessary re-renders?

**Answer:**

* State changes
* Parent re-render
* New object/function references

**Explanation:**
Optimized using memoization techniques.

---


