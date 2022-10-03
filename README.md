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

Building an Inheritance Hierarchy: Introducing Polymorphism: 
- You use inheritance to create new classes from existing ones. 
- When you do not explicitly specify the base class for a new class, Python assumes that the class inherits directly from class object. 
- To inherit from a class, you must first import its definition. 
- Each subclass _init_ must explicitly call its base class's _init_ to initialize the data attributes inherited from the base class. 
- The notation super._init_ uses the built in function super to locate and call the base class's _init_ method, passing the five arguments that initialize the inherited data attributes. 

Duck Typing and Polymorphism: 
- Duck typing is a programming style which does not look at an object's type to determine if it has the right interface; instead, the method or attribute is simply called or used. 

Operator Overloading: 
- The + operator adds numeric values, concatenating lists, concatenating strings and adding a value to every element in a NumPy array. 
- The [] operator for accessing elements in lists, tuples, strings, and arrays. 
- The * operator for multiplying numeric values, repeating a sequence and multiplying every element in a NumPy array by a specific value. 
- Restrictions in overloading: 
  - Precedence of an operator cannot be changed. 
  - Left-to-right or right-to-left grouping of an operator cannot be changed by overloading. 
  - "arity" of an operator cannot be changed. 
  - Cannot create new operators. 
  - The meaning of how an operator works cannot be changed. 

Class Complex Definition:
- The class's _init_ method receives parameters to initialize the real and imaginary data attributes
- The special method _add_ defines how to overload the + operator for use with two Complex objects 
- Special method _iadd_ to define how the += operator adds two Complex objects. 

Exception Class Hierarchy and Custom Exceptions: 
- Exception classes inherit directly or indirectly from base class Base-Exception and are defined in module exceptions. 
- Python has four primary BaseException subclasses
  - SystemExit terminates program execution and when uncaught does not produce a traceback like other exception types.
  - KeyboardInterrupt exceptions occur when the user types the interrupt command on most systems. 
  - GeneratorExit exceptions occur when a generator closes - normally when a generator finishes producing values on when its close method is called explicitly. 
  - Exception is the base class for most common exceptions you'll encounter. 

Named Tuples: 
- The python standard library's collections module also provides named tuples that enable you to reference a tuple's members by name rather than by index number. 
- Function namedtuple creates a subclass of the built-in tuple type. 
- OrderedDict dictionary representation of the objects member names and values. 

A brief into to Python 3.7's New Data Classes:
- Data classes autogenerate method _eq_, which overloads the == operator. 
- All classes inherit class object's default _ne_, method implementation, which returns the opposite of _eq_. 
- Use ClassVar and List from the Python Standard Libarary's typing module to indicate that FACES and SUITS are class variables that refer to lists. 
- Variable annotation refers to a list of strings. 

Unit Testing with Docstrings and doctest:
- doctest module helps you test your code and conveniently retest it after you make modifications. 
- testmod function inspects your functions, methods, and classes docstrings looking for sample Python statements preceded by >>>, each followed on the next line by the given statement's expected output. 

Namespaces and Scopes:
- namespaces associate identifiers with objects and are implemented "under the hood" as dictionaries. 
- local namespaces associate local identifiers. 
- global namespace associate a module's global identifiers. 
- built-in namespace contains assiciates identifiers for Python's built-in functions and types with objects that define those functions and types. 
- nested functions are functions inside other functions or methods. 
- LEGB - local, enclosing, global, built-in 

Intro to Data Science: Time Series and Simple Linear Regression
- Univariate time series have one observation per time
- Multivariate time series have two or more observations per time. 
- Time series analysis, which looks at existing time series data for patterns. 
- Time series forecasting, which uses past data to predict the future. 
- Simple linear regresion, make predictions by finding a linear relationship. 

Chapter 15 Notes: 

Machine Learning: 
- Scikit-Learn conveniently packages the most effective machine-learning algorithms as estimators. 
- Supervised machine learning works with labeled data and unsupervised learning works with unlabeled data. 
- Supervised machine learning goes into two categoreis (classification and regression). 
- Classification is supervised machine learning, which attempts to predict the distinct class to which a sample belongs. 
- Binary classification problem because there are two classes. 
- The confusion matrix shows the correct and incorrect predicted values.
- The correct predictions are shown on the diagonal from top-left to bottom-right, called principal diagonal. 
- classification_report produces a table of classification metrics based on expected and predicted values.  
  - Precision is the total number of correct predictions for a given digit divided by total number of predictions for that digit. 
  - recall is the total number of correct predictions for a given digit divided by thr yoysl number of samples that should have been predicted as that digit. 
  - f1-score is the average of the precision and the recall. 
  - support is the number of samples with a given expected value. 
- A heat map displays values as colors, often with values of higher magnitude displayed as more intense colors. 

Overfitting/Underfitting:
- Underfitting occursr when a model is too simple to make predictions, based on its training data. 
- Overfitting occurs when your model is too complex. 



