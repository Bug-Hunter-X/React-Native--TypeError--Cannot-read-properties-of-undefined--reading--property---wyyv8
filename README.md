# React Native: TypeError: Cannot read properties of undefined (reading 'property')

This repository demonstrates a common error in React Native applications: attempting to access a property of an object that is null or undefined.  The `bug.js` file shows the problematic code, while `bugSolution.js` provides a solution.

## Problem

Asynchronous operations (like fetching data from an API) can result in a component trying to render before the data has arrived, leading to the `TypeError: Cannot read properties of undefined (reading 'property')` error.  This occurs when the application attempts to read a property from an object that has not yet been assigned a value, resulting in it being `undefined` or `null`.

## Solution

The solution involves using optional chaining (`?.`) or the nullish coalescing operator (`??`) to safely access properties.  These operators prevent errors by returning `undefined` if the object or property is nullish (i.e., `null` or `undefined`).  Additionally, conditional rendering can prevent the component from rendering until the data is available.