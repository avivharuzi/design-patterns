# Template Method

Defines the skeleton of an algorithm in the super­class but lets sub­class­es over­ride spe­cif­ic steps of the algorithm with­out chang­ing its structure.

## Examples

* [PHP](php)
* [Python](python)
* [TypeScript](typescript)

## How to Implement

1. Analyze the tar­get algorithm to see whether you can break it into steps. Con­sid­er which steps are com­mon to all sub­class­es and which ones will always be unique.
2. Cre­ate the abstract base class and declare the tem­plate method and a set of abstract meth­ods rep­re­sent­ing the algorithms steps. Out­line the algorithms structure in the tem­plate method by exe­cut­ing corresponding steps. Con­sid­er mak­ing the tem­plate method final to pre­vent sub­class­es from over­rid­ing it.
3. It’s okay if all the steps end up being abstract. How­ev­er, some steps might ben­e­fit from hav­ing a default implementation. Sub­class­es don’t have to implement those methods.
4. Think of adding hooks between the crucial steps of the algorithm.
5. For each variation of the algorithm, cre­ate a new con­crete sub­class. It must implement all of the abstract steps, but may also over­ride some of the option­al ones.

![Template Method](/images/template-method.png)
