# Recursion-and-Closure
Here is short information about important JavaScript topics: Recursion and Closures


## Recursion
Recursion is a process where a function calls itself repeatdly to solve a problem. It is useful for problems that can be divided into smaller, similar sub-problems.

Key Points:
- Base Case and Recursive Case:
A recursive function must have a base case to stop the recursion; otherwise, it can lead to infinite calls and cause a stack overflow.
- Applications:
Recursion is commonly used for tasks such as traversing trees, solving mathematical problems (e.g., factorial, Fibonacci), and implementing algorithms like quicksort or mergesort.

` Example: Factorial Calculation `

```
function factorial(n) {
    if (n === 0) return 1; // Base case
    return n * factorial(n - 1); // Recursive case
}

console.log(factorial(5)); // Output: 120
```

##  Closures
A closure is where a function is defined inside another function, and the inner function can access local variables (and parameters) defined in the local scope of the outer function.

Key Points:
- Closures are a powerful way to make functions "remember" their environment.
- Closures help in maintaining state: Closures can keep track of information (state) between function calls, like counting or saving user data.

` Example: Closure `

```
function counter() {
    let count = 0; // Private variable
    return function() {
        count++;
        return count;
    };
}

const increment = counter();
console.log(increment()); // Output: 1
console.log(increment()); // Output: 2

```

