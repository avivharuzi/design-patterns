# Adapter

Allow objects with incompatible interfaces to collaborate.

## Examples

* [PHP](php)
* [Python](python)
* [TypeScript](typescript)

## How to Implement

1. Make sure that you have at least two class­es with incompatible interfaces:
    * A use­ful ser­vice class, which you can’t change (often 3rd-party, legacy or with lots of exist­ing dependencies).
    * One or sev­er­al client class­es that would ben­e­fit from using the ser­vice class.
2. Declare the client inter­face and describe how clients com­mu­ni­cate with the service.
3. Cre­ate the adapter class and make it fol­low the client inter­face. Leave all the meth­ods empty for now.
4. Add a field to the adapter class to store a reference to the ser­vice object. The com­mon practice is to initialize this field via the constructor, but some­times it’s more convenient co to pass it to the adapter when call­ing its methods.
5. One by one, implement all meth­ods of the client inter­face in the adapter class. The adapter should del­e­gate most of the real work to the ser­vice object, handling only the inter­face or data for­mat conversion.
6. Clients should use the adapter via the client inter­face. This will let you change or extend the adapters with­out affect­ing the client code.

![Adapter](/images/adapter.png)
