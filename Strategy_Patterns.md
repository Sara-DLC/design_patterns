# Strategy Pattern

The strategy pattern (also known as the policy pattern) is a behavioral software design pattern that enables selecting an algorithm at runtime.

It defines a family of algorithms and encapsulates each one and makes them interchangeable. Strategy lets the algorithm vary independently from the clients that use it. 

`Duck -> quack() & display()`

    Wild Duck -> Is a duck() <-inherited from Duck()

    City Duck -> Is a duck() <-inherited from Duck() but also has a fly() method only on city duck

# Solution

`Duck -> quack() & display() & fly()`

    Behaviors:

    flyBehavior() -> simpleFlying() & jetFlying()
    displayBehavior() -> displayGraphics() & displayText()
    quackBehavior() -> simpleQuack() & noQuack()

    Clients:

    Duck -> quack() & display() & fly()

Need to extract logic for behaviors such as display(), fly(), quack() and now no need for subclasses. 


# Code Example (JS)

    Function Duck (flyBehavior=None, displayBehavior=None, quackBehavior ) {
        this.flyBehavior = flyBehavior;
        this.displayBehavior = displayBehavior;
        this.quackBehavior = quackBehavior;
    }

    const cityDuck = new Duck ("jet", "text", "quack")



