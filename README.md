# React useEffect setInterval Memory Leak

This repository demonstrates a common mistake in React applications: using `setInterval` inside `useEffect` without a cleanup function. This leads to memory leaks and unpredictable behavior.

## The Problem
The `setInterval` function, when used without proper cleanup, continues to run even after the component unmounts.  This causes the component's state to update even when it's no longer rendered, leading to wasted resources and potential bugs.

## The Solution
The solution is to use the return function of `useEffect` to clear the interval when the component unmounts, preventing the memory leak.

## How to Run
1. Clone the repository.
2. Navigate to the repository's directory in your terminal.
3. Run `npm install`.
4. Run `npm start`.

Observe the behavior of the `bug.js` example, and then compare it to the corrected `bugSolution.js` example.