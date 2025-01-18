# CSS Specificity and Inheritance Conflict

This repository demonstrates a subtle bug in CSS related to the interaction between inheritance and specificity.  A more specific selector's property is unexpectedly overridden by an inherited property from a less specific ancestor.  The `!important` flag is the only workaround in this scenario.

## Bug Description
The bug arises from the order of operations in CSS processing.  Inheritance occurs *before* specificity calculations. This can lead to situations where a more specific rule is overridden by an inherited property from a less specific ancestor.

## Solution
The solution is to use the `!important` flag on the more specific selector's rule in order to override the inherited property.

While using `!important` is generally discouraged due to its potential for making CSS hard to maintain, in this particular case it is the most direct and reliable way to resolve this uncommon inheritance/specificity conflict.