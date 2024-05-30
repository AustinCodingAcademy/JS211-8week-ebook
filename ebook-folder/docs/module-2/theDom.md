# The DOM

*Hardships often prepare ordinary people for an extraordinary destiny. —C.S. Lewis*

## Overview

<iframe src="https://player.vimeo.com/video/382387151" width="900" height="600" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe>

In the next class you'll be creating **GUI**s, or Graphical User Interfaces, for your Pig Latin and Tic Tac Toe apps. So far you've built those apps with a CLI, command line interface. Be sure to brush up on your DOM knowledge and skills.

The DOM (Document Object Model) is a representation of our webpage and our code in the index.html file. Think of it as a go-between. It has a memory of all the elements you've coded as well as all the texts and attributes. These "memories" are called **nodes**. The DOM represents the document as **nodes** and objects in an **upside-down like tree** so that programming languages can connect to the page to do interesting things with the elements. Therefore, each HTML tag you code is a node. Each attribute inside those tags is a node, and each text in between the tags is a node. The DOM, then, has access to all of these nodes and can do neat things with each one using built-in functions or methods. For instance, we can tell the browser to welcome the user to our website with a **pop-up alert** as soon as the page loads by including:

`<body onload="window.alert('Welcome to my home page!');">` inside the opening body tag.

Notice the attribute: `onload`? This is just a built-in method telling the browser to do whatever is after the = when the page loads. Then, we see `window` that is telling the browser to access the window object of the webpage, which is the entire browser window. The . then tells the browser to go inside the `window` node and find something called `alert()` which is a built-in method. The `()` after the `alert` is how we invoke, or call, a method. To give the method/function the stuff we want it to do something with, we pass in an argument in between the `(` and `)`. In this case we're asking the `alert()` method/function to display: 'Welcome to my home page!' It's as simple as that!

Try it yourself. Go to your landing page's index.html file and replace your opening body tag with this line of code:
`<body onload="window.alert('Welcome to my home page!');">`

Then try changing the text: "Welcome to my home page!". Run live-server and see what happens.

Now google different methods you can call on for your `<body/>` element. Play around. Nerd out! This is how you get good!

A very short, non-exhaustive, list of some of the built-in methods on the DOM:

```javascript
  document.getElementById(id)
  document.getElementsByTagName(name)
  document.createElement(name)
  parentNode.appendChild(node)
  element.innerHTML
  element.style.left
  element.setAttribute()
  element.getAttribute()
  element.addEventListener()
  window.content
  window.onload
  window.dump()
  window.scrollTo()
```

  > NOTE: While you've been coding HTML elements you have been blissfully unaware of these methods...until now—but now you know that every element you build comes with these and many more methods baked right in!
  > NOTE 2: A method is actually a little more than a function. It can be invoked like a function but because it is an object on another object, the Document, it is read and stored slightly differently than a function you build. This is a pretty advanced topic, so don't worry too much about it right now. However, if you'd like to learn more, you can read this [forum](https://stackoverflow.com/questions/15285293/method-vs-functions-and-other-questions){:target="_blank"} to get a deeper understanding.

## Know Your Docs

* [MDN Docs - the DOM](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction){:target="_blank"}

## Additional Resources

Before you move on, read the documentation over the DOM. This is a requirement!

These videos are assigned learning but also might be useful during your next project.

* [Video - JS & DOM pt. 1](https://youtu.be/hM9h1wN4rfU){:target="_blank"}
* [Video - HTML/JS TicTacToe](https://youtu.be/gN0fXvWbJSk){:target="_blank"}

## Practice It - Accessing the DOM

- [ ] Open and fork the CodePen below.
- [ ] Click on the button. What happens? Why?
- [ ] Refresh the page. Now try to change the number of rows that are created.
    > Hint: Look at line 16 in the JS file.
- [ ] Be sure to save each time you change the code.
- [ ] Refresh and try to change the number of columns created when you click the button.
- [ ] In the JS file, change the name of the function from "generate_table()" to "make_a_table()"
- [ ] Click the button. What happened? Why?
- [ ] Now look in the HTML file and change the value of "onclick=" from "generate_table()" to "make_a_table()"
- [ ] Run it. Now what happens? Do you see how the two connect?

  > NOTE: In the CodePen, you do not see the actual links between the JS file, CSS file and the HTML file, this is happening behind the scenes. When you start writing JS, you will need to link your JS file in the head tag of your HTML, much the same way you link your CSS files. You will use something like this: `<script src="myscripts.js"></script>`

<iframe height="600" style="width: 100%;" scrolling="no" title="Example: Creating a HTML table dynamically (Sample1.html)" src="https://codepen.io/hipperger/embed/GwEbea?height=265&theme-id=dark&default-tab=js,result" frameborder="no" allowtransparency="true" allowfullscreen="true" loading="lazy">
  See the Pen <a href='https://codepen.io/hipperger/pen/GwEbea'>Example: Creating a HTML table dynamically (Sample1.html)</a> by Clayton Berger
  (<a href='https://codepen.io/hipperger'>@hipperger</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>


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

=== "Javascript"

    ```javascript
    ```

=== "Python"

  ```python
  ```

cp workspace/resources/templateFile.md docs/module-

-->