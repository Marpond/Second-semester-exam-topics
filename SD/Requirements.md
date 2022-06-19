## Use-case model
Describes the functional requirements, and related non-functional requirements. It is a set of all use cases, a model of the system's functionality and environment.

**Actor**
Something with behavior, such as a person, computer system, organization, etc.

**Scenario (use case instance)**
A sequence of actions and interactions between actors and the system under discussion.

**Use case**
A collection of related success and failure scenarios that describe actors using a system to support a goal.
 
## Use-case formats

**Brief**


**Casual**


**Fully dressed**

## Tests for use-case validity
**The boss test**
If a use case fails the boss test, it means it is not strongly related to achieving results of measurable value.

**The EBP test**
If a use case fails the EBP test, it is not a task performed by one person at one location at one time in response to a business event, which adds measurable business value and leaves the data in a consistent state. It should be a task done in a single session (couple minutes - one hour).

**The size test**
If it is too short it fails. Can't explain it better.

## Use-case diagram and priorities
#### Diagram

**System
- Visualized as a rectangle
- Could be a website, business process, etc

**Actor
- Visualized as a stickman
- Is someone/something that interacts with the system
- Can be primary (left side) or secondary (right side)

**Use case
- Visualized as an oval thingy

**Relationships
- Association
	- Visualized with a normal line
- Include
	- Visualized with a dashed line (from base to included)
	- Dependency between a base and an included use-case
- Extend
	- Visualized with a dashed line (from extended to base)
	- If base is executed the extended *might* be executed
- Inheritance
	- Visualized as a normal line with a triangle (from children to parent)
	- The children share the common behavior of the parent but they add something more

#### Prioritization

## User stories
An informal, general explanation of a software feature written from the perspective of the end user. Who, what and why.

## StartUp use case

## Basic  UML notation
