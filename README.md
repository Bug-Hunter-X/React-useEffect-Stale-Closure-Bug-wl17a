# React useEffect Stale Closure Bug

This repository demonstrates a common bug in React applications related to the `useEffect` hook and its dependency array.  Incorrectly specifying the dependencies can lead to stale closures, resulting in unexpected behavior and potentially difficult-to-debug issues.

## Bug Description

The `bug.js` file contains a React component that uses `useEffect` to log the current count. However, the dependency array for `useEffect` is missing the `count` variable. This means that the effect doesn't re-run when `count` changes, leading to a stale closure.

## Solution

The `bugSolution.js` file demonstrates the correct way to use `useEffect` by including the `count` variable in the dependency array. This ensures that the effect runs whenever the `count` value changes.