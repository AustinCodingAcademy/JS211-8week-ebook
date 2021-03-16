# Object-Oriented pt. 2

*Your mind is a powerful thing. When you fill it with positive thoughts, your life will start to change.*

## Overview

We covered the the basics of object-oriented programming through very visual tasks and concrete ideas. Today we're going to go into a little more detail as to why OOP is a common paradigm of programming, including weird words like: `_proto_`, prototype and *prototypal inheritance*. The meaning behind these words isn't absolutely necessary for you to understand at this very moment or this week, but it is important that you know of them because eventually, when you're a mid-level programmer, you will need to understand them to advance to the next stage of your career. Today, let's just get into what each are and what we can do with them now.


### _proto_ vs prototype

We won't spend too much time on this because it's an advanced subject in a very muddy part of JavaScript. If you remember in the pre-work to this class, JavaScript was a language that wasn't planned, designed and built well by a full team. It was, for the most part, hacked together because the internet was becoming a thing and the people at the time didn't understand the full capacity of the internet or how dependent we would be on JavaScript in the future. Because of that, the language has grown organically and, more or less, been patched as developers recognized flaws. Like `null` [returns](https://stackoverflow.com/questions/18808226/why-is-typeof-null-object#18808270) an object!?! This is actually a bug and can't be fixed else it would break the internet! Again, if you look at all these "flaws" as bits of character you can truly fall in love with this language and learn to enjoy these amusing quirks.

For short, remember: `_proto_` **is a property on an object while** `prototype` is a property on a function. These two properties are used by the objects and functions we create so that we have built-in methods that follow each of our objects or functions around. This following around is called delegation. The objects or functions you create don't have to be painstakingly written out to have all the methods we like to use. Remember when we learned the methods of an array like `.split()`, `.pop()`, etc.? The objects and functions we build can delegate the task of acquiring those fun and useful methods through the internal prototype chain. For now, don't worry about knowing all the ins-and-outs of the [prototype chain](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Inheritance_and_the_prototype_chain). Just know 1) that it's there so when you need to access the `_proto_` or `prototype` object you're not bewildered by it and 2) that inheritance should really be called **delegation**.

### Read It - _proto_ vs prototype

- [ ] [Forum, Quora - Prototypal Inheritance](https://www.quora.com/What-is-prototypal-inheritance)
- [ ] [Blog, Medium - Master the JS Interview](https://medium.com/javascript-scene/master-the-javascript-interview-what-s-the-difference-between-class-prototypal-inheritance-e4cd0a7562e9)

### See It - _proto_ vs prototype

<iframe width="655" height="368" src="https://www.youtube.com/embed/DqGwxR_0d1M" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Object.create()

The `.create()` method was added to JavaScript as a way to utilize prototype inheritance more effectively. Remember, prototype inheritance, or delegation, is useful to us not only because we can use the built-in methods but also because it builds faster in the JavaScript engine. All of the fun and useful methods we've grown to love don't have to be built again and again for every single object we make. Instead, we can just reference the methods we need, exactly when we need them through the prototype chain. However, there may be a case like: we want to add a specific method to an object that we will use multiple times throughout the app, just not on *every* object we make. We don't want to add it to the _proto_ or prototype because then it would be added as a method for ALL of the objects in our app and slow down our JS engine making our app less performant[sic]. A work around is `.create()`. `Object.create()` lets us point the new object(s) we create in our app to another object to use as it's prototype. If you're lost, it's okay. This is tough stuff. Luckily you don't have to master this yet but it may help you to start understanding the power of JavaScript's "flaws" and begin to use them to your advantage. Check out the upcoming video to get a better understanding of `.create()`.

### Read It - Creating Objects using the Prototype Chain

- [ ] [Article, CodeBurst - Ways to Create Object in JS](https://codeburst.io/various-ways-to-create-javascript-object-9563c6887a47)
- [ ] [Article, SitePoint - Object Creation Best Practices](https://www.sitepoint.com/javascript-object-creation-patterns-best-practises/)

### See It - Object.Create

<iframe width="655" height="368" src="https://www.youtube.com/embed/CDFN1VatiJA" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Know Your Docs

* [MDN Docs - Object.create()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/create)

## Additional Resources

- [ ] [YT, FunFunFunction - `_proto_` vs `prototype`](https://youtu.be/DqGwxR_0d1M)
- [ ] [YT, FunFunFunction - Object.create()](https://youtu.be/CDFN1VatiJA)

<!-- 

```javascript

```

height/width = 1.777 ---- width="655" height="368"

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