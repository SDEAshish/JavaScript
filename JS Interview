---

### 1. **What is the difference between `var`, `let`, and `const`?**
- **`var`**: Function-scoped. Can be redeclared and updated. Hoisted with *undefined*.
- **`let`**: Block-scoped. Can be updated but not redeclared in the same scope.
- **`const`**: Block-scoped. Cannot be updated or redeclared (must be initialized).

---

### 2. **Explain closures in JavaScript.**
A **closure** is when a function "remembers" the environment in which it was created, even after the outer function has finished execution.

Example:
```javascript
function outer() {
  let count = 0;
  return function inner() {
    count++;
    console.log(count);
  }
}
const counter = outer();
counter(); // 1
counter(); // 2
```

---

### 3. **What is hoisting in JavaScript?**
Hoisting is JavaScript's default behavior of moving **declarations** to the top of the current scope before code execution.

- Variables declared with `var` are hoisted (initialized with `undefined`).
- `let` and `const` are hoisted too but stay in a "Temporal Dead Zone" until they are declared.

---

### 4. **What are promises?**
A **Promise** is an object that represents the eventual completion or failure of an asynchronous operation.

States:
- **Pending**
- **Fulfilled**
- **Rejected**

Example:
```javascript
let promise = new Promise(function(resolve, reject) {
  resolve("Success!");
});
promise.then((message) => console.log(message));
```

---

### 5. **What is the difference between `==` and `===`?**
- `==` checks for value equality with **type coercion**.
- `===` checks for value and type equality (strict equality).

Example:
```javascript
'5' == 5   // true
'5' === 5  // false
```

---

### 6. **Explain event bubbling and event delegation.**
- **Event Bubbling**: When an event triggers on the deepest target first, and then bubbles up to its ancestors.
- **Event Delegation**: Instead of adding an event listener to each child, you add one to the parent and use event.target to detect the child.

Example of delegation:
```javascript
document.getElementById('parent').addEventListener('click', function(e) {
  if (e.target && e.target.matches('button.classname')) {
    console.log('Button clicked');
  }
});
```

---

### 7. **What are arrow functions?**
Arrow functions are a shorthand syntax for writing functions and **do not bind their own `this`**.

Example:
```javascript
const add = (a, b) => a + b;
```

---

### 8. **What is the difference between synchronous and asynchronous JavaScript?**
- **Synchronous**: Code executes line by line, blocking further execution until the current task is complete.
- **Asynchronous**: Code allows other operations to run while waiting for the previous one to complete (e.g., setTimeout, fetch, Promises).

---

### 9. **Explain `call()`, `apply()`, and `bind()`.**
- **`call()`**: Calls a function with a given `this` and arguments one by one.
- **`apply()`**: Same as `call()`, but arguments are passed as an array.
- **`bind()`**: Returns a new function, permanently binding `this` to the provided value.

Example:
```javascript
function greet() {
  console.log(this.name);
}
const person = { name: "Ashish" };
greet.call(person);  // Ashish
greet.apply(person); // Ashish
const newGreet = greet.bind(person);
newGreet(); // Ashish
```

---

### 10. **What is a "this" keyword in JavaScript?**
`this` refers to the object that is executing the current function.

- In the global scope, `this` refers to the global object (`window` in browsers).
- In a method, `this` refers to the object the method is called on.
- In strict mode, `this` can be `undefined`.

---






**JavaScript coding challenges**

---

## 1. **Reverse a String**
**Input:** `"hello"`  
**Output:** `"olleh"`

```javascript
function reverseString(str) {
  return str.split('').reverse().join('');
}
```

---

## 2. **Check for Palindrome**
**Input:** `"racecar"`  
**Output:** `true`

```javascript
function isPalindrome(str) {
  let reversed = str.split('').reverse().join('');
  return str === reversed;
}
```

---

## 3. **Find the Largest Number in an Array**
**Input:** `[1, 2, 10, 5, 3]`  
**Output:** `10`

```javascript
function largestNumber(arr) {
  return Math.max(...arr);
}
```

---

## 4. **FizzBuzz Problem**
Print numbers 1 to n.  
- For multiples of 3 print `"Fizz"`,  
- For multiples of 5 print `"Buzz"`,  
- For multiples of both 3 and 5 print `"FizzBuzz"`.

```javascript
function fizzBuzz(n) {
  for (let i = 1; i <= n; i++) {
    if (i % 15 === 0) console.log('FizzBuzz');
    else if (i % 3 === 0) console.log('Fizz');
    else if (i % 5 === 0) console.log('Buzz');
    else console.log(i);
  }
}
```

---

## 5. **Remove Duplicates from an Array**
**Input:** `[1, 2, 2, 3, 4, 4, 5]`  
**Output:** `[1, 2, 3, 4, 5]`

```javascript
function removeDuplicates(arr) {
  return [...new Set(arr)];
}
```

---

## 6. **Count the Number of Vowels in a String**
**Input:** `"hello world"`  
**Output:** `3`

```javascript
function countVowels(str) {
  return str.match(/[aeiou]/gi)?.length || 0;
}
```

---

## 7. **Find the Factorial of a Number**
**Input:** `5`  
**Output:** `120`

```javascript
function factorial(n) {
  if (n === 0) return 1;
  return n * factorial(n - 1);
}
```

---

## 8. **Find the Missing Number in an Array**
Array from 1 to n, one number missing.  
**Input:** `[1,2,4,5,6]`  
**Output:** `3`

```javascript
function missingNumber(arr) {
  let n = arr.length + 1;
  let total = (n * (n + 1)) / 2;
  let sum = arr.reduce((acc, num) => acc + num, 0);
  return total - sum;
}
```

---

## 9. **Check if Two Strings are Anagrams**
**Input:** `"listen"` and `"silent"`  
**Output:** `true`

```javascript
function areAnagrams(str1, str2) {
  return str1.split('').sort().join('') === str2.split('').sort().join('');
}
```

---

## 10. **Flatten a Nested Array**
**Input:** `[1, [2, [3, 4], 5], 6]`  
**Output:** `[1, 2, 3, 4, 5, 6]`

```javascript
function flattenArray(arr) {
  return arr.flat(Infinity);
}
```

---

### ⭐ Bonus Tip:
For interviews, also be prepared to solve these without built-in methods (like `flat`, `sort`, etc.), using recursion or loops.

---

Would you like me to send you a **practice set** with a timer (like a real interview round)?  
⏳ (15–30 minutes challenges)  
It can seriously help in building speed! 🚀  
Would you like that?
