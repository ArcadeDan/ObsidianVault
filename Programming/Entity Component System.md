
Entity Component System #ECS

Components =  Unit of user-types e.g structs
Entity = Set of Components
System = Controller and Holder


ECS Understanding:
    I believe that it is one logical interpretation to understand the idea of the System as an
    abstraction of the Object-Oriented paradigm. If I wanted to be literal, perhaps
    System-Oriented would be a more descriptive meaning.

    (Let us understand that the Entity is analogous to an Object in OO; Objects are instantiated from a class
    as a blueprint that dictates both behavior and control of its own data, whereas Entities are an encapsulation i.e. A set of components.)
    
    The System at every tick runs user-defined behavior(s) that manipulate a group of components data. These implementations have their own run()
    call that is called alongside the System. Entities provide a way of grouping information during run-time to influence behavior for the System.
    For example, if I run the system for behaviors that are never possible due to the system not having information, then the progran panics.
    How can A goblin get decapitated by a mutated rat with golden teeth if the system doesn't know the rat can have teeth, but describes it with having golden teeth?

    It just breaks!


    Entities are the relation of data and behavior. if behaviors rely on data that doesn't exist at run-time internally, then it ceases to function. 
    I describe it as System-Oriented since we are ultimately defining valid behavior to be ran.
