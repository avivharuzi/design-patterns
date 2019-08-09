# Builder

Lets you construct complex objects step by step. The pat­tern allows you to pro­duce dif­fer­ent types and representation of an object using the same construction code.

## Examples

* [PHP](php)
* [Python](python)
* [TypeScript](typescript)

## How to Implement

1. Make sure that you can clear­ly define the com­mon construction steps for build­ing all avail­able prod­uct representation. Oth­er­wise, you won’t be able to pro­ceed with implementing the pattern.
2. Declare these steps in the base builder interface.
3. Cre­ate a con­crete builder class for each of the prod­uct representation and implement their construction steps.
4. Think about cre­at­ing a direc­tor class. It may encapsulate var­i­ous ways to construct a prod­uct using the same builder object.
5. The client code creates both the builder and the direc­tor objects. Before construction starts, the client must pass a builder object to the direc­tor. Usu­al­ly, the client does this only once, via parameters of the direc­tor’s constructor. The direc­tor uses the builder object in all further construction. There’s an alternative approach, where the builder is passed directly the construction method of the director.
6. The construction result can be obtained direct­ly from the direc­tor only if all products fol­low the same inter­face. Oth­er­wise, the client should fetch the result from the builder.

![Builder](/images/builder.png)
