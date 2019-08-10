# State

Lets an object alter its behavior when its inter­nal state changes. It appears as if the object changed its class.

## Examples

* [PHP](php)
* [Python](python)
* [TypeScript](typescript)

## How to Implement

1. Decide what class will act as the con­text. It could be an exist­ing class which already has the state-dependent code; or a new class, if the state-spe­cif­ic code is distributed across mul­ti­ple classes.
2. Declare the state inter­face. Although it may mir­ror all the meth­ods declared in the con­text, aim only for those that may con­tain state-spe­cif­ic behavior.
3. For every actual state, cre­ate a class that derives from the state inter­face. Then go over the meth­ods of the con­text and extract all code related to that state into your newly cre­at­ed class. While mov­ing the code to the state class, you might dis­cov­er that it depends on private members of the con­text. There are sev­er­al workarounds:
    * Make these fields or meth­ods public.
    * Turn the behavior you’re extract­ing into a pub­lic method in the con­text and call it from the state class. This way is ugly but quick, and you can always fix it later.
    * Nest the state class­es into the con­text class, but only if your pro­gram­ming language sup­ports nest­ing classes.
4. In the con­text class, add a reference field of the state inter­face type and a pub­lic set­ter that allows over­rid­ing the value of that field.
5. Go over the method of the con­text again and replace empty state conditionals with calls to corresponding meth­ods of the state object.
6. To switch the state of the con­text, cre­ate an instance of one of the state class­es and pass it to the con­text. You can do this with­in the con­text itself, or in var­i­ous states, or in the client. Wherever this is done, the class becomes dependent on the con­crete state class that it instantiates.

![State](/images/state.png)
