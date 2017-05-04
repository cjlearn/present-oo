# Class-based Object-oriented Programming

There are at least two OOP models in common use, _class-based_
OOP (as used in Java and C++) and _prototypal_ OOP (as used in
Javascript). Some languages include features from both models.
I have heard class-based OOP referred to as classical OOP but
I think that is one of those language accidents you sometimes
hear about.

Class-based OOP is centered around _classes_. A class is a
specification for how an object should be constructed, what
data comprises its state, and what operations can be applied.

Different languages might add additional parts to a class
specification: static methods, for example, or whether a class
can be extended through _interitance_.

The parts of a class common to most languages are _constructors_,
_data members_ and _function members_ or _methods_.

## Constructor

A constructor specifies how to create a new _instance_ of a
class. An instance is what people usually mean when they say
_object_. A constructor is just a function and it might or
might not take parameters. Many languages allow multiple
constructor functions to be defined for one class.

```java
class Food {
  // ...

  // constructor
  Food(String name) {
    // initialize all the data for a new
    // instance of "Food."
  }

  // ...
}

Food bean = new Food("lima");
```

## Data Member

The data members of a class specify what information will comprise
an instance's _state_. These usually look like variable declarations
inside of a class specifiation.

```c++
class vehicle {
private:
  // data members
  int mileage;
  date manufactured;

// ...
};
```

# Function Member
The function members of a class define the operations its instances
can perform.
Typically, a function member operates on an instance's data members.

```java
class Counter {
  // data members
  private int value;
  
  // function members
  public void increment() {
    value = value + 1;
  }
  public void decrement() {
    value = value - 1;
  }
  public int value() {
    return value;
  }
}
```

