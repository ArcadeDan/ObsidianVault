#Pattern 

To build some sort of object, you will need the right tools to create each individual component that is finalized into the object.

A kid (**director**) made **complex** objects (monkey or kitten toy) out of parts produced by other objects (head, body, arm, leg, and tail) that need special care (**decorate**) when being built 

same process of building objects are used to build complex objects



MonkeyBuilder:
* BuildAnimalArm()
* BuildAnimalBody()
* .........
* MonkeyBuilder()

overrides

AnimalBuilder():
* BuildAnimalArm()
* BuildAnimalBody()
* .........

implements

Monkey:
Eat() : abstract method


```java
public class MonkeyBuilder extends Animal Builder {
	public MonkeyBuilder() {
		_animal = new Monkey();
	}
	public void BuildAnimalHead() {
		_animal.Head = "Kitten's Head has been built"
	}
}
```

```java
public class Monkey extends Animal {
	public void Eat() {
		System.out.println("Since I am a Monkey, I like to eat banana!")
	}
}
```

// Alice used Monkey mold to make a monkey

Builder
* specifies an abstract interface for creating parts of a Product object

ConcreteBuilder
* constructs and puts together parts of the product by implementing the builder interface



When to use:
	The algorithm for creating a complex object should be independent of the parts that make up the object and how they're assembled.
	the construction process must allow different representations for the object that is constructed


URL builder

https://        mywebsite    :8080    /companies    ?companyName=xyz
protocol      hostname      port       path pattern   query param
                                      |
     ESSENTIAL                                           OPTIONAL


Can have one object that delegates the instantiation of other objects
AKA

[[Abstract Factory]]


abstract is different families of product objects

Consequences:
* it lets you vary a product's internal representation.
* it isolates code for construction and representation
* it gives you finer control over the construction process

