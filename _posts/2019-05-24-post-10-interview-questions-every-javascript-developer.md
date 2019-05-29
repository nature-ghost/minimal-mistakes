---
title: "Post: 10 Interview Questions Every JavaScript Developer Should Know"
date: 2019-05-24T02:00:00:00+09:00
categories:
  - Study 
tags:
  - Javascript
  - Functional Programming
  - Development 
  - Technology
  
excerpt: "AKA: The Keys to JavaScript Mastery"
header:
  overlay_image: assets/images/2_10_interview_questions.jpeg
  teaser: assets/images/2_10_interview_questions.jpeg
  overlay_filter: 0.5 # same as adding an opacity of 0.5 to a black background
  caption: "Photo credit: [**Eric Elliott**]"
  actions:
    - label: "More Info"
      url: "https://medium.com/javascript-scene/10-interview-questions-every-javascript-developer-should-know-6fa6bdf5ad95"
---

At most companies, management must trust the developers to give technical interviews in order to assess candidate skills. If you do well as a candidate, you'll eventually need to interview. Here's how.

---
### It Starts With People

In ["How to Build a High Velocity Development Team"](https://medium.com/javascript-scene/how-to-build-a-high-velocity-development-team-4b2360d34021), I made a couple points worh repeating:

> *"Nothing predicts business outcomes better than an exceptional team. If your're going to beat the odds, you need to invest here, first."*

As Marcus Lemonis says, focus on the 3 P's:

---

### *"People, Process, Product"*

---

<iframe width="560" height="315" src="https://www.youtube.com/embed/37rMZSA6oLk?controls=0" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

Your early hires should be very strong, senior-level candidates. People who can hire and mentor other developers, and help the mid-level and junior developers you'll eventually want to hire down the road.

Read ["Why Hiring is So Hard in Tech"](https://medium.com/javascript-scene/why-hiring-is-so-hard-in-tech-c462c3230017) for a good breakdown of the general do's and don'ts of candidate evaluation.

---


### *The best way to evaluate a candidate is a pair programming exercise.*

---

Pair program with the candidate. Let the candidate drive. Watch and listen more than you talk. A good project might be to pull tweets from the Twitter API and display them on a timeline.

That said. no single exercise will tell you everything you need to know. An interview can be a very useful tool as well, but don't waste time asking about syntax or language quirks. You need to see the big picture. Ask about architecture and paradigms -- the big decisions that can have major impact on the whole project.

Syntax and features are easy to Google. It's much harder to Google for software engineering wisdom or the common paradigms and idioms JavaScript developers pick up with experience.

JavaScript is special, and it plays a critical role in almost every large application. What is it about JavaScript that makes it meaningfully different from other languages?

Hear are some questions that will help you explore the stuff that really matters:

### **1. Can you name two programming paradigms important for JavaScript app developers?**

JavaScript is a multi-paradigm language, supporting **imperative/procedural** programming along with **OOP** (Object-Oriented Programming) and **functional programming**. JavaScript supports OOP with **prototypal inheritance**.

#### Good to hear:

* Prototypal Inheritance (alsl: prototypes, OLOO).

* Functional programming (also: closures, first class functions, lambdas).

#### Red flags:

* No clue what a paradigm is, no mention of prototypal oo or functional programming.

#### Learn More:


* ["The Two Pillars of JavaScript Part 1]({{ site.baseurl }}{% link _posts/2019-05-24-post-the-two-pillars-of-javascript.md %}) -- Prototypal OO.

* ["The Two Pillars of JavaScript Part 2]({{site.baseurl }}{% link _posts/2019-05-24-post-the-two-pillars-of-javascript-part2.md %}) -- Functional Programming.
 

###  **2. What is functional programming?**
 
 Functional programming produces programs by composing mathematical functions and avoids shared state & mutable data. Lisp (specified in 1958) was among the first languages to support functional programming, and was heavily inspired by lambda calculus. Lisp and many Lisp family languages are still in common use today.
 
 Functional programming is an essential concept in JavaScript (one of the two pillars of JavaScript). Several common functional utilities were added to JavaScript in ES5.
 
#### Good to hear:
 
 * Pure functions / function purity.
 
 * Avoid side-effects.
 
 * Simple function composition.
 
 * Examples of functional languages: Lisp, ML, Haskell, Erlang, Clojure, Elm, F Sharp, OCaml, etc...
 
 * Menthion of features that support FP: first-class functions, higher order functions, functions as arguments/values.
 
#### Red flags:
 
 * No mention of pure functions / avoiding side-effects
 
 * Unable to provide examples of functional programming languages.
 
 * Unable to identify the features of JavaScript that enable FP.
 
#### Learn More:
 
 * [The Two Pillars of JavaScript Part 2]({{site.baseurl }}{% link _posts/2019-05-24-post-the-two-pillars-of-javascript-part2.md %})
 
 * [The Dao of Immutability.](https://medium.com/javascript-scene/the-dao-of-immutability-9f91a70c88cd)
 
 * [Composing Software.](https://medium.com/javascript-scene/composing-software-an-introduction-27b72500d6ea)
 
 * [The Haskell School of Music.](http://haskell.cs.yale.edu/wp-content/uploads/2015/03/HSoM.pdf)
 
### **3. What is the difference between classical inheritance and prototypal inheritance?**
 
 **Class Inheritance:** instances inherit from classes (like a blueprint -- a description of the class), and create sub-class relationships: hierarchical class taxonomies. Instances are typically instanctiated via constructor functions with the *\`new\`* keyword. Class inheritance may or may not use the *\`class\`* keyword from ES6.
 
 **Prototypal Inheritance:** instances inherit directly from other objects. 
 Instances are typically instantiated via factory functions or *\`Object.create()\`*. Instances may be composed from many different objects, allowing for easy selective inheritance.
 
 ---
 
### *In JavaScript, prototypal inheritance is simpler & more flexible than class inheritance.*
 
 ---
 
 
#### Good to hear:

* Classes: create tight coupling or hierachies/taxonomies.

* Protypes: mentions of concatenative inheritance, prototype delegation, functional inheritance, object composition.

#### Red Flags:

* No preference for prototypal inheritance & composition over class inheritance.

#### Learn More:

* ["The Two Pillars of JavaScript Part 1]({{ site.baseurl }}{% link _posts/2019-05-24-post-the-two-pillars-of-javascript.md %}) -- Prototypal OO.

* [Common Misconceptions About Inheritance in JavaScript.](https://medium.com/javascript-scene/common-misconceptions-about-inheritance-in-javascript-d5d9bab29b0a)

<iframe title="vimeo-player" src="https://player.vimeo.com/video/69255635" width="640" height="360" frameborder="0" allowfullscreen></iframe>

### *4. What are the pros and cons of functional programming vs object-oriented programming?*

**OOP Pros:** It's easy to understand the basic concept of objects and easy to interpret the meaning of method calls. OOP tends to use an imperative style rather than a declarative style, which reads like a straight-forward set of instructions for the computer to follow.

**OOP Cons:** OOP Typically depends on shared state. Objects and behaviors are typically tacked together on the same entity, which may be accessed at random by any number of functions with non-deterministic order, which may lead to undesirable behavior such as race conditions.

**FP Pros:** Using the functional paradigm, programmers avoid any shared state of side-effects, which eliminates bugs caused by multiple functions ocmpeting for the same resources. With features such as the availability of point-free style (aka tacit programming), functions tend to be radically simplified and easily recomposed for more generally reusable code compared to OOP.

FP also tends to favor declarative and denotational styles, which do not spell out step-by-step instructions for operations, but instead concentrate on **what** to do, letting the underlying functions take care of the **how**. This leaves tremendous latitude for refactoring and performance optimization, even allowing you to replace entire algorithms with more efficient ones with very little code change. (e.g., memoize, or use lazy evaluation in place of eager evaluation.)

Computation that makes use of pure functions is also easy to scale across multiple processors, or across distributed computing clusters without fear of threading resource conflicts, race conditions, etc...

 **FP Cons:** Over explotition of FP features such as point-free style and large compositions can potentially reduce readability because the resulting code is often more abstractly specified, more terse, and less concrete.
 
 More people are familiar with *OO* and imperative programming than functional programming, so even common idioms in functional programming can be confusing to new team members.
 
 FP has a much steeper learning curve than OOP because the broad popularity of OOP has allowed the language and learning materials of OOP to become more conversational, whereas the languages of FP tends to be much more academic and formal. FP concepts are frequently written about using idioms and notations from lambda calculus, algebras, and category theory, all of which requires a prior knowledge foundation in those domains to be understood.
 
#### Good to hear:
 
 * Mentions of trouble with shared state, different things competing for the same resources, etc...
 
 * Awareness of FP's capability to radically simplify many applications.
 
 * Awareness of the differences in learning curves.
 
 * Articulation of side-effects and how they impact program maintainabliity.
 
 * Awareness that a highly functional codebase can have a steep learning curve.
 
 * Awareness that a highly OOP codebase can be extremely resitant to change and very brittle compared to an equivalent FP codebase.
 
 * Awareness that immutability gives rise to an extremely accessible and malleable program state history, allowing for the easy addition of features like infinite undo/redo, rewind/replay, time-travel debugging, and so on. Immutability can be achieved in either paradigm, but a proliferation of shared stateful objects complicates the implementation in OOP.
 
#### Red flags:
 
 * Unable to list disadvantages of one style of another -- Anybody experienced with either style should have bumped up against some of the limitations.
 
#### Learn More:
 
 * [The Two Pillars of JavaScript Part 1]({{ site.baseurl }}{% link _posts/2019-05-24-post-the-two-pillars-of-javascript.md %}) -- Prototypal OO.
 
 * ["The Two Pillars of JavaScript Part 2]({{site.baseurl }}{% link _posts/2019-05-24-post-the-two-pillars-of-javascript-part2.md %}) -- Functional Programming.
  
### **5. When is classical inheritance an appropriate choice?**

The answer is never, or almost never. Certainly never more than one level. Multi-level class hierarchies are an anti-pattern. I've been issuing this challenge for years, and the only answers I've ever heard fall into one of several [common misconceptions](https://medium.com/javascript-scene/common-misconceptions-about-inheritance-in-javascript-d5d9bab29b0a). More frequently, the challenge is met with silence.

> *"If a feature is sometimes useful and sometimes dangerous and if there is a better option then **always use the better option**."
>
> *~Douglas Crockford*


#### Good to hear:

* Rarely, almost never, or never.

* A single level is sometimes OK, from a framework base-class such as ```React.Component```.

* "Favor object composition over class inheritance."

#### Learn More:

* [The Two Pillars of JavaScript Part 1]({{ site.baseurl }}{% link _posts/2019-05-24-post-the-two-pillars-of-javascript.md %}) -- Prototypal OO.

* [JS Objects -- Inherited a Mess](http://davidwalsh.name/javascript-objects)

### **6. When is prototypal inheritance an appropriate choice?**

There is more than one type of prototypal inheritance:

* **Delegation** (i.e., the prototype chain).

* **Concatenative** (i.e., mixins, *'Object.assign()'*).

* **Functional** (Not to be confused with functional programming. A function used to create a closure for private state/encapsulation).


