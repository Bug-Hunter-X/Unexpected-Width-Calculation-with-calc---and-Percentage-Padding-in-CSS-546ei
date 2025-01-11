# Unexpected Width Calculation with calc() and Percentage Padding in CSS

This repository demonstrates an uncommon error in CSS involving the `calc()` function, percentage padding, and width calculations.  The issue highlights the order of operations within `calc()` and how percentage padding is relative to the element's calculated dimensions, not its parent's.

## The Bug

The `bug.css` file contains a CSS snippet where the width of an element is calculated using `calc()` to subtract 10 pixels from 100% of its parent container's width. However, the element also has a percentage-based padding. Because the padding is calculated after the initial width calculation, it results in a wider element than expected.

## The Solution

The `bugSolution.css` file presents a solution using the `box-sizing` property. Setting `box-sizing: border-box;` ensures that padding and border are included in the element's total width.  This allows for more predictable and accurate width calculations when using `calc()` with percentages.