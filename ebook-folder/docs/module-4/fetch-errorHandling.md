# Error Handing with Fetch

One of the downsides to using fetch is that it doesn't have proper error handling. This is one of the reasons we use isomorphic-fetch or Axios, which we will get to next class. For now, we're going to have to figure out a way around error handling because you'll be working with a new API tomorrow and you will almost certainly type in the wrong characters. For this you will want error handling to give you a neat and tidy error message to help you debug. *REMEMBER*: **error messages are good!!**

## See It - Handling a Failed HTTP Request

<iframe width="675" height="380" src="https://www.youtube.com/embed/b8DaQrxshu0" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Practice It - Error Handling

**HEY!! You MUST do these practice problems before class!!!**

- [ ] Go back to your [practice problem](./fetch-API.md#practice-it-fetch) from the last homework and add error handling to it.
- [ ] Use this code to get started:

```javascript
  const getPosts = () => {
    fetch('http://jsonplaceholder.typicode.com/posts')
    .then(res => {
      if(!res.ok) {
        throw Error(res.statusText)
      } return res.json()
    })
    .then(posts => arrayOfPosts = posts)
    .catch(err => console.log(`Error,  ${err}`))
  }
```
- [ ] Make sure you add error handling to all your requests in the practice problem.

### Push Yourself Further

- [ ] Can you move your error handling into a separate function as you saw in the video before?
- [ ] Intentionally break your fetch URL to test your error handling. Hint: simply changing one character in the URL will break the fetch and return and error.

## Know Your Docs

* [MDN Docs - Using Fetch](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch)

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