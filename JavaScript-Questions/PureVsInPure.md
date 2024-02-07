# Pure Vs Inpure Functions

## Pure Functions

Pure funtions are functions that will produce the same output for the same input and does not have any side effects.
It only depends on its input paramaters and doesn't modify any external states.


```
function add(a, b) {
  return a + b;
}
```

The results of add is dependants only on the values provided. 

## Impure Functions

Impure functions in a type of funtion in javascript that can produce results for the same input and has a side effects.

Unlike pure function, impure funtions can depend on and modify external state making their behavior less predictable
```
let result = 0;

function addToResult(value) {
  result += value;
  return result;
}
```
