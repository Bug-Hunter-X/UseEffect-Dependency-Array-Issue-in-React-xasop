# React useEffect Dependency Array Issue

This repository demonstrates a common mistake when using the `useEffect` hook in React: incorrectly specifying the dependency array.  The example shows how omitting or incorrectly including variables in the dependency array can lead to unexpected behavior and performance problems.

## Problem

The `useEffect` hook in the `bug.js` file is used to log the `count` variable to the console. However, the dependency array is empty (`[]`), causing the effect to run after every render, even when `count` hasn't changed. This leads to unnecessary console logs and potential performance degradation.

## Solution

The `bugSolution.js` file corrects the issue by including `count` in the dependency array (`[count]`). Now, the effect only runs when the value of `count` changes.