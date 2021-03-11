# Type Boolean

<!-- *STARLING QUOTE -Author* -->

The next easiest **data type** for us to begin learning with is, undoubtedly, Boolean. A **Boolean** is darn simple, it can only be one of two things: true or false! Let's say that again, a **Boolean** data type can only be true or false. That's it.

It may sound simple, but really, Booleans are the most useful of the data types because they determine on/off, yes/no, do/do not so all other data types can be used. Take a look...

## What's False and What's True?

All values in JavaScript can be summed up as having a true or false value. That is to say, all values can be evaluated as either having a true value or a false value. We often use the terms **"truthy"** or **"falsey"** to say this very thing. A 0 will evaluate to `false` while a 1 would be evaluated as `true`.

However, a pure **Boolean** value just means it's either `true` or `false`. The code snippet below shows two variables that hold these two different values:

```javascript
  const myVariableOne = true
  const myVariableTwo = false
```

But when we're asking if another value is "truthy" or "falsey" it just means what is the value of the value or is the value actually there (does it actually exist). Let's start with "falsey" values. Here is a complete list of ALL JavaScript values that will evaluate to "falsey":

* `undefined`,
* `NaN`,
* `Null`,
* `0`,
* `-0`,
* `false`, `''` or `""` (**empty strings**)
  
  > This means that LITERALLY every other value in JavaScript (literally everything else) will evaluate to "truthy". ie. `true`, `10`, `"name"`, '.'.

### The Power of Booleans in JavaScript

Think about the process of signing into your favorite app. When you type your username and password in, the front-end app sends that information to the server which has to use your username to pull your info out of a database and compare your inputted password to your actual password that's saved in the database. If the two passwords match, this is a true evaluation and you can be logged into your account. If not, that would be a false value.

While programming we will perform various evaluations on **Boolean values**, in order to produce some kind of result. When properly implemented, they're kind of like asking a "yes or no" question about some piece of data at a particular point in your application. When we get a "yes/no" answer we can then start performing "if/else" procedures. Do you see where this is going yet?

Back to that sign-in process. We could write:

```javascript
  if (inputtedPassword === actualPassword) {
    return logUserIn()
  } else {
    return "Wrong username or password. Please try again."
  }
```

We'll talk about if/else statements, also known as **conditional statements**, in a few lessons, but by now you might be able to see why we need to have and to use Boolean values.

## The Comparison Operators

As you learned in the last section the `=` is known as the assignment operator because it points, or *assigns* value to a variable. We still need to compare values so let's look at how we can do that.

### The Double-Equals "==" vs the Triple-Equals "==="

If we want to compare values we'll need to use two variations of the equal sign:

`==`, checks if two values are equal.
`===`, **first** checks if two values are of the **same type** *then* checks if the values are equal.

> The two tokens/symbols above are doing two different things but also the same thing. One is checking if things are equal, ==. BUT, because JavaScript likes to coerce data types, we have to use the === on occasion to first check the type of data then to check the equality of the values. Check out the examples below:

```javascript
  64 == '64' // true
  64 == 'sixty-four' // false

  // the string 'sixty-four' won't be coerced but '64' will be

  64 === '64' // false

  // 64 is of type Number where '64' is of type String so they are not equal in the strictest sense
```

Let's look at each a little more closely on an individual basis.

#### Value Only Comparison, "=="

The `==` is used to compare values.

```javascript
  'blue' == 'blue' // true
  // or
  'blue' == 'black' // false
```

  > Above we see that the string `blue` equals `blue` but does not equal `black`. Now that you have that down, check this craziness out. Below, the string `'3'` equals the number `3`:

```javascript
  3 == '3' // true
```

If you use the `==` in a comparison like the one above, JavaScript will try to **coerce** the String type of `'3'` into a Number type `3` and then compare the two.

Again, JavaScript will try to change the string of `"3"` to the number of `3` and will result in the comparison being `true`. There is a **big problem** here. JS is type switching the type of one of our pieces of data and we don't want that!! This can result in poor program behavior, or **side-effects**. Because of this problem, there was a patch to the JavaScript language which introduced the **Identity Operator**, or **Strictly Equals**(slang): `===`.

#### Strictly Equals: "==="

To fix this problem of **type switching** or **type coercion** we use the **identity operator**. It looks like this: `===`. And it not only evaluates equality but also evaluates **type of data, first.** That is, it won't perform an evaluation unless the data types first match each other.

Therefore:

```javascript
  3 === '3' // false
```

Strictly equals `===` is much safer, since each **operand** gets tested by its **data type first**.

```javascript
  1 === '1' // false
  1 === 1   // true
```

This doesn't mean you can't use `==` but you will hear most developers say that you can't. Word to the wise, always know what you're writing and what you intend it to do. If you feel a `==` works in the case do it. Otherwise, stay with the safer `===`. This will be a debate you'll have for years to come.

## Practice It

1. Read the code below and try to guess what the console.log will be. In other words, what will each line log out?
2. Copy the console logs below and paste them into your text-editor and run them.
3. Why do you think line 9 and 10 logged out different values?

```javascript
  console.log("line 1 is: " + (1 === 1));

  console.log(2 === 1);

  console.log("yes" === "yes");

  console.log("yes" === "no");

  console.log("line 5 is: " + (true === true));

  console.log(true === false);

  console.log(1.2 === 1.2);

  console.log(1.2 === 1.20);

  console.log("line 9 is: " + (12 === '12'));

  console.log("line 10 is: " + (12 == '12'));
```

  > NOTE: `console.log()` - the console is your "terminal" object in your browser and `.log()` is a built-in method that prints information on it.

  > NOTE 2: Now that you've downloaded Node.js you can use it to run scripts like this in your computer's terminal by running the command `node` + ++enter++. The press ++cntrl+c+ twice to exit.

## Know Your Docs

* [MDN Docs - Type Boolean](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean)
