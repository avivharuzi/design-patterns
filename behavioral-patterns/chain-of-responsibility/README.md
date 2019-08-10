# Chain of Responsibility

Lets you pass requests along a chain of handlers. Upon receiving a request, each handler decides either to process the request or to pass it to the next handler in the chain.

## Examples

* [PHP](php)
* [Python](python)
* [TypeScript](typescript)

## How to Implement

1. Declare the handler inter­face and describe the signature of a method for handling requests.
2. To eliminate duplicate boil­er­plate code in con­crete handlers, it might be worth cre­at­ing an abstract base handler class, derived from the handler interface.
3. One by one cre­ate con­crete handler sub­class­es and implement their handling meth­ods. Each handler should make two decisions when receiving a request:
  * Whether it’ll process the request.
  * Whether it’ll pass the request along the chain.
4. The client may either assemble chains on its own or receive pre-built chains from other objects. In the lat­ter case, you must implement some fac­to­ry class­es to build chains accord­ing to the configuration or environment settings.
5. The client may trig­ger any handler in the chain, not just the first one. The request will be passed along the chain until some handler refuses to pass it further or until it reach­es the end of the chain.
6. “Due to the dynamic nature of the chain, the client should be ready to han­dle the fol­low­ing scenarios:
  * The chain may consist of a sin­gle link.
  * Some requests may not reach the end of the chain.
  * Oth­ers may reach the end of the chain unhandled.

![Chain of Responsibility](/images/chain-of-responsibility.png)
