# Class 2: Rock, Paper, Scissors

<!-- ! HIDE FROM STUDENT; INSTRUCTOR ONLY CONTENT -->
<!-- ## Instructor Only Content - HIDE FROM STUDENTS -->

<!-- ! END INSTRUCTOR ONLY CONTENT -->

*The pessimist sees difficulty in every opportunity. The optimist sees opportunity in every difficulty. —Winston Churchill*

## Greet, Outline, and Objectify

<!-- SMART: Specific, Measurable, Attainable, Relevant, and Timely. -->
<!-- https://examples.yourdictionary.com/well-written-examples-of-learning-objectives.html -->

Today we're going to:
  
* GENERIC OBJECTIVE: *Understand the use of logic gates by applying their understanding of them to build a Rock, Paper, Scissors game.*

- [ ] Questions for Student Led Discussion
- [ ] Interview Challenge
- [ ] Student Presentations
- [ ] Creation Time Project: R.P.S. - 70 mins
    - [ ]  Fork & Clone the [RPS Repo](https://github.com/AustinCodingAcademy/JS211_RockPaperScissorsProject.git)
    - [ ]  Ensure you have installed all dependencies/packages: `npm install`
    - [ ]  Instructor covers the `package.json` and what the `"scripts":` and `"test":` objects are.
    - [ ]  Ensure you know how to run tests for each program: `npm test main.js`
    - [ ]  Whiteboard a solution to building a Rock, Paper, Scissors program
    - [ ]  Translate the broad ideas to pseudo code
    - [ ]  Convert the pseudo code to real JavaScript code
    - [ ]  Type into your text editor the JavaScript code you've come up with one step at a time
    - [ ]  Work through your bugs
    - [ ]  Achieve green checks for each of your unit tests
- [ ] Push Yourself Further
- [ ] Blog to Show You Know
- [ ] Exit Recap, Attendance, and Reminders

### Questions for Student Led Discussion, 15 mins
<!-- This section should be structured with the 5E model: https://lesley.edu/article/empowering-students-the-5e-model-explained -->

[Questions to prompt discussion](./../additionalResources/questionsForDiscussion/qfd-class-2.md)

### Interview Challenge, 15 mins
<!-- The last two E happen here: elaborate and evaluate  -->
<!-- this sections should have a challenge that can be solved with the skills they've learned since their last class. -->
<!-- ! HIDDEN CONTENT: INSTRUCTOR ONLY -->

- [ ] Restate the question aloud.
- [ ] Write the question out at the top of the whiteboard.
- [ ] Ask any clarifying questions you need.
- [ ] Invoke the function and write out the expected output given the sample input. If none is given, make it up.
- [ ] Write out a code plan to the side of the whiteboard.
- [ ] Speak aloud every thought you have. THIS IS THE MOST IMPORTANT PART!
- [ ] Build the structure of your function(s).
- [ ] Slowly work through your code plan building the steps you need.

Don't be afraid to mess up and say it aloud. It's not about finding the solution. It's about collaborating and working toward a solution! After you finish, take a picture and transfer it to a Repl.it when you get home.

**PROMPT: Hourglasses Puzzle** - How do you measure 9 minutes from a 4 minute hourglass and a 7 minute hourglass?

  > We have only 2 sand timers: 4 minutes and 7 minutes but we need to measure 9 minutes. How do we do it?
<!-- ! END HIDDEN CONTENT: INSTRUCTOR ONLY -->

### Student Presentations, 15 mins

[See Student Presentations List](./../additionalResources/studentPresentations.md)

## Creation Time, 60-90 minutes

Your first terminal application!! YAY!! Today, you're going to build a function, or two, that will take in an input from a user then another input from another user and compare them against one another to determine the winner of the game!

Fork & Clone the [RPS Repo](https://github.com/AustinCodingAcademy/JS211_RockPaperScissorsProject.git) then follow the `README.md` file.

- [ ] `User1` input of `rock`, `paper`, or `scissors`.
- [ ] `User2` input of `rock`, `paper`, or `scissors`.
- [ ] Compare `User1` input to `User2` input.
- [ ] If `User1` input is `'rock'` and `User2` input is `'scissors'`, `User1` wins.
- [ ] If `User1` input is `'rock'` and `User2` input is `'paper'`, `User2` wins.
- [ ] If `User1` input is `'rock'` and `User2` input is `'rock'`, it's a tie.
- [ ] If `User1` input is `'paper'` and `User2` input is `'rock'`, `User1` wins.
- [ ] If `User1` input is `'paper'` and `User2` input is `'scissors'`, User2 wins.
- [ ] If `User1` input is `'paper'` and `User2` input is `'paper'`, it's a tie.
- [ ] If `User1` input is `'scissors'` and `User2` input is `'paper'`, User1 wins.
- [ ] If `User1` input is `'scissors'` and `User2` input is `'rock'`, `User2` wins.
- [ ] If `User1` input is '`scissors'` and `User2` input is `'scissors'`, it's a tie.

Can you think of a simpler way?

> Where are you going to clone this project to? What directory?

### Additional Resources

<iframe src="https://player.vimeo.com/video/377156267" width="900" height="600" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe>

### Push Yourself Further

- [ ] What should the program return if the user inputs something that isn't "rock", "paper", or "scissors"?
- [ ] Can you use `.trim()` to solve the problem if a user types in a space with their input?
- [ ] Minimize redundancy: D.R.Y. up your code. Are their ways to not type as much as you've typed? Can you make the code smaller?
- [ ] Compartmentalize your code into individual functions. This game doesn't have to run just one function. Can you pull code blocks out and put them into other functions that can be called from `rockPaperScissors`?

## Student Feedback

<iframe src="https://docs.google.com/forms/d/e/1FAIpQLSd85nNCk_MdnaXCsX7fWl3vYgcqvozzlK2cKq26d2g67Zh8Kg/viewform?embedded=true" width="640" height="600" frameborder="0" marginheight="0" marginwidth="0">Loading…</iframe>

## Blog, to Show You Know

Every other class will end with a discussion over these questions. If you have no idea about them, ask your instructor. Nevertheless, you will need to research the topics on your own and record what you learned in a blog. You will then turn in a link with the url of the published blog in Zollege. Feel free to copy/paste the question into google and read about what comes up. These interview questions are meant to broaden your knowledge and cover more ground than we can possibly get to in these few weeks. We want you to be well prepared for the rigors of interviewing for development jobs and knowing the answers to these questions will ensure that you have every tool you need to succeed!

[Blog Prompts](./../additionalResources/blogPrompts.md)

## Exit Recap, Attendance, and Reminders, 5 mins

* Create RPS Assignment
* Create Blog Prompt - 201 Assignment
* Prepare for Class 3 by completing all of your pre-class lessons
* Complete the feedback survey

## Student Feedback

<iframe src="https://docs.google.com/forms/d/e/1FAIpQLScjuL10i2xFGMWRwkjtgAL8F1Y5ipMPPjtTCDzkO1ZBcxUYZA/viewform?embedded=true" width="640" height="500" frameborder="0" marginheight="0" marginwidth="0">Loading…</iframe>

<!-- INSERT Student Feedback From -->
<!-- <iframe id="openedx-zollege" src="https://openedx.zollege.com/feedback" style="width: 100%; height: 500px; border: 0">Browser not compatible.</iframe>
<script src="https://openedx.zollege.com/assets/index.js" type="application/javascript"></script> -->

<!-- TODO Create 3 question exit questions -->
<!-- TODO INSERT *HIDDEN* Instructor Feedback Form -->