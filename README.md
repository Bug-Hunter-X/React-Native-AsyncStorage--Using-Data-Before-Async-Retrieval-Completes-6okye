# React Native AsyncStorage: Handling Asynchronous Data Retrieval

This repository demonstrates a common error in React Native when working with AsyncStorage: accessing stored data before the asynchronous retrieval operation has completed.

The `bug.js` file showcases the incorrect usage, while `bugSolution.js` provides the corrected implementation using async/await for better error handling and code readability.

## Problem
AsyncStorage's `getItem` method is asynchronous.  If you attempt to use the retrieved value immediately after calling `getItem`, there's a race condition: your subsequent code might execute before the value is available, resulting in `undefined` or unexpected behavior.

## Solution
The solution involves using async/await or promises to ensure the data is retrieved before it is used.  The example in `bugSolution.js` shows how async/await makes the code cleaner and easier to read.