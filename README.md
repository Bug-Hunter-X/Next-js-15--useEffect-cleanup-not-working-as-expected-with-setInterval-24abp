# Next.js 15 useEffect Cleanup Issue

This repository demonstrates a problem with the `useEffect` hook cleanup function in a Next.js 15 application.  The counter on the about page continues incrementing even after navigating away from that page because the `setInterval` isn't properly cleared.

## Problem Description
The `setInterval` function is used to update a counter. The `useEffect` hook is used to start and stop this interval based on the component's lifecycle.  However, the `clearInterval` in the cleanup function doesn't work as expected leading to the counter continuing to increment even after leaving the page.  This is an uncommon error usually caused by an incorrect or missing cleanup function in useEffect, or a misunderstanding of how React's lifecycle affects timers.

## Solution
The provided solution shows how to correctly implement cleanup function in useEffect to ensure that the `setInterval` is cleared when the component unmounts or navigates away preventing the counter from continuing to increment.