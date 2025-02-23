# F# Mutable Variable Scope Issue

This example demonstrates a common issue in F# when dealing with mutable variables within functions.  The `swap` function attempts to swap the values of `x` and `y`, but it fails to modify the original variables because it operates on copies of the variables.

**Bug:** The `swap` function does not modify the original `x` and `y` variables. The output will be 10 20, not 20 10.

**Solution:** Use a `byref` parameter to pass the variables by reference, allowing in-place modification.
