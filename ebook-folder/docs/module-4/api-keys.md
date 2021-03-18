# API Documentation and API Keys

*Most of the important things in the world have been accomplished by people who have kept on trying when there seemed to be no hope at all. —Dale Carnegie*

As mentioned in the last pre-homework, some APIs require the setup of an account with an API key attached to it. This process is pretty standard and common. You should get familiar with this process and understand it before your next assignment which is to build a small app that uses an API that requires an API key, or permission and proof of permission.

## APIs - Setting up an Account

The process for each API is usually the same: agree to the terms, create an account, verify the account through email then get the key through email. Each may have it's own quirks but it generally looks like that.

For tonight's homework we're going to get an API key from the [NYC MTA](http://bustime.mta.info/wiki/Developers/Index). Go ahead and click the link to get an API key and fill out the Google Form.

### See It - API Keys

<iframe width="891" height="501" src="https://www.youtube.com/embed/1yFggyk--Zo" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Keeping Your API key a Secret with a `.env` file

Obviously you don't want your API key to be used by other people. Therefore you shouldn't commit it to your repo on GitHub. To make sure you can still use your API keys while keeping them secret, make sure you understand how to use the node package: [dotenv](https://medium.com/@thejasonfile/using-dotenv-package-to-create-environment-variables-33da4ac4ea8f) to keep up with your private api keys. We'll also go deeper into this in class.

### Practice It

Use the previous **See it - API Keys** video to request data just in your browser for now.

Here's the Chrome Extension she mentions in the video: [JSON-Formatter](https://chrome.google.com/webstore/detail/json-formatter/bcjindcccaagfpapjjmafapmmgkkhgoa?hl=en) from Chrome

## Reading API Documentation

Documentation is key!! To work with an API you **must, must, must read the documentation**. Someone else, another person, has built the program you want to interface with and has given you, in English, how to interact with it and use the data. Quite honestly, if developers build an API and fail to deliver the documentation for it, the API will not get used and fall out of favor and fashion. As an example, even this [funny, strange, and offensive API](https://www.foaas.com/) has very clear documentation. As you can see, changing the path `/version` "Will return content with the current FOAAS version number." You can practice the request in your browser, then bring it into a `fetch()` request.

### See it - REST API Concepts

[YT, WebConcepts - REST API Concepts and Examples](https://youtu.be/7YcW25PHnAA)

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