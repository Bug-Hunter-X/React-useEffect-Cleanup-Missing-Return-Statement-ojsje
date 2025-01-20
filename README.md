# React useEffect Cleanup Missing Return Statement

This repository demonstrates a common React bug: a missing return statement in the cleanup function of a `useEffect` hook.  This bug can lead to memory leaks and unexpected behavior.

## Bug Description
The provided code snippet uses `useEffect` to update a counter every second. However, it lacks a proper cleanup function to clear the `setInterval` when the component unmounts or the dependencies change. This results in multiple intervals continuing to run, consuming resources and potentially causing performance issues.

## Solution
The corrected version includes a return statement within the `useEffect` hook that clears the `setInterval` using `clearInterval`.  This ensures that the interval is stopped when the component is unmounted, preventing memory leaks.
