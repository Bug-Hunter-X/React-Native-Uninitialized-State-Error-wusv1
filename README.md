# React Native Uninitialized State Error

This repository demonstrates a common error in React Native: accessing a state variable before it has been initialized. This often occurs when dealing with asynchronous operations, such as fetching data from an API.

## The Problem

The `bug.js` file shows an example of this error. The component attempts to access `this.state.data.someProperty` before the asynchronous `fetch` call has completed and updated the state. This results in a runtime error because `this.state.data` is initially `null`.

## The Solution

The `bugSolution.js` file provides a solution by using conditional rendering.  It checks if `this.state.data` is null or undefined before attempting to access its properties. This prevents the error and handles the case where the data hasn't yet been fetched.