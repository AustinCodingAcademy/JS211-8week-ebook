# Higher Order Functions pt. 2

*Hard times don’t create heroes. It is during the hard times when the ‘hero’ within us is revealed. —Bob Riley*

## **Reg**ular **Ex**pression

Regular Expression is a shortcut for finding patterns in data. It looks scary at first but it's actually really easy because it, itself, follows a pattern. You can use RegEx to quickly and efficiently find keywords or characters that you would otherwise have to type out manually. While we're learning callbacks like .filter() and .reduce(), we should also learn about RegEx and start thinking about ways we can use this new tool to our advantage.

What's even better? RegEx translates to all languages. Use [the RegEx docs on Mozilla](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions) to figure your way through the following practice section.

### See It - RegEx

<!-- TODO these should be replaced with original content -->
- [ ] [YT, TechSith - RegEx in JS](https://youtu.be/rPNGB0ZLvdw)
- [ ] [YT, Corey Shafer - How to Match Any Pattern](https://www.youtube.com/watch?v=sa-TUpSx1JA&t=1347s)

### Practice RegEx

[RegEx Tutorial](https://regexone.com/#)

## Reduce

We've covered quite a bit of ground in JavaScript so far. Think about it: you've learned how to create variables, access objects, loop over arrays, build functions, pass variables to functions, and now you're passing arrays to functions that then get passed to functions!!

We have just one more higher order function to cover: `.reduce()`. Like the other higher order functions we learned about, `.reduce()` takes a callback function, but instead of an argument representing each element it's iterating over in the array, the first argument in the callback is an accumulator. This accumulator keeps up with the total value of the elements it has iterated over and the current element respective of operations you put inside the callback function.

Look at the example on the Mozilla docs on [`.reduce()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/Reduce). See how the `accumulator` and the `currentValue` are added together in the callback function on line 2, then how the callback function is passed to the `.reduce()` function on line 5?

### See It - Reduce

- [ ] [YT, FunFunFunction- Reduce](https://youtu.be/Wl98eZpkp-c)

### Practice It - Loops, Array Methods, HOFs

- [ ] Copy/paste the following code into a Repl.it and make sure you know how each loop works.

```javascript
  // For Loop

  for (let x = 1; x <= 10; x ++){
    console.log(x);
  }

  // create a for loop to print out every multiple of 3 up to 100.  
  // Do....While Loop

  let age = 0;
  do {
    age += 1;
    console.log("You are " + age + " years old and cannot buy alcohol!");
  } while (age < 21);
  While Loop

  let grade = 0;
  while (grade < 60) {
    grade += 10;
    console.log("You have a " + grade + " in this class and cannot move on to the next class until your grade is higher than a 70.");
  }
```

- [ ] `.some()`:
    * [ ] In a Repl.it, build a `.some()` function from scratch
    * [ ] Make sure you know the specifications of `.some()`
    * [ ] Use this [resource](https://youtu.be/l155liDxty8) as well.
- [ ] `.every()`:
    * [ ] In a Repl.it, build a `.every()` function from scratch
    * [ ] Make sure you know the specifications of `.every()`
    * [ ] Use this [resource](https://youtu.be/jY1WZ29YOkM) as well.
- [ ] `.reduce()`:
    * [ ] Use a `.reduce()` function to add up an array of numbers
    * [ ] Use a `.reduce()` function to find the product of an array of numbers
    * [ ] Make sure you know the specifications of `.reduce()`

## Additional Resources

- [ ] [YT, TechSith - RegEx in JS](https://youtu.be/rPNGB0ZLvdw)
- [ ] [YT, Corey Shafer - How to Match Any Pattern](https://youtu.be/rPNGB0ZLvdw)
- [ ] [YT, FunFunFunction - Reduce](https://youtu.be/Wl98eZpkp-c)
- [ ] [YT, Steve Griffith - JS .every()](https://youtu.be/jY1WZ29YOkM)
- [ ] [YT, Steve Griffith - JS .some()](https://youtu.be/l155liDxty8)

<!-- 
## Know Your Docs

* [MDN Docs - ...]() -->

<!-- 

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

cp workspace/resources/templateFile.md docs/module-

-->