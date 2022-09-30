# 608-mod7

**Chapter 10 Notes:**

Introduction: 
- Object Based Programming: You primarily create and use objects of existing classes. 
- Classes are new data types. 
- Can create dozens of classes for different applications. 
- Polumorphism enables you to conveniently program "in the general" rather than "in the specific". 

Custom Class Account:
- A constructor expression builds and initializes an object of the class, similar to the way a house is constructed from a blueprint then painted with the buyer's preferred colors. 
- Each new class you create becomes a new data type that can be used to create objects. This is one reason why Python is said to be an extensible language. 

Account Class Definition: 
- A class definition begins with the keyword class followed by the class's name and a colon. This line is the class header. 

Composition: Object References as Members of Classes: 
- Embedding references to objects of other types is a form of software reusability known as composition and is sometimes reffered to as the "has a" relationship. 
- A class's _init_ method is called by a constructor expression to initialize a new object of the class. 

Controlling Access to Attributes: 
- A class's client code is any code that uses objects of the class. 
- Most object-oriented programming languages enable you to encapsulate an object's data from the client code. --> Such data in these languages is said to be private data. 

Properties for Data Access: 
- Properties provide the convenience of data attributes for getting and modifying an object's data. 
- Properties are implemented as methods, so they may contain additional logic, such as specifying the format in which to return a data attribute's value or validating a new value before using it to modify a data attribute. 
- You can also modify these properties. 
- Assigning a value that isn't allowed results in a ValueError. 
- The @property decorator preceds the property's getter method, which recieves only a self parameter. 
- @property_name.setter precedes the properties setter method. Recieves two parameters - self and a parameter representing the value being assigned to the property. 
- A read-write property has both a getter and a setter. 
- A read-only property has only a getter. 
- _repr_ returns the "official" string representation of the object. 
- eval recieves the preceding string as an argument and use it to create and initialize a Time object containing values specified in the string. 
- unary * operator to unpack the time_tuple's values, then passes them as an individual arguments. 

Class Time Definition Design Notes:
- Public interface: the set of properties and methods programmers should use to interact with objects of the class. 
- Utility methods are used only inside the class and are not intended to be part of the class's public interface used by client code. 
- A class's interface is the set of public properties and methods programmers should use to interact with objects of the class. 
- A class's utility methods are used only inside the class and are not intended to be used by client code. 

Simulating "Private" Attributes: 
- Class members that may not be accessed outside a class definition are private and visible only within the class that defines them. 

Case Study: Card Shuffling and Dealing Simulation: 
- A class attribute represents class-wide information. It belongs to the class, not to a specific object of that class. 
- _format_ is clalled when an object is formatted as a string. 
- Subplots create a Figure object in which we'll display the images as 52 subplots with 4 rows and 13 columns. 

Inheritance: Base Classes and Subclasses:
- A base class is a relative term and is vague, whereas subclasses get more specific. 
- Class hierarchy is also called an inheritance hierarchy. 
- With single inheritance a class is derived from one base class. 
- With multiple inheritance a subclass inherits from two or more base classes. 
- A base-class exists in a hierarchical relationship with its subclasses. 
- In this section's shape class hierarchy, TwoDimensionalShape is a subclass of Shape and a base class of circle, square, and triangle. 

Building an Inheritance Hierarchy; Introducing Polymorphism: 
- 




