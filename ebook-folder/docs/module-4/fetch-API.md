# The Fetch API

Now to what we'll really be using in class...`fetch()`.

Fetch is actually REALLY, VERY EXTREMELY easy to use! As you can see in the following video: `fetch()` takes a URL to request data from then its response, usually shortened as res, is turned into Javascript Object Notation, JSON, with the method: `.json()` like so: `res.json()`. then, the now [JSON](https://www.w3schools.com/js/js_json_intro.asp) formatted response is passed to a callback function as a named argument like post and the callback function does something with it. In the case we see in the video it's logged to the console. In the Practice It section ahead you'll get it into the DOM.

## See It - Fetch API

* [YT, Paul Halliday - How to Use Fetch with JavaScript](https://youtu.be/tVQgfKqbX3M)

## Practice It - Fetch

- [ ] Create a new repo in your GitHub called `FetchPractice-1`
- [ ] Clone it into your `devFolder`
- [ ] Inside the new repo create two files: `index.html` and `main.js`
- [ ] Copy/paste the code below into the respective files
- [ ] While working throughout this fetch practice make sure you reference and read in its entirety the [MDN Docs on fetch()](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API)
- [ ] Using the documents at [jsonplaceholder](https://jsonplaceholder.typicode.com/), for each of the `buttons` listed in the `index.html` file:
- [ ] Create a function that fetches the data the button should fetch
- [ ] Push the response into an array: `arrayOfPosts`
- [ ] Display them as an `li` in a `ul`
- [ ] Using the docs on [jsonplaceholder](https://jsonplaceholder.typicode.com/), post a new post to the database.
- [ ] Using the docs, put (edit) a post.
- [ ] Get this all finished before coming into class.
- [ ] If you don't you will be very unprepared

=== "index.html"

    ```html
    <!DOCTYPE html>
    <html lang="en">
    <head>
      <meta charset="UTF-8">
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      <meta http-equiv="X-UA-Compatible" content="ie=edge">
      <title>Fetch Practice</title>
    </head>
    <body>

      <!-- When you click this button, the posts collected in the fetch request will be logged in the console in your devtools tray -->
      <button onclick="consolePosts()">Console Posts</button>

      <!-- When you click this button the posts collected from the fetch request will be displayed below in the ul element with the id='all-posts' -->
      <button onclick="displayPost()">Display Posts</button>
      <button onclick="">Fetch 5 Posts</button>
      <button onclick="">Fetch Comments</button>
      <button onclick="">Fetch Users</button>
      <div>
        <h3>All Posts</h3>
        <ul id='all-posts'></ul>
      </div>
      <script src="./main.js"></script>
    </body>
    </html>
    ```

=== "main.js"

    ```javascript
    let arrayOfPosts;

    // This function waits for the web page to be loaded, when it does it will run the code inside of it which happens to be getPosts()
    window.onload = function() {
      getPosts()

    }

    // This function is going to make a fetch request to the URL inside its parameter brackets (). Then it will turn the response (data it's getting back), saved here as res. The res.json will not be saved as posts and saved into the variable, arrayOfPosts
    const getPosts = () => {
      fetch('http://jsonplaceholder.typicode.com/posts')
        .then(res => res.json())
        .then(posts => arrayOfPosts = posts)
    }

    // This function logs the results in your browser's console
    const consolePosts = () => {
      console.log(arrayOfPosts)
    }

    // this function creates elements inside the all-posts ul, then appends text inside it with the posts that were returned in the request.
    const displayPost = () => {
      const allPosts = document.getElementById('all-posts')
      arrayOfPosts.map((post, index) => {
        const li = document.createElement('li')
        const text = document.createTextNode(`#${index}, Title: ${post.title}:  ${post.body}, by user: ${post.userId}`)
        li.appendChild(text)
        allPosts.append(li)
      })
    }

    /* 
    Your job now is to follow the functions above and use them as templates 
     to build the functionality the buttons in the index.html file already 
     have laid out in it. This way you can learn how to build fetch requests 
     and work with other APIs and become a real developer!! 
    */
    ```

## Know Your Docs

* [MDN Docs - Web APIs](https://developer.mozilla.org/en/docs/Web/API)
* [MDN Docs - Fetch](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API)

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