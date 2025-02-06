# Unnecessary Re-renders in React useEffect Hook

This repository demonstrates a common React bug involving the `useEffect` hook causing unnecessary re-renders.  The `useEffect` hook, without proper optimization, runs after every render, which can lead to performance issues, especially in complex components.

## Bug

The original `MyComponent` uses `useEffect` without any dependencies, causing it to run on every render. This leads to excessive console logging and unnecessary re-renders, potentially impacting performance.  The `bug.js` file shows this problematic code.

## Solution

The solution utilizes `useCallback` to memoize the effect function and optimize the execution of `useEffect`. This ensures the effect runs only when necessary, resolving the performance issue. The `bugSolution.js` file illustrates the improved implementation.