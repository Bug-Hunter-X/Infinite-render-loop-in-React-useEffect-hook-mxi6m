# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The `useEffect` hook, without proper dependency management, can lead to an infinite render loop. This example showcases the problem and its solution.

## Bug Description

The `MyComponent` component uses the `useEffect` hook to log a message to the console on every render. However, the dependency array for the `useEffect` hook is missing, causing it to run on every render and triggering a new render cycle, resulting in an infinite loop. 

## Solution

The solution involves adding the `count` state variable to the dependency array of the `useEffect` hook. This ensures the effect only runs when the `count` changes.