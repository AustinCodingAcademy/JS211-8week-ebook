# Type String

*Success is liking yourself, liking what you do, and liking how you do it. — Maya Angelou*

## Overview

<iframe src="https://player.vimeo.com/video/384024751" width="900" height="600" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe>

## The Methods of Strings

Moving a little deeper into the complexity of data types, Strings are commonly used and have quite a few built-in methods we can leverage to manipulate them.

To begin, you'll always know a string by the single-quotes or double-quotes wrapped around the characters. Notice I said characters and not numbers. That's because `"1976"` is a string, and so is `"I have a dog."` as well as `"My address is 89 Parmer Way."` Literally, any set of characters between quotes is a string.

We use strings to store data when we don't need to do calculations on them like we would with numbers, when we don't need to iterate through multiple pieces of data, and when what we're storing is relatively simple like text and even phone numbers: `"214-990-0009"`.

### Dot-Notation

Before we can learn the built-in methods of String we should cover that little `.` you've seen before in the Number and Math methods, called the **Member Operator**.

Below you'll see a few of the built-in methods you can use on strings. To access them you'll notice a . between the variable that holds the string value and the method that's called.

This **Dot Notation** is very common and you've actually already seen it before, but let's spend just a bit of time understanding why we need to use it.

With objects like functions and standard JavaScript objects we can access the **properties** on them with a .. Look at the JavaScript object below:

```javascript
  const myObject = {
    id: 1693,
    name: "John Proctor"
  }

  console.log(myObject.id) // => 1693
  console.log(myObject.name) // => John Proctor
```

Although there is a little bit more syntax in this example than you've seen so far, you can see the properties on the object: `id` and `name`. We can access each of these with a ., i.e. `myObject.id` = 1693.

We can do the same thing with our String data types because they each reference the same object in the JavaScript library: the prototype. As we create a new variable and assign it a string variable, our computer will point the variable to the prototype object so that we have access to the built-in methods of the String data type. Therefore, we can simply type `myString.length` and get the length of the string instead of `prototype.myString.length`.

**DON'T WORRY ABOUT THE PROTOTYPE RIGHT NOW,** we'll talk about it in depth later on.

You can use dot notation on any object as long as you know the **key** or **attribute** of the thing you're trying to reference. But let's get back to strings!

### A Short List of Common String Methods

Remember, you will have to [reference the documentation](https://www.w3schools.com/js/js_string_methods.asp) on each data type regularly to learn and remember each of their methods, but here we'll talk about some of the most common ones which should include the one's you'll need to complete the Pig Latin app.

* `.length` returns the number of characters in a string including spaces.
  > NOTE: length doesn't require parenthesis. Why?
* `.indexOf()` method returns the index (position) of the first occurrence of a specified text in a string.
* `.lastIndexOf()` method returns the index of the last occurrence of a specified text in a string.
* `.search()` method searches a string for a specified value and returns the position of the match.
* `.concat()` ...(see docs)
* `.substring()` ...(see docs)
* `.replace()` ...(see docs)
* `.charAt()` ...(see docs)
* `.trim()` ...(see docs)
* `.split()` changes a string to an array - Useful for PigLatin
* `.slice()` takes in **two parameters** to extract and return a part of a string.

In the following example we see the `.slice()` method used on a string. * `.slice()` takes the characters between the two indexes you provide in the arguments. In this example we invoke `.slice(6, 10)`.

```javascript
  const exampleString = "Apples are delicious!";
  const exampleSlice = exampleString.slice(6, 10);

  console.log(exampleSlice) // => "are"
```

When we count the positions in strings, we must remember that they are **0 indexed**. This means that the first position of a string is 0, the second position is 1, the third position is 2 and so forth.

Because of this, the indexes in the example above are:

* `exampleString[0] = "A"`,
* `exampleString[1] = "p"`,
* `exampleString[4] = "e"`,
* `exampleString[6] = " "`,
* `exampleString[9] = "e"`,
* `exampleString[11] = "d"`

So `slice(7,13)` will return the characters from the indexes between 7 and 13. Pop that code into a Repl.it and play to make sure you understand **0 indexed**.

### Bracket-Notation

We just did something back there with the `[]` that helped us access the values of the string. Let's take a look at that.

With lists of items like a string or `arrays` we can access any position we want using **bracket notation**, `[]`, because each of the positions are **indexed**. So if we want to get the `"!"` in the `"Apples are delicious!"` string example, we would write: `exampleString[20]` which will return `"!"`. Try it yourself if you don't believe me.

Because the positions are indexed, we can also **loop** over each position with a **for loop** just like we would with an Array, as you'll do in Pig Latin:

```javascript
  // create an example string to play with
  const myString = "Love"

  // create a function that will loop over ANY string given to it
  const anExampleForLoop = (str) => {
    for(let i = 0; i < str.length; i++) {
      console.log(str[i])
    }
  }

  // pass the string into the function
  anExampleForLoop(myString)
```

> In the example above, we created a for loop that:

>   * sets `i` to be 0 so we can access the first position of the string
>   * then continues to move forward as long as `i` is less than the length of `myString` or, in the **scope** of the function: `str`
>   * each time it loops, the value of `i` is increased by 1: `i++`
>   * during each loop it logs to the console the character in the current position of `str[i]`
    
> The expected return of this code snippet should be:

```terminal
L
O
V
E
```

#### Try it Yourself!!

Throw it into a [REPL.IT](https://REPLIT.com)!

The great thing about bracket notation is that you can use variables inside the `[]` just like the i you see above. In that example, `i` is a variable. We don't know the value of it at any given point but we assume it will be 0, then 1, then 2, then 3.

> Simple rule to live by: If you need to use a variable or a number to access a position of something, you will need to use `[]` and **not** ..

## Know Your Docs

* [MDN Docs - Type String](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)
* [Article - Dot- vs Bracket-Notation](https://codeburst.io/javascript-quickie-dot-notation-vs-bracket-notation-333641c0f781)


<!-- ## Additional Resources

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

cp workspace/resources/templateFile.md docs/preCourse/

-->