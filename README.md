# React 19 useState Hook Unexpected Behavior

This repository demonstrates an uncommon bug related to the `useState` hook in React 19.  The counter in `MyComponent` intermittently fails to update correctly, displaying stale values.  This appears to be related to certain timing conditions and how updates are batched.

## Bug Description:
The `incrementCount` function should reliably increment the count state.  However, in this example, the counter occasionally remains unchanged or shows an incorrect value after clicking the increment button.

## Solution:
The solution involves using a functional update with `setCount` to ensure that the update relies on the latest state value, resolving the race condition that might occur with the previous implementation.

## How to reproduce:
1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the counter's behavior; it will show inconsistencies in the count after repeated increments.