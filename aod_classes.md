# Python Classes

## Example
A **UML Class Diagram (Unified Modeling Language)** is a graphical representation of a class. It shows the **signatures** of a class’s code.

Examine the following diagram for a `Point` class.

| Point |
| :-- |
| x: float|
|y: float|
|`slope(Point): float`|
|`distance_to(Point): float`|

And here is an implementation of this class in Python:
```py
    class Point:
        def __init__(self, x, y):
            self.x = x
            self.y = y

        def slope(self, other_point):
            y_diff = (self.y - other_point.y)
            x_diff = (self.x - other_point.x)
            return y_diff / x_diff

        def distance_to(self, other_point):
            y_diff = (self.y - other_point.y)
            x_diff = (self.x - other_point.x)
            return ((y_diff**2)+(x_diff**2))**0.5

    p1 = Point(0, 0)
    p2 = Point(2, 0)
    m = p2.slope(p1) # 0.0
    d = p1.distance_to(p2) # 2.0


```
1. What is the syntax for defining a class in Python?
    class [ClassName]
2. What is stored in the variable `p1`?
    `p1` is an an object of type Point.
3. What does the `slope()` function do, and how is it used?
    It takes two points as input and uses (y2-y1)/(x2-x1) to find the slope. We have a self argument and a passed-in argument. We pass in a point to compute its slope with a known point.
    `Point.slope(p2, p1)` is equivalent to `p2.slope(p1)`.

## Theory
1. What is a "class"? When and why do we use them?
    A class is a user-defined blueprint or prototype from which objects are created. Classes provide a means of bundling data and functionality together. Creating a new class creates a new type of object, allowing new instances of that type to be made.
2. What are some examples of classes that you've used before?
    All data types (int, string, dictReader, float, list, dictionary, etc.) are classes. For example, `"Hello".lower()` is a method of the string class that converts a passed-in string to lowercase.
3. What is a constructor method?
    A constructor method makes an instance of the class with specified characteristics. An example of a constructor method above is `__init__` above.

## Practice
1. Create a ComplexNumber class with a constructor method.
2. Write methods for addition, subtraction, multiplication, and division with objects of your ComplexNumber class.
3. Write a __str__ method for your class. What is special about this method? What is the difference between your __str__ method and the default one for your class?
    ```py
    class ComplexNumber:
      def __init__(self, a, b):
            self.a = a
            self.b = b

      #inputs: self, other ComplexNumber object
      #output: ComplexNumber object representing the sum of the inputs
      def addition(self, other):
            real = (self.a + other.a)
            imaginary = (self.b + other.b)
            complex_sum = ComplexNumber(real, imaginary)
            
            return(complex_sum)

      def subtraction(self, other):
            return self.addition(ComplexNumber(-other.a, -other.b)) #we add the negative of the other complex number

      def multiplication(self, other):
            real = (self.a * other.a) - (self.b * other.b)
            imaginary = (other.a * self.b) - (self.a * other.b)

      #__str__ converts an object into a human-readable data type
      #a __str__ method comes default, and we are overloading it (replacing it) with our own __str__ method
      def __str__(self):
            if self.b == 0:
                  return str(self.a)
            elif self.b < 0:
                  return f"{self.a} - {abs(self.b)}i"
            else:
                  return f"{self.a} + {self.b}i"

    c1 = ComplexNumber(4, 3)
    c2 = ComplexNumber(5, 3)

    print(c1.addition(c2))
    print(c1.subtraction(c2))
    ```

## Application
Design a DataFrame class to store generic tabular data. Consider how your constructor method should work. What other methods should your class have (or in other words, what other operations do you want to be able to perform on a generic data set)? Implement your class.

