# S.O.L.I.D Principle

## What is the S.O.L.I.D Priciple

SOLID is an ancronym for five principle that help software developers design maintainable and extendable classes 

## Single Responsibility

>Ever class is responsible for one thing and one thing only.

It means that the code has only one readin to change. If you chage and make a class responsible for two things and you changed anything, the risk would be high that you break the second behavior. 



## Open-Closed

>You should be able to extend a class behavior without modifying it.

Your classes should be open for extension but closed for modification. Usually this is achieved with inheritance. 


```
// Example Class 1
Class parentClassCar {
    constructor(a , b) {
        this a = a;
        this b = b
    }

    brake() {
      console.log('Slow Down the Car')
    }
}


// example Class #2

Class childClassCar extends parentClassCar {
     constructor(a , b) {
        this a = a;
        this b = b
    }

    slowDownAndTurnOnLightBreak() {
        super.break();
        console.log('Turn On The Break Lights For the Car')
    }
}
```

In the example above we see how the childClassCar extends the parent class and adds onto the break class that will use the parents class to slow down the car and 

## Liskov Substiution

> Derived class must be substitutable for their base classes 

Assume we have a class B which is a subclass of A. If you program works with an object a of class A then you can replace that object b of class b without changing the behavior of the program.

How about an example? 

```
class Car {
    constructor() {}

    drive() {
        console.log("I am moving forward")
    }
}

class Tesla extends Car {
    constructor() {}

    drive() {
        super.drive()

        console.log("I am moving forward by AI");
    }
}

// This 
function driveToNewCar(car){
    console.log(this.car.drive, "to New York! Hopefully some guy will tell me Hey watch it! Im walking herrrrr!!!!")
}

let redCar = Car();

function(redCar);
// Logs : I am moving forward to New York! Hopefully some guy will tell me Hey watch it! Im walking herrrrr!!!!
redCar = Tesla();
function(redCar)
// Logs : I am moving forward by AI to New York! Hopefully some guy will tell me Hey watch it! Im walking herrrrr!!!!

```

In the example above the program will work even if I change the type or instance of the redCar because tesla is a subset of the class Car

## Interface Segregation

> Make fine grained interface that are client specific

Classes should be as specialized as possible. We don't want to make any god cover all classes. 

## Dependency Inversion

> Depend on abstractions, not on concretions

Classes should not depend on concreate details of other classes. Even classes from a high domain level should not handle specific details of components from a lower level. Both low and high level classes should depend on the same abstractions. 