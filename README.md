# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The bug is caused by an incorrect or missing dependency array, leading to an infinite rendering loop. 

## Bug Description

The `MyComponent` component uses the `useEffect` hook to log the current count to the console. However, the `count` variable is missing from the dependency array, which means the effect runs on every render. Since the effect updates the `count` variable and causes a re-render it will run infinite loop. 

## Solution

The solution involves correctly specifying the dependency array. By including `count` in the dependency array, the effect only runs when the value of `count` changes.