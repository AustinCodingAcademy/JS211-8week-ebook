# Data Types in JavaScript

<iframe src="https://player.vimeo.com/video/377406276" width="900" height="600" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe>

## Why Different Data Types?

When we program, we need to hold values and access them later on. Think about typing into a calculator: **7 + 54**.

1. We first type **7** which gets held into a variable,
2. Then we type **+** which gets held into a variable,
3. Then we type **54** which also gets held into a variable,
4. When we type **=** these three variables get passed into the "calculate" function which returns the expected value, 61.

With this very simple program we can learn quite a bit. First, **7** is a Number, **54** is a Number, and **+** and **=** are both functions. This means we're using two different types of data: type Number and type Function.

If we gave our "calculate" function the values **"cat" + 54** it wouldn't be able to calculate a value for us because we gave it two different types of data: type String("cat") and and type Number(54).

All the things you see on your screen and the information you send and receive online comes in the form of different types of data. We call these types of data **data types**.

## How Many Data Types

There are [seven main data types in JavaScript](https://www.w3schools.com/js/js_datatypes.asp) in total. We can divide them into two main categories: **Complex** and **Primitive**.

### The Primitive Types

* **String**, i.e. `"cat"`, `"dog"`, `"700"`, `"Peter woke at 9 a.m."`
* **Number**, i.e. `70`, `43`, `2`, `10000000`, `-1`, `0`
* **Boolean**, i.e. `true` or `false`
* **Undefined**, i.e. `undefined` (literally undefined)

### The Complex Types

* **Function**, i.e. `const add = (num1, num2) => { return num1 + num2` }
* **Object**, i.e. `const vehicle = {color: "red", wheels: 4}`
* **Array**, i.e. `const passengers = ["David", "Julia", "Pete"]`

  > There is also "Not a Number" - `NaN`, which technically isn't a primitive or complex type but we'll talk about it when we need to. It occurs when you try to add "cat" to 54.

Each of the **data types** can hold specific types of values but also come with special built in **methods** we can use to compare and manipulate them. For instance, Number type data can be calculated but String type data can't be calculated. And Array type data can be looped over but Functions types can't. Because of this, we need each type of data for specific reasons and we'll learn about each as we move through this course.