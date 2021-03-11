# Practice Variables and Functions

*The mind is everything. What you think you become. —Buddha*

<iframe src="https://player.vimeo.com/video/377416059" width="900" height="600" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe>

## What's a Variable

A variable in JavaScript is just a "bucket" to put data inside. It's a means of storage for values we'll need to use, access, compare, or manipulate later as we're programming.

In a variable we can store any type of data, from a person's name to a person's phone number from a list of a person's friends to a collection of a person's interests—we can hold anything in this variable "bucket".

Imagine you're holding two apples in either hand. You could compare the two pieces of **data**, "apple A" and "apple B", to one another with your two **variables**, your left hand and your right hand.

In JavaScript, to use a variable you must:

1. **Declare** the variables name `let myVariable`
2. **Assign** it a value with the `=` operator
3. And **define** its value by putting the value after the `=`: `let myProblems = 99`

* The name must start with a letter, *not a number*, and must not be a [reserved word](https://www.w3schools.com/js/js_reserved.asp) in JavaScript.
* JavaScript is a case sensitive language. `const Score` and `const score` would be treated as two different variables.
* Declare and name variables once **and only once**.

### Declare A Variable

In older versions of JS you'll see the keyword `var` BUT DO NOT USE THIS WORD FOR ANYTHING YOU BUILD in the future! The `var` keyword is out of date/**deprecated**. Instead use one of the two other keyword: `let` or `const`

The simplest, way to remember which to use is make all variables a `const` until you realize its value needs to dynamically change them make it a `let`.

You can name your variables almost anything you want, i.e. `myVariable`, `user`, `bonsaiTree`, but there are some guidelines, *see below*:

* **Descriptive Naming** - remember: variables are for us humans to reference later. It's helpful for you and your team if you name a variable what you expect to be in the variable, i.e. `userPhoneNumber` is better than `userNumber`.
* **camelCased** - first letter is lower-cased, all other words will have their first letter upper-cased.

### Assign

Simply use the token/symbol `=` to assign a value to a variable.

The **Assignment Operator**, `=`, does not mean "equal". Instead it means "this is set to the value of..." i.e. in `const userName = "Joseph"`, `"userName"` is set to the value of "Joseph".

### Define

The last step to creating a variable is to define its value. In the next lesson we'll learn what types of values you can place in a variable but for now here are examples of what values can go in a variable:

```javascript
  const myVariable = true
  const user = "Pete Williams"
  const bonsaiTree = {size: "small", age: 404}
  const score = 900
```

## Know Your Docs

From here on out, you'll see this section telling you to go to the linked website and BOOKMARK the page so you can easily reference it. It's not important that you memorize everything in JavaScript, only that you know how to find what you're looking for.

Let's start by reading the [syntax of a variable in JS](https://www.w3schools.com/js/js_syntax.asp) and bookmarking it in a bookmark folder called "JavaScript".

* [W3S Docs - JS Reserved Words](https://www.w3schools.com/js/js_reserved.asp)
* [W3S Docs - Syntax of a Variable in JS](https://www.w3schools.com/js/js_syntax.asp)

## Practice It

- [ ] Go to the [CodePen](https://codepen.io/austincoding/embed/eYmRdZB?height=265&theme-id=dark&default-tab=js,result) below, click the top-right corner "Edit on CodePen"
- [ ] Sign-in and Fork it to your account (button at the very bottom to the right).
- [ ] If not already collapsed, drag the HTML and CSS windows to the left so you're only looking at the JS file.
- [ ] If not open, click on the console button at the very bottom left to open the console.
- [ ] Then click the clear button at the top right of the console.
- [ ] Follow the instructions listed in the code comments after the `//`

<iframe height="600" style="width: 100%;" scrolling="no" title="Variable&amp;DataTypesPractice" src="https://codepen.io/austincoding/embed/eYmRdZB?height=265&theme-id=dark&default-tab=js,result" frameborder="no" allowtransparency="true" allowfullscreen="true" loading="lazy">
  See the Pen <a href='https://codepen.io/austincoding/pen/eYmRdZB'>Variable&amp;DataTypesPractice</a> by Austin Coding Academy
  (<a href='https://codepen.io/austincoding'>@austincoding</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>
