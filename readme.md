---
title: Subclassing and Interfaces
type: Homework
duration: "1:00"
creator:
    name: Charlie Drews
    city: NYC
---

# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Subclassing, Abstract Classes, and Interfaces

> ***Note:*** _You can discuss with classmates, but everyone must submit their own answers_

## Exercise

#### Requirements

- Fork this repo, then add your answers direcly to this **readme.md** file
  - After forking, you can clone, edit the readme in the text editor of your choice, and push back to Github...
  - Or, you can edit the readme [right from the browser](https://help.github.com/articles/editing-files-in-your-repository/)
- After adding your answers, submit a **pull request**

#### Questions

1. What is the difference between *member variables* (also called *instance variables*) and *class variables* (w/ keyword `static`)? Which can be accessed without creating an instance of the class?
Member variables are unique to each object/instance of a class that is instantiated and the values can be all the same or it can all be different. Changing the instance variable of an object will not effect the values of other objects. Class variables however has the same value for all objects created. Changing a class variable value will apply this value for all other objects 

2. Does it make sense to write  *getter* and *setter* methods for a `public` member variable? What about `private` variables?
It doesn't make sense to write "getters" and "setters" methods for a 'public' member variable because everything is already accessible. It is necessary for 'private' member variable because it can only be seen by the class they are in, so in order for the it to access by other classes, they need the "getter" and "setter" methods

3. What are some benefits of making member variables `private`?
There is no access to them besides the people allowed to access private so it protects the variables from people who try to access your code

4. If class A extends class B, which is the super class and which is the sub class? Which would you call parent, and which would you call child?
B is the super class which is the parent, and A is the sub class which is the child

5. What does it mean for a class to *inherit* methods and/or variables from its parent class?
Inheriting methods and/or variables from the parent class allows the child to also have those methods and/or variables to use in addition to its own methods/variables

6. Consider the following code, where class Refrigerator extends class Appliance, and `getTemperature()` is a method in Refrigertor, but NOT in Appliance:
  ```
  Appliance myAppliance = new Refrigerator();
  double temperature = myAppliance.getTemperature();
  ```
  Why will this call to `getTemperature()` cause an error? How will *casting* help solve this issue?
  It causes an error because myAppliance is and object which does not include a getTemperature() method and by casting the object to Refrigertor it will be allowed to access that method

7. In a normal class (also called a *concrete* class), do you need to *implement* all of the methods, or can your simply *declare* some? What about in an `abstract` class?
A concrete class requires all methods to be implemented even when the scope is empty. An abstract class allows you to just declare abstract methods because it expects the first concrete child to implement it

8. What about an `interface`? Can you implement any methods in an interface? Can you declare methods in an interface?
Methods in an interface are abstract so they need to be declare and not implemented

9. Can you create an instance of an `abstract` class? Also, look up the Java keyword `final` and see if you can explain why a class CANNOT be both `abstract` and `final`.
No you cannot create an instance of an abstract class because final cannot be extended while an abstract class requires you to extend it

10. What happens when a method *overrides* another method? If a parent and child class have methods with the same name, when you call that method on an instance of the child class, which implementation of the method will be executed?
'overrides' will override a method and the scope of that method for the child class and when you call that method the child class version will execute it

11. What is the relationship between `List`, `LinkedList`, and `ArrayList`? Why do we call a method *polymorphic* if it takes an input of type `List` rather than an input of type `LinkedList` or `Arraylist`, and why is that useful?
They are all collections of a List by using parameters that take a List. The List makes it possible to send in any of the child classes which can be useful when you need to change code later on and save you time

#### Deliverable

This file, with your answers added

## Additional Resources

Refer to the [Classes lesson](https://github.com/ga-adi-nyc/Course-Materials/tree/master/lessons/java-essentials/classes-lesson), the [Subclassing lesson](https://github.com/ga-adi-nyc/Course-Materials/tree/master/lessons/java-essentials/subclasses-lesson), and the [Interfaces & Abstract Classes lesson](https://github.com/ga-adi-nyc/Course-Materials/tree/master/lessons/java-essentials/interfaces-and-abstract-classes-lesson).

Feel free to google these concepts as well. There are plenty of Java tutorial websites and StackOverflow posts that can help you. But be sure to write up your answers in your own words - copying and pasting some text does NOT help you actually learn!
