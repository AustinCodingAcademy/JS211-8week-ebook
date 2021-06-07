# Class 4: Tic Tac Toe

<!-- ! HIDE FROM STUDENT; INSTRUCTOR ONLY CONTENT -->
<!-- ## Instructor Only Content - HIDE FROM STUDENTS -->

<!-- ! END INSTRUCTOR ONLY CONTENT -->

## Greet, Outline, and Objectify

*Don't let the success of others discourage you. Let it inspire you.*

<!-- SMART: Specific, Measurable, Attainable, Relevant, and Timely. -->
<!-- https://examples.yourdictionary.com/well-written-examples-of-learning-objectives.html -->

Today we're going to:
  
*OBJECTIVE - Today students will practice to understand and internalize:*

* *Unit testing as it relates to development.*
* *Looping over arrays.*
* *Conditional statements in conjunction with loops.*

- [ ] Questions for Student Led Discussion
- [ ] Interview Challenge
- [ ] Student Presentations
- [ ] Creation Time - [Tic Tac Toe](https://github.com/AustinCodingAcademy/JS211_TicTacToeProject.git)
  - [ ]  Unit Test Overview
  - [ ]  Build TTT
- [ ] Push Yourself Further - Build GUI for TTT
- [ ] Blog to Show You Know
- [ ] Exit Recap, Attendance, and Reminders

### Questions for Student Led Discussion, 15 mins
<!-- This section should be structured with the 5E model: https://lesley.edu/article/empowering-students-the-5e-model-explained -->

[Questions to prompt discussion](./../additionalResources/questionsForDiscussion/qfd-class-4.md)

### Interview Challenge, 15 mins
<!-- The last two E happen here: elaborate and evaluate  -->
<!-- this sections should have a challenge that can be solved with the skills they've learned since their last class. -->
<!-- ! HIDDEN CONTENT: INSTRUCTOR ONLY -->
[See Your Challenge Here](./../additionalResources/interviewChallenges.md)
<!-- ! END HIDDEN CONTENT: INSTRUCTOR ONLY -->

### Student Presentations, 15 mins

[See Student Presentations List](./../additionalResources/studentPresentations.md)

## Creation Time, 60-90 minutes

### Part 1: Unit Tests

- [ ] Open your RPS folder.
- [ ] `git push` your latest changes
- [ ] `git checkout -b unit-test-practice` to create a new branch to safely work within.
- [ ] Use the examples below to build additional tests for your application to pass:
    - [ ]  What if a user adds a space before or after their input?
    - [ ]  What if the user hit ENTER before typing in an input?
    - [ ]  Brainstorm with your classmates to test for even more **edge cases**.

```javascript
  if (typeof describe === 'function') {

    describe('#rockPaperScissors()', () => {
      it('should detect a tie', () => {
        assert.equal(rockPaperScissors('rock', 'rock'), "It's a tie!");
        assert.equal(rockPaperScissors('paper', 'paper'), "It's a tie!");
        assert.equal(rockPaperScissors('scissors', 'scissors'), "It's a tie!");
      });
      it('should detect which hand won', () => {
        assert.equal(rockPaperScissors('rock', 'paper'), "Hand two wins!");
        assert.equal(rockPaperScissors('paper', 'scissors'), "Hand two wins!");
        assert.equal(rockPaperScissors('rock', 'scissors'), "Hand one wins!");
      });
      it('should scrub input to ensure lowercase with "trim"ed whitepace', () => {
        assert.equal(rockPaperScissors('rOcK', ' paper '), "Hand two wins!");
        assert.equal(rockPaperScissors('Paper', 'SCISSORS'), "Hand two wins!");
        assert.equal(rockPaperScissors('rock ', 'sCiSsOrs'), "Hand one wins!");
      });
    });
  } else {

    getPrompt();
  }
```

### Part 2: Build TTT

- [ ] Fork and clone [Tic Tac Toe Repo](https://github.com/AustinCodingAcademy/JS211_TicTacToeProject.git)
- [ ] Read the `README.md` and the comments in `main.js`
- [ ] Figure out the process of playing tic tac toe using a whiteboard.
- [ ] Run the tests, run the program. What is happening in its current state?
- [ ] What are the steps the computer will need to do to complete the task of placing a mark?
- [ ] What about changing between "X" and "O"?
- [ ] How does it determine a win?
- [ ] Translate your ideas into pseudo code.
- [ ] Translate your pseudo code into real JavaScript code.

### Push Yourself Further

- [ ] Connect this Tic Tac Toe logic to your [TTT-GUI from Web 101](https://github.com/AustinCodingAcademy/TicTacToe-101).

## Student Feedback

<iframe src="https://docs.google.com/forms/d/e/1FAIpQLScjuL10i2xFGMWRwkjtgAL8F1Y5ipMPPjtTCDzkO1ZBcxUYZA/viewform?embedded=true" width="640" height="500" frameborder="0" marginheight="0" marginwidth="0">Loading…</iframe>

## Blogs to Show You Know

Every other class will end with a discussion over these questions. If you have no idea about them, ask your instructor. Nevertheless, you will need to research the topics on your own and record what you learned in a blog. You will then turn in a link with the url of the published blog in Zollege. Feel free to copy/paste the question into google and read about what comes up. These interview questions are meant to broaden your knowledge and cover more ground than we can possibly get to in these few weeks. We want you to be well prepared for the rigors of interviewing for development jobs and knowing the answers to these questions will ensure that you have every tool you need to succeed!

[Blog Prompts](./../additionalResources/blogPrompts.md)

## Exit Recap, Attendance, and Reminders, 5 mins

* Create TicTacToe Assignment
* Create 202 Blog Assignment
* Prepare for next by completing all of your pre-class lessons
* Complete the feedback survey

<!-- <iframe id="openedx-zollege" src="https://openedx.zollege.com/feedback" style="width: 100%; height: 500px; border: 0">Browser not compatible.</iframe>
<script src="https://openedx.zollege.com/assets/index.js" type="application/javascript"></script> -->


<!-- TODO Create 3 question exit questions -->

<!-- TODO INSERT Student Feedback From -->

<!-- TODO INSERT *HIDDEN* Instructor Feedback Form -->

<!-- cp workspace/resources/classOutlineTemplate.md docs/module-1/class-.md -->