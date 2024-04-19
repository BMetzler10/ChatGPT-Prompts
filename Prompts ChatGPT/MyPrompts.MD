prompt:
What is a class in JavaScript?

In JavaScript, a class is a type of function that serves as a blueprint for creating objects. It encapsulates data for the object and functions to manipulate that data. Classes provide a way to define the structure and behavior of objects in a more organized and reusable manner. They were introduced in ECMAScript 2015 (ES6) to bring object-oriented programming features to JavaScript.

Here's a basic example of a class in JavaScript:
class Rectangle {
  constructor(width, height) {
    this.width = width;
    this.height = height;
  }

  // Method to calculate the area of the rectangle
  calculateArea() {
    return this.width * this.height;
  }
}

// Creating an instance of the Rectangle class
const rect = new Rectangle(5, 10);

// Accessing properties and calling methods
console.log(rect.width); // Output: 5
console.log(rect.height); // Output: 10
console.log(rect.calculateArea()); // Output: 50

In this example:

Rectangle is the name of the class.
constructor is a special method that initializes new objects created from the class. It's automatically called when a new instance of the class is created.
calculateArea is a method defined within the class that calculates the area of the rectangle.
Classes in JavaScript can also have inheritance, where one class can inherit properties and methods from another class. This is achieved using the extends keyword:
class Square extends Rectangle {
  constructor(side) {
    super(side, side); // Call the constructor of the parent class with the same parameters
  }
}

// Creating an instance of the Square class
const square = new Square(5);

// Accessing properties and calling methods
console.log(square.calculateArea()); // Output: 25
In this example, Square is a subclass of Rectangle, and it inherits the calculateArea method from the Rectangle class. It also defines its own constructor, which calls the constructor of the parent class using super.FF