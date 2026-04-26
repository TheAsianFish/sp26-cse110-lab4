# DevTools - Debugging

## Question 1
`num1` and `num2` are retrieved from the DOM using `.value`, which always returns a string. When `+` is applied to two strings, JavaScript concatenates them instead of adding them numerically.

## Question 2
Convert the inputs to numbers using `Number()` before passing them to `calculateSum()`:

let num1 = Number(document.getElementById("num1").value);
let num2 = Number(document.getElementById("num2").value);

See fix.png for a screenshot of the fix.