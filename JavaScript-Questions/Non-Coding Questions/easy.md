## Question 1

**Explain the difference between == (loose equality) and === (strict equality) in JavaScript.**

In JavaScript, == (loose equality) compares two values and returns true if they are equal, allowing type coercion. On the other hand, === (strict equality) checks if the two values are equal and have the same type, without allowing type coercion.

```
Code Examples:
console.log(1 == "1"); // true, because after type coercion, the values are equal
console.log(1 === "1"); // false, because the types are different (number vs. string)
```

## Question 2
