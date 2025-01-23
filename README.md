# React Router Dom Nested Route Matching Issue

This repository demonstrates a common issue when working with nested routes in React Router Dom v6.  The problem arises when defining a nested route that unintentionally overrides a parent route, preventing it from being accessed.

## The Bug
The provided `App.js` file contains two routes:

- `/`: This route points to the `Home` component.
- `/about`: This route points to the `About` component.
- `/about/*`: This is an incorrectly placed nested route and is causing the issue.

The issue is that the nested route `/about/*` will match any path starting with `/about`, including `/about` itself. This means the `/about` route will never be accessed, and only the nested `/about/*` route will be matched.

## The Solution
The solution is provided in `AppSolution.js`.  The issue is resolved by simply removing the nested route ` /about/*` as its not needed and is unintentionally overriding the parent route.