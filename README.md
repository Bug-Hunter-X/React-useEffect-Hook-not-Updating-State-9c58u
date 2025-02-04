# React useEffect Hook Unexpected Behavior

This example demonstrates a common issue with the React `useEffect` hook where the empty dependency array `[]` prevents the effect from running on state updates. This leads to an unexpected behavior where the count does not update correctly.

## Bug Description
The `useEffect` hook is intended to run after every render. However, when provided with an empty dependency array, it only executes once when the component mounts.  Therefore, the console log occurs only once. 

## Solution
Add the state variable as a dependency to ensure that the effect runs whenever the count changes, fixing the unexpected behavior.  This change ensures the effect re-runs when the count is updated.