# Composite

Lets you compose objects into tree structures and then work with these structures as if they were individual objects.

## Examples

* [PHP](php)
* [Python](python)
* [TypeScript](typescript)

## How to Implement

1. Make sure that the core model of your app can be rep­re­sent­ed as a tree structure. Try to break it down into sim­ple elements and con­tain­ers. Remember that con­tain­ers must be able to con­tain both sim­ple elements and other containers.
2. Declare the component inter­face with a list of meth­ods that make sense for both sim­ple and complex components.
3. Cre­ate a leaf class to rep­re­sent sim­ple elements. A pro­gram may have mul­ti­ple dif­fer­ent leaf classes.
4. Cre­ate a con­tain­er class to rep­re­sent complex elements. In this class, pro­vide an array field for stor­ing references to sub-elements. The array must be able to store both leaves and con­tain­ers, so make sure it’s declared with the component inter­face type.
5. Final­ly, define the meth­ods for adding and removal of child elements in the container.

![Composite](/images/composite.png)
