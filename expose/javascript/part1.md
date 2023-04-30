# Javascript Part 1
  1. Line 9 will print out `values added: 20`
  2. Line 13 will print out `values added: 20`
  3. Line 9 will print out `values added: 20`
  4. Line 13 will have an error, since the variable `result` is only defined in the if-statement block and hence cannot be used outside of the block on line 13.
  5. Line 9 will have a TypeError, as we are re-assigning the value of a `const` variable.
  6. Line 13 won't print out anything since the function will stop executing at line 9, due to the error in question 5. Also, `const` variables have the same scoping as `let`, so if it did execute tot hat line, then the code will give the same error as 4.