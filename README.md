# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React's `useEffect` hook: omitting the dependency array, leading to an infinite loop.  The `bug.js` file contains the erroneous code. The solution is provided in `bugSolution.js`.

## Problem

The `useEffect` hook without a dependency array runs after every render, triggering a continuous fetch cycle. This causes infinite re-renders and may impact application performance.

## Solution

The correct use of `useEffect` involves including a dependency array to specify when the effect should run.  In this case, it only needs to run once on mount; if we need to re-run the fetch on a change in a particular variable then we should include that variable in the dependency array.