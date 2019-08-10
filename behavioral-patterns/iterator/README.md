# Iter­a­tor

Lets you tra­verse elements of a collection with­out expos­ing its under­ly­ing representation (list, stack, tree, etc.).

## Examples

* [PHP](php)
* [Python](python)
* [TypeScript](typescript)

## How to Implement

1. Declare the iter­a­tor inter­face. At the very least, it must have a method for fetch­ing the next element from a collection. But for the sake of convenience you can add a cou­ple of other meth­ods, such as fetch­ing the pre­vi­ous element, track­ing the cur­rent position, and check­ing the end of the iteration.
2. Declare the collection inter­face and describe a method for fetch­ing iter­a­tors. The return type should be equal to that of the iter­a­tor inter­face. You may declare sim­i­lar meth­ods if you plan to have sev­er­al dis­tinct groups of iterators.
3. Implement con­crete iter­a­tor class­es for the collections that you want to be tra­vers­a­ble with iter­a­tors. An iter­a­tor object must be linked with a sin­gle collection instance. Usu­al­ly, this link is establish via the iter­a­tor’s constructor.
4. Implement the collection inter­face in your collection class­es. The main idea is to pro­vide the client with a short­cut for cre­at­ing iter­a­tors, tailored for a par­tic­u­lar collection class. The collection object must pass itself to the iter­a­tor’s constructor to establish a link between them.
5. Go over the client code to replace all of the collection tra­ver­sal code with the use of iter­a­tors. The client fetch­es a new iter­a­tor object each time it needs to iter­ate over the collection elements.

![Iter­a­tor](/images/iter­a­tor.png)
