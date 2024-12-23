# React useEffect Hook Dependency Array Issue

This repository demonstrates a common issue with React's `useEffect` hook: omitting state variables from the dependency array.  When this happens, the effect may not update as expected, leading to stale closures and bugs.

## Bug
The `bug.js` file contains a component with a `useEffect` hook that's missing a crucial dependency. This results in the effect not re-running when the `count` state variable changes.

## Solution
The `bugSolution.js` file provides the corrected version. By including `count` in the dependency array, the effect runs whenever `count` updates, ensuring the latest value is used.