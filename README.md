# Tailwind CSS JIT Mode: Unexpectedly Ignored Classes

This repository demonstrates an uncommon bug in Tailwind CSS's JIT (Just-In-Time) mode. The bug causes classes to be unexpectedly ignored, typically occurring when using Tailwind with frameworks like Next.js or Nuxt.js.

## Problem Description

In JIT mode, Tailwind generates CSS only for the classes used in your project.  If a class is misspelled or not defined in your `tailwind.config.js`, Tailwind won't include it in the generated CSS, leading to the class having no effect.  This can be difficult to debug since there's no obvious error message; the class simply seems to be ignored.

## Reproduction

The `bug.js` file demonstrates the issue.  A class ('typo-class') is intentionally misspelled, leading to the corresponding style not being applied.

## Solution

The `bugSolution.js` file shows the solution.  The typo is corrected ('typo-class' becomes 'typo-class'), ensuring that the class is properly recognized and the style is applied by Tailwind during the build process.

## How to Run

1.  Clone the repository.
2.  Run `npm install` to install the required dependencies (if any).
3.  Compare the output of `bug.js` and `bugSolution.js` to observe the effect of the typo.

This example highlights the importance of careful attention to detail when using Tailwind CSS, especially in JIT mode, and reinforces the need for thorough testing.