# useEffect Runs on Every Render in React

This repository demonstrates a common yet subtle bug in React's `useEffect` hook where the effect runs on every render instead of only when the specified dependencies change.

## Bug Description
The `useEffect` hook in the provided `MyComponent` runs on every render, causing unnecessary console logs and potentially performance issues.  This is because the dependency array `[]` is empty, resulting in the effect running after every render.

## Solution
The solution involves correctly specifying the `count` variable in the dependency array. By adding `[count]` the effect now only runs whenever `count` changes.