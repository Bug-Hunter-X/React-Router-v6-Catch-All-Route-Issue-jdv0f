# React Router v6 Catch-All Route Bug

This repository demonstrates a common issue encountered when using catch-all routes ('/*') in React Router v6.  The catch-all route unintentionally overrides other, more specific routes, leading to incorrect rendering.

The `App.js` file shows the problematic code.  The `AppSolution.js` file demonstrates the solution.

## Problem
The catch-all route, intended to handle 404 errors, matches *all* paths, preventing other routes from working as expected. This is because it is placed after the more specific routes and matches first.

## Solution
To fix this, the catch-all route should always be placed last in the route order.  This ensures that only when no other routes match is the catch-all route used.