# CSS Calc() Overflow Bug

This repository demonstrates a subtle CSS bug related to using the `calc()` function in conjunction with padding. The issue arises when the calculated width, combined with the padding, exceeds the available width of the parent container.

The `bug.css` file contains the problematic CSS rule, and `bugSolution.css` provides a fix.

## Bug Details

The bug is in the calculation of the width of the div. While `calc(100% - 20px)` aims to make the div 20px smaller than its parent, adding padding further increases the div's overall size. This can cause unexpected overflow if the parent container has a limited width.

## Solution

The solution involves using the `box-sizing` property to include padding in the element's total width calculation. By setting `box-sizing: border-box;`, the padding is included within the `100%` calculation, resolving the overflow issue.