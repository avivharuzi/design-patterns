# Bridge

Lets you split a large class or a set of close­ly related class­es into two sep­a­rate hierarchies abstraction and implementation which can be developed independently of each other.

## Examples

* [PHP](php)
* [Python](python)
* [TypeScript](typescript)

## How to Implement

1. Identify the orthogonal dimensions in your class­es. These independent concepts could be: abstraction/plat­form, domain/infrastructure, front-end/back-end, or inter­face/implementation.
2. See what operations the client needs and define them in the base abstraction class.
3. Deter­mine the operations avail­able on all plat­forms. Declare the ones that the abstraction needs in the gen­er­al implementation interface.
4. For all plat­forms in your domain cre­ate con­crete implementation class­es, but make sure they all fol­low the implementation interface.
5. Inside the abstraction class, add a reference field for the implementation type. The abstraction del­e­gates most of the work to the implementation object that’s referenced in that field.
6. If you have sev­er­al variants of high-level logic, cre­ate refined abstractions for each variant by extend­ing the base abstraction class.
7. The client code should pass an implementation object to the abstractions constructor to associate one with the other. After that, the client can for­get about the implementation and work only with the abstraction object.

![Bridge](/images/bridge.png)
