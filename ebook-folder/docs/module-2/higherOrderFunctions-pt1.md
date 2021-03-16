# Higher Order Functions pt. 1

*If you set goals and go after them with all the determination you can muster, your gifts will take you places that will amaze you —Les Brown*

## Why

You have already learned about arrays and array methods. Some of the most commonly used array methods are higher-order functions, or functions that take another function as one of their parameters. These functions are useful because they make your code more concise and easier to understand.

## Higher Order Functions(Methods) Intro

There are many higher-order functions built into JavaScript that help make our code efficient, readable and reusable. For now, we will discuss three array methods that are higher-order functions: Array.prototype.forEach, **Array.prototype.map**, and **Array.prototype.filter**. As you begin to create more complex programs and work with single page applications such as React and Angular, these will be some of the most frequently used methods in your code.

### Array.prototype.forEach()

The [.forEach()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach) method can be called on any array. The `prototype` you see is just the basis of the array in the language of JavaScript. For now, don't worry or focus your attention on prototype, this is something you can figure out later. It is irrelevant at the moment. `.forEach()` takes a callback function as its only parameter. This function iterates through all of the values in an array and uses the callback function passed to it to do something with the value. If you have ever used a for loop that looks something like this: `for (let i = 0; i < arr.length; i++){//do something}` then you have essentially created the functionality of a forEach loop in long-hand.

Here is an example of a forEach loop:

```javascript
  const colors = ['orange', 'red', 'blue', 'yellow', 'green', 'purple'];

  colors.forEach((color) => {
    console.log(`My favorite color is ${color}`);
  });
```

Copy/paste the above code into a Repl.it and run it. You will notice that a sentence starting with "My favorite color is" gets logged to the console one time for each value in the array.

Unlike the other two higher-order functions you will learn about in today's prep work, forEach will never be assigned to a new variable because it always returns undefined. Also notice the () => {} inside the `()` of the `.forEach()`. This `() => {}` is an **anonymous function** passed to the forEach. The parameter inside the `()` of the `() => {}` like color in the above example represents the individual element in the array as the forEach loops through the array.

### Array.prototype.map()

The [.map()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map) method of an array is used to create a new array that is, in some way, a transformation of an existing array. Similarly to a forEach loop, it takes a **[callback function](https://javascriptissexy.com/understand-javascript-callback-functions-and-use-them/)**, `() => {}`, as its only parameter and passes every value/element in the array into the callback function. In the new array returned by the map method, each new value is assigned to be equal to whatever the callback function returns when passed the original value. Let's look at an example of a map function in action:

```javascript
  const colors = ['orange', 'red', 'blue', 'yellow', 'green', 'purple'];

  const tieDyes = colors.map((color) => {
    return `tieDyed-${color}`;
  });

  console.log(tieDyes);
```

Run the above code in a Repl.it. Notice that what is stored in the tieDye variable is an array that is equal in length to the colors array, but each value from the color array has been transformed to start with `"tieDyed-"` and end with the original color. If you will look at the code, you will see this is exactly what is returned in the callback function passed to `colors.map`.

* [Video FunFunFunction - .map()](https://youtu.be/bCqtb-Z5YGQ)

### Array.prototype.filter()

The .[filter()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter) method does exactly what it sounds like it would do. It iterates through an array and returns only values that follow a specified rule. The filter method is passed a callback function as its only parameter. The filter method returns a new array by passing each value in the original array into the callback function. If the callback function returns true or any truthy value, that value is included in the new array, but if the callback function returns false or any falsy value, that value is not included in the new array. If all of the values passed into the callback function return a falsy value, then the filter method returns an empty array: `[]`.

Let's look at an example of the filter method:

```javascript
  const colors = ['orange', 'red', 'blue', 'yellow', 'green', 'purple'];

  const sixOrMore = colors.filter((color) => {
    return color.length > 5;
  });

  console.log(sixOrMore); //=> ['orange', 'yellow', 'purple']
```

  > Copy the above code and run it in a Repl.it. Notice that the new array is not equal in length to the original array. This is because the new array only included values which passed the test of containing strings with a length greater than five. For all of the words with five or fewer letters the callback function returned false and thus the values were not included in the new array.

  > Before moving on make sure you watch the video **Functional Programming w/Anjana Vakil**, in the [Additional Resources](#additional-resources)!

* [Video FunFunFunction - .filter()](https://youtu.be/BMUiFMZr7vk)

## Practice It - pt. 1

- [ ] Go to the CodePen below, click the top-right corner.
- [ ] Fork it to your account.
- [ ] If not already collapsed, drag the HTML and CSS windows to the left so you're only looking at the JS file.
- [ ] Follow the instructions in the comment lines in the JS file.

<iframe height="600" style="width: 100%;" scrolling="no" title="Higher-Order Functions Part I - Practice" src="https://codepen.io/kdybvig/embed/darmmQ?height=265&theme-id=dark&default-tab=js,result" frameborder="no" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href='https://codepen.io/kdybvig/pen/darmmQ'>Higher-Order Functions Part I - Practice</a> by Keith
  (<a href='https://codepen.io/kdybvig'>@kdybvig</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

## Practice It - pt. 2

in a Repl.it...

```javascript
  forEach

  const colors = ['orange', 'red', 'blue', 'yellow', 'green', 'purple'];

    // build a function that returns the sentence: "The color we're on right now is: orange"
    // remember to invoke the function
  map

    const users = ['Olivia', 'Victoria', 'Paulina', 'Yolanda', 'Georgina', 'Bill'];

    // Build a function that return the sentence: `The user's name is: ${name}`
    // remember to invoke the function
  filter

    const colors = ['peaceful', 'red', 'ants', 'lovely', 'bud', 'witness', 'purple', 'clouds'];

    // build a function that only returns words that are less than 4 letters in length
    // remember to invoke the function
```



## Additional Resources

* [Video Traversy - JS Higher Order Functions + Arrays](https://youtu.be/rRgD1yVwIvE)
* [Video JS Conf - Functional Programming w/Anjana Vakil](https://youtu.be/e-5obm1G_FY)

## Know Your Docs

* [MDN Docs - filter() Method](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter)
* [MDN Docs - forEach() Method](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach)
* [MDN Docs - map() Method](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map)

<!-- 

* [Video - ]()
* [Video - ]()

```javascript

```

- [ ] Task Two
    *  [ ] Task Two.a
    *  [ ] Task Two.b
    *  [ ] Task Two.c


| Method      | Description                          |
| ----------- | ------------------------------------ |
| `GET`       | Fetch resource                       |
| `PUT`       | Update resource |
| `DELETE`    | Delete resource |


* [MDN Docs - ...]()

- [ ] ...
- [ ] ...


```javascript

``` 

- [ ] ...
- [ ] ...
  * [ ] ...
  * [ ] ... 

    `line numbers`
:do you like 'em?

++slash++

https://facelessuser.github.io/pymdown-extensions/extensions/keys/ 

=== "Javascript"

    ```javascript
    ```

=== "Python"

  ```python
  ```

cp workspace/resources/templateFile.md docs/module-

-->