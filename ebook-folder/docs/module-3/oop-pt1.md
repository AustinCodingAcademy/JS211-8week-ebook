# Object-Oriented Programming Part One

*I really think a champion is defined not by their wins but by how they can recover when they fall. —Serena Williams*

## Context of OOP

<iframe src="https://player.vimeo.com/video/378322407" width="900" height="600" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe>

As you read over, watch the videos, and play with the practice problems, you might feel there is some redundancy or repetition from previous homework lessons. While this is partly true, it is very important for you to understand these concepts: OOP, functional programming, closure, `class`, constructors, function factories, `bind`, and `this`.

Because these ideas can be complex and take time for one to construct a mental model of, we are covering them a little at a time, building up, gradually, your knowledge and understanding of each of them.

### Read It - OOP

[Object-oriented programming](https://en.wikipedia.org/wiki/Object-oriented_programming) is a fundamental way to program. Most languages use this model, and JavaScript is no different. However, JavaScript is very different in that it also implements functional programming, but we won't get into all of its wonderful characteristics just yet. For now, let's get to what OOP (object-oriented programming) is.

Let's say we want to build a bicycle. Before we go shopping for all of the pieces to build a bike, it would be a good idea to know what we will **need** for the bicycle. We could say we need a frame, wheels, seat, brakes, handlebars, and reflectors. Wonderful! Now we have a shopping list of the parts needed to build a bicycle. But what if now we wanted to build a **new** bicycle for each of our family members and friends? There really isn't a point in re-writing our shopping list for each bike. On top of that, each person might just want a different color of frame, type of wheels or handlebars! We could call these different colors and types values and the basic items we need properties or keys. Do you remember building objects before where we had key-value pairs? I hope so, because it's going to come in handy here. Let's build an object-literal called `myBicycle` :

```javascript
  const myBicycle = {
    frame: "green mountain",
    wheels: "all-terrain",
    seat: "soft leather",
    brakes: "dual-discs",
    handlebars: "straight",
    reflectors: 0
  }
```

Now we have an object that represents the bicycle I want to build, or a list of items to buy. But now Kate wants a blue bicycle with road touring wheels, a synthetic seat and horn shaped handlebars. Let's build a `kateBicycle`:

```javascript
  const kateBicycle = {
    frame: "blue road",
    wheels: "road touring",
    seat: "small synthetic",
    brakes: "dual-discs",
    handlebars: "horned",
    reflectors: 4
  }
```

Do you notice a pattern? Even as I typed this example, I copy/pasted the key-value pairs of `myBicycle` and changed the values for `kateBicycle`. It can get pretty old doing this over and over again (repeating ourselves), especially if we plan to build dozens of bicycles or have thousands of users on our app. The solution to this problem is **object-oriented programming**. We know what our object is going to look like so we build a `class` that can then be called over and over again to have **new** values put inside it. Here are all the parts of a `bicycle` that make up `myBicycle` and `kateBicycle` turned into a `class`:

```javascript
  class Bicycle {
    constructor(frame, wheels, seat, brakes, handlebars, reflectors){
      this.frame = frame;
      this.wheels = wheels;
      this.seat = seat;
      this.brakes = brakes;
      this.handlebars = handlebars;
      this.reflectors = reflectors;
    }
  }
```

Let's take a minute to look at what we just did. First, we figured out the "shopping-list" we need to build a bicycle. Then we put all of the things into something called a `class`. After that we called it something generic like `bicycle` or `user`. Then we added a special method to it called constructor. Inside the ( arguments ) of the `constructor` we passed in all the things NEEDED to make a bicycle. This is the syntax you're going to be using. Just familiarize yourself with it and start memorizing it by typing it out each time to do the practice problems.

Inside the code block of the constructor we have a weird word called `this`. You've seen `this` before but let's cover it again. `this` refers to **this** instance of the `class`. Think about it as a reference to the object as we pass through the `class`.

  > A `class` is a function that returns an object.

Each time we call the `class bicycle` we are going to pass through it declaring certain values to each of the keys. Remember the key-value pairs?? So on this next pass-through with the creation of `myBicycle` we'll assign values to it based on this instance of the pass-through. If we didn't have the this we wouldn't be able to use the `class bicycle` as a template to be used multiple times and still keep the memory of each bicycle we made like `kateBicycle` and `momBicycle`, etc.

If you could talk to the `constructor` it might say something like this: "Hey, I'm a constructor and I require a value for every argument inside my (). If you don't give a value for every argument I will assign undefined to the last arguments. **Meaning, the order of the arguments matters!** And if you want `null` for something you better put `null` in for the value."

From here we can make **new** bicycles using the `class bicycle` object. Take a look below at how we call the `class bicycle` with the keyword new and pass in the values we want to assign it.

```javascript
  const myBicycle = new Bicycle("Green-Mountain", "All-Terrain", "Soft-Leather", "Dual-Discs", "Straight", 0)

  console.log(myBicycle.brakes);  // Dual-Discs
  console.log(myBicycle.seat);  // Soft-Leather
  console.log(myBicycle.reflectors);  // 0
  console.log(myBicycle.frame);  // Green-Mountain
```

Notice the `new` keyword. I've made sure to bold all mentions of **new** throughout this text so you can anticipate a **new** thing being made with the keyword `new`. Above we're creating a variable called `myBicycle` and we're assigning it the value of a `new` object that has the same structure as `class Bicycle` and passing to the constructor the values we want to assign to each of the keys. After calling `new Bicycle` the way we did just above, we would have an object that looks like this:

```javascript
  const myBicycle = {
    frame: "green mountain",
    wheels: "all-terrain",
    seat: "soft leather",
    brakes: "dual-discs",
    handlebars: "straight",
    reflectors: 0
  }
```

Look familiar?

We could do this again for Kate's bicycle:

```javascript
  const kateBicycle = new Bicycle("blue road", "road touring", "small synthetic", "dual-discs", "horned", 4)

  console.log(kateBicycle) // => {frame: "blue road", wheels: "road touring", seat: "small synthetic", brakes: "dual-discs", handlebars: "horned", reflectors: 4 }
```

In short, [object-oriented programming](https://www.codeproject.com/Articles/22769/Introduction-to-Object-Oriented-Programming-Concep) allows us to type less, reuse more, standardize our data structures and pass objects to other objects.

### See It - OOP & Bind-This

#### OOP

In this video we see the big four of OOP and why it's useful. Follow along and notice the use of methods that are created on the objects. We didn't build methods on our `class bicycle` above but we could have!!

Now might be a good time to introduce [D.R.Y.](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself) In programming there are a few principles to follow while you build any program. As a noobie-developer it isn't so important to focus on these principles, so much as it is to be aware of them. This DRY principle simply says, **D**on't **R**epeat **Y**ourself!

In the `class bicycle` example above, we could have created a new object for each bicycle manually but that would be **R**epeating ourselves. Instead, we build one    template and call it each time we need to create a new bicycle object.

<iframe width="655" height="368"  src="https://www.youtube.com/embed/pTB0EiLXUC8" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

#### Bind and This

Pause and play it as you need. Really take the time to look at the code and figure out what each `.bind()` and `this` is doing.

<iframe width="655" height="368" src="https://www.youtube.com/embed/PIkA60I0dKU" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

### Practice It - OOP

#### Practice It Pt. 1

Go to the practice problems in the link and work through **all 18 Object problems**.

> Seriously, do this for yourself. Yeah, you're tired and want to sleep but you came to school to change your career to improve your lifestyle and sleep more and work less. Let's put the time in now! It's called sacrifice. Sacrifice makes us stronger, more flexible, and better humans.

[W3S Tutorial - OOP in JS](https://www.w3resource.com/javascript-exercises/javascript-object-exercises.php)

#### Practice It Pt. 2

- [ ] In the markdown code below, read through to see what you can make of it.
- [ ] Copy the code into Repl.it and run it.
- [ ] Create a new human with your name and information.
- [ ] Now make your human say their name.
- [ ] Next, create a new AcaStudent that extends Human and is learning 'C#'.
- [ ] Add a new method to the AcaStudent class that lets the human say the language they are learning.
- [ ] Make them say what language they're learning.

```javascript
  constructor(name, height, weight, dob){
      this.name = name;
      this.height = height;
      this.weight = weight;
      this.dob = dob;
    }
    greeting() {
      return "Hello " + this.name + "!";
    }
  }

  class AcaStudent extends Human {
    constructor(codingLanguage, name, height, weight, dob){
      super(name, height, weight, dob);
      this.codingLanguage = codingLanguage;
    }
    greeting() {
      console.log("Hello, my name is " + this.name + "! I am learning how to code!");
    }
  }

  const dan = new AcaStudent("JavaScript", "Dan", "5 ft 6 in", "160 lbs", "February 25th, 1986");
  dan.greeting();
  dan.codingLanguage;
```



## Additional Resources

The best two things you can read to get a solid grasp of classes are:

- [ ] [Article, Javascript.info - OOP](https://javascript.info/class)
- [ ] [Article, CodeProject - OOP](https://www.codeproject.com/Articles/22769/Introduction-to-Object-Oriented-Programming-Concep)
- [ ] [YT, FunFunFunction - Bind & this](https://youtu.be/PIkA60I0dKU)
- [ ] [YT, Programming with Mosh - OOP in 7 mins](https://youtu.be/pTB0EiLXUC8)

## Know Your Docs

* [MDN Docs - Class + OOP](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes)

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