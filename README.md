# React 19 useEffect Cleanup Issue

This repository demonstrates a common error in React 19's `useEffect` hook: forgetting to return a cleanup function. This can lead to memory leaks if event listeners or other resources aren't properly released when the component unmounts.

The `bug.js` file contains the code with the error. The `bugSolution.js` file provides the corrected version.

## Problem

The `useEffect` hook in `bug.js` adds an event listener but doesn't include a cleanup function to remove the listener when the component unmounts. This means that the event listener will continue to exist even after the component is no longer in the DOM, potentially causing memory issues and unexpected behavior.

## Solution

The `bugSolution.js` file shows the corrected code.  A cleanup function is returned from `useEffect` to remove the event listener. This ensures that the event listener is removed when the component unmounts, preventing potential memory leaks.