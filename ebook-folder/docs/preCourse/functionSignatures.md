# Function Signatures

<!-- *STARLING QUOTE -Author* -->

<iframe src="https://player.vimeo.com/video/377425124" width="900" height="600" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe>


## What's Next

Now that you have a few data types to use—operators, variables, and methods—you'll need to have a way to run each of those **code blocks**. You'll see your first assignment, [CurrentDate & Time](https://github.com/AustinCodingAcademy/JS211_CurrentDateTimeProject/blob/master/README.md), asks for you to "Write a JavaScript program that...". This means you need to write a program that can be **executed**, or **called**, or what we like to say: **invoked**. These programs can be complex with many functions that call each other or they can be incredibly simple like the ones this assignment asks for. Today we'll focus on the very simplest of programs/functions.

## What are Functions

Functions are **executable** blocks of code. They are used to performed predetermined tasks and return a value that can be captured and used by other functions.

Think of a function as a recipe. Specifically let's think of it as a cocktail recipe so our bartender can call upon it and make us an old fashioned when we order one.

From across the bar top we can call our bartender and order/**invoke** an oldFashioned(). Then the bartender (**JavaScript Engine/Web Browser**) can find the recipe/**function**, read the recipe/**function** and then perform the predetermined tasks specified in the function. Let's see how that could work. Read the lines of code to see how a function's **syntax** is written, as well as the comments to see what is happening:

```javascript
  // create a function called gatherIngredients which takes a cocktail name as a parameter
  const gatherIngredients = (typeOfCocktail) = {
    return typeOfCocktail.listOfIngredients
  }

  // invoke the function and pass in oldFashioned as an argument and save that to a variable named oldFashionedIngredients
  const oldFashionedIngredients = gatherIngredients(oldFashioned)

  // this will return a list of ingredients so oldFashionedIngredients now equals a list/array of recipes.

  const oldFashionedIngredients = [{1 1/2 oz Bourbon}, {Angostura bitters}, {A Sugar cube}, {Water}, {Ice Cubes}, {Old Fashioned glass}, {Cocktail cherry}]
```

  > Obviously the words above are not real words in JavaScript, but they get the idea through if you really read through them.

```javascript
  // Hold the ingredients needed to build an old fashioned
  const oldFashionedIngredients = [ {1 1/2 oz Bourbon}, {Angostura bitters}, {A Sugar cube}, {Water}, {Ice Cubes}, {Old Fashioned glass}, {Cocktail cherry} ]

  // then create the instructions to build an old fashioned which takes a list of ingredients as a parameter
  const buildAnOldFashioned = (...ingredients) => {
    Place sugar cube in old fashioned glass();
    then();
    saturate with bitters();
    then();
    add a dash of plain water();
    then();
    Muddle until dissolved();
    then();
    Fill the glass with ice cubes();
    then();
    pour 1.5 ounce whiskey in to Old Fashioned glass();
    finally();
    Garnish with cocktail cherry();

    return cocktail to guest();
  }

  // pass the ingredients as an argument into the function to invoke the function
  buildAnOldFashioned(oldFashionedIngredients);
```

You see, a function is just a recipe, written somewhere in a file, held in the memory of the computer, so it can be **called/executed/invoked** with certain ingredients/**arguments** to return a desired result.

Put another way, functions provide a way for us to perform the same task with any set of **parameters**, over and over. Think of a calculator which has a few simple functions (+, -, /, *) that are used over and over again with different arguments/numbers (0, 1, 2, 3, 4, 5, 6, 7, 8, 9). All other functions work this same way!!

## Rules About Functions

* Functions must **FIRST** be declared before they can be **invoked**.
    * Function declaration: `const myFunc = (arg1) => { return arg1 + 2}`
    * Function invocations: `myFunc(15), myFunc(10), myFunc(20)`
    The returns of these functions would be: `17, 12` and `22`
    * Functions must `return` something.
- Functions are camelCased just like variables.
- Functions should be named descriptively for their purposes and the data types that they return, i.e.
    * `isValidInput(input1)` would be a function that evaluates if a value is `true` or `false` and it would return a Boolean type value.
    * `sumOfTwoNumbers(num1, num2)` would be a function that takes two numbers and returns their sum.
- You can recognize when a function is being used by recognizing the `()`, examples:
    * `sumOfTwoNumbers(3, 4)` - is a function that is being **invoked/called/executed**
    * `const divideTwoNumbers = (num1, num2) => { num1/num2}` - is a function that is being **declared/defined**

### More Examples

Below is a JavaScript program called `sumOfTwoNumbers` that returns the sum of two numbers and is being called twice with different arguments.

```javascript
  // declaration with two parameters
  const sumOfTwoNumbers = (num1, num2) => {
    return num1 + num2;
  }

  // invocation with two arguments
  sumOfTwoNumbers(7,9) // => 16
  sumOfTwoNumbers(300, 400000); // => 400300
```

In the example below we see that function **declarations** have **parameters** but when we **invoke** a function we "pass in" **arguments**.

```javascript
  // Declare the function with parameters: a and b
  const productOfTwoNumbers = (a, b) => {
    const product = a * b;

    return product + " Yay! You returned something!";
  }

  // Invoke the function with two arguments: 2 and 8
  productOfTwoNumbers(2, 8);
```

Below, `loadContent` is a function, written in an o=**older version of JavaScript** that is being declared. *Notice the **function** keyword.*

```javascript
  function loadContent(user) {
    
    return "content loaded"
  }
```

And this example is written the same way and also being invoked.

```javascript
  // the function declaration comes first
  function ourFunFunc() {
    return "Thanks for putting me above where you invoked me";
  }

  // Invoke the function below it
  ourFunFunc();
```

**STOP**!!! There's something that must be discussed!

So far you've seen **function signatures** as:

```javascript
  const ourFunFunc = () => { }
```

But just now you saw:

```javascript
  function ourFunFunc() {
  }
```

What gives? Well, the one with the const is the newer and more preferred way of writing a **function signature**. Under the hood it provides better [scope](https://www.reddit.com/r/javascript/comments/5spw31/why_const_foo_vs_function_foo/) but that's not something you should worry about right now. We need you to be familiar with both because you will see both in the wild.

However, get comfortable with using `const functionName` instead of the keyword `function`.

## Know Your Docs

* [MDN Docs - Function Declarations](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function#difference_between_function_constructor_and_function_declaration)

## Additional Resources

* [Intro to Functions in JS](https://youtu.be/KWk9BNBtFtg)
  
    > CAUTION: In this video he does a great job explaining function syntax, he uses a different keyword and syntax to declare constants and functions. He shouldn't be using `let` but instead should be using `const` for the function declarations.

<!-- 

```javascript

``` 

* [MDN Docs - ...]()

- [ ] ...
- [ ] ...


```javascript

``` 

- [ ] ...
- [ ] ...
  * [ ] ...
  * [ ] ...

-->