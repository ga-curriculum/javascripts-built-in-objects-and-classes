# ![Using JavaScript Classes - Built-In Classes](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will be able to understand and recognize built-in JavaScript classes and utilize their values and methods.

## Built-In Classes

The JavaScript Math object in the previous lesson contains a lot of useful methods and values that we can reference. We don't characterize the Math object as a class though because we cannot use it to instantiate (create) new objects. This makes sense, I mean, how many instances of the number `4` would we actually need?

So let's take a look at a JavaScript [built-in class](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects) now.

A great example of a common built-in JavaScript class is its [`Date` class](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date). There are many reasons for creating different instances of `Date` objects (*for example, birthdays, anniversaries, dates and times for timecards, dates for to do lists, calendar events, etc.*).

Let's utilize JavaScript's `Date` class to instantiate a new `Date` object using a string:

```js
const birthday = new Date("2023-05-31");
```

Our new date object is stored in the variable, `birthday`. We can now use methods from the date class on date objects, also know as ***instance methods***. There are also methods we can call on the `Date` class itself and these are called ***static methods***.

## Instance methods

If we would like to get the time of our `birthday` object, we can run the instance method, [`.getTime()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date/getTime) 

```js
birthday.getTime() // => 1685491200000
```

To see a much more user friendly date, we can use the [`.toLocaleDateString()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date/toLocaleDateString) method on `birthday` to see something like `05/30/2023`:

```js
birthday.toLocaleDateString()
```

> 📚 This is another example of an ***instance method***.

## Static (class) methods

Above, we created a `Date` object using a specific date entered as a parameter. Let's say we instead wanted to create a `Date` object that reflects ***"right now"***, like when someone clicks on a `submit` button or hits `enter`/`return`. To capture that time, we can call the [`.now()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date/now) method directly on the `Date` class:

```js
Date.now() // example: 1703121829554
```

Because the values of `birthday.getTime()` and `Date.now()` are numbers, we can actually compare them to see if one date may precede the other.

```js
if (birthday.getTime() < Date.now()) {
    console.log("Happy belated birthday!")
}
```
