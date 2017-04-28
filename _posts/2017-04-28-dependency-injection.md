---
layout: post
title: Dependency Injection
pulished: true
---

### What is it?
Dependency Injection is a technique where an object provides the dependencies of another object. The dependency is an object that can then be used. The injection is the passing of a dependency to an object that is dependent upon it.

The goal of Dependency Injection is to decouple objects such that no client code needs to be changed if an object it depends on needs to be changed to something different in the future. Dependency Injection is a form of Inversion of Control where high level code can receive low level code from which it can call down to.

For more information check out the <a href="https://en.wikipedia.org/wiki/Dependency_injection">Wikipedia page for Dependency Injection</a>.

### Implementation
There are a number of ways to implement Dependency Injection. I'll cover 3 simple methods of doing so if your using an object-oriented langauge. Each of the three methods revolve around the idea of setting each dependency as an instance variable on an object so it can be accessed from almost anywhere.

* Constructor Injection - dependencies are provided through class constructor
* Setter Injection - client exposes a property (setter method) that the injector can use to inject the dependency
* Interface Injection - dependency gives an injector method that will inject the dependency into any client given to it. The client needs to implement an interface that exposes a property (setter method) that accepts a parameter for the dependency.

Here is a simple example of a method without Dependency Injection:
```
public theClass() {
    this.theObject = objFactory.GetNewObject();
}
```

Here is another example, but this time with Dependency Injection:
```
public theClass(Factory aFactory) {
    this.factory1 = aFactory;
    // after this you can now call this.factory1.GetNewObject() anywhere in the class
}
```

### Dependency Injection Container
A dependency Injection Container, aka Inversion of Control Container, is used to handle the set up of necessary dependencies so you don't have to duplicate instantiation code throughout the application. This container is where you'd want to write it.

Instead of this:
```
Service service1 = new Service(new GreatService(), new BestService(), new Configuration());
```

You could use a Dependency Injection Container and write:
```
Service service1 = DIC.Resolve<IService>();
// The instantiation of Service is delegated to the DIC container which deals with creating the object. 
// So now the DIC container is the single place for handling dependencies.
```

### Conclusion
Dependency Injection is a great design pattern that can help to improve readability and maintainability of your code. It can consume a lot of time upfront in order to plan it out, but in the long run it can save a ton of development time and prevent headaches.
