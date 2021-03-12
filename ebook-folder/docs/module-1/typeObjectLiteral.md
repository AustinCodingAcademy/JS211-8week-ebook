# Type: Object-Literal

*Don’t compromise yourself. You’re all you’ve got. —Janis Joplin*

## Overview

So far we've been working with primitive data types, like data type: Number, String, and Boolean. These are great for storing small isolated bits of information, but what happens when you want to store related information such as the make, model, color, VIN, drive-train, passenger capacity, fuel type, and CarFax history of every the car in a dealership's parking lot of cars? Or if you want to store the names of all of a user's friends on a social media platform? By using the data type: **Object-Literal** we can group related pieces of data together in a way that makes our database easier to access and manipulate.

  > The name "Object-Literal" is used because all things are objects as you learned in 101 but because this type is syntactically written out the way all objects are under-the-hood we call them "Object-Literals" as in *Literally an Object*.

The first wonderful aspect of [objects](http://eloquentjavascript.net/06_object.html) is that they store data by unique **keys**. Instead of indexes like arrays, objects have **keys** that reference each of the various values stored in the object. The **keys** and values together are called **key-value** pairs.

The simple rule about creating an object's **keys** is that they must be strings, usually words, or even symbols while the **values** can be any data type including Array, Object, Function, Boolean, Number, String, or Byte.

Unlike arrays, when we access values in an object, order does not matter. Let's take this code snippet for example:

```javascript
  const exampleObject = {
      name: "Pete",
      age: 58,
      weight: "150 lbs",
      id: 6089,
      pets: [ 
        {species: 'canine', name: 'Fido'}, 
        {species: 'feline', name: 'Pandora'}
      ],
      employment: {company: 'GE', role: 'engineer', salary: 98000}
  };

  console.log(exampleObject.id) // => 6089
  console.log(exampleObject.weight) // "150 lbs"
```

To get the value of the `id` key of this object we use **dot-notation**, `exampleObject.id`. It would not matter if id was the first key or the three thousandth key, all we would need to access that information/data is the object's variable name, `exampleObject`, and the key name, `id`.

### Creating and Object-Literal

You create an object the same way you declare any other data type:

- [ ] First declare `const`
- [ ] Then name the object, `person`
- [ ] Point it at the object-literal, `=`
- [ ] But instead of square-brackets, use **curly-braces**, `{}`
- [ ] After that separate the **keys** and **values** by colons, `:`
- [ ] Finally, separate **key-value** pairs by commas, `,`
Check it out below:

```javascript
  const person = {
    firstName: "Keith",
    lastName: "Murgic",
    age: 31,
    eyeColor: "brown"
  };
```

`person` is the name of the object, `firstName`, `lastName`, and `eyeColor` are properties or **keys** of `person`, and the corresponding property **values** are `"Keith"`, `"Murgic"`, `31`, and `"brown"`.

### Accessing Object-Literals

You can access information stored in objects in two ways:

```javascript
  // Dot-Notation: objectName.propertyName
  console.log(person.firstName) // => "Keith"

  // Bracket-Notation: objectName["propertyName"]
  console.log(person["firstName"]) // => "Keith"
```

Just like accessing built-in methods, we can use **dot-notation**: `.firstName`. It's important to know that dot notation can only be used when you know the property's key name. This may seem obvious but when we move on to calling the values by some conditional `if` statement we won't know which will be called at any given time, so we have to wrap the value in quotation marks, `"firstName"`, and pass that into the square brackets, `["firstName"]`.

### Writing Data into Objects-Literals

Before pushing forward, it's important to discuss the difference between **read** and *write*, as they relate to computers.

* **Read** means we're accessing data and displaying it somewhere without changing it.
* **Write** means we're changing the data either from scratch or editing it.

Therefore to **write**, or change, or add a new key:value pair in an object, simply access the value and set it equal to the new value as you would do when you declare a new variable or re-point a variable to a new value. See below:

```javascript
  const person = {
    firstName: "Keith",
    lastName: "Murgic",
    age: 31,
    eyeColor: "brown"
  };

  // Before we change the value
  console.log(person.age) // => 31

  // Use either a dot or brackets
  person.age = 50
  person["age"] = 50

  // Now a new value will be returned
  console.log(person.age) // => 50

  // Add a key:value
  person.birthDate = "1/16/1860"

  console.log(person) // => {  firstName: "Keith", lastName: "Murgic", age: 50, eyeColor: "brown", birthDate: "1/16/1860" }

  // also see Object.assign()
```

When building your objects remember, each key must be unique. There can never be two keys that are the same. However, values can be repeated as many times as needed. The following object would not be a properly formatted object because there are two `id` keys:

```javascript
  const anObject = {id: 5, name: ‘Renee’, id: 7}
  // This, however, is a properly formatted object:

  const anObject = {id: 5, name: ‘Renee’, label: 7}
```

  > You might be asking why these objects are on one line but the others we've looked at are on multiple lines. This is only for legibility. **Whitespace** makes code easier to read by the human eye.

### Accessing Nested Data

In real world data, you will see objects with arrays as values and arrays with objects as values, so it’s critical that you can access nested data, or objects within arrays, arrays within objects, arrays within arrays and so forth! Getting good at this is worth the time spent NOW!!

Let's take a look at the object below:

```javascript
  const user = {
      accessCodes: [49303, 493020, 904040, 900404],
      env: ["PA", "NY", "CT" , "VT"],
      filter: {id: 580, branch: "origin"}
  }

  console.log(user.accessCodes)  // => [49303, 493020, 904040, 900404]
  console.log(user.accessCodes[1]) // =>  493020
```

Remember to access data one step at a time. In order to access the **second item** in the `accessCodes` array, first you need to access the `accessCode` property then use the return of that first step (which is an array) to access the second item in the array. This can be accomplished in two ways, bracket or dot notation: `user[‘accessCodes’][1]` or `user.accessCodes[1]`. Both ways return: `493020`.

  > On your own, think about how you would access the `age` property of the second element, `Zuke`, in the friends array below.
  > Copy/paste the object into a Repl.it and experiment.

```javascript
  const user = {
    name: 'Keith',
    friends: [{name: 'Meghan', age: '27'}, {name: 'Zuke', age: '3'}]
  }
```

## The Methods of Object-Literals

The reason you've been able to access all of these built-in methods of strings, arrays, numbers, or Booleans is because they're all created through a **prototype**, which is an object in JavaScript that says: "Hey, when a JavaScript *thing* is created, use this template, or **prototype**, to make it so that all JavaScript *things* operate the same way."

Because of this, all strings have the same methods, and arrays have the same methods as other arrays. We don't need to go into depth with the prototype thing right now but it's important for you to understand that it is an object just like the ones you're studying right now. Just like an HTML element in the Document Object Model (DOM) and just like a CSS rule with its `{}`.

With all of that, take a look at this code snippet:

```javascript
  const person = {
    firstName:"Keith",
    lastName:"Murgic",
    age:31,
    eyeColor:"brown",
    talk: function (friend) {
      console.log("Hello, " + friend)
    }
  };

  console.log(person.talk("Peter"))
```

We see there is a function called `talk` set as a property on this object. Using dot notation we can access this function: `person.talk("Peter")`.

```javascript
  person.talk("Peter")  // => 'Hello, Peter'
```

Any time a function is put on an object like this, it's called a **method**. :) Sound familiar? Yes, all of those **methods** you've used for strings, arrays, and numbers are all functions built on the prototype object/template of those data types just like this .talk() method is built on person. Again, don't worry about understanding the prototype, it's not important right now.

But, speaking of methods, objects come with their own [built-in methods](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Working_with_Objects) and you should look at them for yourself before class!

### Commonly Used Methods of the Object-Literal

The first method we'll cover is [.create()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/create#) because it helps introduce **OOP**, *object-oriented programming*, in a small and helpful way. You see, when we create an app with multiple users, each of our users will have similar data structures like: `name`, `id`, `password`, `email`, `phone`, `address`, and `username`. Each of these pieces of data will become our keys which create a template for all new users of our app to follow. This template structure is the basis of object-oriented programming where we only have to build the template once so we can reuse it over and over again as our app and database grow:

```javascript
  // Create a template object that holds the keys we'll need for each of our users
  const ourUserTemplate = {
    name: "",
    id: Number,
    password: "",
    email: "",
    phone: "",
    address: "",
    username: "",
    location: "",
    printNameOnHomeScreen: function () {
      return `Hello, ${this.name}. It looks like you're in ${this.location}.`;
    }
  }

  // Create a new user with the Object.create() method and the template object passed into it
  const constantineAlfonso = Object.create(ourUserTemplate)

  // Add a value to the name key of the new object & a value to the location key
  constantineAlfonso.name = "Constantine Alfonso"
  constantineAlfonso.location = "Dallas, TX"

  // Log out the value
  console.log(constantineAlfonso.printNameOnHomeScreen())
```

Copy/paste the code above in to your own Repl.it and see what's happening for yourself. Notice the way we use the `.create()` method. Instead of calling it directly on the template object, we call it on the **Object prototype** and pass in the template we'd like it to use. Then we can change values afterwards.

Google each of these and use the code sample above with each one in a Repl.it to see what you can find out on your own.

  * `.entries()`
  * `.assign()`
  * `.keys()`
  * `.is()`

Of course, you should push to learn a new one everyday but these will be good ones to start with.

## Practice it - Object-Literals

- [ ] Go to the CodePen below, click the top-right corner.
- [ ] Fork it to your account.
- [ ] If not already collapsed, drag the HTML and CSS windows to the left so you're only looking at the JS file.
- [ ] Follow the instructions in the JS file.

<iframe height="600" style="width: 100%;" scrolling="no" title="Objects Practice" src="https://codepen.io/kdybvig/embed/wRQxoL?height=265&theme-id=dark&default-tab=js,result" frameborder="no" allowtransparency="true" allowfullscreen="true" loading="lazy">
  See the Pen <a href='https://codepen.io/kdybvig/pen/wRQxoL'>Objects Practice</a> by Keith
  (<a href='https://codepen.io/kdybvig'>@kdybvig</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>


## Know Your Docs

* [MDN Docs - Object Literal](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)

## Additional Resources

- [ ] [Eloquent JS - Object-Literals](http://eloquentjavascript.net/06_object.html)
- [ ] [Video - What Are Objects in JS?](https://youtu.be/4uVwGw317QM)
- [ ] ...



<!-- 

```javascript

``` 

* [MDN Docs - ...]()

- [ ] ...
- [ ] ...


```javascript

``` 

- [ ] ...
- [ ] ...
  * [ ] ...
  * [ ] ...

cp workspace/resources/templateFile.md docs/preCourse/

-->