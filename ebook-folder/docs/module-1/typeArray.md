# Type Array

*Another flaw in the human character is that everybody wants to build and nobody wants to do maintenance. —Kurt Vonnegut*

## Overview

<iframe src="https://player.vimeo.com/video/385371365" width="900" height="600" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe>

So far we've been working with primitive data types, like data type: Number, String, and Boolean. These are great for storing small isolated bits of information, but what if we have large amounts of data, many names of users, phone numbers, and emails we want to use to contact our clients? It would be rather hard to maintain all of that if we had to declare a variable for each one, and then we would have to build functions for each one, too!

To solve this problem of listing items we have **arrays** which are just that, lists or collections of items grouped together in one variable.

> All arrays are objects, but not all objects are arrays. This is a confusing phrase but don't worry, it'll make sense later on.

Let's start by learning how to declare an [array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array). You declare an array just like you would a variable but instead of quotes like a string, use brackets like this: `[]`. Now you can put the items inside the `[]` (brackets) and separate the items in an array with a comma (see below).

```javascript
  const exampleArray = ['h','e','l','l','o']
  const ourCarTypes = ["Saab", "Volvo", "BMW"]
  const itemArray = ['item1', 'item2']
  const arrayOfNumbers = [1, 200, 98, 75, 4, 4000]
  An array is a collection or list of items. This collection of items could be a collection of anything, like a collections of numbers:

  const anArrayOfNumbers = [3, 6, 7, 9, 10]
  Or a collection/list of strings:

  const anArrayOfStrings = ["cat", "mail", "stars", "hero"]
  Or a collection/list of Booleans:

  const anArrayOfBooleans = [true, false, true, true, false, true]
  Or a collection/list of multiple data types:

  const anArrayOfMixedTypes= [true, 12, "people", false, 6, 29, "happy"]
  It could even be a collection of functions or more arrays within the array:

  const addTwo = (num1, num2) => num1 + num2
  const anArray = [2, 5, 7, 68, 12]

  const anArrayOfMoreObjects = [addTwo, anArray]
```

Really, we can store **any** JavaScript thing in an array. There are a few useful reasons we would store items in an array, including:

  * Anything can be stored in an array.
  * Each item in an array has an **index**, meaning we can access the items in the array by the order in which they are listed!
  * You can **loop** over arrays. That is to say, we can write code that will grab each item in an array and do whatever we tell it to do with each item!
  * Arrays have many, many useful **methods** already built in to them!!!

For all of these reasons, type Array is probably one of the most useable data types in JavaScript!!!

### Array Indexes Start with 0

Items in an array each have a unique **index** that represents the order in which they appear. You access items in an array by their index, so order is important. It's also important to remember, just like strings, **arrays are 0 indexed. 0 indexed** means the first item in an array has an index of 0, the second item has an index of 1, the third item has an index of 2 and so forth. Basically, counting begins at 0, not 1.

```javascript
  // an array of letters
  const exampleArray = ['h','e','l','l','o']
  console.log(exampleArray[1])
```

Using the example code above: `console.log(exampleArray[1])` would log to the console e because arrays are **0 indexed**. To access `'h' ` you would need to use `exampleArray[0]`.

You can re-assign items in the array in a similar manner: `exampleArray[1] = ‘y’` would rewrite the data in the array to look like this: `[‘h’,’y’,’l’,’l’,’o’]`.

Again, the items stored in an array can be of any primitive or higher-order data type you've learned about so far: Number, null, String, Array, Object, Function, Boolean, Node, etc.

> Side-note: When we put arrays inside arrays we call this **nesting** which creates a fancy thing called a **multi-dimensional array**. See below:

```javascript
  const multiArrays = [[1, 2, 3, 6, 9, 5], [90, 5, 8, 65, 3], ["dog", "tooth", "friend"]]

  console.log(multiArrays[1]) // => [90, 5, 8, 65, 3]
  console.log(multiArrays[0]) // => [1, 2, 3, 6, 9, 5]
  console.log(multiArrays[0][3]) // => 6
  console.log(multiArrays[2][2]) // => "friend"
```

Notice that multiArrays has three arrays inside of it. When we `console.log` indexes `0`, `1`, or `2` we get the whole array at that index, but we can go even deeper by tacking two square-brackets on top of each other: `[][]` and putting numbers in them: `[1][4]`. This tells the computer to find the array we're seeking, of index `[1]`, then go inside that array and get the item we're seeking with an index of `[4]`, from that array.

This can go deeper: `anArray[2][2][0]`, and deeper: `anArray[2][2][0][7]`, and deeper: `anArray[2][2][0][7][2]` depending on how many arrays are nested within the original array.

##### Practice Nested Arrays

- [ ] Copy/Paste the following code into a Repl.it

  ```javascript
    const numArr = [
      [4, 7, 9],
      [10, 45, 300],
      [88, 64, 37, 93]
    ];
  ```

- [ ] Write a `console.log` statement that prints out the number **300** from the given array.
- [ ] Write a `console.log` statement that prints out the number **64** from the given array.
- [ ] Write a `console.log` statement that prints out the number **4** from the given array.

## Looping Over an Array

<iframe src="https://player.vimeo.com/video/385377379" width="900" height="600" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe>

### The For Loop

A **for loop** repeats an action over and over until a specified condition evaluates to false. What that means is that we tell the for loop what conditions to meet and what actions to do until those conditions are met.

First things first:

- A `for` loop is a function that takes in arguments like any other function. Those arguments look like this:
  * declare a variable that will hold an iterator: *Initial Expression*
  * loop until the iterator meets a specific value: *Condition*
  * how much the iterator should increase or decrease: *Increment Expression*

Look at the syntax below:

```javascript
  for ([initialExpression]; [condition]; [incrementExpression]) {
    action statement
  }

  // or, the same thing with real numbers and variables

  const myArr = [2, 33, 4, 54, 13, 8, 79]
  let sum = 0

  for (let i = 0; i <= myArr.length - 1; i++) {
    sum += myArr[i]
  }
```

In the code snippet above, the for loop states:

* Set an iterator variable, `i`, at 0.
* While the iterator, `i`, is less than or equal to the length of `myArr` minus 1, continue doing the action statement *(We need to subtract 1 because the last index will be one less than the total length. Remember 0 indexed?)*.
* After each loop, add 1 to the value of `i`.
* Inside the *Action Statement*, we add to the variable `sum` the value of sum + the value at the current index of the loop, which is held in the iterator, `i`.

### Try it yourself,

Copy/paste the following code into a Repl.it and run it!

```javascript
  const myArr = [2, 33, 4, 54, 13, 8, 79]

  const myFunFunction = (arr) => {
    let sum = 0

    for (let i = 0; i <= arr.length - 1; i++) {
      console.log("The value of 'i' is: " + i + " and the value at that index is: " + arr[i])
      sum += arr[i]
    }
    return console.log("The final sum is: " + sum)
  }  

  myFunFunction(myArr)
```

- [ ] Create a for loop to print out numbers from 1 - 10.
- [ ] Create a for loop to print out every multiple of 3 up to 100.

## The Methods of Array Types

<iframe src="https://player.vimeo.com/video/385392247" width="900" height="600" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe>

By now, we've talked about **methods** as baked-in functions that JavaScript things come with so we can manipulate those things easily.

You don't have to do anything special to get them to work—all you have to do is learn about them and then call them by name when you want to use them. As you learn more about the language you'll come to learn and appreciate all of the wonderful methods JavaScript has to offer, specifically for arrays, since they come with some of the most powerful methods in the JavaScript environment!

As an example, `.length` is a simple and yet very powerful method used all the time! You saw this method used above. When you call `.length` on an array, it will return the number of items in the array.

```js
  const multiArrays = [[1, 2, 3, 6, 9, 5], [90, 5, 8, 65, 3], ["dog", "tooth", "friend"]]
```

Example: If we `console.log(multiArrays.length)` from the example above we would get `3` because that array has three items in it. If we `console.log(multiArrays[0].length)` we would get `6`.

  > Note: The **index** of the last item in an array is always equal to the `.length` of the array minus one (`console.log(multiArrays[1].length - 1) // => 4`).

You can use this method to get the value of the last item too! c`onsole.log(multiArrays[1][multiArrays[1].length - 1]) => 3`

Start looking at these [array methods](https://www.w3schools.com/Jsref/jsref_obj_array.asp){:target="_blank"} and see if you can play with some dummy variables with them. Simply copy/paste some of the code snippets above into a [Repl.it](https://repl.it/){:target="_blank"}, add more data to them and try some of these methods inside a console.log statement. See what you come up with.

### The Most Important Methods

For Pig Latin you will need the first 8 array methods listed below. Open a new Repl.it, create some dummy arrays and begin playing with these methods just the same way you've played with strings, numbers, and Booleans.

- [ ] [.slice()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/slice?v=example){:target="_blank"}
- [ ] [.splice()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/splice?v=example){:target="_blank"}
- [ ] [.toString()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/toString){:target="_blank"}
- [ ] [.concat()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/concat?v=example){:target="_blank"}
- [ ] [.includes()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/includes){:target="_blank"}
- [ ] [.pop()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/pop?v=example){:target="_blank"}
- [ ] [.push()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/push?v=example){:target="_blank"}
- [ ] [.join()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/join?v=example){:target="_blank"}
- [ ] [.length](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/length){:target="_blank"}
- [ ] [.indexOf()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/indexOf){:target="_blank"}
- [ ] [.shift()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/shift?v=example){:target="_blank"}
- [ ] [.unshift()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/unshift?v=example){:target="_blank"}
- [ ] [.every()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/every){:target="_blank"}
- [ ] [.flat()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/flat){:target="_blank"}
- [ ] [.find()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/find){:target="_blank"}
- [ ] [.reverse()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/reverse?v=example){:target="_blank"}
- [ ] [.forEach()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach){:target="_blank"}

Hint: For Pig Latin you'll also need the string method: [.split()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/splitStudy){:target="_blank"} each method now and make flashcards to memorize them and make your programming faster!

### No Two Arrays Are Equal

**BIG NOTE:** One important thing to remember about arrays: no two arrays are the same array. So, even if you declared two arrays and gave them the same values, they will not be equal. See below:

```javascript
  const arr1 = [1,2,3]
  const arr2 = [1,2,3]

  arr1 === arr2 // =>  false
```

> Questions: How would you find out if two arrays contain the same values? Think about it and see if you can come up with an answer before class.

### Mutability

<iframe src="https://player.vimeo.com/video/385348888" width="900" height="600" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe>

Before moving forward we should learn about a word called **mutability**. Derived from the word "mutate", to change; as in [Teenage Mutant Ninja Turtles](https://www.youtube.com/watch?v=bojx9BDpJks){:target="_blank"}.

In programming terms, this simply means that the original data we are working with can be changed or is permanently changed. Permanently changing the original data/data structure is something that should generally be avoided. This is where the word **immutable** comes into play.

We bring up immutability here because some of the array methods you just learned about permanently change the data in the array while others return a new array without mutating the original data. While you're discovering the methods, make sure to ask **these four questions** of each method:

1. What does the method do?
2. What does the method return?
3. What arguments does the method take?
4. Does the method change the original data?

You'll learn when to change data and when not to as you go [deeper](https://www.codingame.com/playgrounds/6181/javascript-arrays---tips-tricks-and-examples){:target="_blank"}, but for now just become aware of what each methods does, what it returns, and if it's changing the original array.

An example of a method that mutates the original array is .`push()` : `exampleArray.push(‘x’)`. This method would add the string `'x'` to the end of `exampleArray` and thereby permanently change the array. The push method also returns the new length of the string. So if exampleArray had 5 elements, and you declared `const newLength = exampleArray.push('x')`, `newLength` would be equal to 6, and the string `'x'` would be added to the end of `exampleArray`.

Adding new items to an array can also be accomplished without mutation by using the concat method, which merges two arrays, or merges values into an array: `const exArr2 = exampleArray.concat('x')`. In this case, `exampleArray` would not be changed, and `exArr2` would be the same as `exArr`, but with the string `'x'` added to the end of the array. This is an example of a non-mutating array method.

To learn more about mutating and non-mutating array methods you can check out this [blog post](https://lorenstewart.me/2017/01/22/javascript-array-methods-mutating-vs-non-mutating/){:target="_blank"}, but keep in mind that unlike in this article, in most cases you will want to declare all of your arrays with `const`, not `let`, whether or not you intend to mutate them.

## Practice It

Before coming into class...

- [ ] Go to the CodePen below, click the top-right corner.
- [ ] Fork it to your account.
- [ ] If not already collapsed, drag the HTML and CSS windows to the left so you're only looking at the JS file.


<iframe height="600" style="width: 100%;" scrolling="no" title="Arrays Practice" src="https://codepen.io/kdybvig/embed/REqBXX?height=265&theme-id=dark&default-tab=js,result" frameborder="no" allowtransparency="true" allowfullscreen="true" loading="lazy">
  See the Pen <a href='https://codepen.io/kdybvig/pen/REqBXX'>Arrays Practice</a> by Keith
  (<a href='https://codepen.io/kdybvig'>@kdybvig</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>


## Know Your Docs

* [MDN Docs - Type Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array){:target="_blank"}

## Additional Resources

* [Video - Arrays for Beginners](https://youtu.be/EUnV-fCY0Pc){:target="_blank"}
* [Video - For Loops for Beginners](https://youtu.be/EUnV-fCY0Pc){:target="_blank"}
* [Video - 15 Array Tricks](https://youtu.be/Rx_JFOSxgpY){:target="_blank"}
* [Video - Diff Two Arrays](https://youtu.be/DAN-PElQ_xw){:target="_blank"}

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

cp workspace/resources/templateFile.md docs/preCourse/

-->