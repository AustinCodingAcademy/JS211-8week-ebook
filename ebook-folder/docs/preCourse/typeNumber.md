# Type Number & Basic Mathematic Operators

Obviously in a calculator we have the basic calculation: +, -, /, *. When we program we also have access to these operations. In JavaScript:

* `+` means add
* `-` means subtract
* `*` means multiply
* `/` means divide
* `**` means exponent

In JavaScript, however, when we use the `=` token, it means "assign" or "point" rather than equals. There for its called the **Assignment Operator**...because it assigns value to a variable.

In our calculator, to return the value of a calculation, we use the **keyword** `return` like so:

```javascript
  const addTwoNumbers = (num1, num2) => {
    return num1 + num2
  }

  addTwoNumbers(7, 54)

  //expected return value >>> 61
```

## The Modulus Operator

The last operator we might want to use on our Numbers is called modulus, as in `11%5` equals `1`. Try it in your console.

When we want the remainder of a division operation we use the `%` operator.

This just means that we can divide a number by another number and get the **remainder**. I.e. 5 divided by 2 has a remainder of 1 because 2 will go into it twice with one left over. That operation in JavaScript would look like this:

```javascript
  5 % 2 // expected return => 1
```

Perhaps the most useful purpose of this operator is to decide if a number is even or not. If the return of the modulus operation by 2 is **0** then the number must be even:

```javascript
  60 % 2 // => 0, even
  61 % 2 // => 1, odd

  100 % 2 // => 0, even
  101 % 2 // => 1, odd

  22 % 2 // => 0, even
  23 % 2 // => 1, odd

  10 % 2 // => 0, even
  11 % 2 // => 1, odd
```

## Built-In Methods of Data Type: Number

Those built-in functionalities we call methods are very useful, as you'll see later on, but for the type Number, there are actually not that many to talk about, which makes for a very easy entry into methods.

The [built-in methods for type Number](https://www.w3schools.com/js/js_number_methods.asp) are:

* `toString()`
* `toExponential()`
* `toFixed()`
* `toPrecision()`

Additionally, we have 3 JavaScript Methods to help us to convert numbers:

* `Number()` - converts a string to a number
* `parseInt()` - converts a number to a string
* `parseFloat()` - converts a string to a decimal number

```javascript
  const x = 123;

  x.toString();            // returns 123 from variable x
  (125).toString();        // returns 123 from literal 125
  (100 + 23).toString();   // returns 123 from expression 100 + 23
```

## Know Your Docs

* [MDN Docs - Type Number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)
* [MDN Docs - JS Operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators)

## Additional Resources

* [Terms of a Division Equation](https://www.splashlearn.com/math-vocabulary/division/division#:~:text=Each%20part%20involved%20in%20a%20division%20equation%20has%20a%20special%20name.&text=Dividend%3A%20The%20dividend%20is%20the,obtained%20in%20the%20division%20process.)
