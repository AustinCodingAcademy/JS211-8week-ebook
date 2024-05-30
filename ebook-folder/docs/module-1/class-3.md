# Class 3: Pig Latin

<!-- ! HIDE FROM STUDENT; INSTRUCTOR ONLY CONTENT -->
<!-- ## Instructor Only Content - HIDE FROM STUDENTS -->

<!-- https://studio.zollege.com/course/course-v1:ACA+JS211+JS211_PT_MASTER?show=block-v1%3AACA%2BJS211%2BJS211_PT_MASTER%2Btype%40sequential%2Bblock%4087929252ffd94fa79b986bf3cd76c652 -->

<!-- ! END INSTRUCTOR ONLY CONTENT -->

*Trust yourself. You know more than you think you do. —Benjamin Spock*

## Greet, Outline, and Objectify

<!-- SMART: Specific, Measurable, Attainable, Relevant, and Timely. -->
<!-- https://examples.yourdictionary.com/well-written-examples-of-learning-objectives.html -->

Today we're going to:
  
*OBJECTIVE: *Today students will practice to understand and internalize:

* *building functions that take in arguments as parameters*
* *passing arguments into functions*
* *function scope and context*
* *fat arrow syntax for functions*

1. Questions for Student Led Discussion
2. Interview Challenge
3. Student Presentations
4. Instructor Walk-through of entire app from `package.json` --> `readline`
5. [Creation Time - Pig Latin](https://github.com/AustinCodingAcademy/JS211_PigLatinProject.git)
6. Push Yourself Further
7. Exit Recap, Attendance, and Reminders

### Questions for Student Led Discussion, 15 mins
<!-- This section should be structured with the 5E model: https://lesley.edu/article/empowering-students-the-5e-model-explained -->

[Questions to prompt discussion](./../additionalResources/questionsForDiscussion/qfd-class-3.md)

### Interview Challenge, 15 mins
<!-- The last two E happen here: elaborate and evaluate  -->
<!-- this sections should have a challenge that can be solved with the skills they've learned since their last class. -->
<!-- ! HIDDEN CONTENT: INSTRUCTOR ONLY -->
[See Your Challenge Here](./../additionalResources/interviewChallenges.md)
<!-- ! END HIDDEN CONTENT: INSTRUCTOR ONLY -->

### Student Presentations, 15 mins

[See Student Presentations List](./../additionalResources/studentPresentations.md)

## Creation Time, 60-90 minutes

From What is [Pig Latin on Wikipedia](https://en.wikipedia.org/wiki/Pig_Latin):

> Pig Latin is a language game in which words in English are altered, usually by adding a fabricated suffix or by moving the onset or initial consonant or consonant cluster of a word to the end of the word and adding a vocalic syllable to create such a suffix. For example, Wikipedia would become Ikipediaway (taking the 'W' and 'ay' to create a suffix). The objective is to conceal the words from others not familiar with the rules. The reference to Latin is a deliberate misnomer; Pig Latin is simply a form of argot or jargon unrelated to Latin, and the name is used for its English connotations as a strange and foreign-sounding language. It is most often used by young children as a fun way to confuse people unfamiliar with Pig Latin.

```javascript
  toPigLatin("Pig Latin") // => Igpay Atinlay
```

Today you're going to build the logic for this fun little program.

- [ ] [Demo - Pig Latin Translator](https://funtranslations.com/pig-latin)
- [ ] Students will build the Pig Latin application using the [Pig Latin Repo starter code](https://github.com/AustinCodingAcademy/JS211_PigLatinProject.git).
- [ ] Why do we need to fork?
- [ ] Why do we need to run `npm i`?
- [ ] The basic idea of Pig Latin is to take the first letters of a word up to the first vowel, move them to the end of the word, and add 'ay' to the end of it.

> Below we see a function called pigLatin that gets multiple words passed into it as arguments. The `// --->` represents what the function will return with the given parameter.

```javascript
  pigLatin('car') //=> 'arcay'
  pigLatin('create') //=> 'eatecray'
  pigLatin('pony') //=> 'onypay'
  pigLatin('egg') //=> 'eggyay'
```

Use a whiteboard to plan how Pig Latin works before building it with code.

### Additional Resources

* [Video - Coding Pig Latin](https://youtu.be/c-ZtRKAc3fY)

### Push Yourself Further

- [ ] Compartmentalize your code into individual functions
- [ ] Minimize redundancy: [D.R.Y.](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself) up your code.
- [ ] Write a unit test for words starting with multiple consonants: "create"
- [ ] Build the functionality for this complexity.
- [ ] Write a unit test for multiple words: "Pig Latin", "Jurassic Park"
- [ ] Build the functionality for this new complexity.

<!-- ## Blogs to Show You Know    EVEN CLASSES ONLY -->

## Student Feedback

<iframe src="https://docs.google.com/forms/d/e/1FAIpQLSd85nNCk_MdnaXCsX7fWl3vYgcqvozzlK2cKq26d2g67Zh8Kg/viewform?embedded=true" width="640" height="600" frameborder="0" marginheight="0" marginwidth="0">Loading…</iframe>

## Exit Recap, Attendance, and Reminders, 5 mins

- [ ] Create Pig Latin Assignment
- [ ] Prepare for next by completing all of your pre-class lessons
- [ ] Complete the feedback survey

<!-- <iframe id="openedx-zollege" src="https://openedx.zollege.com/feedback" style="width: 100%; height: 500px; border: 0">Browser not compatible.</iframe>
<script src="https://openedx.zollege.com/assets/index.js" type="application/javascript"></script> -->


<!-- TODO Create 3 question exit questions -->

<!-- TODO INSERT Student Feedback From -->

<!-- TODO INSERT *HIDDEN* Instructor Feedback Form -->