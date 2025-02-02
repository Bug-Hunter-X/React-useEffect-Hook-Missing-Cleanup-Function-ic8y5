# React useEffect Hook Missing Cleanup Function
This repository demonstrates a common React bug: forgetting to include a cleanup function in the `useEffect` hook. This can lead to memory leaks and unexpected behavior.

## The Bug
The `bug.js` file shows an example of an `useEffect` hook missing a return statement for the cleanup function.  Specifically, the effect logs 'Component mounted' upon initial render but never cleans up after the component unmounts. This could lead to memory issues in scenarios where this component frequently mounts and unmounts.

## The Solution
The `bugSolution.js` file demonstrates the correct way to use the useEffect hook.  The return statement now provides a cleanup function that addresses the memory leak issues.

## How to Reproduce
1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the console logs to see the difference in behavior between `bug.js` and `bugSolution.js`.
