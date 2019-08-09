# Prototype

Lets you copy existing objects without making your dependent on their classes.

## Examples

* [PHP](php)
* [Python](python)
* [TypeScript](typescript)

## How to Implement

1. Cre­ate the pro­to­type inter­face and declare the clone method in it. Or just add the method to all class­es of an exist­ing class heir­ar­chy, if you have one.
2. A pro­to­type class must define the alternative constructor that accepts an object of that class as an argument. The constructor must copy the val­ues of all fields defined in the class from the passed object into the newly cre­at­ed instance. If you’re chang­ing a sub­class, you must call the par­ent constructor to let the super­class han­dle the cloning of its private fields.
3. The cloning method usu­al­ly consists of just one line: running a new operator with the pro­to­typ­i­cal ver­sion of the constructor. Note, that every class must explicitly over­ride the cloning method and use its own class name along with the new operator. Oth­er­wise, the cloning method may pro­duce an object of a par­ent class.
4. Option­al­ly, cre­ate a centralized pro­to­type registry to store a cat­a­log of frequently used prototypes.

![Prototype](/images/prototype.png)
