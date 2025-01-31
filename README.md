# React setInterval Cleanup Issue

This repository demonstrates a common mistake in React components: using `setInterval` within a `useEffect` hook without providing a cleanup function. This leads to memory leaks and unexpected behavior when the component unmounts.

## Problem
The `MyComponent` component uses `setInterval` to update a counter every second. However, it fails to provide a cleanup function within the `useEffect` hook.  This means that when the component unmounts, the interval continues to run in the background, consuming resources and potentially interfering with other parts of the application.

## Solution
The solution involves returning a cleanup function from the `useEffect` hook.  This function will clear the interval when the component is unmounted, preventing the memory leak.

## How to run the code
1. Clone this repository.
2. Navigate to the project directory using the command line
3. Run the following command : `npm install` to install required packages.
4. Run the following command : `npm start` to start development server

