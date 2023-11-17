## Question 1

**Explain the difference between == (loose equality) and === (strict equality) in JavaScript.**

In JavaScript, == (loose equality) compares two values and returns true if they are equal, allowing type coercion. On the other hand, === (strict equality) checks if the two values are equal and have the same type, without allowing type coercion.

```
Code Examples:
console.log(1 == "1"); // true, because after type coercion, the values are equal
console.log(1 === "1"); // false, because the types are different (number vs. string)
```

## Question 2
**Interview Question: Explain the concept of a closure in JavaScript and provide an example.**

Answer: A closure is a function that has access to its own scope, the scope of the outer function, and the global scope. It is created when a nested function references a variable from its containing function.
```
Code Example:

function outerFunction() {
  var outerVariable = "I am outside!";

  function innerFunction() {
    console.log(outerVariable);
  }

  return innerFunction;
}

var closureFunction = outerFunction();
closureFunction(); // Output: "I am outside!"
```

**Explain the difference between null and undefined in JavaScript.**

Answer: In JavaScript, null is an assignment value that represents no value or no object. It is an intentional absence of any object value. On the other hand, undefined is a type itself and represents a variable that has been declared but has not yet been assigned a value.

Code Examples:
```
var nullVar = null;
console.log(nullVar); // Output: null

var undefinedVar;
console.log(undefinedVar); // Output: undefined
```
