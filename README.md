# React useEffect Infinite Loop Bug
This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The bug causes an infinite loop due to a missing dependency in the `useEffect`'s dependency array.  The solution demonstrates the correct way to manage dependencies to avoid this issue.

## Bug
The `bug.js` file contains a React component that updates a count using the `useState` hook.  The `useEffect` hook is designed to log the updated count. However, because the count variable is not listed as a dependency in the useEffect, the effect runs on every render, causing an infinite loop. 

## Solution
The `bugSolution.js` file demonstrates the correct implementation by including the `count` variable within the dependency array of the `useEffect` hook. This ensures the effect runs only when the `count` value changes.