# Part 1

## Question 1
`values added: 20`

## Question 2
`final result: 20`

## Question 3
`var` is function-scoped not block-scoped, so variables declared inside conditionals or loops leak out into the rest of the function.

## Question 4
`values added: 20`

## Question 5
ReferenceError — `let` is block-scoped, so `result` no longer exists outside the `if` block.

## Question 6
TypeError — `const` variables cannot be reassigned after their initial declaration. Line 7 attempts to reassign `result`, which will throw a TypeError.

## Question 7
This line is never reached due to the TypeError on line 7. Even without it, `const` is block-scoped like `let`, so `result` would be out of scope anyway.