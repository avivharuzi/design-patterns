# Memento

Lets you save and restore the pre­vi­ous state of an object with­out reveal­ing the details of its implementation.

## Examples

* [PHP](php)
* [Python](python)
* [TypeScript](typescript)

## How to Implement

1. Deter­mine what class will play the role of the orig­i­na­tor. It’s important to know whether the pro­gram uses one central object of this type or mul­ti­ple small­er ones.
2. Cre­ate the memento class. One by one, declare a set of fields that mir­ror the fields declared inside the orig­i­na­tor class.
3. Make the memento class immutable. A memento should accept the data just once, via the constructor. The class should have no setters.
4. If your pro­gram­ming language sup­ports nest­ed class­es, nest the memento inside the orig­i­na­tor. If not, extract a blank inter­face from the memento class and make all other objects use it to refer to the memento. You may add some meta­da­ta operations to the inter­face, but nothing that expos­es the orig­i­na­tor’s state.
5. Add a method for pro­duc­ing mementos to the orig­i­na­tor class. The orig­i­na­tor should pass its state to the memento via one or mul­ti­ple arguments of the mementos constructor.
6. Add a method for restoring the orig­i­na­tor’s state to its class. It should accept a memento object as an argument. If you extract­ed an inter­face in the pre­vi­ous step, make it the type of the para­me­ter. In this case, you need to type­cast the incoming object to the mediator class, since the orig­i­na­tor needs full access to that object.
7. The care­tak­er, whether it represents a command object, a his­to­ry, or some­thing entire­ly dif­fer­ent, should know when to request new mementos from the orig­i­na­tor, how to store them and when to restore the orig­i­na­tor with a par­tic­u­lar memento.
8. The link between care­tak­ers and orig­i­na­tors may be moved into the memento class. In this case, each memento must be connected to the orig­i­na­tor that had cre­at­ed it. The restoration method would also move to the memento class. How­ev­er, this would all make sense only if the memento class is nest­ed into orig­i­na­tor or the orig­i­na­tor class provides sufficient setters for over­rid­ing its state.

![Memento](/images/memento.png)
