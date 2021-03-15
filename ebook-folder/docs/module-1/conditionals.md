# Conditional Statements

*Acknowledging the good that you already have in your life is the foundation for all abundance. —Eckhart Tolle* 

## Function Signatures Review

<iframe src="https://player.vimeo.com/video/377206571" width="900" height="600" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe>

## Intro to Conditionals

<iframe src="https://player.vimeo.com/video/377363180" width="900" height="600" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe>

### Why Conditionals

Just like we saw in our pre-work, we can compare data and return the results. Using conditionals within functions we can return or do something entirely different based on the results of the comparison. Check it out!

If we asked our friend Dave to check on two buckets that are catching water from a leaky roof: "Dave, could you check bucket "x" and "y"? If "x" is more full dump it out, else, dump out "y" and tell me how much is in each bucket afterwards.

Translated into JavaScript it would look like this:

```javascript
  const bucketX = 18
  const bucketY = 20

  // declare a function that takes in two parameters (buckets of water)
  const checkWater = (x, y) => {

    // compare the two values
    if (x > y) {
      // if x is greater, set x to equal 0
      x = 0
    } else {
      // else, if y is greater, set y to equal 0
      y = 0
    }
    // return the values to us.
    return "the value of x is: " + x + " and the value of y is: " + y
  }

  // invoke the function and pass the two arguments
  checkWater(bucketX, bucketY)
```

  > RUN IT! Copy/paste this code in a new Repl.it and play with it for yourself!

### How Conditionals

To use conditionals, we simply put them into a conditional statement like an if/else statement that asks "Is this comparison `true` or `false`?". Example:

```javascript
  if (6 === 6) {
    return "yes six equals six."
  } else {
    return "Nope, those are not equal."
  }

  // if we ran the code block we would get a return of "yes six equals six." because, of course, 6 does equal 6.

  if (6 === 7) {
    return "yes six equals six."
  } else {
    return "Nope, those are not equal."
  }

  // But if we ran this code block we would get: "Nope, those are not equal."
```

  > You see, an if/else statement asks if a condition is true and, if so, do the first thing, else do the second thing.

#### More Conditional Demos

An if/else statement will run a block of code if what we evaluate in the **evaluation parentheses** evaluates to truthy; else do what's in the **else** statement.

Below we see the double-pipes to see if either of the operands is truthy. Literally: is input1 or input2 truthy?

```javascript
  const input1 = 88; // truthy
  const input2 = 0; // falsey

  if (input1 || input2) {
      return true
  } else {
      return false
  } // return true
```

And here we see that we can use the **double-ampersand** to ask if **BOTH** `input1` and `input2` are truthy.

```javascript
  const input1 = 'hello'; // truthy
  const input2 = null; // falsey

  if (input1 && input2) {
      return true
  } else {
      return false
  } // returns false
```

Let's use our `typeof` operator: The if statement performs a specified operation if the **condition** you provide is **"truthy"**.

```javascript
  const name = 'jerry';
  const number = 10

  if (typeof name === string) {
    console.log(`${name} is a string.`);
  } else {
    return false
  }

  // will return false
  if (typeof name === number) {
    console.log(`${name} is a string.`);
  } else {
    return false
  }
```
  
  > Above we see the use of **template literals** as in: ``${name} is a string``. This is just a simple way to add values of constants with strings like: "is a string." We could use concatenation like this:`name + " is a string"`, but it's much easier to use template literals. For now, you can do whichever is easier for you.

If the condition is **"falsey"**, an **alternative operation** can be specified with an **optional** `else` **clause**.

```javascript
    const name = 'elaine';

    if (typeof name === string) {
      console.log(`The type of 'name' - ${name} - is a string.`);
    } else {
      console.log(`'name' is not a string - it is a ${typeof name}`);
    }
```

Multiple **else statements**: You can also provide one or more alternatives that perform conditional evaluations using `else if`:

```javascript
  // this is a handy way to get a random whole number
  const number = parseInt(Math.random() * 100, 10);

  if (number < 10) {
    console.log(`The 'number' - ${number} - is less than 10.`);
  } else if (number > 11 && number < 20) {
    console.log(`The 'number' - ${number} - is less than 20, but greater than 11.`);
  } else {
    console.log(`The 'number' - ${number} - is greater than 20, but less than 100.`);
  }
```

  > Above we see the use of [parseInt()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/parseInt) which is a built-in method in JS we can use whenever we need a whole number. We also see Math and .random() which generates a random decimal number.

Go to the MDN docs on [parseInt()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/parseInt)  and [Math.random()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/random) and explain the following:

- [ ] Why do you think we multiply it by 100?
- [ ] Can you explain why number is always going to be less than 100?
- [ ] Also, what does the 10 being passed to parseInt do?

### Alternatives to Conditional Statements

<iframe src="https://player.vimeo.com/video/377400170" width="900" height="600" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe>

#### Switch Statement (optional alternative to if/else)

**Switch statements** can sometimes be used to more concisely express conditional operations. A switch statement is used if you are only evaluating the value of one constant.

```javascript
  const numbers = [1, 2, 3, 4, 5];
  const randomIndex = parseInt((Math.random() * 10 / 2), 10);
  const randomNumber = numbers[randomIndex];

  switch (randomNumber) {
    case 1:
      console.log(`The value at randomIndex ${randomIndex} is 1: ${randomNumber}`);
      break;
    case 2:
      console.log(`The value at randomIndex ${randomIndex} is 2: ${randomNumber}`);
      break;
    case 3:
      console.log(`The value at randomIndex ${randomIndex} is 3: ${randomNumber}`);
      break;
    default:
      // Statements executed when none of the cases match the switch expression
      console.log(`The value at randomIndex ${randomIndex} is 4 or more: ${randomNumber}`)
      break;
  }
```

### Ternary (another alternative to if/else)

Ternary Operators `?` / `:` can be used as a shorthand for `if` / `else` statements:

```javascript
  const randomNumber = parseInt(Math.random() * 10, 10);

  const isEvenOrOdd = (number) => {
    return number % 2 === 0 ? `even: ${number}` : `odd: ${number}`
  }

  isEvenOrOdd(randomNumber)
```

They look a little strange at first, but it helps to think of the entire expression as an oddly-punctuated question-and-answer:

```javascript
  // is the remainder of 'evenOrOdd' ÷ 2 equal to Zero ?       <--- `if`
  return number % 2 === 0

  // if so, return 'even:' along with the value :              <--- `then return`
  ? `even: ${number}`

  // otherwise, return 'odd:' along with the value.            <--- `else return`
  : `odd: ${number}`
```

  > Note that the placement of the operators `?` / `:` at the beginning or end of the line doesn't affect the validity of the expression—either way, it will be executed. For that matter, you can write it all on the same line.

However, for the sake of readability, it is recommended that you break the operations onto separate lines, with the **operators at the beginning of each separate line**:

```javascript
  const randomNumber = parseInt(Math.random() * 10, 10);

  const isEvenOrOdd = (number) => {
    return number % 2 === 0
      ? `even: ${number}`
      : `odd: ${number}`
  }

  isEvenOrOdd(randomNumber)
```

Formatted like so, it is easy to quickly scan your eyes along the left side of the code and see a **ternary expression**.

  > This might sound frivolous and nitpicky, but bear in mind that one stylistic **downside** of using ternary expressions is **readability** (or lack thereof). They might be more elegant than if / else statements, but they're not always as recognizable at a glance. So use discretion when using them.

## Practice It - Conditionals

For each of the following, create a new Repl.it called the title you see in bold and also name the function the same as the title. Then copy/paste the prompt at the top with the "//" so you'll have the challenge right there for you to reference.

- [ ] **//sumOfTwoNums** - write a function that returns the sum of two numbers if both arguments are numbers.
- [ ] **//bothTrue** - write a function that returns 'both are true' if both arguments are true.
- [ ] **//checkStrings** - write a function that takes 3 parameters and if all 3 parameters are strings, return true
- [ ] **//evaluateMonth** - write a switch statement that evaluates a variable month, and for each of the 12 months, returns the number of days in that month.

```javascript
  // starter code
  const evaluateMonth = (month) => {
    switch (month) {
      case 'day':
      case 'Jan': {
        return 31
      }

      default: return '45'
    }
  }
```

## Know Your Docs

* [MDN Docs - Conditional Statements](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/if...else)

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