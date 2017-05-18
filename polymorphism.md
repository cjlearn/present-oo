# Inheritance and Polymorphism

## Inheritance

Inheritance is a way for one kind of data to extend another. In
class-based OOP, the language supports this through _sub-classing_.
In most OOP languages, sub-classing often implies _subtyping_
although the distinction is often not made. People use the terms
interchangeably.

In C++:

```c++
class transport {
private:
  float capacity;
  //...
};

class hovercraft : public transport {
private:
  float cushionPressure;
  //...
};
```

## Polymorphism

Polymorphism is the ability for an operation to behave differently
depending on the kind of data on which it is operating.

There are many kinds of polymorphism in software development. The kind
people usually mean when they are talking about OOP is _subtype polymorphism_.
In subtype polymorphism, an operation associated with a class can
behave differently for different subtypes of the class. For example,
in Java:

```java
class Error {
  public String message() {
    return "an error occurred";
  }
}

class OvenTemperatureError extends Error {
  private final float maximumTemp;
  private final float minimumTemp;
  private final float actualTemp;
  //...
  @Override
  public String message() {
    return "oven temprature: " + actualTemp + " is outside safe range: " + minimumTemp + " to " + maximumTemp;
  }
}

Error err = new OvenTemmperatureError(1, 2, 3);
System.out.println(err.message());

```

