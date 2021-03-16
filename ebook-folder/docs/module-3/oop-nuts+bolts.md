# Nuts & Bolts of OOP

## Example 2

Review the material below and practice ALL of the code snippets to make sure you start to see how objects can use other objects as part of their properties and how we can assign new properties to objects as needed. We'll use the this keyword in functions when we want to assign something to this instance of the object.

Object-oriented programming consists of classes and objects.

Classes are like templates. For example, a template of a human may include: name, height, weight, date of birth, etc.
A class is named with a capital letter.
We use a constructor function to define the properties of class.
We use the this keyword to set individual properties. See the example below:

```javascript
  class Human {
    constructor(name, height, weight, dob){
      this.name = name;
      this.height = height;
      this.weight = weight;
      this.dob = dob;
    }
  }
```

  > We can assign methods to classes using the following syntax:

```javascript
  class Human {
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
```

We can **instantiate** or copy an object from a `class` just as a chef can use a recipe to replicate the same entree.

  > To **instantiate** means to create an instance of. Below we create an instance of the `class Human`, which will be an object named 'chris':

```javascript
  const chris = new Human("Chris", "6 ft 2 in", "230 lbs", "July 24th, 1988");
```

## See It - Class Keyword

<iframe width="655" height="368" src="https://www.youtube.com/embed/Tllw4EPhLiQ" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Practice It

### Part 1: Using a Class

In a Repl.it, copy the code examples below and follow along with the objectives.

- [ ] Experiment with accessing the properties and methods below using dot-notation(`.`):

  ```javascript
    class Human {
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

    const chris = new Human("Chris", "6 ft 2 in", "230 lbs", "July 24th, 1988");

    console.log(chris.name);
    console.log(chris.dob);
    console.log('replace me to get weight ');
    chris.greeting();
  ```

- [ ] Instantiate a new Human with your name, height, weight, and DoB. Work on accessing the properties and call the greeting method.

  ```javascript
    class Human {
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
  ```

- [ ] Experiment further with the example below:

  ```javascript
    class Square {
      constructor(sideLength) {
        this.sideLength = sideLength;
      }
      calcArea() {
        return this.sideLength * this.sideLength;
      }
    }

    const square1 = new Square(10);

    console.log(square1.sideLength);
    square1.calcArea();
  ```

### Part 2: Create Your Own Classes

Build these in a Repl.it. Seriously, this will prepare you for the BankAccount project.

- [ ] Create a Rectangle class. Instantiate at least one object that takes two arguments in its constructor and calculate its area.
- [ ] Create a Triangle class. Instantiate at least one object and calculate its area.



## Additional Resources

- [ ] [YT, FunFunFunction - Class Keyword](https://youtu.be/Tllw4EPhLiQ)

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

height/width = 1.777 ---- width="655" height="368"

-->