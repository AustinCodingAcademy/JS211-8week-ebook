# Closures

<!-- *STARLING QUOTE -Author* -->

## Overview

While not quite tied to OOP, closures are an important concept to begin to understand. If you haven't come across this word in your readings so far, you're doing well, don't worry. **Closure** refers to the scope of a variable, meaning: if it is accessible within a function, outside the function, or to other functions.

In the most basic of terms scope is the area (or context) available for a function to access variables. You've probably heard of the global scope or local scope. You're using global scope when you install npm modules with: `npm install lodash --global`. This means that lodash, *an npm package we'll work with at the end of 211*, would be available to every program on your computer. This isn't needed and we shouldn't do this because we only need it to be available to our program's scope, not our word processor or Chrome. But it works the same for the functions we build. When a function needs a variable it will look for the variable within its own context **first**. If it doesn't find it it will go up a level to its parent's scope. If it doesn't find it there it will go up to its grandparent's scope, and so on until it gets up to the global scope.

Closure is a tricky concept to internalize and many developers don't understand it fully without years of practice. For now, give yourself a break and just try to be aware of what variables are available to a function.

There is no substitute for the MDN Docs on JavaScript when you're learning JavaScript. Dig into [this article](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Closures) and find ways to use closure to your advantage. If you can master closure you can master any programming concept.

- [ ] [MDN Docs - Closures](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Closures)

## See It - Closures

<iframe width="878" height="494" src="https://www.youtube.com/embed/CQqwU2Ixu-U" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Practice It - Closures

- [ ] Go to [this JSFiddle](https://jsfiddle.net/78dg25ax/?utm_source=website&utm_medium=embed&utm_campaign=78dg25ax).
- [ ] Create a new line after line 3.
- [ ] Create variable called name and assign it a different name than Mozilla.
- [ ] Run the Fiddle. ++cmd+enter++ or ++ctrl+enter++.
- [ ] What's different?
- [ ] Now remove it and see what happens.
- [ ] Why?

## Additional Resources

- [ ] [YT, FunFunFunction - Closure](https://youtu.be/CQqwU2Ixu-U)

## Know Your Docs

- [ ] [MDN Docs - Closures](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Closures)

<!-- 

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

-->