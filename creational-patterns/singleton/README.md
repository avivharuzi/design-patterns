# Singleton

Lets you ensure that a class has only one instance, while providing a global access point to this instance.

## Examples

* [PHP](php)
* [Python](python)
* [TypeScript](typescript)

## How to Implement

1. Add a private sta­t­ic field to the class for stor­ing the sin­gle­ton instance.
2. Declare a pub­lic sta­t­ic creation method for get­ting the sin­gle­ton instance.
3. Implement "lazy initialization" inside the sta­t­ic method. It should cre­ate a new object on its first call and put it into the sta­t­ic field. The method should always return that instance on all subsequent calls.
4. Make the constructor of the class private. The sta­t­ic method of the class will still be able to call the constructor, but not the other objects.
5. Go over the client code and replace all direct calls to the sin­gle­ton’s constructor with calls to its sta­t­ic creation method.

![Singleton](/images/singleton.png)
