# Flyweight

Lets you fit more objects into the avail­able amount of RAM by sharing com­mon parts of state between mul­ti­ple objects instead of keep­ing all of the data in each object.

## Examples

* [PHP](php)
* [Python](python)
* [TypeScript](typescript)

## How to Implement

1. Divide fields of a class that will become a fly­weight into two parts:
    * The intrinsic state: the fields that con­tain unchanging data duplicated across many objects.
    * The extrinsic state: the fields that con­tain con­tex­tu­al data unique to each object.
2. Leave the fields that rep­re­sent the intrinsic state in the class, but make sure they’re immutable. They should take their initial val­ues only inside the constructor.
3. Go over meth­ods that use fields of the extrinsic state. For each field used in the method, intro­duce a new para­me­ter and use it instead of the field.
4. Option­al­ly, cre­ate a fac­to­ry class to man­age the pool of fly­weights. It should check for an exist­ing fly­weight before cre­at­ing a new one. Once the fac­to­ry is in place, clients must only request fly­weights through it. They should describe the desired fly­weight by pass­ing its intrinsic state to the factory.
5. The client must store or cal­cu­late val­ues of the extrinsic state (con­text) to be able to call meth­ods of fly­weight objects. For the sake of convenience, the extrinsic state along with the fly­weight-ref­er­enc­ing field may be moved to a sep­a­rate con­text class.

![Flyweight](/images/flyweight.png)
