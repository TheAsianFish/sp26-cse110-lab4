 ## Question 1
`3` is printed. `i` is declared with `var`, so it is function-scoped and doesn't disappear after the loop ends. After iterating over 3 elements, `i` equals `3` (the value that exited the loop condition).

## Question 2
`150` is printed. `discountedPrice` is declared with `var`, so it is function-scoped and accessible after the loop ends. The last iteration processes `prices[2] = 300`, so `discountedPrice = 300 * (1 - 0.5) = 150`.

## Question 3
`150` is printed. `finalPrice` is declared with `var` outside the loop, so it is function-scoped and accessible anywhere in the function. After the last iteration, `finalPrice = Math.round(300 * 0.5 * 100) / 100 = 150`.

## Question 4
`[50, 100, 150]` — the function loops through each price with a 0.5 discount, pushes each discounted value into the `discounted` array, and returns it.

## Question 5
ReferenceError — `i` is declared with `let` inside the `for` loop, so it is block-scoped to the loop. Once the loop ends, `i` no longer exists and accessing it throws a ReferenceError.

## Question 6
ReferenceError — `discountedPrice` is declared with `let` inside the `for` loop, so it is block-scoped to the loop and inaccessible outside of it.

## Question 7
`150` is printed. `finalPrice` is declared with `let` outside the loop, so it is scoped to the entire function. After the last iteration, `finalPrice` holds `150`.

## Question 8
`[50, 100, 150]` — Each discounted price is correctly pushed onto the `discounted` array, which is returned at the end.

## Question 9
ReferenceError — `i` is declared with `let` inside the `for` loop, so accessing it outside the loop throws a ReferenceError.

## Question 10
`3` is printed. `length` is declared with `const` outside the loop and assigned `prices.length = 3`. It is never reassigned and is accessible at line 12.

## Question 11
`[50, 100, 150]` — `const` on `discounted` doesn't affect the return since the array is never reassigned, only mutated via `.push()`. Each loop iteration is its own block scope, so `const discountedPrice` is a fresh declaration each time with no conflict.

## Question 12
A. `student.name`
B. `student['Grad Year']`
C. `student.greeting()`
D. `student['Favorite Teacher'].name`
E. `student.courseLoad[0]`

## Question 13 - Arithmetic
- A. `'32'` - `2` is coerced to a string and concatenated.
- B. `1` - No string `-` operation, so `'3'` is coerced to a number and subtraction occurs.
- C. `3` - `null` coerces to `0`, so `3 + 0 = 3`.
- D. `'3null'` - `null` coerces to the string `'null'` and concatenation occurs.
- E. `4` - `true` coerces to `1`, so `1 + 3 = 4`.
- F. `0` - `false` coerces to `0` and `null` coerces to `0`, so `0 + 0 = 0`.
- G. `'3undefined'` - `undefined` coerces to the string `'undefined'` and concatenation occurs.
- H. `NaN` - `undefined` coerces to `NaN`, and any arithmetic with `NaN` returns `NaN`.

## Question 14 - Comparison
- A. `true` - `'2'` is coerced to a number, and `2 > 1` is true.
- B. `false` - Both are strings so comparison is alphabetical. `'2'` comes after `'1'`, so `'2' < '12'` is false.
- C. `true` - `==` coerces types, so `'2'` becomes `2` and `2 == 2` is true.
- D. `false` - `===` does not coerce types. A number and string are never strictly equal.
- E. `false` - `true` coerces to `1`, and `1 == 2` is false.
- F. `true` - `Boolean(2)` is `true` since any non-zero number is truthy, so `true === true` is true.

## Question 15 - == vs ===
`==` coerces both values to the same type before comparing. `===` compares both value and type with no coercion. For example, `2 == '2'` is `true` but `2 === '2'` is `false`.

## Question 17
`[2, 4, 6]` — `modifyArray` loops through `[1, 2, 3]` and calls `doSomething` on each element, which multiplies it by `2`. Each result is pushed into `newArr`, which is returned at the end.

## Question 19
`1, 4, 3, 2`

`1` prints immediately. Then both `setTimeout` calls are registered — the one for `3` has a delay of `0ms` and the one for `2` has `1000ms`, but both are async and get pushed to the event queue regardless. `4` prints next since it's synchronous. Once the call stack is clear, `3` prints first, then `2` prints after 1000ms.
