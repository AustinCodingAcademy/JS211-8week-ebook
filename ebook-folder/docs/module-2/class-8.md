# Class 8: Loops, find(), findIndex()

<!-- ! HIDE FROM STUDENT; INSTRUCTOR ONLY CONTENT -->
<!-- ## Instructor Only Content - HIDE FROM STUDENTS -->

<!-- ! END INSTRUCTOR ONLY CONTENT -->

*Everything you’ve ever wanted is on the other side of fear. —George Addair*

## Greet, Outline, and Objectify

<!-- SMART: Specific, Measurable, Attainable, Relevant, and Timely. -->
<!-- https://examples.yourdictionary.com/well-written-examples-of-learning-objectives.html -->

Today we're going to:
  
*OBJECTIVE: Build higher order functions from scratch to learn from creative and effective patterns while strengthening our ability to communicate in code.*

- [ ] Questions for Student Led Discussion
- [ ] Interview Challenge
- [ ] Student Presentations
- [ ] Creation Time
    - [ ]  Loops
    - [ ]  `.find(`) from scratch
    - [ ]  `.findIndex()` from scratch
- [ ] Push Yourself Further
- [ ] Interview Questions - BlogPost_204
- [ ] Exit Recap, Attendance, and Reminders

### Questions for Student Led Discussion, 15 mins
<!-- This section should be structured with the 5E model: https://lesley.edu/article/empowering-students-the-5e-model-explained -->

[Questions to prompt discussion](./../additionalResources/questionsForDiscussion/qfd-class-8.md)

### Interview Challenge, 15 mins
<!-- The last two E happen here: elaborate and evaluate  -->
<!-- this sections should have a challenge that can be solved with the skills they've learned since their last class. -->
<!-- ! HIDDEN CONTENT: INSTRUCTOR ONLY -->
[See Your Challenge Here](./../additionalResources/interviewChallenges.md)
<!-- ! END HIDDEN CONTENT: INSTRUCTOR ONLY -->

### Student Presentations, 15 mins

[See Student Presentations List](./../additionalResources/studentPresentations.md)

## Creation Time, 60-90 mins

* Instructor to Demonstrate with Examples, Explain and Set Expectations
* Group Students in 3s
  * plan and implements
* Partner with other groups for elaboration
* Share with the class for evaluation (potentially carry into the next class)

By now you should be fairly familiar with loops; however, you can never get enough practice! Loops are used all the time and you should get used to using them and very comfortable with implementing them.

- [ ] Create a new repo & Clone it
- [ ] Create a branch called `loops` off of `master`.

Complete each of the following exercises:

- [ ] Use a do...while loop to `console.log` the numbers from 1 to 1000.
- [ ] Create an object (with keys and values) called person with the following data:
    - [ ]  `firstName: "Jane",`
    - [ ]  `lastName: "Doe",`
    - [ ]  `birthDate: "Jan 5, 1925",`
    - [ ]  `gender: "female"`
- [ ] Create a function that logs out the keys of the object using `Object.keys()`.
- [ ] Create a function that logs out the keys and values of the object using `Object.entries()`.
- [ ] Create an `arrayOfPersons` that contains multiple "people" objects. You can simply copy/paste the person object you made above multiple times. Feel free to change the values to reflect multiple people you might have in your database.
- [ ] Create a function that uses a for...of loop and an if statement to `console.log `the value associated with the key birthDate of each object if the birth year is an odd number.
- [ ] Use `.map()` to map over the `arrayOfPersons` and `console.log()` their information.
- [ ] Use `.filter()` to filter the persons array and `console.log` 0only males in the array.
- [ ] Create a function that returns true if the value of `birthDate` is before Jan 1, 1990.
- [ ] Use `.filter()` to filter the `persons` array and `console.log` only people that were born before Jan 1, 1990.
- [ ] **BONUS** - Create a function that returns true if the date passed to it is `>= 21` years in the past.
- [ ] **BONUS** - `.filter()` out the people in the array who are younger than 21.

### Pt. 2 - From Scratch .find() & .findIndex()

- [ ] Whiteboard
- [ ] Code plan
- [ ] Pseudo code
- [ ] JavaScript code in a Repl.it for both functions
- [ ] Turn in URL of Repl.it

#### Resources

- [ ] [YT, dcode - .find()](https://youtu.be/N1QcR8F3xFY)
- [ ] [YT, dcode - .findIndex()](https://youtu.be/QL5jKmVPvUY)

### Push Yourself Further

When searching for specific data, [regular expression or RegEx](https://en.wikipedia.org/wiki/Regular_expression) is a useful tool to know how to use. Paired with the methods you've been practicing lately, you will be a JavaScript ninja in no time.

We're only going to introduce RegEx briefly. It's a subject for you to truly learn only on your own. This is by no means a requirement to pass this course or to graduate. But eventually you will want to know and use RegEx professionally. Do yourself a favor and add [reading and practicing RegEx](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions) to your daily exercises.

```javascript
  var re = /p+l/;
  const re = new RegEx('p+l')

  // the two expressions above both match the 'ppl' in 'apple' and the 'pl' in 'people'
  // the '+' looks for one or as many instances of the character that precedes it. In this case it's 'p'.
```

[Solve this problem in a Repl.it](https://www.hackerrank.com/challenges/matching-specific-string/problem)

### Additional Resources

- [ ] [YT, DevTips - RegEx](https://youtu.be/VrT3TRDDE4M)
- [ ] [Tool - MDN RegEx Cheatsheet](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions/Cheatsheet)
- [ ] [Tool - RegEx Pal](https://www.regexpal.com/)
- [ ] [Tool - RegExr](https://regexr.com/)
- [ ] [Practice - RegEx on HackerRank](https://www.hackerrank.com/domains/regex)

## Student Feedback

<iframe src="https://docs.google.com/forms/d/e/1FAIpQLSd85nNCk_MdnaXCsX7fWl3vYgcqvozzlK2cKq26d2g67Zh8Kg/viewform?embedded=true" width="640" height="600" frameborder="0" marginheight="0" marginwidth="0">Loading…</iframe>

## Blogs to Show You Know

[Blog Prompts](./../additionalResources/blogPrompts.md)

## Exit Recap, Attendance, and Reminders, 5 mins

* Create Loop Practice Assignment
* Create Scratch: Find & FindIndex Assignment
* Create 204 Blog Assignment
* Prepare for next by completing all of your pre-class lessons
* Complete the feedback survey

<!-- <iframe id="openedx-zollege" src="https://openedx.zollege.com/feedback" style="width: 100%; height: 500px; border: 0">Browser not compatible.</iframe>
<script src="https://openedx.zollege.com/assets/index.js" type="application/javascript"></script> -->


<!-- TODO Create 3 question exit questions -->

<!-- TODO INSERT Student Feedback From -->

<!-- TODO INSERT *HIDDEN* Instructor Feedback Form -->

<!-- cp workspace/resources/classOutlineTemplate.md docs/module-1/class-3.md -->