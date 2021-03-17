# Promises

You've already learned and worked with higher order functions like `.map()`, `.filter()` and `.reduce()`. Each of these takes a callback function that does something after the first function does something. Promises do the same thing! They are a function that take a [callback function](https://codeburst.io/javascript-what-the-heck-is-a-callback-aba4da2deced) to do something after something else happens.

Straight from the [MDN Docs](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Asynchronous/Promises) on `Promises {}`:

  > "Essentially, a Promise is an object that represents an intermediate state of an operation — in effect, a promise that a result of some kind will be returned at some point in the future. There is no guarantee of exactly when the operation will complete and the result will be returned, but there is a guarantee that you'll be able to set up code to run only when the operation completes, either to do something else with a successful result, or to gracefully handle a failure case."

We use `Promises {}` to fetch data from somewhere else when we don't know how long it will take because we need to set up the other code before and after the `Promise {}`. We call this asynchronous code. Parts of the code can be built by the computer/executed while other parts are still waiting to receive results. As you've seen before, lines of code are executed sequentially or synchronously in your previous terminal apps. With Promises your code will be able to run asynchronously or out of order. This allows fetching of data to happen without your computer crashing.

There are multiple ways to request information from APIs including [AJAX](https://en.wikipedia.org/wiki/Ajax_%28programming%29) or Asynchronous Javascript and XML (used with jQuery), [isomorphic-fetch](https://www.npmjs.com/package/isomorphic-fetch) which has been a standard in the Node community for the past few years, and recently [Axios](https://www.npmjs.com/package/axios) has become a favorite. Each has their own strengths and weaknesses but each does the job we need. To start out with we'll keep it simple, but as you progress as a developer in your understanding and confidence you will reach to new ways like isomorphic-fetch and Axios which we'll, of course, talk about later. For the next few class days we'll be using the [Fetch API](https://flaviocopes.com/fetch-api/) in your browser!

In the following video we see MPJ using babelify to [polyfill](https://javascript.info/polyfills), which really means that it fills in sections of the code when certain browsers can't read it. To use it you would have to `npm init` your working directory/folder and add [babel and babelify](https://www.npmjs.com/package/babelify) to your projects via `npm install`. This is certainly an option and definitely one you may use sooner rather than later. **But for our next couple of classes** we're going to use [Fetch API](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API) which is now a standard feature in browser JavaScript environments and, as of this writing, is compatible with all the main browsers: Chrome, Firefox, Safari and Opera. Therefore, we can safely use it without having to use polyfills for the moment.

### See It - Promises

<iframe width="782" height="440" src="https://www.youtube.com/embed/2d7s3spWAzo" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

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