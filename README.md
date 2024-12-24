# React useEffect Dependency Array Bug

This repository demonstrates a common error in React's `useEffect` hook: an infinite render loop caused by an incorrectly configured dependency array.

## Bug

The `bug.js` file contains a component that uses `useEffect` to log the render count. However, the `count` state variable is not included in the dependency array, causing the effect to run after every render, leading to an infinite loop.

## Solution

The `bugSolution.js` file provides the corrected version. By including `count` in the dependency array, the effect now only runs when the `count` value changes, resolving the infinite render loop.

## How to reproduce

1. Clone the repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the infinite console logs in the browser's console, indicating the infinite loop in `bug.js`. Then replace `bug.js` with `bugSolution.js` and observe the corrected behavior.
