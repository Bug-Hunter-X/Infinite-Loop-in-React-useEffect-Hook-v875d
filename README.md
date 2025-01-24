# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook. The bug causes an infinite loop due to a missing dependency in the `useEffect` call.

## Bug Description

The `useEffect` hook is used to perform side effects in functional components. However, if a dependency array is omitted or incomplete, the effect will run after every render, potentially leading to an infinite loop.

In this example, the `useEffect` hook logs the current count to the console.  Without the `[count]` dependency array, the effect runs continuously, triggering a re-render, which triggers the effect again and so on.

## Bug Solution

The solution is to correctly specify the dependencies array to include any variables used inside the effect that are not passed as props. In this case, the only such variable is `count`.
