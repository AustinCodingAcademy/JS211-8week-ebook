# Coding & Programming

**Programming** is the process of solving a problem. **Coding** is the process of communicating that solution for the computer to execute.

## Programming

<iframe width="891" height="501" src="https://www.youtube.com/embed/3tWMQ3ZMjbg" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

For the sake of the class I want you to think of **programming** as figuring out the steps of a process(program) and telling the computer in a very detailed, non-ambiguous way how to execute the steps in the process(program).

In this way, you're looking at a problem from a higher point-of-view using your vision, hearing and even touch to figure out solutions to the problem and then to implement a process of steps whereby to arrive at the solution.

For instance:

### A Simple Program Example

*Given a list of numbers: 2, 5, 6, 7 and 9, add 1 to each number and return a list of the new values and the sum of all of those new values*

Perfect! Let's walk through this step by step to see how we might **program** a solution to this problem.

- [ ] Our **given input** is `[2, 5, 6, 7, 9]`.
- [ ] We have the first action: add 1 to each number in the list.
- [ ] A second action: return the list of new numbers.
- [ ] And we have a third action: return the sum of the new list of numbers!

We can even deduce another piece of the puzzle:

- [ ] If our input is a list of numbers like: `[2, 5, 6, 7, 9]` into our program, our **expect output** will be `[3, 6, 7, 8, 10]` with a sum value of `34`.

Now that we know what our program's actions(steps) are and what the expected output or our program should be we can begin to reverse-engineer the solution.

- [ ] Action 1: add 1 to each number
    * [ ] tell the computer to loop though the list of numbers and for each number add 1 to its value
  
- [ ] Action 2: return the list of new numbers
    * [ ] collect the new values in another list
    * [ ]in the return statement include the new list

- [ ] Action 3: Return the sum of the new list
  * [ ] hold the value of the new numbers in a place
  * [ ] in the return statement include the place you were holding sum of new numbers

Hopefully, you can see now how we can approach any problem. We begin with a bigger view of the problem and work our way down to the small details of it. In this way we use our natural human ability to solve complex problems with mental models and abstraction then list them into short, clear directives to give to the computer.

And this, for our purposes, is programming. We have been given a challenge and we found a solution and listed out the steps needed to make it a process. From here we can translate(code) it into any language we want: C, C++, C#, Python, Swift, Rust, Go, Dart, Java, Erlang, or Cobol. In the next section, we're going to translate(code)these steps into Javascript.

## What is Coding?

<iframe width="891" height="501" src="https://www.youtube.com/embed/N7ZmPYaXoic" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

As you just saw, **programming** is listing out all the steps a program will need to accomplish a task given by a human so that it can return an expected result. **Coding**, on the other hand, is the language we use to communicate to other humans our intent for a computer's task while also telling the computer what we expect it to repeat over and over in a precise and predictable way.

It is also important to note that **no** coding language is actually what the computer reads. All languages are **compiled** down to **binary**, the language a computer can understand. Therefore, you could use nearly any language you want to accomplish most tasks. There are restrictions, of course (i.e. all front-end apps have to be written in JS), preferences (Python for analytics), and logistical things (full coverage testing, support, open-source, and technical cost) to consider but keep in mind, the characters ([tokens](https://techterms.com/definition/token) you type into the text editor) are not really read by the computer the same way you see them on the screen.

> Now we're going to turn those programming steps from the last section into JavaScript code so that a computer can complete the tasks we created for it.

Below are the instructions we wrote out while learning to **program**, next to **code** that describes the action steps in JavaScript code. You'll see `//comments` in the code that describe what's happening

But, **STOP**, create a new [Repl.it](https://repl.it) and follow along! ...SERIOUSLY!!

### Simple Coding Example

- [ ] Before we can perform Action 1, let's build a function (program/process) we can call to do something at some point. Let's call it: `addOneWithSum`

  ```javascript
  const addOneWithSum = () => {

  }
  ```

- [ ] Then let's make sure it can take in an array of numbers like the one given to us in the example above: `const exampleArray = [2, 5, 6, 7, 9]`

  ```javascript
  const addOneWithSum = (ourArray) => {

  }
  ```

- [ ] Now let's do **Action 1: add 1 to each number**

  ```javascript
  const addOneWithSum = (ourArray) => {
    // tell the computer to loop though the list of numbers and for each number add 1 to its value
    for (let i = 0; i < ourArray.length; i++) {
      ourArray[i] + 1
    }
  }

  // More details:
  // the for() loop states:
    // let i = 0; - set i to 0, (i stands for iterator)
    // i < ourArray.length; - and while i is less than the length of ourArray keep doing what is inside the code block
    // i++  - and each time you loop through ourArray once add 1 to the value of i so that we keep iterating through all of the numbers in the list.
  // ourArray[i] + 1 - inside the {} of the for() loop we add 1 to each item in ourArray
  ```

- [ ] **Action 2: return the list of new numbers**

  ```javascript
  const addOneWithSum = (ourArray) => {
    // collect the new values in another list(array)
    let newList = []
    for (let i = 0; i < ourArray.length; i++) {
      newList.push(ourArray[i] + 1)
    }
    // in the return statement include the new list
    return newList
  }

  // let newList = []  -  creates a place we can hold the new values of the list
  // newList.push(ourArray[i] + 1)  -   the .push() method pushes the new values into the newList array/list
  // return newList  -  and then we returned the newList as the output of this program
  ```

- [ ] **Action 3: Return the sum of the new list**

  ```javascript
  const addOneWithSum = (ourArray) => {
    let newList = []
    // hold the value of the new numbers in a place/variable
    let sum = 0
    for (let i = 0; i < ourArray.length; i++) {
      sum += (ourArray[i] + 1)
      newList.push(ourArray[i] + 1)
    }
    // in the return statement include the place you were holding sum of new numbers
    return newList + ' ' + sum
  }

  // let sum = 0  -  Now we create a place to hold the sum of the new numbers: sum
  // sum += (ourArray[i] + 1)  -  and inside our for() loop we continually add to the value of sum
  // then we return sum as part of our output.
  // in the return we added a space, ' ' , between newList and sum so that the return would be easier to read.
  ```

- [ ] The final step to this is to feed our function(program) the input and call our newly built function(program):

  ```javascript
  const exampleArray = [2, 5, 6, 7, 9]

  const addOneWithSum = (ourArray) => {
    let newList = []
    let sum = 0
    for (let i = 0; i < ourArray.length; i++) {
      sum += (ourArray[i] + 1)
      newList.push(ourArray[i] + 1)
    }
    return newList + ' ' + sum
  }

  addOneWithSum(exampleArray)

  ```

## Practice It

1. Throw this code into a repl.it and practice for yourself!
1. Solve this problem: given an array of numbers: [2, 4, 6, 8, 10], divide each number by two, return the new array and the product (multiplied all together) of the new array.
1. Continue reading about the [differences btw coding vs programming](https://www.educba.com/coding-vs-programming/).

## Summary

A deciding factor in your success with programming is your ability to think critically about how to solve problems. After all, that's really what we do as engineers; whether we're building software or designing rocket ships—we solve problems.

To ensure your success as a web developer, our hope is not just that you learn how to code, but that you develop the skills necessary to be an effective problem-solver. The latter is arguably more important when it comes down to what will get you hired.

With that in mind, consider this section as your first lesson in fundamental programming concepts, as well as a guided tour of the kind of thinking we'd like we need you to practice as you move forward in the course. Programming and problem-solving go hand in hand—so long as you practice, ask questions and seek answers, you'll develop proficiency with both skill sets.