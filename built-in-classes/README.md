# ![[Using Classes] - Built-In Classes](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will be able to understand and recognize built-in JavaScript classes and utilize their values and methods.

## Built-In Classes

The JavaScript Math object in the previous lesson contains a lot of useful methods and values that we can reference. We don't characterize the Math object as a class though because we cannot use it to instantiate (create) new objects. This makes sense, I mean, how many instances of the number `4` would we actually need?

So let's take a look at a JavaScript [built-in class](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects) now.

A great example of a common built-in JavaScript class is its [`Date` class](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date). There are many reasons for creating different instances of `Date` objects (*for example, birthdays, anniversaries, dates and times for timecards, dates for to do lists, calendar events, etc.*)

Let's utilize JavaScript's `Date` class to instantiate a new `Date` object using a date string:

```js
const bigDay = new Date("2023-12-18");
```

Great! We now have a new instance! Our new date object is stored in the variable, `bigDay`. We can now use methods from the date class on date objects, also know as ***instance methods***. There are also methods we can call on the `Date` class itself and these are called ***static methods***.

## Instance methods

If we would like to get the time of our `bigDay` object, we can run the instance method, [`.getTime()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date/getTime) ([we will actually see a large number based on the epoch](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date#the_epoch_timestamps_and_invalid_date)):

```js
bigDay.getTime() // => 1702857600000
```

> 🧠 To see a much more user friendly date, we can use the [`.toLocaleDateString()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date/toLocaleDateString) method on `bigDay` to see something like `12/18/2023`. This is how we would call it:

```js
bigDay.toLocaleDateString()
```

> 📚 This is another example of an ***instance method***.

## Static (class) methods

For `bigDay` above, we created a `Date` object using a specific date entered as a parameter. Let's say we wanted to create `Date` object ***"right now"***, like when someone clicks on a `submit` button or hits `enter`/`return`. To capture that time, we can call the [`.now()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date/now) method directly on the `Date` class:

```js
Date.now() // example: 1703121829554
```

Interesting. Because the values of `bigDay.getTime()` and `Date.now()` are numbers, we can actually compare them to see if one date may precede the other.

```js
if (bigDay.getTime() < Date.now()) {
    console.log("Once upon a time...")
}
```

From this samples of code above, we can get some basic ideas of what classes do:
- Classes create objects through the [new](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/new) operator.
- Each ***object*** has some properties (data or method) added by the class.
- The ***class*** stores some properties (data or method) itself, which are usually used to interact with instances.