## Singleton
When only one instance of the class is needed.
Define a static method of the class the returns the singleton.

## Adapter
Resolves incompatible interfaces, or provides a stable interface to similar components with different interfaces by converting the original interface of a component into another interface, through an intermediate adapter object.

## Strategy
Solves the issue of designing for varying but related algorithms --and also for the ability to change them-- , by defining each algorithm in a separate class with a common interface.

## DAO
Data Access Object Pattern is used to separate low level data accessing API or operations from high level business services. 

**Participants:**
1. DAO Interface
	- Defines the standard operations to be performed on a model object.
2. DAO Class
	- Implements said interface. It's responsible to get data from a data source.
3. Model Object
	- Simple object containing get/set methods to store data retrieved using the DAO Class.