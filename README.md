# Tailwindcss @apply Directive Issue in Imported CSS Files

This repository demonstrates a common issue encountered when using Tailwind CSS's `@apply` directive within imported CSS files.  The `@apply` directive, designed for applying pre-defined utility classes, fails to function correctly when the CSS file containing it is imported after the standard Tailwind directives (@tailwind base; @tailwind components; @tailwind utilities;).

## Problem
The `@apply` directive is processed during the Tailwind build process.  If your CSS file with `@apply` is imported *after* the Tailwind directives are processed, the `@apply` directives will be ignored, resulting in no styles being applied.

## Solution
The solution involves restructuring your CSS files to ensure that `@apply` directives are processed *before* the importing of external files.  This ensures Tailwind's build process correctly handles and applies the utility classes. 

## Steps to reproduce
1. Clone this repository
2. Run `npm install` to install dependencies (if any)
3. Build your project with Tailwind. 
4. Examine the generated CSS to see the missing `@apply` styles. Then switch to the solution to see how this problem is resolved. 
