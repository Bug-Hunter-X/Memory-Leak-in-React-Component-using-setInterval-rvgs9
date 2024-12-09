# React setInterval Memory Leak

This repository demonstrates a common React bug involving the improper use of `setInterval` within a `useEffect` hook.  The bug causes memory leaks because the interval continues running even after the component is unmounted.

The `bug.js` file contains the problematic code. The `bugSolution.js` file shows the corrected implementation.

## How to Reproduce

1. Clone the repository.
2. Navigate to the project directory.
3. Run `npm install` to install dependencies.
4. Run `npm start` to start the development server.

Observe that the counter continues to increment even if you navigate away from the page. This indicates a memory leak.

## Solution

The corrected code in `bugSolution.js` shows how to properly handle `setInterval` within `useEffect` using the return function to clear the interval when the component unmounts.