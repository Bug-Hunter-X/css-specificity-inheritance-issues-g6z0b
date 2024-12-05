# CSS Specificity and Inheritance Bug

This repository demonstrates a subtle bug in CSS related to the interaction between specificity and inheritance.  The bug showcases a scenario where a more specific selector's style is unexpectedly overridden by a less specific selector due to inheritance.

## Bug Description

A common assumption is that more specific selectors always take precedence.  However, in cases of inheritance, a parent's style might override a more specific child selector's style if the parent's style is inherited.

## How to Reproduce

1. Open `bug.css`.
2. Observe that the `<span>` within a paragraph inside the container unexpectedly has blue text, not red, despite the more specific selector `container p span { color: red; }`

## Solution

The `bugSolution.css` file provides a corrected version. In the solution, the specificity issue is addressed either by removing inheritance or by adding more specific styles.