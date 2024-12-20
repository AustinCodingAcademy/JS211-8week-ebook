# Interview Challenges

## Why Train for Interviews?

Interviewing for development jobs is tough! To prepare you for the challenges ahead we will practice whiteboarding in front of the class every day. Think of it as a warm-up for the project that awaits. The whiteboarding challenges should be taken seriously and practiced even outside of class. Help yourself by following these steps to attack the problem, work through the problem and collaborate with your interviewer (instructor):

## How to Solve Your Challenge

- [ ] Restate the question aloud.
- [ ] Write the question out at the top of the whiteboard.
- [ ] Ask any clarifying questions you need.
- [ ] Invoke the function and write out the expected output given the sample input. If none is given, make it up.
Write out a code plan to the side of the whiteboard.
Speak aloud every thought you have. THIS IS THE MOST IMPORTANT PART!
- [ ] Build the structure of your function(s).
- [ ] Slowly work through your code plan, building the steps you need.
- [ ] Don't be afraid to mess up and say it aloud.
- [ ] It's not about finding the solution. It's about collaborating and working toward a solution!
- [ ] After you finish, take a picture and transfer it to a Repl.it when you get home.

## The Prompts

### Class 1 Prompt: Two Eggs & 100 Floors** -

*The following is a description of this famous puzzle involving 2 eggs and a building with 100 floors. Suppose that we wish to know which stories in a 100-story building are safe to drop eggs from, and which will cause the eggs to break on landing. What strategy should be used to drop eggs such that the total number of drops in the worst case is minimized and we find the required floor?*

    > We may make a few assumptions:
      > - An egg that survives a fall can be used again.
      > - A broken egg must be discarded.
      > - The effect of a fall is the same for all eggs.
      > - If an egg breaks when dropped, then it would break if dropped from a higher floor.
      > - If an egg survives a fall then it would survive a shorter fall.

### Class  2 Prompt: Hourglasses Puzzle - 

*How do you measure 9 minutes from a 4 minute-glass and a 7 minute-glass?*

    > We have only 2 sand timers: 4 minutes and 7 minutes but we need to measure 9 minutes. How do we do it?
  
### Class 3 Prompt: sumPoweredByTwo

*Take an array of numbers, raise each number by the power of two and return the sum of the new array.*

    ```javascript
      const myArr = [ 1, 2, 3]

      sumOfPoweredByTwo(myArr) // --> 14
    ```

### Class 4 Prompt: FizzBuzz

*Write a program that prints the numbers from 1 to 100, but for multiples of three print "Fizz" instead of the number and for the multiples of five print "Buzz". For numbers which are multiples of both three and five print "FizzBuzz".*

Bonus: What's the Big O of your algorithm? 

### Class 5 Prompt: isUnique

*Write a function that determines if a string contains all unique characters.*

  ```javascript
    isUnique('egg') // --> false
    isUnique('Artemis') // --> true
  ```
Bonus: What's the Big O of your algorithm? 

### Class 6 Prompt: wordLength

*Build a program to find the length of the longest word in a string excluding punctuation and removing whitespace.*

    ```javascript
      const myString = "This is for your own personal journey. May you have excellent navigation as a developer using your own compass."

      findLongestWord(myString) => 'navigation', 10
    ```

Requirement: What's the Big O of your algorithm? 

### Class 7

- [ ] **Prompt 1: sortedScores** - *Return unsorted scores in a descending sorted array.*

    ```javascript
      /*Example*/
      const unsortedScores = [37, 89, 41, 65, 91, 53]
      sortedScores(unsortedScores) => [91, 89, 65, 53, 41, 37]
    ```

- [ ] **Prompt 2: float precision** *What will be the output of this code? `console.log(0.1 + 0.2 == 0.3);`*

Requirement: What's the Big O of your algorithm? 

### Class 8

  **Prompt 1: reverseArray** - *Build a function that takes in an array and returns it in reverse order.*
  **Prompt 2: duplicate** - *make this work* `duplicate([1,2,3,4,5]); // [1,2,3,4,5,1,2,3,4,5]`

Requirement: What's the Big O of your algorithm? 

### Class 9

  **Prompt 1: powOfTwoSumEven** - *Given an array of numbers, raise each number by the power of 2 and return the sum of all the numbers that are evenly divisible by 4, i.e.* `const myArr = [1, 5, 10, 4, 2] // => 120`
  **Prompt 2: Function Currying** - *How would you make the following work? What's the utility of it?*
  
  ```javascript
    add(2, 5); // --> 7
    add(2)(5); // --> 7
  ```
Requirement: What's the Big O of your algorithm? 

### Class 10

- [ ] **Prompt 1: isPalindrome** *Build a function that would determine if a string was a palindrome.*
- [ ] **Prompt 2: Method Chaining** *What value is returned from the following statement?* `"i'm a lasagna hog".split("").reverse().join("");`

Requirement: What's the Big O of your algorithm? 

### Class 11

- [ ] **Prompt 1: inPlaceMoveZeros** *Given an array `nums`, write a function to move all 0s to the end of the array while maintaining the relative order of the non-0 numbers:*

  ```console
    Input: [0,1,0,3,12]
    Output: [1,3,12,0,0]
  ```

- [ ] **Prompt 2: Questionable Value** *What is the value of window.foo?* `( window.foo || ( window.foo = "bar" ) );`

Requirement: What's the Big O of your algorithm? 

### Class 12

- [ ] **Prompt 1: Summing the Array:** *Given an array of numbers, return the sum of all the numbers.*
- [ ] **Prompt 2: Bubble Sort** Hand built bubble sort:

  ```javascript

    bubbleSort([120, 315, 43, 56, 22, 8224, 8, 68, 90, 10, 32, 23, 45, 5, 20, 34, 250])
    // returns => [ 8224, 315, 250, 120, 90, 68, 56, 45, 43, 34, 32, 23, 22, 20, 10, 8, 5]

  ```

Requirement: What's the Big O of your algorithm? 

### Class 13

- [ ] **Prompt 1: MaxValueOfArray** *Talk through: Given an array, find the maximum value of the array*
- [ ] **Prompt 2: Merge Sort** *Hand build merge sort*
- [ ] **Prompt 3: FizzBuzz Sum** *If we list all the natural numbers below 10 that are multiples of 3 or 5, we get 3, 5, 6 and 9. The sum of these multiples is 23. Build a function to find the sum of all the multiples of 3 or 5 below 1000.*

Requirement: What's the Big O of your algorithm? 

### Class 14

- [ ] **Prompt 1: The Fibonacci Sequence...** *Each new term in the [Fibonacci sequence](https://en.wikipedia.org/wiki/Fibonacci_number) is generated by adding the previous two numbers together. By starting with 1 and 2, the first 10 numbers will be:*`0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89, ...` *By considering the terms in the Fibonacci sequence whose maximum value does not exceed four million, find the sum of the even-valued terms.*
- [ ] **Prompt 2: Scope** *What is the outcome of the two alerts below?*

  ```javascript
  var foo = "Hello";
    (function() {
      var bar = " World";
      alert(foo + bar);
    })();
    alert(foo + bar);
  ```
  
- [ ] **Prompt 3: length** *What is the value of foo.length?*
  
  ```javascript
    var foo = [];
    foo.push(1);
    foo.push(2);
  ```
Requirement: What's the Big O of your algorithm? 

### Class 15

- [ ] **Prompt 1: What is Foo?** *What is the value of foo.x in the code below?*

  ```javascript
    var foo = {n: 1};
    var bar = foo;
    foo.x = foo = {n: 2};
  ```

- [ ] **Prompt 2: Quick** *As a class, build a quick sort by hand.*

Requirement: What's the Big O of your algorithm? 

### Class 16

- [ ] **Prompt 1: Reduce Function** *Everyone, build Reduce sort function. Start with the 4 questions of any method.*
- [ ] **Prompt 2: Promise** *What does the following code print?*

  ```javascript
    console.log('one');
    setTimeout(function() {
      console.log('two');
    }, 0);
    Promise.resolve().then(function() {
      console.log('three');
    })
    console.log('four');
  ```

- [ ] **Prompt 2: Filter Function** *Everyone build a Filter function, start with those 4 questions!!*


<!-- Create a function that estimates the read time for a web page based on average reading speed -->

<!-- https://medium.com/frontend-development-with-js/answers-of-front-end-job-interview-coding-questions-3c227d59016c -->