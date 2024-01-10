# ![Using JavaScript Classes - Built-In Objects](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will be able to understand and recognize built-in JavaScript objects and utilize their values and methods.

## Built-In Objects

One commonly used built-in JavaScript object is [`Math`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math). If you've ever required the use of random numbers in code you've written, for example, then `Math` has many **methods** that are extremely useful, saving you the time of writing commonly reused code.

Key among them is `.random()`, a method that returns a number greater than or equal to 0, and less than 1: 

```js
Math.random() // example result: 0.5570349614485068
```

Some of these methods also take in arguments. Such is the case with the `.floor()` method, which rounds down an argument:

```js
let num = 1.21
Math.floor(num) // => 1
```

This method has a return value of the largest integer less than or equal to the value of `num`. In other words, it truncates everything after the decimal.

When combined, you can see how the built-in Math object can dramatically shorten code and make life easier. Without having to code out either method, we can create a function that gets a random integer from a maximum value: 

```js
function getRandomInt(max) {
  return Math.floor(Math.random() * max);
}
```

In addition to **methods**, the JavaScript Math object also contains certain values, such as PI:

```js
Math.PI // => 3.141592653589793
```

Now that we've taken a look at an example of a built-in Javascript object and refreshed ourselves on dot notation, let's take a look at a built in class.
