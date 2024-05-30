# Objects, JSON, .bind() & this

*Success means doing the best we can with what we have. Success is the doing, not the getting; in the trying, not the triumph. Success is a personal standard, reaching for the highest that is in us, becoming all that we can be. —Zig Ziglar*

## JSON/Objects & Arrays pt. 2

Objects and arrays are both used to store data in different ways.

Later in this course we'll be making fetch requests to web APIs that are connected to a database. These fetch requests will return data we can use to render on our websites. Most data that is returned from the database will be a complex data structure of nested objects and arrays. When working with JavaScript and a front-end web app we'll be dealing with data in the format of [JSON](https://json.org/){:target="_blank"} or [JavaScript Object Notation](https://en.wikipedia.org/wiki/JSON){:target="_blank"}. Below is a common looking JSON Object you might receive from a fetch request.

```json
  {
    "firstName": "John",
    "lastName": "Smith",
    "isAlive": true,
    "age": 27,
    "address": {
      "streetAddress": "21 2nd Street",
      "city": "New York",
      "state": "NY",
      "postalCode": "10021-3100"
    },
    "phoneNumbers": [
      {
        "type": "home",
        "number": "212 555-1234"
      },
      {
        "type": "office",
        "number": "646 555-4567"
      }
    ],
    "children": [],
    "spouse": null
  }

  // source: https://en.wikipedia.org/wiki/JSON
```

  > Notice the `""` around the **keys**. This is a major distinction in syntax between JSON and JavaScript.

Accessing data in complex data structures is one of the most important tasks in front-end development and the first step in receiving data from the backend and displaying it to the user. Take a look at the JSON object in this [example](https://www.sitepoint.com/database-json-file/){:target="_blank"} link and see if you know how to access each object, its `product_name` and `unit_cost`.

```json
  [{
    "_id": {
      "$oid": "5968dd23fc13ae04d9000001"
    },
    "product_name": "sildenafil citrate",
    "supplier": "Wisozk Inc",
    "quantity": 261,
    "unit_cost": "$10.47"
  }, {
    "_id": {
      "$oid": "5968dd23fc13ae04d9000002"
    },
    "product_name": "Mountain Juniperus ashei",
    "supplier": "Keebler-Hilpert",
    "quantity": 292,
    "unit_cost": "$8.74"
  }, {
    "_id": {
      "$oid": "5968dd23fc13ae04d9000003"
    },
    "product_name": "Dextromathorphan HBr",
    "supplier": "Schmitt-Weissnat",
    "quantity": 211,
    "unit_cost": "$20.53"
  }]
```

Try it. Store it in a variable in a repl.it and see if you can log the values to the console.

### Accessing Large Objects

When accessing complex data structures, keep in mind the structure that you are accessing and what the return will be.

```javascript
  const userObj = {
      likes: [
          {id: 1, name: 'basketball'},
          {id: 2, name: 'football'},
          {id: 3, name: 'cooking'},
      ],
      firstName: 'Tom',
      lastName: 'Riddle',
      posts: {
          1/4/2018: 'today I ate pizza',
          2/14/2018: 'happy valentines day',
          2/15/2018: 'its 5 o’clock somewhere'
      }
  }
```

For example, if you received the user object above from the database, and you wanted to display the user's most recent like:

First you would determine what type of data structure userObj is. In this case, it’s an object. To access a value, I would need the key name. For this problem, it’s `likes`. So the first step is:

  > `userObj["likes"][0]`, which would return `{id: 1, name: 'basketball'}`

The second step returns an object, which still isn’t a very consumable piece of information for the user, ideally we would just show a string. So to access the name value in this object, an additional locator is needed for the `name` key:

  > `userObj['likes'][0]['name']`, which would return `'basketball'`

Sometimes, you need to display all of the information in an object by looping over every key. However, objects do not have access to the concise and convenient loops that arrays have access to.

The method `Object.keys() `will return an array of object keys. Then you can use that returned array to loop through each of the object keys. And since the values in an object can be accessed by the key names, each time you loop through a key name, you can also access the value.

For example, if I wanted to show the end user all of the posts from the `userObj`, first I would access the `post` object. `userObj[‘posts’]` would return an object:

```javascript
  {
    1/4/2018: 'today I ate pizza',
    2/14/2018: 'happy valentines day',
    2/15/2018: 'its 5 o’clock somewhere'
  }
```

`Object.keys(userObj["posts"])` returns an array of the keys `[ "1/4/2018","2/14/2018", "2/15/2018"]` Remember, objects are made of key-value pairs! If we use the [.keys()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/keys){:target="_blank"} object prototype method we will get the keys of all the key-value pairs in the objects. If we use the object prototype method [.entries()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/entries){:target="_blank"}, we'll get the values of all the key-value pairs in the object.

A forEach loop is the best option to use here. It has decreased scope, simplified syntax, and doesn’t have the possibility of an infinite loop.

```javascript

  Object.keys(userObj[‘posts’]).forEach((key) => {
      console.log(key)
  });

  // I am using key as the variable name because I want to be as descriptive as possible.
  // This would print out in the console:

  // 1/4/2018
  // 2/14/2018
  // 2/15/2018
```

Because I have both the key and the object, I can also gain access to the value associated:

```javascript
  Object.keys(userObj["posts"]).forEach((key) => {
      console.log(`The key is ${key}, and the post is: ${userObj["posts"][key]}`)
  })

  // This would print out in the console =>

  // The key is 1/4/2018, and the post is: today I ate pizza
  // The key is 2/14/2018, and the post is: happy valentines day
  // The key is 2/15/2018, and the post is: its 5 o’clock somewhere
```

**Before** you finish up here, make sure to watch the videos in the [Additional Resources](#AdditionalResources)

## .bind() & this

from [MDN, The `.bind()` method](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function/bind){:target="_blank"}

  > creates a new function that, when called, has its `this` keyword set to the provided value, with a given sequence of arguments preceding any provided when the new function is called.

from [MDN, `this`:](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/this){:target="_blank"}

  > ES5 introduced the `bind()` method to set the value of a function's `this` regardless of how it's called, and ES2015 introduced arrow functions which don't provide their own `this` binding (they retain the `this` value of the enclosing **lexical context**).

`this` and `.bind()` are complex ideas. However they are concepts we must accept, understand and use if we want to grow in our programming abilities with JavaScript as our scripting language. Today we'll simply scratch the surface of these two topics in preparation of our next two weeks' subjects: OOP (object-oriented programming) and higher order functions.

We will definitely come back to these two concepts again. For a short summary, think of `this` as referring to this instance of where the function is called. Inside the object it refers to this instance. Think of  `.bind()` as forcing or binding a variable to a specific function regardless of instance.

For now, think of JavaScript as a beautiful mix of OOP and functional language, and watch the following video by MPJ.

<iframe width="655" height="368" src="https://www.youtube.com/embed/GhbhD1HR5vk" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

* [Video FunFunFunction - bind & this](https://youtu.be/GhbhD1HR5vk){:target="_blank"}

## Practice It

Copy/paste the following code into a Repl.it and run it. Then follow the instructions in the comments at the bottom.

```javascript
  const person = {
    firstName: "Kevin",
    lastName: "Colten",
    age: 29,
    eyeColor: "brown",
    talk: function () {
      console.log("Hello!");
    }
  };

  console.log(person.firstName);

  console.log(person["lastName"]);

  person.talk();

  // practice by creating a new object called dog
  // then follow the video with MPJ to recreate the scenario for making the dog bark
```

## Additional Resources

* [Video Steve Griffith - Nested Loops with Arrays & Objects](https://youtu.be/AqgVLYpBWG8){:target="_blank"}
* [Video Hitesh Choudary - Objects in JavaScript](https://youtu.be/-P04pE6zRNE){:target="_blank"}

## Know Your Docs

* [MDN Docs - Working with Objects](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Working_with_Objects){:target="_blank"}

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

=== "Javascript"

    ```javascript
    ```

=== "Python"

  ```python
  ```

cp workspace/resources/templateFile.md docs/module-

-->