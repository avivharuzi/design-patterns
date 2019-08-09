# Abstract Factory

Lets you pro­duce fam­i­lies of related objects with­out spec­i­fy­ing their con­crete classes.

## Examples

* [PHP](php)
* [Python](python)
* [TypeScript](typescript)

## How to Implement

1. Map out a matrix of dis­tinct prod­uct types ver­sus variants of these products.
2. Declare abstract prod­uct inter­faces for all prod­uct types. Then make all con­crete prod­uct class­es implement these interfaces.
3. Declare the abstract fac­to­ry inter­face with a set of creation meth­ods for all abstract products.
4. Implement a set of con­crete fac­to­ry class­es, one for each prod­uct variant.
5. Cre­ate fac­to­ry initialization code some­where in the app. It should instant­ti­ate one of the con­crete fac­to­ry class­es, depend­ing on the application configuration or the cur­rent environment. Pass this fac­to­ry object to all class­es that construct products.
6. Scan through the code and find all direct calls to prod­uct constructors. Replace them with calls to the appropriate creation method on the fac­to­ry object.

![Abstract Factory](/images/abstract-factory.png)
