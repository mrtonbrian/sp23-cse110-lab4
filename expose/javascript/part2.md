# Part 2
  1. The code will print out `3`, since that is `prices.length` (and the loop stops executing when `i` equals `prices.length`). It prints this because `i` is not block-scoped, so it retains its value at the end of the loop at line 12.
  2. At line 13, the code will print out `150`. This is because the variable `discountedPrice` is a function-scoped variable (as it is defined inside the function), so it can be accessed anywhere within the function definition. Thus, at line 13, it will have the value of what it was for the last iteration in the loop, where `prices[i] = 300`. So, we would print out `300 * (1 - 0.5) = 150`.
  3. The code would print `150`. This is because the variable `discountedPrice` is a function-scoped variable (as it is defined inside the function), so it can be accessed anywhere within the function definition. Thus, at line 14, it will have the value of what it was for the last iteration in the loop. We know from question 2 that `discountedPrice` is `150`. Thus, we would print out `150 * 100 / 100 = 150`.
  4. This function will return `[50, 100, 150]`, as they are the results after applying our `0.5x` discount to each of the values in `prices` (i.e. after halving each value). They are obtained by calulating the discount in lines 7-8, then individually pushing them at the end of the list in line 9.
  5. At line 12, we will get a `ReferenceError` since we defined our `i` using `let`, which makes it block-scoped and hence only accessible within the `for`-loop.
  6. At line 13, we will get a `ReferenceError` since we defined our `discountedPrice` using `let`, which makes it block-scoped and hence only accessible within the `for`-loop.
  7. At line 14, the code will print `150` for the same reason as in number 3 (that it is the discounted price for the last item in the array, `300`). It doesn't have the same issues as 5 and 6 since while `finalPrice` is defined using `let`, it is defined **outside** the for loop and hence can be referenced anywhere inside the function.
  8. The function will return `[50, 100, 150]` for the same reason as question 4 (that they are the values after halving each price). It doesn't have the same issues as 5 and 6 since while `discounted` is defined using `let`, it is defined **outside** the for loop and hence can be referenced anywhere inside the function.
  9. At line 11, there would be a `ReferenceError`, as `i` is defined using `let`, which means it can only be used inside the for loop that it is defined for.
  10. The code will print out `3`, as `length` is set to `prices.length` at the beginning of the function, which was `3`, as there were `3` items in the array.
  11. The function will return `[50, 100, 150]` for the same reason as question `4`. The `const` does not change the return value, as in this case, the `const` means that `discounted` is a `const` **reference** (not necessarily a `const` value), which means that we are able to push items into the array.
  12. Answers:
      a. `student.name`
      b. `student['Grad Year']`
      c. `student.greeting()`
      d. `student['Favorite Teacher'].name`
      e. `student.courseLoad[0]`
  13. Answers:
      a. `'32'` since integers get mapped to their exact string representations (the `+` is treated as concatenation).
      b. `1` since `'3'` will map to `3` under the `-` arithmetic operator.
      c. `3` since `null` will map to `0`.
      d. `'3null'` since `null` gets mapped to `'null'` (the `+` is treated as concatenation).
      e. `4` since `true` maps to `1`.
      f. `0` since `false` and `null` both map to `0`.
      g. `3undefined` since `undefined` will map to its string representation `'undefined'`.
      h. `NaN` since `'3'` will map to `3` under the arithmetic operator `-` and `undefined` will map to `NaN`.
  14. Answers:
      a. `true` since `'2'` will become the number `2` and `2 > 1`.
      b. `false` since `'2'` comes after `'12'` lexicographically (as `1` comes before `2`).
      c. `true` as `'2'` will become the number `2` and `2 == 2`.
      d. `false` as Javascript will compare types as well, and `'2'` is a string while `2` is an integer.
      e. `false` since `true` will map to `1`, but `1` does not equal `2`.
      f. `true` since `Boolean(2)` will map to `1` and `true` will map to `1` as well
   15. `===` will look for strict equality, where both the values and the datatypes are compared, while `==` will convert the types of the operands before comparison
   16. See `part2-question16.js`
   17. The function will return `[1, 2, 3]`. In the `modifyArray` function, the loop will iterate over each item in the array, and apply the `callback` function to it, then pushes it to the end of the array, and in this case, our `callback` is the `doSomething` function, which just doubles the number. Hence, the result would just be the double of each number in the original.
   18. See `part2-question18.js`
   19. The code will print `1` then `4` then `3` then `2` (`2` will be printed 1 second later). The `3` gets printed after the `4` since the callback will be invoked asynchronously, hence Javascript will wait until after the synchronous code runs (i.e. the regular `console.log` statements) to execute `console.log(3)`.
   20. 