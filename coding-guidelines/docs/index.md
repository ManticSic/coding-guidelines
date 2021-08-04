# Introduction

## What is this?
This document attempts to provide guidelines for multiple programming languages.
Of course, if you create such a document you should practice what you preach.
So rest assured, these guidelines are representative to what I do in my
day-to-day work. Notice that not all guidelines have a clear rationale. Some
of them are simply choices I have made. In the end, it doesn't matter what
choice you made, as long as you make one and apply it consistently.

## Why would you use this document?

Although some might see coding guidelines as undesired overhead or something
that limits creativity, this approach has already proven its value for many
years. This is because not every developer:

- is aware that code is generally read 10 times more than it is changed.
- is aware of the potential pitfalls in one programming language, which are
  a good way in other.
- is aware of the impact of using (or neglecting to use) particular solutions
  on aspects like security, performance, multi-language support, etc.
- realizes that not every developer is as capable, skilled or experienced to
  understand elegant, but potentially very abstract solutions.

## Basics
Even if this document covers many scenarios, it will not cover every possible
scenario. But Unlike what some (junior) developers believe, just because
something is not explicitly listed as bad, it does not mean that using it is
okay.

There is a set of rules than can be applied to all situations, regardless of
their context. The include the following:

- [Principle of least astonishment (a.k.a. POLA)][pola]: you should choose
  solution that everyone can understand, and that keeps them on the right track.
- [Keep it simple, stupid (a.k.a. KISS)][kiss]: the simplest solution is more
  than sufficient.
- [You aren't gonna need it (a.k.a. YAGIN)][yagin]: create a solution for the
  problem at hand, not for the ones you think may happen later on. Can you
  predict the future?
- [Don't repeat yourself (a.k.a. DRY)][dry]: avoid duplication within a
  component, a source control repository or a
  [bounded context][bounded-context], without forgetting the
  [Rule of Three][rule-of-three] heuristic.
- The [four principles of object-oriented programming][oop]: encapsulation,
  abstraction, inheritance and polymorphism.
- In general, generated code should not need to comply with coding guidelines.
  However, if it is possible to modify the templates used for generation, try to
  make them generate code that complies as much as possible.

Regardless of the elegance of someone's solution, if it's too complex for the
ordinary developer, exposes unusual behavior, or tries to solve many possible
future issues, it es very likely the wrong solution and needs redesign. The
worst response a developer can give yo to these principles is: "But it works!".

## Wie fange ich an?
- Ask all developers to carefully read this document at least once. This will
  give them a sense of the kind of guidelines the document containes.
- Make sure evereybody agrees with the rules.
- Create a [project checklist][project-checklist] with the most important rules
  and use this checklist for your [Peer Review][peer-review].
- Consider forking the original source and create your own internal version of
  the document.
- Use tools, e. g. IDEs, compiler plugins or build tools, to be able to comply
  with these guidelines. THe most IDEs have a intelligent code instpection
  engine, with some configuration, already supporting many aspects of the
  Coding Guidelines.

## Inspiration
This document is inspired by [C# Coding Guidelines][csharp-coding-guidelines].

In the last years I often created some kind of code styles and coding
guidelines, which I used in both, private and professional projects. Now I
would like to use this knowledge to write some general guidelines.

## Is this a coding standard?
Definitely not! This document does not state that projects must comply with
these guidelines, neither does it say which guidelines are more important than
other. It is intended to be a guide for anyone who does not want to deal with
creating own rules but still wants to have a homogeneous developer experience
within one team, but also across multiple teams.

However, to help with decisions about which rules may be important, I have added
a recommendation level to each rule:

<img src="/img/1.png" alt="recommendation level 1" /> Guidelines that you should
never skip and should be applicable to all situations.

<img src="/img/2.png" alt="recommendation level 2" /> Strongly recommended
guidelines

<img src="/img/3.png" alt="recommendation level 1" /> May not be applicable in
all situations


[pola]: https://en.wikipedia.org/wiki/Principle_of_least_astonishment
[kiss]: https://en.wikipedia.org/wiki/KISS_principle
[yagin]: https://en.wikipedia.org/wiki/You_aren%27t_gonna_need_it
[dry]: https://en.wikipedia.org/wiki/Don%27t_repeat_yourself
[rule-of-three]: https://lostechies.com/derickbailey/2012/10/31/abstraction-the-rule-of-three/
[bounded-context]: https://martinfowler.com/bliki/BoundedContext.html
[oop]: https://en.wikipedia.org/wiki/Object-oriented_programming
[project-checklist]: https://www.continuousimprover.com/2010/03/alm-practices-5-checklists.html
[peer-review]: https://www.continuousimprover.com/2010/02/tfs-development-practices-part-2-peer.html
[csharp-coding-guidelines]: https://csharpcodingguidelines.com/
