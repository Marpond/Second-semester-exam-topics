## Life and death of an object
Objects live in the heap. An object's life entirely depends on the life of references referring to it.
Ways to get rid of an object's reference:
- The reference goes out of scope
```java
void go() {
	Life z = new Life();
}
```
- The reference is assigned to a new object
```java
Life z = new Life();
z = new Life();
```
- The reference is explicitly set to null
```java
Life z = new Life();
z = null;
```

## Objects and encapsulation
Encapsulation is a mechanism of wrapping variables and methods together as a single unit. Variables of a class will be hidden from other classes, and can be accessed only through the methods of their current class.
Encapsulation = Classes with private instance variables with getters and setters.

## Methods
A sequence of instructions with a name. They can have parameters, etc.

## Inheritance
In object-oriented design, **inheritance** is a relationship between a more general class (called the **super class**) and a more specialized class (called the **subclass**). The subclass inherits data and behavior from the superclass.

## References


## Object class
Every class extends the Object class if it is declared without an explicit *extends*.

## Interface
A general and reusable mechanism for processing objects which focuses on the essential operations that an algorithm needs.