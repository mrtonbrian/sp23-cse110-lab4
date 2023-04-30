# Devtools Part 2
 1. The bug is that there is no type conversion happening after Javascript accesses the input values, so it grabs the values as strings. Then, the `calculateSum` function concatenates the strings, rather than adds the underlying numbers.
 2. I would use the `parseInt()` function to convert `num1` and `num2` after accessing their values.