# Class 10: Bank Account

<!-- ! HIDE FROM STUDENT; INSTRUCTOR ONLY CONTENT -->
<!-- ## Instructor Only Content - HIDE FROM STUDENTS -->

<!-- ! END INSTRUCTOR ONLY CONTENT -->

*Success is not final, failure is not fatal: it is the courage to continue that counts. —Winston Churchill*

## Greet, Outline, and Objectify

<!-- SMART: Specific, Measurable, Attainable, Relevant, and Timely. -->
<!-- https://examples.yourdictionary.com/well-written-examples-of-learning-objectives.html -->

Today we're going to:
  
*OBJECTIVE: Create a banking app that uses classes to manage fund accurately.*

- [ ] Questions for Student Led Discussion
- [ ] Interview Challenge
- [ ] Student Presentations
- [ ] Creation Time
    * [ ] Discuss how to create the BankAccount and Transaction classes.
    * [ ] Create the BankAccount and Transaction classes.
- [ ] Push Yourself Further
- [ ] Interview Questions - BlogPost_205
- [ ] Exit Recap, Attendance, and Reminders

### Questions for Student Led Discussion, 15 mins
<!-- This section should be structured with the 5E model: https://lesley.edu/article/empowering-students-the-5e-model-explained -->

[Questions to prompt discussion](./../additionalResources/questionsForDiscussion/qfd-class-10.md)

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

Today students will apply their knowledge of object-oriented programming to create two classes: one that can be used to represent a bank account and another to represent the transactions the bank account holds.

**BankAccount class** - This class represents a bank account.

1. The class should have the following fields:
    - [ ] `accountNumber` - String representing the account number
    - [ ] `owner` - String representing the owner of the account
    - [ ] `transactions` - An array of transactions representing the history of all transactions associated with this account

2. The constructor should take in the following input:
    - [ ] `accountNumber` - The account Number
    - [ ] `owner` - The name of the person who owns this account

      > NOTE: When an account is created, you should initialize the transactions array to be an empty array

3. The class should have the following 3 methods:
    - [ ] `balance()` - This method does not take any input, and returns the current balance on the account. The balance is computed by summing up the amounts in the transactions array.
    - [ ] `deposit(amt)` - This method takes in a single input, the deposit amount. This method should create a new transaction representing the deposit, and add it to the transactions array.

      > NOTE: You should not be able to deposit a negative amount

    - [ ] `charge(payee, amt)` - This method takes in the payee and amount, creates a new transaction with the payee and amount, and adds the transaction to the transaction array.

      > NOTE: You should not be able to charge an amount that would make your balance dip below 0

**Transaction class** - This class represents a single transaction in a bank account.

1. The class should have the following fields:
    - [ ] `date` - The date of the transaction
    - [ ] `amount` - The amount of the transaction. Positive amounts are money going into the account (deposit, refund). Negative amounts are money coming out of the account (a charge or debit).
    - [ ] `payee` - The description or payee on the transaction

2. The constructor should take in the following input:
    - [ ] `amount` - The amount on the transaction
    - [ ] `payee` - The payee or description on the transaction

    > NOTE: The `date` is not passed into the constructor. The constructor should set the date to be the current date automatically.

### Additional Resources

- [ ] [Video, Yousif Seedhom - Bank Account Walk-through](https://zoom.us/rec/play/tMUkduiqqj43GICQtASDBvVxW465e6qsgSEf__pZxRqwVnkGOlryN-FHYuZdNxZb7FoqDrBjCiF3WCIW)

### Push Yourself Further

**SavingsAccount class** - This class should extend the BankAccount class.

1. The class should have an additional field:
    - [ ] `interestRate` - This value represents the rate at which the account earns interest

1. The constructor should take the following as input:
    - [ ] `accountNumber` - See BankAccount class
    - [ ] `owner` - See `BankAccount` class
    - [ ] `interestRate` - The rate that is used to compute interest

1. Additional methods:
    - [ ] `accrueInterest()` - This method should use the `balance()` to get the current balance and add a new transaction representing a deposit of the appropriate amount.

## Blogs to Show You Know

[Blog Prompts](./../additionalResources/blogPrompts.md)

## Exit Recap, Attendance, and Reminders, 5 mins

* Create Bank Account Assignment
* Create BlogPost_205 Assignment
* Prepare for next by completing all of your pre-class lessons
* Complete the feedback survey

<!-- <iframe id="openedx-zollege" src="https://openedx.zollege.com/feedback" style="width: 100%; height: 500px; border: 0">Browser not compatible.</iframe>
<script src="https://openedx.zollege.com/assets/index.js" type="application/javascript"></script> -->


<!-- TODO Create 3 question exit questions -->

<!-- TODO INSERT Student Feedback From -->

<!-- TODO INSERT *HIDDEN* Instructor Feedback Form -->

<!-- 
cp workspace/resources/classOutlineTemplate.md docs/module-
 -->