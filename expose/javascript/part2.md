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