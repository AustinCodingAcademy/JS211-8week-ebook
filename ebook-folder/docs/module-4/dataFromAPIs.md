# Data From APIs

*Whatever you hold in your mind on a consistent basis is exactly what you will experience in your life. ―Tony Robbins*

## Overview

So far we've learned how to access arrays and objects, extract their values, return them in functions and display them in the DOM. But all of the arrays and objects we've worked with have been [static](https://en.wikipedia.org/wiki/Static_web_page), in that they don't change. We know how many items are in the array and exactly what key-value pairs are in the objects. But to work with a real, production-ready websites we'll need to know how to access data we don't exactly know the structure of or number of items yet, in order to build a [dynamic](https://en.wikipedia.org/wiki/Dynamic_web_page) website! This data will be given to us from a database via an **API**, or [application programming interface](https://en.wikipedia.org/wiki/Application_programming_interface). This is a big fancy word for a computer program that gives us something when we ask for it. The reason it's a programming interface is that it doesn't have a screen for us as humans to see. Instead the computer program takes requests via promises. These promises are simply functions that request information, wait for a response and when they get a response they promise to do something with it afterwards. The reason we have to have it promise to us to do something after the response is that these APIs we'll be requesting information from are remote; they can be hundreds and thousands of miles away from us or our users. Therefore, there will be some time latency between the request and the return of the requested information. Let's get into the details and syntax of this, shall we?

### What's an API?

As we just discussed, an API is a program that takes a request, passes it to the right place and returns to you the thing you requested. There are [hundreds of thousands of APIs available for you to use](https://www.programmableweb.com/apis/directory). Some are [completely free](https://apilist.fun/) and you can request from them now! [Others require you to sign up](https://www.webdesignerdepot.com/2011/07/40-useful-apis-for-web-designers-and-developers/) and get an [API key](http://infomory.com/what-is/what-is-an-api-key/) to have permission to request from the API, while others require you to pay a certain amount of money either per request or per month. So you can get started for free to practice and eventually graduate to integrate someone else's API into an app you build and deploy! Either way, two things are certain, 1) we will be using some free APIs in the next few classes along with a couple that require you to register an account to get an API key, and 2) in the next course term after 211 you will learn how to build your own API to serve your own app and/or share with the world!!

### See It - APIs

<iframe width="655" height="368" src="https://www.youtube.com/embed/s7wmiS2mSXY" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

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