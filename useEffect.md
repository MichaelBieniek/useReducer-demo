# useEffect

## What is a side effect?

Any change in state that is outside of the function (component).

Examples include:
- Modifying the DOM (e.g. update page title, register event listeners)
- Making an AJAX request (e.g. fetching data)

## Anatomy of useEffect

```js
useEffect(() => {
  // 1. Side effect
  return cleanupFunc; // 2. Side effect clean-up
}, [depsArray]);  // 3. Dependency array
```

## When does useEffect fire?

`useEffect` runs *after* React renders the component. It may run several times based on how the dependency array is structured. Before, subsequent runs of the effect funciton, the clean-up function will be invoked first.

## The dependency array

Q: What is the dependency array?
