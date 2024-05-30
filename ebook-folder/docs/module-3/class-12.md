# Class 12: Hackathon

<!-- ! HIDE FROM STUDENT; INSTRUCTOR ONLY CONTENT -->
<!-- ## Instructor Only Content - HIDE FROM STUDENTS -->

<!-- ! END INSTRUCTOR ONLY CONTENT -->

*Believe in yourself. You are braver than you think, more talented than you know, and capable of more than you imagine. ―Roy T. Bennett* 

## Greet, Outline, and Objectify

<!-- SMART: Specific, Measurable, Attainable, Relevant, and Timely. -->
<!-- https://examples.yourdictionary.com/well-written-examples-of-learning-objectives.html -->

Today we're going to:
  
*OBJECTIVE: Today is about creation, synthesis using previously learned skills. This is where you become a programmer!*

- [ ] Questions for Student Led Discussion
- [ ] Interview Challenge
- [ ] Student Presentations
- [ ] Creation Time
    - [ ]  Choose a challenge
    - [ ]  Choose a team of 2-3
    - [ ]  Whiteboard, code plan, pseudo code, JavaScript
    - [ ]  Test
    - [ ]  Present!
- [ ] Push Yourself Further
- [ ] Interview Questions - BlogPost_206
- [ ] Exit Recap, Attendance, and Reminders

### Questions for Student Led Discussion, 15 mins
<!-- This section should be structured with the 5E model: https://lesley.edu/article/empowering-students-the-5e-model-explained -->

[Questions to prompt discussion](./../additionalResources/questionsForDiscussion/qfd-class-12.md)

### Interview Challenge, 15 mins
<!-- The last two E happen here: elaborate and evaluate  -->
<!-- this sections should have a challenge that can be solved with the skills they've learned since their last class. -->
<!-- ! HIDDEN CONTENT: INSTRUCTOR ONLY -->
[See Your Challenge Here](./../additionalResources/interviewChallenges.md)
<!-- ! END HIDDEN CONTENT: INSTRUCTOR ONLY -->

### Student Presentations, 15 mins

[See Student Presentations List](./../additionalResources/studentPresentations.md)

## Creation Time, 60-90 mins

Using the algorithms you've been learning about so far you will join forces with a group of 3 total students and choose one of the following prompts to build a solution for the challenge. Work as a team, divide the work, share a repo and get a working prototype up by the end of class.

### Prompt 1: Hang Man

**Project Objective** - This is a terminal based app. Reveal a letter from a word if a user inputs that letter and it exists in the word. If it doesn't let the user know.

=== "Example"

    ```console
      Input: Any letter
      _ _ _ _ _

      L (input)
      _ _ L L _ (return)

      H (input)

      H _ L L _

      E (input)

      H E L L _

      O (input)

      H E L L O
    ```

=== "Instructions"

    ```markdown
      1. First build this project in the terminal
      2. Then attach it to the DOM
      3. Work through the challenge together
      4. As always whiteboard it and make a code plan
      5. Translate from English to pseudo code then to JavaScript
      6. Test
      7. Present to class
      8. Turn in the URL to your repo, once for each person in your group
    ```

=== "Push Yourself Further"

    ```markdown
      Further Practice Challenge - Keep track of the user's lives, so if they guess incorrectly they lose a life.

      Challenge example:

      _ _ _ _ _

      V (input)

      "V" is not in the word! 4 lives left!

      _ _ _ _ _
    ```

### Prompt 2: Ramp Numbers

A ramp number is a number whose digits from left to right either only rise or stay the same. 1234 is a ramp number and so is 1124 and 13569. But 1032 is not and neither is 1528.

Challenge: Given the input of a number, build a program that will find the total number of ramp numbers that are less than it.

Example:

=== "Code Example"

    ```javascript
      const numOfRampsBelow = (num) => {
        //  Your code goes here
      }

      numOfRampsBelow(99999) // => "2001 total ramp numbers are less than 99999"
    ```

=== "Example 2"

    ```markdown
      Given: A positive integer, n.

      Output: The number of total ramp numbers less than n.

      Example input: 123

      Example output: 65 total ramp numbers are less than 123
    ```

=== "Instructions"
    ```markdown
      1. First build this project in the terminal
      2. Then attach it to the DOM
      3. Work through the challenge together
      4. As always whiteboard it and make a code plan
      5. Translate from English to pseudo code then to JavaScript
      6. When you finish work on the Further Practice Challenge
      7. Test
      8. Present to class
      9. Turn in the URL to your repo, once for each person in your group
    ```

=== "Push Yourself Further"
    
    ```markdown
      Further Practice Challenge - Display all of the ramp numbers that are less than the input number (n).
    ```

### Prompt 3: Count It

Given a sentence, paragraph or novel, count the letters in the string. Ignore whitespace and anything not `[a-z][A-Z]`, i.e. punctuations and numbers.

=== "Example"

    ```console
      Given: A string - like "Hello World"

      Output: Letters and how often they show up. - d:1 e:1 h:1 l:3 o:2 r:1 w:1
    ```

=== "Instructions"

    ```markdown
      1. First build this project in the terminal
      2. Then attach it to the DOM
      3. Work through the challenge together
      4. As always whiteboard it and make a code plan
        > Hint: convert all to lowercase first
      5. Translate from English to pseudo code then to JavaScript
      6. Test
      7. Present to class
      8. Turn in the URL to your repo, once for each person in your group
      
      > Use this challenge input: "The quick brown fox jumps over the lazy dog and the sleeping cat early in the day."
    ```

=== "Push Yourself Further"

    ```markdown
      1. Use RegEx
      2. Make a word count
      3. Count each word's appearance
      4. [Calculate the grade level/proficiency of English](https://www.thoughtco.com/calculating-reading-level-1857103) for the sentence, paragraph or novel
    ```

## Student Feedback

<iframe src="https://docs.google.com/forms/d/e/1FAIpQLSd85nNCk_MdnaXCsX7fWl3vYgcqvozzlK2cKq26d2g67Zh8Kg/viewform?embedded=true" width="640" height="600" frameborder="0" marginheight="0" marginwidth="0">Loading…</iframe>

## Blogs to Show You Know

[Blog Prompts](./../additionalResources/blogPrompts.md)

## Exit Recap, Attendance, and Reminders, 5 mins

* Create Hackathon CHECKPOINT Assignment
* Create 206 Blog Assignment
* Prepare for next by completing all of your pre-class lessons
* Complete the feedback survey

<!-- <iframe id="openedx-zollege" src="https://openedx.zollege.com/feedback" style="width: 100%; height: 500px; border: 0">Browser not compatible.</iframe>
<script src="https://openedx.zollege.com/assets/index.js" type="application/javascript"></script> -->


<!-- TODO Create 3 question exit questions -->

<!-- TODO INSERT Student Feedback From -->

<!-- TODO INSERT *HIDDEN* Instructor Feedback Form -->

<!-- 
height/width = 1.777 ---- width="655" height="368"
cp workspace/resources/classOutlineTemplate.md docs/module-
 -->