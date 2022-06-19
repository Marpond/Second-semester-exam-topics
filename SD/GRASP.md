**General Responsibility Assignment Software Patterns** abbreviated **GRASP**, is a set of nine fundamental principles in object design and responsibility assignment

## 1. Information expert
Assign those responsibilities to the object which the object has the information to fulfill. 

## 2. Creator
The Controller is responsible for creating a new instance of ProgressSegment.

## 3. Controller
The Controller receives and coordinates a system operation beyond the UI layer.

## 4. High cohesion
Each class has functions dedicated to a very specific thing.
Don't talk to strangers.

## 5. Low coupling
Low dependency, low change impact.
We don't want unrelated objects to be connected to each other.

## 6. Pure fabrication
A class specifically designed for a purpose, it has no meaning in the domain model.

## 7. Polymorphism
How to handle related but varying elements based on element type? Which object is responsible for handling those varying elements.

## 8. Indirection
Create an intermediate object between other components or services so that they are not directly coupled.

## 9. Protected variations
Design objects, systems and subsystems so that the variations or instability in these elements do not have an undesirable impact on others. Identify the points of predicted variation and instability, assign responsibilities to create a stable interface around them.