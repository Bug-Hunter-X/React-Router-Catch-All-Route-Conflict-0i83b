# React Router Catch-All Route Conflict

This repository demonstrates a common issue with React Router's catch-all route (`/*`). When placed incorrectly within the `Routes` component, it can interfere with other routes, leading to unexpected rendering behavior or preventing other routes from matching correctly.

The problem arises because the catch-all route is too broad and intercepts requests intended for other routes. By placing it last, we guarantee that it only matches routes that don't match any more specific route definitions.

## Solution
The solution involves reordering the routes within the `Routes` component, ensuring the catch-all route (`/*`) is defined last.  This ensures the catch-all route acts as a true fallback, only matching if no other route is a match.
