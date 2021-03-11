# Comparison Operators

<!-- *STARLING QUOTE -Author* -->

<iframe src="https://player.vimeo.com/video/384017864" width="900" height="600" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe>

Now that you have the differences between `=`, `==` and `===`, let's look at how to use greater than, less than, **bang** and the other **combinators**.

## Non-Equality Operators

Th equality operators `==` and `===` are simply checking if both **operands** are equal to one another. Unlike the single `=` we saw when we assigned a value to a variable, to check for equality we must use a double `==` sign or a triple `===` sign. Both operands on either side must be truthy for the operation to evaluate to `true`, otherwise, the operation evaluates to `false`.

But what about the opposite? What if we wanted to do something if the evaluation was false? Enter the **bang**: `!`.

To evaluate if something is false you can use the bang-equal operators, `!=` / `!==`. This simply says, "if these don't equal each other do something". See the example below:

```javascript
  8 != 7 // => true
  90 !== 91 // => true
  100 != 100 // => false


  // -- or --

  // evaluates to false
  !true

  // -- or --

  const yourVariable = 0; // => falsey

  if (!yourVariable) {
      console.log("Is not truthy")
      };
```

  > NOTE: This can be literally read: if yourVariable is not truthy then print out "Is not truthy".

### Practice It - Bang Operator `!==`

- [ ] Copy/paste the following code into a Repl.it.
- [ ] Read the code and try to guess what the console will "log" out **before you run it**.
- [ ] Run it.
- [ ] Replace the "a" on line 3 with "b" and run it again. What happened?
- [ ] Revert the "b" back to an "a" but delete " = 'I am defined'" from the first line and run the app again.
- [ ] Why do you think that happened?

```javascript
  let a = "I am defined";

  // declared but not defined variable
  let b;

  if (a !== undefined) {
    console.log("'a' is defined, so 'a' is truthy")

  } else {
    console.log("'a' isn't truthy")
  }
```

### Greater-Than/Less-Than Operators

Just like you learned in 6th grade, `<` and `>` are still applicable in comparisons.

```javascript
  6 < 88 // true

  88 > 6 // true
```

* `>` means greater than
* `<` means less than

In combination with `==` or `=` the `<` and `>` signs can make useful statements:

* **Type first** greater than or equal to: `>==`
* **Type first** less than or equal to: `<==`
* Greater than or equal to: `>=`
* Less than or equal to: `<=`

#### Try It - Greater-Than/Less-Than

- [ ] Copy/paste the code below into another Repl.it.
- [ ] Assign the value of the variables "a" and "b" to different values
- [ ] Run the code multiple times to experiment and find out what's going on.
- [ ] Notice the code is using let and not var. Why do you think so?
- [ ] Bring it to class.

```javascript
  let a = 5;
  let b = 5;

  if (a > b) {
    // here the "+" is being used to concatenate multiple values together
    console.log(a + " is greater than " + b)
  } else if(a < b) {
    console.log(a + " is less than b " + b)
  } else if(a === b) {
    console.log(a + " is equal to B " + b)
  } else {
    console.log(a + " does not(!) equal " + b)
  }
```

  > The expressions between parentheses are **evaluated** for truthiness. JavaScript will try to convert the values inside those parentheses to `true` or `false`.

## Logical Operators

* `&&` (AND)
* `||` (OR)

We can also create multiple evaluations to determine if we want to do a specific actions. Using our sign-on procedure we might compare our username and password:

```javascript
  if (inputtedUserName === actualUserName && inputtedPassword === actualPassword) {
    return logUserIn()
  } else {
    return "Sorry, wrong username or password."
  }
```

  > The above code says "If the usernames match **AND** the passwords match log the user in."

```javascript
  const myVariable = 50; //truthy
  const yourVariable = 90; // truthy

  if (myVariable && yourVariable) {
      console.log("Both are truthy")
    };
```

  > This can be literally read as: if `myVariable` and `yourVariable` are truthy then print out "Both are truthy".

`&&`, read as "And" is just what it states, 'this and that'. With &&, you can kind of think of your logical operations as, "If everything in this expression is truthy, then it will evaluate to true"

```javascript
  true && true   // true
  true && false  // false
  false && true  // false
  false && false // false
```

  > The above statements, like all others are read or **evaluated** from left to right. If the first expression is true the second expression won't even be evaluated.

### The "Or" Operator - ||

The double-pipes (||) reads as "or" in our comparison statements:


```javascript
  const myVariable = 50; // truthy
  const yourVariable = 0; // falsey

  if (myVariable || yourVariable) {
      console.log("One is truthy")
    };
```

  > The above statement can be literally read: if myVariable or yourVariable are truthy then print out "One is truthy".

`||`, read as "or": "If **at least one** operand in this expression is truthy, it will still evaluate to true"

```javascript
  true || true   // true
  true || false  // true
  false || true  // true
  false || false // false
```

  > NOTE: An operand is simply a piece of data being evaluated in the expression.

## Know Your Docs

* [MDN Docs - Logical Operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators#binary_logical_operators)
