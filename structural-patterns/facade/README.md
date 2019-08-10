# Facade

Provides a simplified interface to a library, a framework, or any other complex set of classes.

## Examples

* [PHP](php)
* [Python](python)
* [TypeScript](typescript)

## How to Implement

1. Check whether it’s pos­si­ble to pro­vide a simpler inter­face than what an exist­ing sub­sys­tem already provides. You’re on the right track if this inter­face makes the client code independent from many of the subsystems classes.
2. Declare and implement this inter­face in a new facade class. The facade should redirect the calls from the client code to appropriate objects of the sub­sys­tem. The facade should be responsible for initializing the sub­sys­tem and man­ag­ing its further life cycle unless the client code already does this.
3. To get the full ben­e­fit from the pat­tern, make all the client code com­mu­ni­cate with the sub­sys­tem only via the facade. Now the client code is protected from any changes in the sub­sys­tem code. For exam­ple, when a sub­sys­tem gets upgraded to a new ver­sion, you will only need to mod­i­fy the code in the facade.
4. If the facade becomes too big, con­sid­er extract­ing part of its behavior to a new, refined facade class.

![Facade](/images/facade.png)
