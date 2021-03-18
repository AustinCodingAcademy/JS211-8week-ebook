# Immutability

<!-- *STARLING QUOTE -Author* -->

It may sound silly at first but most of the time we do not want things to change in our app's system. In the database? Yes. But that's a different subject for another time. This is something we covered earlier when we introduced array methods like `.slice()`, `.push()` and so on. Each of these mutates the original array. But this isn't necessarily the way we want to do things. Instead we want to return new arrays without mutating the original.

Unfortunately, JS doesn't yet have immutable data structure like Clojure and some other more sophisticated languages. In fact, the reason we have `const` now is that `var` is completely mutable in all scopes. `let` and `const` restrain the scope of their variables, but with const you will get warnings if you change the value, hence `const`ant.

So, moving forward, if you plan for something to change, like a for loop, it should be labeled a `let` variable. And if you plan for it to stay the same, like a function, it should be a `const`. That's the rule!

To make up for JavaScript's lack of truly immutable data structures like immutable objects and arrays, there are a couple of libraries we can use. The most common is [immutable.js](https://github.com/immutable-js/immutable-js).

This article does a really good job at explaining [immutability](https://www.sitepoint.com/immutability-javascript/).

## See Immutable Data Structures

<iframe width="655" height="368" src="https://www.youtube.com/embed/Wo0qiGPSV-s" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## See It Node Modules

<iframe width="655" height="368"  src="https://www.youtube.com/embed/teDVlOjOCT0" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

### Practice It

Using node modules is pretty easy. In fact, so easy, you will import `lodash` into a project tonight on your own!!

Importing goes just like this:

- [ ] Create a new repo called: "Module Practice"
- [ ] Clone it and `npm init` it.
- [ ] Follow the [NPM instructions](https://www.npmjs.com/package/lodash): `npm i --save lodash`
- [ ] Then, in your js file at the top add: `import _ from 'lodash'`
- [ ] And you're done!! Now you can make a fetch request to some API of your choice and use the methods in lodash to manipulate the data you get back.
- [ ] Try it yourself!!! Go to [lodash documentation](https://lodash.com/docs/4.17.11) and start finding methods you find interesting. See if you can use a few of them.
- [ ] Honestly, this is how you get good.
- [ ] This is how you get jobs.
- [ ] You nerd out about this fun stuff!!

## Know Your Docs

* [MDN Docs - Mutable](https://developer.mozilla.org/en-US/docs/Glossary/Mutable)
* [Lodash Docs](https://lodash.com/docs/4.17.11)


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

### Prompt 3:

=== "Example"
    ```console
      .
    ```

=== "Instructions"
    ```markdown
      .
    ```

=== "Push Yourself Further"
    ```markdown
      .
    ```

cp workspace/resources/templateFile.md docs/module-

height/width = 1.777 ---- width="655" height="368"

-->