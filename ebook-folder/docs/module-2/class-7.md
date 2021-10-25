# Class 7: MasterMind

<!-- ! HIDE FROM STUDENT; INSTRUCTOR ONLY CONTENT -->
<!-- ## Instructor Only Content - HIDE FROM STUDENTS -->

<!-- ! END INSTRUCTOR ONLY CONTENT -->

*Step out of the history that is holding you back. Step into the new story you are willing to create. —Oprah Winfrey*

## Greet, Outline, and Objectify

<!-- SMART: Specific, Measurable, Attainable, Relevant, and Timely. -->
<!-- https://examples.yourdictionary.com/well-written-examples-of-learning-objectives.html -->

Today we're going to:
  
*OBJECTIVE: Deepen our understanding and appreciation for built-in higher order methods by rebuilding them ourselves and using them to solve complex problems.*

- [ ] Questions for Student Led Discussion
- [ ] Interview Challenge
- [ ] Student Presentations
- [ ] Creation Time
    - [ ]  Whiteboard, code plan, and build `.forEach()` from scratch
    - [ ]  Whiteboard, code plan, and build MasterMind
    - [ ]  [Build Tests for MasterMind](https://github.com/AustinCodingAcademy/JS211_MasterMind)
- [ ] Push Yourself Further
- [ ] Exit Recap, Attendance, and Reminders

### Questions for Student Led Discussion, 15 mins
<!-- This section should be structured with the 5E model: https://lesley.edu/article/empowering-students-the-5e-model-explained -->

[Questions to prompt discussion](./../additionalResources/questionsForDiscussion/qfd-class-7.md)

### Interview Challenge, 15 mins
<!-- The last two E happen here: elaborate and evaluate  -->
<!-- this sections should have a challenge that can be solved with the skills they've learned since their last class. -->
<!-- ! HIDDEN CONTENT: INSTRUCTOR ONLY -->
[See Your Challenge Here](./../additionalResources/interviewChallenges.md)
<!-- ! END HIDDEN CONTENT: INSTRUCTOR ONLY -->

### Student Presentations, 15 mins

[See Student Presentations List](./../additionalResources/studentPresentations.md)

## Creation Time, 60-90 mins

<!-- 
  * Instructor to Demonstrate with Examples, Explain and Set Expectations using the Rubric for the Project
  * Group Students in 3s 
    * plan and implements
  * Partner with other groups for elaboration
  * Share with the class for evaluation (potentially carry into the next class) 
-->

### Pt. 1 - .forEach() from Scratch

When working with the many built-in methods of JavaScript or any language, it's important to know how they work internally so you are not constrained by their usage or unaware of their "gotchyas". Create a Repl.it and turn in the URL of it.

### Pt. 3 - MasterMind

[Mastermind](https://en.wikipedia.org/wiki/Mastermind_(board_game%29)) is a code-breaking game, where a player tries to guess the code based on a limited amount of information given from an incorrect guess. You can [play the game here](http://www.web-games-online.com/mastermind/).

#### MasterMind App Specs

- [ ] Create a new branch called "masterMind"
- [ ] **Spec 0 - Define a test solution**: Helpful suggestion: while developing you can set a default solution for you to test against. At the top of `mastermind()`, simply set const `solution = 'abcd';` as a global variable.
- [ ] **Spec 1 - Detect a correct solution**: In `mastermind()`, if the guess you passed in equals the `solution`, return `'You guessed it!';`
Spec 2 - Generate a hint: `generateHint()` should take one argument, guess.
- [ ] **Spec 2.1 - Split up the solution and guess**: In `generateHint()`, create variables `solutionArray` and `guessArray` that each split up passed in arguments, [.split](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/splitting on `''` (empty string).
- [ ] **Spec 2.2 - Determine correct "letter-locations"**: Create a variable `correctLetterLocations` and set it to `0`. This variable will record how many correct "letter-locations" were guessed. For instance, a guess of `aabc` against a solution of `deba` would yield one correct "letter-location" (b). In a `for` loop, iterate over the solutionArray, comparing each index of `solutionArray` against the same index of `guessArray`. If the item matches, increment `correctLetterLocations`, and set that index in `solutionArray` to `null`.
- [ ] **Spec 2.3 - Determine correct "letters"**: Now that we have `null`ed the already counted `correctLetterLocations`, we can see if the `guessArray` contains any `correctLetters` that were not in the correct location. Set a variable `correctLetters` equal to `0`, and in a `for` loop, again iterate over the `solutionArray`. Using .[`indexOf`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/indexOf), determine if the item at the current index in `guessArray` appears inside of `solutionArray`. Save that index in a variable called `targetIndex`. Now, `if` `targetIndex` is greater than `-1`(it exists in the array), increment `correctLetters` and set the item in `solutionArray` at that index equal to `null`.
- [ ] **Spec 2.4 - `return` hint string**: Optionally, you can use the [colors package](https://www.npmjs.com/package/colors), return a string that prints out the hints you generated, with `correctLetterLocations` being red, `correctLetters` being white, and separated by a hyphen.
    > (NOTE: If you choose to use this color package, only `console.log` the result. If you `return` the result your program will fail the tests.)
- [ ] **Spec 3 - Add guess and hint to the board**: Define a variable called hint that collects the returned value of `generateHint(guess)`. `.push` the `guess` and the `hint` (as a combined string) into the board.
- [ ] **Spec 4 - End the game**: After 10 incorrect guesses, if the `board` `length` equals `10`, `return` `'You ran out of turns! The solution was `' and the `solution`. Otherwise, return `'Guess again.'`.

### Additional Resources

 - [ ] [Video, Lydia Hallie - map, filter, reduce](https://youtu.be/UXiYii0Y7Nw)
 - [ ] [Video, pressmantoy - How to Play Mastermind](https://youtu.be/dMHxyulGrEk)

### Push Yourself Further

- [ ] Create a [.map()](https://youtu.be/hfYa4ugeyuc) function from scratch in a Repl.it
- [ ] Create a [.reduce()](https://youtu.be/g1C40tDP0Bk) function from scratch in a Repl.it
- [ ] Make a GUI representation for your MasterMind logic.

<!-- 

## Blogs to Show You Know    

EVEN CLASSES ONLY 
[Blog Prompts](./../additionalResources/blogPrompts.md)

Every other class will end with a discussion over these questions. If you have no idea about them, ask your instructor. Nevertheless, you will need to research the topics on your own and record what you learned in a blog. You will then turn in a link with the url of the published blog in Zollege. Feel free to copy/paste the question into google and read about what comes up. These interview questions are meant to broaden your knowledge and cover more ground than we can possibly get to in these few weeks. We want you to be well prepared for the rigors of interviewing for development jobs and knowing the answers to these questions will ensure that you have every tool you need to succeed!

-->

## Student Feedback

<iframe src="https://docs.google.com/forms/d/e/1FAIpQLScjuL10i2xFGMWRwkjtgAL8F1Y5ipMPPjtTCDzkO1ZBcxUYZA/viewform?embedded=true" width="640" height="500" frameborder="0" marginheight="0" marginwidth="0">Loading…</iframe>

## Exit Recap, Attendance, and Reminders, 5 mins

* Create MasterMind Assignment
* Prepare for next by completing all of your pre-class lessons
* Complete the feedback survey

<!-- <iframe id="openedx-zollege" src="https://openedx.zollege.com/feedback" style="width: 100%; height: 500px; border: 0">Browser not compatible.</iframe>
<script src="https://openedx.zollege.com/assets/index.js" type="application/javascript"></script> -->

<!-- TODO Create 3 question exit questions -->

<!-- TODO INSERT Student Feedback From -->

<!-- TODO INSERT *HIDDEN* Instructor Feedback Form -->

<!-- cp workspace/resources/classOutlineTemplate.md docs/module- -->