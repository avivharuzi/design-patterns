# Flyweight

Lets you fit more objects into the avail­able amount of RAM by sharing com­mon parts of state between mul­ti­ple objects instead of keep­ing all of the data in each object.

## Examples

* [PHP](php)
* [Python](python)
* [TypeScript](typescript)

## How to Implement

1. If there’s no pre-exist­ing ser­vice inter­face, cre­ate one to make proxy and ser­vice objects inter­change­able. Extract­ing the inter­face from the ser­vice class isn’t always pos­si­ble, because you’d need to change all of the ser­vice’s clients to use that inter­face. Plan B is to make the proxy a sub­class of the ser­vice class, and this way it’ll inherit the inter­face of the service.
2. Cre­ate the proxy class. It should have a field for stor­ing a reference to the ser­vice. Usu­al­ly, prox­ies cre­ate and man­age the whole life cycle of their servers. In rare occasions, a ser­vice is passed to the proxy via a constructor by the client.
3. Implement the proxy meth­ods accord­ing to their pur­pos­es. In most cases, after doing some work, the proxy should del­e­gate the work to the ser­vice object.
4. Con­sid­er intro­duc­ing a creation method that decides whether the client gets a proxy or a real ser­vice. This can be a sim­ple sta­t­ic method in the proxy class or a full-blown fac­to­ry method.
5. Con­sid­er implementing lazy initialization for the ser­vice object.

![Flyweight](/images/flyweight.png)
