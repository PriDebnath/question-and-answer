# Advanced React Interview Questions

### 1. What happens during React reconciliation?

React reconciliation is the process of comparing the new Virtual DOM with the previous one to determine what changes are needed.

* Uses **diffing algorithm**
* Updates only changed elements (efficient DOM updates)
* Uses **keys** to optimize list updates

---

### 2. How does React Fiber work?

React Fiber is the new reconciliation engine.

* Breaks rendering work into small units
* Enables **interruptible rendering**
* Supports **concurrent features**
* Prioritizes updates (important vs non-important)

---

### 3. What is Concurrent Rendering in React?

Concurrent rendering allows React to:

* Pause rendering
* Resume later
* Prioritize urgent updates (like user input)

Improves UI responsiveness.

---

### 4. Difference between useEffect and useLayoutEffect?

useEffect:

* Runs after DOM is painted
* Non-blocking

useLayoutEffect:

* Runs before DOM paint
* Blocking (can affect performance)

---

### 5. What are stale closures in React?

A stale closure happens when a function captures an outdated state value.

Example issue:

```js
useEffect(() => {
  setInterval(() => {
    console.log(count); // old value
  }, 1000);
}, []);
```

Solution:

* Use dependencies
* Or useRef

---

### 6. How does React handle batching?

React batches multiple state updates into a single re-render.

* Improves performance
* In React 18 → automatic batching everywhere

---

### 7. What is the difference between controlled vs uncontrolled inputs at scale?

Controlled:

* React manages state
* More control, validation easier

Uncontrolled:

* DOM handles state
* Better performance in large forms

---

### 8. Explain useRef in depth

useRef:

* Stores mutable values
* Doesn’t trigger re-render
* Used for:

  * DOM access
  * Persisting values between renders

---

### 9. How does React.memo work internally?

* Performs **shallow comparison of props**
* Prevents re-render if props unchanged

Limit:5

* Doesn’t deeply compare objects

---

### 10. When should you NOT use memo/useMemo/useCallback?

Avoid when:

* Component is simple
* No performance issue
* Adds unnecessary complexity

---

### 11. What is prop drilling and how do you avoid it?

Prop drilling = passing props deeply through components.

Solutions:

* Context API
* Redux / Zustand
* Component composition

---

### 12. Explain Context API performance issues

Problem:

* All consumers re-render when context value changes

Solutions:

* Split contexts
* Memoize values
* Use selectors (advanced)

---

### 13. What is a custom hook?

A custom hook is a reusable function using hooks.

```js
function useFetch(url) {
  const [data, setData] = useState(null);
  // logic
  return data;
}
```

---

### 14. What are render props?

A pattern where a component shares logic via a function prop.

```jsx
<Component render={(data) => <UI data={data} />} />
```

---

### 15. What are Higher Order Components (HOC)?

A function that takes a component and returns a new component.

```js
const withAuth = (Component) => {
  return () => <Component />;
};
```

---

### 16. Difference: HOC vs Hooks

HOC:

* Wrapper pattern

Hooks:

* Cleaner, reusable logic
* Preferred in modern React

---

### 17. What is code splitting?

Splitting bundle into smaller chunks.

* Improves performance
* Reduces initial load time

---

### 18. What is tree shaking?

Removes unused code from bundle.

* Done by bundlers like Webpack

---

### 19. What are portals in React?

Portals allow rendering outside parent DOM hierarchy.

```jsx
ReactDOM.createPortal(child, document.body);
```

---

### 20. What is hydration in React?

Hydration attaches event listeners to server-rendered HTML.

Used in:

* Next.js
* SSR apps

---

### 21. What is SSR vs CSR?

CSR:

* Rendering in browser

SSR:

* Rendering on server
* Faster initial load, better SEO

---

### 22. What is React Strict Mode?

A development tool that:

* Detects bugs
* Runs components twice (dev only)

---

### 23. How does React handle forms efficiently at scale?

* Controlled components for validation
* Libraries:

  * React Hook Form (performance optimized)
  * Formik

---

### 24. What is event delegation in React?

React attaches events at root (not each element).

* Improves performance
* Uses synthetic events

---

### 25. What are synthetic events?

React’s wrapper around native events.

* Cross-browser compatible
* Same API everywhere

---

### 26. What is the difference between key and index as key?

Bad:

```jsx
key={index}
```

Good:

```jsx
key={item.id}
```

Why:

* Index can break UI on reorder

---

### 27. What is debouncing and throttling in React?

Debouncing:

* Delay execution until user stops typing

Throttling:

* Limit execution rate

Used in:

* Search inputs
* Scroll events

---

### 28. How do you optimize React performance?

* React.memo
* useMemo / useCallback
* Code splitting
* Avoid unnecessary re-renders
* Virtualization (react-window)
• React.lazy loading 
---

### 29. What is virtualization?

Rendering only visible items in large lists.

Example:

* react-window
* react-virtualized

---

### 30. Explain React architecture for a scalable app

* Component-based structure
* Separation of concerns
* State management (Redux/Zustand)
* API layer separation
* Reusable hooks
* Lazy loading modules

---

## Tip for Interview
Always:

* Explain concept
* Give example
* Mention trade-offs

---

