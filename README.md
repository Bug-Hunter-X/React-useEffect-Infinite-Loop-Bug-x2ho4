# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug involving the `useEffect` hook.  The `useEffect` hook, while powerful, can easily lead to infinite loops or unexpected behavior if not used correctly.  This example showcases such an issue and provides a solution.

## The Bug

The `bug.js` file contains a component that uses `useEffect` without proper dependency management.  The `useEffect` hook, as written, runs after every render (including the initial render), resulting in an infinite loop where the count constantly increments and the console repeatedly logs messages.  This behavior can quickly overwhelm the browser's rendering process.

## The Solution

The `bugSolution.js` file provides a corrected implementation.  The key change is adding the `count` variable as a dependency array to the `useEffect` hook.  This ensures that the effect only runs when the value of `count` changes. This prevents the infinite loop. Note the functional update approach to state update for safety. 
