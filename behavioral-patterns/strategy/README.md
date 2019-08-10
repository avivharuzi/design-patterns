# Strategy

Lets you define a fam­i­ly of algorithms, put each of them into a sep­a­rate class, and make their objects inter­change­able.

## Examples

* [PHP](php)
* [Python](python)
* [TypeScript](typescript)

## How to Implement

1. In the con­text class, identify an algorithm that’s prone to frequent changes. It may also be a massive conditional that selects and exe­cutes a variant of the same algorithm at runtime.
2. Declare the strategy inter­face com­mon to all variants of the algorithm.
3. One by one, extract all algorithms into their own class­es. They should all implement the strategy interface.
4. In the con­text class, add a field for stor­ing a reference to a strategy object. Pro­vide a set­ter for replacing val­ues of that field. The con­text should work with the strategy object only via the strategy inter­face. The con­text may define an inter­face which lets the strategy access its data.
5. Clients of the con­text must associate it with a suit­able strategy that match­es the way they expect the con­text to per­form its pri­ma­ry job.

![Strategy](/images/strategy.png)
