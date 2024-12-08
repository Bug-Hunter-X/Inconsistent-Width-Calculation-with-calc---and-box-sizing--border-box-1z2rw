# Inconsistent Width Calculation with calc() and box-sizing: border-box

This repository demonstrates an uncommon issue related to CSS width calculation when using `calc()` and `box-sizing: border-box` together. The problem arises from the order of calculation and the way `box-sizing` affects the element's final dimensions.

## The Bug
The provided `bug.css` file contains a CSS rule that sets the width of a `div` element using `calc()` while also using `box-sizing: border-box`. If the parent element of this `div` has padding or border, the width calculated by `calc()` will not include this padding and border, resulting in an element that's smaller than intended.

## The Solution
The `bugSolution.css` file provides a solution to this problem, ensuring that the calculated width accounts for the parent element's padding and border. The approach involves adjusting the `calc()` expression to subtract the padding and border width to avoid unexpected width calculations.