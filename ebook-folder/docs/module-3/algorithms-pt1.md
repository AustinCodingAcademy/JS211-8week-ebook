# Algorithms Part One

*Start by doing what’s necessary; then do what’s possible; and suddenly you are doing the impossible. —Francis of Assisi*

## Why Algorithms?

Algorithms! This is a fancy buzz word I'm sure you hear all the time. It may even strike a little fear or awe in you heart that either you don't know them or that only really smart people can build them.

![social-network-gif](https://66.media.tumblr.com/tumblr_lx3vm93sil1r2l5gfo1_250.gif)

The truth is, an algorithm is simply a recipe. It's a list of tasks given to a computer to do in order, over and over again until the job is complete (the condition is met.) Today we're going to go over the most common and basic algorithms so you can get a feel for what they are before you start building your own and conquering the world!!

## See It - Algorithms

<iframe width="655" height="368" src="https://www.youtube.com/embed/6hfOvs8pY1k" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Sorting Algorithms

Algorithms are actually [numbered and named like species](https://www.geeksforgeeks.org/sorting-algorithms/#algo) of animals. Number one is bubble sort.

### Bubble Sort

[Bubble sort](https://www.geeksforgeeks.org/bubble-sort/) is the least efficient of algorithms in that it takes a longer time to do the task it accomplishes than another algorithm could do. The basis of this algorithm is that it checks to see if the number after another number is greater than the first number. If so, it moves on to the next number. If not, it switches the order and then moves to the next number. But this doesn't change the fact that the first numbers could still be greater than the ones we just switched. Because of this the computer has to loop back through the array and redo the tasks, over and over again until the entire array is in ascending (or descending) order. The video below uses Java to build this algorithm but you can do it for yourself in JavaScript. And you should in a new Repl.it.

<iframe width="655" height="368" src="https://www.youtube.com/embed/6Gv8vg0kcHc" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

### Insertion Sort

With [insertion sort](https://www.geeksforgeeks.org/insertion-sort/), we start with a marker, telling us we have one number in the sort portion of the array. We then move over one number at a time to see if it's greater than the one to its left. If it's less, move it to the left of the number. We repeat this for each number in the unsorted part of the array. When the number is greater than the number it's compared to it stays in place and we grab the next unsorted number.

<iframe width="655" height="368" src="https://www.youtube.com/embed/OGzPmgsI-pQ" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

### Merge Sort

For [merge sort](https://www.geeksforgeeks.org/merge-sort/) and quick sort we'll need to know something about a strange word called: **recursion**. We won't be covering this in class in detail for another week. For now, read this [recursion article](https://medium.com/@zfrisch/understanding-recursion-in-javascript-992e96449e03) and make sure you understand that a function can call itself. In the following algorithms you'll need a function that can call itself if the condition is not met.

  > NOTE: In this video, Rob works backwards to make sure we know how to merge two lists. Then he shows how to separate them before merging again.

<iframe width="655" height="368" src="https://www.youtube.com/embed/Pr2Jf83_kG0" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

### Quick Sort

Like merge, [quick sort](https://www.geeksforgeeks.org/quick-sort/) uses a pivot element as a partition then looks at numbers to the left and right of the partition to see if they need to be moved over or not. Then it repeats the sequence on the left and right sides of the partitions. Then again and again until all the numbers are in order.

BIG NOTE HERE: The woman in the video is [Gayle Laakmann-McDowell](http://www.gayle.com/). She wrote [Cracking the Coding Interview](http://www.crackingthecodinginterview.com/) which is the bible on coding interviews.

<iframe width="655" height="368" src="https://www.youtube.com/embed/SLauY6PpjW4" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<iframe width="655" height="368" src="https://www.youtube.com/embed/ZHVk2blR45Q" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Practice It

### Part 1: First Algorithms

In a Repl.it:

- [ ] Build a bubble sort
- [ ] Build an insertion sort

### Part 2: JS Fundamentals

We're now at a point where we'll be introducing new features and concepts of JavaScript that will then require your full understanding of how to program and code in JavaScript. To make sure you're ready for next class and the rest of 211, work through these [116 problems](https://www.w3resource.com/javascript-exercises/fundamental/index.php).

1. Start with just the evens.
1. Commit to solving 4 per day for the next two weeks.
1. Put each in a new Repl.it so you have a journal and reference of your learning and code.
1. Your future self will thank you so much for this!!

## Know Your Docs

* [Geeks4Geeks - quick sort](https://www.geeksforgeeks.org/quick-sort/)
* [Geeks4Geeks - merge sort](https://www.geeksforgeeks.org/merge-sort/)
* [Geeks4Geeks - bubble sort](https://www.geeksforgeeks.org/bubble-sort/)

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

cp workspace/resources/templateFile.md docs/module-

height/width = 1.777 ---- width="655" height="368"

-->