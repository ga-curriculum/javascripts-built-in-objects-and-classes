# ![[Using Classes] - Built-In Classes](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will be able to understand and recognize built-in JavaScript objects and utilize their values and methods.

## Built-In Objects

If you have some hands-on experience with JavaScript, you have probably already used some of its [built-in objects and classes](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects). Let's take a look at a built-in JavaScript object before we get to a class.

### Math object

Let's use a ***very common*** built-in JavaScript object to allow us to work with object **methods (functions)** and **values**. The following line of code may seem familiar to you:

```js
Math.random() // example result: 0.5570349614485068
```

If you've ever required the use of random numbers in code you've written, JavaScript's [`Math` object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math) has many **methods** contained within it that are extremely useful to developers such as yourself, saving you the time of writing commonly reused code.

Some of these methods also take in arguments. Such is the case with the `.floor()` method in the Math object.

```js
let num = 1.21
Math.floor(num) // => 1
```

Passing in a variable with a value of type `Number` (or just the raw value of a `Number`) this method has a return value of the largest integer less than or equal to the value of `num`. In other words, it truncates everything after the decimal.

In addition to **methods**, the JavaScript Math object also contains certain values, such as PI:

```js
Math.PI // is equal to: 3.141592653589793
```

Now that we've taken a look at an example of a built-in Javascript object and refreshed ourselves on dot notation, let's take a look at a built in class.