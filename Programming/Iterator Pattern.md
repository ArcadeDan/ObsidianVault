#Pattern 

Clients must process one by one in a warehouse, but not allowed to enter the warehouse (information hiding)

clerks can process an item for a client (iterator)



* An **aggregate object** allows access of objects without the underlying internal structure, allows for traversal of different methods


Iterator:
	defines an interface for accessing and traversing elements

ConcreteIterator
	implements the iterator interfaces
	keeps track of current position in traversal of aggregate

Aggregate
	defines an interface for creating an Iterator object

ConcreteAggregate
	implements the Iterator creation interface
	to return an instance of the proper ConcreteIterator



##  Solution
