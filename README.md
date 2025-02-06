# React useEffect Hook Missing Dependency
This repository demonstrates a common bug in React applications involving the `useEffect` hook: missing dependencies in the dependency array. This leads to an infinite render loop, as the effect constantly triggers.

## Bug Description
The `MyComponent` uses `useState` to manage a count.  The `useEffect` hook logs the count to the console after every render.  However, without `count` in the dependency array, the effect runs after every render, causing the component to re-render, triggering the effect again, and so on.

## Solution
The solution involves adding `count` to the dependency array of the `useEffect` hook. This ensures that the effect only runs when the `count` value changes.