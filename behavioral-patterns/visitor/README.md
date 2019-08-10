# Visitor

Lets you sep­a­rate algorithms from the objects on which they operate.

## Examples

* [PHP](php)
* [Python](python)
* [TypeScript](typescript)

## How to Implement

1. Declare the vis­i­tor inter­face with a set of “vis­it­ing” meth­ods, one per each con­crete element class that exists in the program.
2. Declare the element inter­face. If you’re work­ing with an exist­ing element class hierarchy, add the abstract "acceptance" method to the base class of the hierarchy. This method should accept a vis­i­tor object as an argument.
3. Implement the acceptance meth­ods in all con­crete element class­es. These meth­ods must sim­ply redirect the call to a vis­it­ing method on the incoming vis­i­tor object which match­es the class of the cur­rent element.
4. The element class­es should only work with vis­i­tors via the vis­i­tor inter­face. Vis­i­tors, how­ev­er, must be aware of all con­crete element class­es, referenced as para­me­ter types of the vis­it­ing methods.
5. For each behavior that can’t be implemented inside the element hierarchy, cre­ate a new con­crete vis­i­tor class and implement all of the vis­it­ing methods.
6. The client must cre­ate vis­i­tor objects and pass them into elements via "acceptance" methods.

![Visitor](/images/visitor.png)
