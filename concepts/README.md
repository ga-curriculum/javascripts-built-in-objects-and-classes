# ![[Using Classes] - Concepts](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will be able understand how built-in classes and objects work in JavaScript.

## Built in Classes and Objects

When it comes to built-in classes and objects in JavaScript, the practical differences between the two can be a bit confusing.

In JavaScript, classes are used to generate or "construct" objects. The class is responsible for specifying what properties and methods will exist on the objects it generates. 
 
At the same time, JavaScript objects inherit properties from *prototypes*. This is why, for example, a new array that you just created has access to a `length` property, or can use the `.join()` method:

```js
const anArray = [1,2,3,4,5];
console.log(anArray.length); // 5
console.log(anArray.join(‘’)); // 12345
```
All arrays will inherit properties from the `Array` object, which has a number of built-in properties and methods that make working with arrays easier. 

What this means is that, in JavaScript, whether working with built-in classes or built-in objects, the end result is similar. The object or class is globally available to reference, and the resulting object will have predefined properties and methods associated with it. 

JavaScript has a number of built-in objects. Some work purely as objects while others allow for a class-like constructor syntax as well.

This module is not designed to be an exhaustive lesson on all of them, or to dive too deeply into *how* exactly they are available to us. Rather, the intention is to explore some of the common globally available classes and objects, and empower you to start using them in your own code.

