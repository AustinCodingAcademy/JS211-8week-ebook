# typeof Operator

<!-- *STARLING QUOTE -Author* -->

Although we haven't covered all of the data types in JavaScript yet, you'll need to know about this special operator to complete your first assignment: [CurrentDate & Time](https://github.com/AustinCodingAcademy/JS211_CurrentDateTimeProject/blob/master/README.md). So let's get this short and easy one out of the way!!

<iframe src="https://player.vimeo.com/video/384029483" width="900" height="600" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe>

## What's the Problem?

To effectively work with data, we need to know the type of data we're working with. Often times we wouldn't know what type of data is coming back to us because, as front-end developers, we usually don't build the back-end that we pull the data from. So we don't always know what to expect in the returned **data stream**. This presents problems because if the **object** we're trying to access is of type **Array** it won't have the same methods built into it as a standard JS object, and vice versa. To tell us what type of data we're working with we use the `typeof` operator.

## How Does it Work?

The `typeof` operator simply returns the data type of a variable or JavaScript object. Using `typeof` is just like asking the JavaScript engine: "What type of data is this thing?" It's really useful when you get into the end of this 211 course and all of 311 because you will be requesting "things" (objects) from a remote database and you won't know exactly what type of data you're getting back...maybe it's a string, ...maybe it's a number, ...maybe it's an object-literal! With the built-in tool, `typeof`, you won't have to guess! Check out the example below:

```javascript
  const variableOne = 0
  const variableTwo = "Peter"
  const variableThree = {id: 350, name: "Peter"}

  typeof variableOne // => of type Number
  typeof variableTwo // => of type String
  typeof variableThree // => of type Object
```

Now run the code below in a [Repl.it](https://Replit.com) to see what each logs out for each line.

```javascript
  console.log('typeof "I love JS!"', typeof "I love JS!");
  console.log('typeof 1.08', typeof 1.08);
  console.log('typeof NaN', typeof NaN);
  console.log('typeof false', typeof false);
  console.log('typeof [1, 2, 3, 4]', typeof [1, 2, 3, 4]);
  console.log('typeof {name:'Victoria', age:26}');
  console.log('typeof new Date()', typeof new Date());
  console.log('typeof function () {}', typeof function () {});
  console.log('typeof myCar', typeof myCar);
  console.log('typeof null', typeof null);
```

  > Try this yourself on another piece of data in a Repl.it. Play. Have fun! Write it down and remember to use it.

## Know Your Docs

* [MDN Docs - typeof Operator](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/typeof)

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

-->