# Function Recursion

<!-- *STARLING QUOTE -Author* -->

Recursion, put simply, is when a function calls itself until a condition is met and then it stops calling itself. Pretty simple right? It may be hard to imagine what it looks like but a function can call itself inside of itself.

```javascript
  let x = 0

  const callMyself = () => {
    x++
    if (x > 9) return

    callMyself()

    return x
  }

  callMyself()
```

  > The function above returns 10. Why?

## More of Recursion

Recursion is very powerful in creating algorithms because you can perform the same tasks on the information over and over with each iteration of the information. Password hashing algorithms use this method. Merging and sorting algorithms use this method. It's all over the place and you need to know how to use it. Watch the following video. Pause and play as you need to make sure you understand what every line is doing.

  > NOTE: MPJ shares some very useful tips to programming in general in the video. Pay attention.

### See Recursion

<iframe width="655" height="368" src="https://www.youtube.com/embed/k7-N8R0-KY4" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

### Practice Recursion

- [ ] In a new Repl.it called: **Factorial of n**:
    * [ ] Write a JavaScript program to calculate the factorial of a number. (In mathematics, the factorial of a non-negative integer `n`, denoted by `n!`, is the product of all positive integers less than or equal to n. For example, `5! = 5 x 4 x 3 x 2 x 1 = 120`

- [ ] In a new Repl.it called: **Integer Range**:
    * [ ] Write a JavaScript program to get the integers in range (x, y)
    * [ ] Example : `range(2, 9) // Expected Output : [3, 4, 5, 6, 7, 8]`

- [ ] In a new Repl.it called: **Recursive Fibonacci**: (*I know...*)
    * [ ] Write a JavaScript program to get the first n of the Fibonacci numbers. The Fibonacci Sequence is the series of numbers: 0, 1, 1, 2, 3, 5, 8, 13, 21, 34, ...
    * [ ] Each subsequent number is the sum of the previous two.
    * [ ] Example `firstOfFib(6) // [0, 1, 1, 2, 3, 5]`


<!-- 
## Additional Resources

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

### Prompt 3:

=== "Example"
    ```console
      .
    ```

=== "Instructions"
    ```markdown
      .
    ```

=== "Push Yourself Further"
    ```markdown
      .
    ```

cp workspace/resources/templateFile.md docs/module-

height/width = 1.777 ---- width="655" height="368"

-->