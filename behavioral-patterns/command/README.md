# Command

Turns a request into a stand-alone object that contains all information about the request. This transformation lets you para­me­ter­ize meth­ods with dif­fer­ent requests, delay or queue a request's exception, and sup­port undo doable operations.

## Examples

* [PHP](php)
* [Python](python)
* [TypeScript](typescript)

## How to Implement

1. Declare the command inter­face with a sin­gle execution method.
2. Start extract­ing requests into con­crete command class­es that implement the command inter­face. Each class must have a set of fields for stor­ing the request arguments along with a reference to the actual receiver object. All these val­ues must be initialized via the commands constructor.
3. Identify class­es that will act as senders. Add the fields for stor­ing commands into these class­es. Senders should com­mu­ni­cate with their commands only via the command inter­face. Senders usu­al­ly don’t cre­ate command objects on their own, but rather get them from the client code.
4. Change the senders so they exe­cute the command instead of send­ing a request to the receiver directly.
5. The client should initialize objects in the fol­low­ing order:
    * Cre­ate receivers.
    * Cre­ate commands, and associate them with receivers if needed.
    * Cre­ate senders, and associate them with spe­cif­ic commands.

![Command](/images/command.png)
