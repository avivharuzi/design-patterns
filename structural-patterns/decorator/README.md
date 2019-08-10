# Decorator

Lets you attach new behaviors to objects by placing these objects inside special wrapper objects that contain the behaviors.

## Examples

* [PHP](php)
* [Python](python)
* [TypeScript](typescript)

## How to Implement

1. Make sure your business domain can be rep­re­sent­ed as a pri­ma­ry component with mul­ti­ple option­al lay­ers over it.
2. Fig­ure out what meth­ods are com­mon to both the pri­ma­ry component and the option­al lay­ers. Cre­ate a component inter­face and declare those meth­ods there.
3. Cre­ate a con­crete component class and define the base behavior in it.
4. Cre­ate a base dec­o­ra­tor class. It should have a field for stor­ing a reference to a wrapped object. The field should be declared with the component inter­face type to allow link­ing to con­crete components as well as dec­o­ra­tors. The base dec­o­ra­tor must del­e­gate all work to the wrapped object.
5. Make sure all class­es implement the component interface.
6. Cre­ate con­crete dec­o­ra­tors by extend­ing them from the base dec­o­ra­tor. A con­crete dec­o­ra­tor must exe­cute its behavior before or after the call to the par­ent method (which always del­e­gates to the wrapped object).
7. The client code must be responsible for cre­at­ing dec­o­ra­tors and com­pos­ing them in the way the client needs.

![Decorator](/images/decorator.png)
