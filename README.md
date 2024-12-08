# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The bug causes an infinite render loop due to a missing or incorrect dependency array.

## Bug Description
The `useEffect` hook, in the provided `MyComponent`, is intended to log the current count whenever it changes.  However, because there is no dependency array, or an incorrect dependency array, the effect runs on every render, causing an infinite loop. This leads to performance degradation and may eventually crash the application.

## Bug Solution
The solution involves correctly specifying the `count` variable as a dependency within the dependency array.  This ensures the effect only runs when the `count` value changes.

## How to Reproduce
1. Clone the repository.
2. Run `npm install`.
3. Run `npm start`.
4. Observe the infinite console logs and potentially a browser crash.