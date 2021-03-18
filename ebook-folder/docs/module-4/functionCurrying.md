# Function Currying

*Strength does not come from physical capacity. It comes from an indomitable will. —Mahatma Gandhi*

**Functional programming (FP)** is an engineering paradigm much like OOP, which is what we've been working on lately. It's definitely an advanced subject and you're going to feel some anxiety when you first approach it. Why? Because it doesn't make as much direct-sense as expressing a function clearly and then invoking it (the imperative way). Today we're going to cover two big pieces of this functional programming thing, but as we work through them you may notice that you have already, inadvertently, been exposed to some of these concepts such as `.map()` and `.reduce()` (the declarative approach). However, before we continue, you need to read these two blogs:

FIRST: [Get the vocab down](https://medium.com/javascript-scene/master-the-javascript-interview-what-is-functional-programming-7f218c68b3a0)—and do the homework at the end!
SECOND: [Prep for libraries](https://www.smashingmagazine.com/2014/07/dont-be-scared-of-functional-programming/)

They should set the stage for the why, where and what we're going to cover today.

**PAUSE**

We'll wait here for you...

## What is Currying

The first thing we'll cover today is a bit of a tricky concept. We'll start by saying this methodology was created by [Haskell Curry](https://en.wikipedia.org/wiki/Haskell_Curry) after whom [Haskell](https://en.wikipedia.org/wiki/Haskell_(programming_language)) was named. The main thing you need to know about [currying](https://en.wikipedia.org/wiki/Currying) is that it is something that you will use but you shouldn't be frustrated about now if you don't get it right away. It's totally okay to not understand it as it's an advanced topic. But we're in the end of our Intermediate course so we're getting to be more advanced students of web development and therefore should be excited to jump into new and challenging concepts!

By now we're familiar with passing multiple arguments into a function like the example below:

```javascript
const myFunction = (arg1, arg2, arg3, arg4) => {
  const newVariable = // do something with the four arguments

  return newVariable
}
```

Above we can pass in 4 arguments to be used inside the function. We don't have to use all four but we have to use 1 and 2 if we want to use 3 **because order matters**. To do that we would call the function like this: `myFunction(null, null, 68)`. Pretty simple right? In fact, you've already used functions that take multiple arguments that you haven't used yet. The callback function that goes inside `.filter()` takes three arguments: the element, the index of the element and the original `array` that `.filter()` was called on. In addition, `.filter()` takes the contextual this as a second argument after the callback function.

```javascript
  arr.filter(callback(element[, index[, array]])[, thisArg])
```

You've used `.filter()` before and have probably not had to use these arguments. That's okay. I only bring them up here because I want you to be aware of unused arguments in functions before we move on to currying.

In brief, we can, instead of passing multiple parameters to a single function, pass a single argument to a function that then returns a single function with a single argument in it that also returns a single function that takes a single argument. And that, in short, is currying.

Sound confusing? Good! It should be. It's going to take a bit for your mind to figure out how this works and to develop a mental model of it for you to understand it in your mind's eye.

### More on Currying

Currying is when you break down a function that takes multiple arguments into a series of functions that take part of the arguments. Here's an example in JavaScript:

```javascript
  const addTwo = (num1, num2) => {
    return num1 + num2
  }
```

This is a function that takes two arguments, num1 and num2, and returns their sum. Let's see what this function looks liked curried:

```javascript
  const addTwo = (num1) => {
    return function (num2) {
      return num1 + num2
    }
```

This is now a function that takes one argument, num1, and returns a function that takes another argument, num2, and that function returns their sum. We can call it like this:

```javascript
  addTwo(5)(6) // => 11

  // or hold the first function as a variable

  const addToFive = addTwo(5)

  // then add it to what ever number we want:

addToFive(6)  // => 11
```

This is what some people may call a closure. The third statement uses the `addToFive` operation to add 5 to 6, again producing 11 as a result.

Still confused? That's okay, it'll sink in with time. For now, read the [4th part of this FP Blog](https://hackernoon.com/javascript-and-functional-programming-currying-pt-4-96e3230782ab) and then watch the following video.

### See Currying

<iframe width="655" height="368" src="https://www.youtube.com/embed/iZLP4qOwY8I" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

### Practice Currying

- [ ] Open a new Repl.it
- [ ] Name it: Curried Function
- [ ] Paste the code below into it and curry it
- [ ] The result should be able to be called like this: `curriedGreet("Hi there")("Howard")("Austin,TX")("Angela");`

```javascript
  const greet = (greeting, name, location, greeter) => {
    console.log(`${greeting}, ${name}! Welcome to ${location}. My name is ${greeter}.`);
  };
```

## Know Your Docs

* [MDN Docs - Function](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function)
* [Javascript.info - Currying](https://javascript.info/currying-partials)

<!-- 
## Additional Resources

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

### Prompt 3:

=== "Example"
    ```console
      .
    ```

=== "Instructions"
    ```markdown
      .
    ```

=== "Push Yourself Further"
    ```markdown
      .
    ```

cp workspace/resources/templateFile.md docs/module-

height/width = 1.777 ---- width="655" height="368"

-->