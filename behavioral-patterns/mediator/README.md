# Mediator

Lets you reduce chaotic dependencies between objects. The pat­tern restricts direct communications between the objects and forces them to col­lab­o­rate only via a mediator object.

## Examples

* [PHP](php)
* [Python](python)
* [TypeScript](typescript)

## How to Implement

1. Identify a group of tight­ly cou­pled class­es which would ben­e­fit from being more independent (e.g., for eas­i­er main­te­nance or simpler reuse of these classes).
2. Declare the mediator inter­face and describe the desired communication pro­to­col between mediators and var­i­ous components. In most cases, a sin­gle method for receiving notifications from components is sufficient.
3. Implement the con­crete mediator class. This class would ben­e­fit from stor­ing references to all of the components it manages.
4. You can go even further and make the mediator responsible for the creation and destruction of component objects. After this, the mediator may resemble a fac­to­ry or a facade.
5. Components should store a reference to the mediator object. The connection is usu­al­ly established in the components constructor, where a mediator object is passed as an argument.
6. Change the components code so that they call the mediators notification method instead of meth­ods on other components. Extract the code that involves call­ing other components into the mediator class. Exe­cute this code when­ev­er the mediator receives notifications from that component.

![Mediator](/images/mediator.png)
