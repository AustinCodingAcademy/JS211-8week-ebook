# Extending a Class

The **extends** keyword is used in `class` declarations or `class` expressions to create a class as a child of another class. Below the child `class` - `AcaStudent` inherits from the parent `class` Human.

```javascript
  class AcaStudent extends Human {
    constructor(codingLanguage, name, height, weight, dob){
      super(name, height, weight, dob);
      this.codingLanguage = codingLanguage;
    }
    greeting() {
      console.log("Hello, my name is " + this.name + "! I am learning how to code!");
    }
  }
```

We use the `extends` keyword, followed by the parent `class` to attach the properties of `Human` to `AcaStudent` along with the properties of `AcaStudent`.
  
To add an additional property to the AcaStudent class, we put the new property `codingLanguage` with all the properties from the Human class `name`, `height`, `weight`, `dob` in the constructor function.

  > **NOTICE** the `super()` keyword. It's used to pass in the original Human class properties `name`, `height`, `weight`, `dob`. Think of it as going to the supervisor of the extended class. In order to get the benefits of having a supervisor or using another class we have to call the `super()` method inside the constructor. This is required!

  > **NOTICE** that we were able to reassign `greeting()` without using `super()`. This illustrates one of the differences between properties and methods. `greeting()` is a property but is ALSO a method because it is a function. Each of the other attributes: `name`, `height`, `weight`, `dob` and `codingLanguage` are only properties.

Copy the following code into a Repl.it and experiment with the example below:

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

Extend the Human class again with your own properties. Practice adding properties and methods.

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

## Practice It - Extending Classes

Solve these problems on your own before coming to class.

- [ ] [Classes Practice 1](https://repl.it/@reneedudley/ClassPracticeI)
- [ ] [Classes Practice 2](https://repl.it/@reneedudley/ClassPracticeII)