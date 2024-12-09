# React Strict Mode Warning: Missing useEffect Dependency

This repository demonstrates a common React bug related to the `useEffect` hook and Strict Mode.  The bug arises when a state variable used within the `useEffect` function is not listed in the dependency array, leading to unexpected behavior and warnings in Strict Mode.

## Bug Description

The provided `MyComponent` uses the `useEffect` hook to log a message each time the component renders.  However, the `count` state variable, which changes when the button is clicked, is not included in the dependency array. This causes the effect to run on every render even when `count` hasn't changed, leading to a warning in Strict Mode. 

## Solution

The solution involves correctly specifying the `count` variable in the dependency array of the `useEffect` hook. This ensures that the effect only runs when the `count` value changes.