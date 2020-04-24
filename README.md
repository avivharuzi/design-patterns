# Design Patterns

Implementation of Design Patterns in many languages.

## Resources

Most of the resources and images are from refactoring guro: https://refactoring.guru

I take the resources and bundle them to make very easy to search for design pattern with examples.

## Content

* [Creational Patterns](creational-patterns)
* [Structural Patterns](structural-patterns)
* [Behavioral Patterns](behavioral-patterns)

## What’s a design pattern?

__Design patterns__ are typical solutions to commonly occurring problems in software design. They are like pre-made blueprints that you can customize to solve a recurring design problem in your code.

You can’t just find a pattern and copy it into your program, the way you can with off-the-shelf functions or libraries. The pattern is not a specific piece of code, but a general concept for solving a particular problem. You can follow the pattern details and implement a solution that suits the realities of your own program.

Patterns are often confused with algorithms, because both concepts describe typical solutions to some known problems. While an algorithm always defines a clear set of actions that can achieve some goal, a pattern is a more high-level description of a solution. The code of the same pattern applied to two different programs may be different.

An analogy to an algorithm is a cooking recipe: both have clear steps to achieve a goal. On the other hand, a pattern is more like a blueprint: you can see what the result and its features are, but the exact order of implementation is up to you.

## What does the pattern consist of?

Most patterns are described very formally so people can reproduce them in many contexts. Here are the sections that are usually present in a pattern description:

* __Intent__ of the pattern briefly describes both the problem and the solution.
* __Motivation__ further explains the problem and the solution the pattern makes possible.
* __Structure__ of classes shows each part of the pattern and how they are related.
* __Code example__ in one of the popular programming languages makes it easier to grasp the idea behind the pattern.

Some pattern catalogs list other useful details, such as applicability of the pattern, implementation steps and relations with other patterns.

## Classification of patterns

Design patterns differ by their complexity, level of detail and scale of applicability to the entire system being designed. I like the analogy to road construction: you can make an intersection safer by either installing some traffic lights or building an entire multi-level interchange with underground passages for pedestrians.

The most basic and low-level patterns are often called idioms. They usually apply only to a single programming language.

The most universal and high-level patterns are architectural patterns. Developers can implement these patterns in virtually any language. Unlike other patterns, they can be used to design the architecture of an entire application.

In addition, all patterns can be categorized by their intent, or purpose. This repository covers three main groups of patterns:

* __Creational patterns__ provide object creation mechanisms that increase flexibility and reuse of existing code.
* __Structural patterns__ explain how to assemble objects and classes into larger structures, while keeping the structures flexible and efficient.
* __Behavioral patterns__ take care of effective communication and the assignment of responsibilities between objects.

![Design Patterns](/images/design-patterns.png)
