---
title: "Post: JavaScript Prototypal Inheritance: Constructors vs. OLOO"
categories:
  - Blog
tags:
  - Javascript
  - OLOO
  - Prototypal
---

One of the first things you learn about when you study JavaScript Object Oriented Programming is Prototypal Inheritance. It can be a confusing subject to learn, especially if you're accustomed to other object oriented languages. In this piece, I'm going to focus on constructors and "Object Linking to Other Objects"(OLOO) prototypal inheritance and how each works behind the scenes.

However, before I go too much into constructors and ```Object.create```, I'm going to give a brief (and rough) overview of prototypal inheritance just so we're all on the same page.

###Prototypal Inheritance Overview
While prototypal inheritance is unique to JavaScript, it is not so special that it can't be compared to inheritance in other programming languages. In Ruby, for example, there are classes; subclasses inherit form superclasses. When a method is called on an object, the program will first look to see if that object has the method that is being called. If it does not, the program will then look up into it's ancestry to see if any of the classes it inherits from has that method. The program will either find the method and call it or not find it and throw an error.

JavaScript works in a somewhat similar fashion. Prototypes can be thought of as blueprints that detail the properties and behaviors any descendent object will inherit.


![Think of JavaScript Prototypes as blueprints]({{site.url}}{{site.baseurl}}/assets/images/1_think_of_javascript_protypes_as_blueprints.jpeg){:class="img-responsive"}

<img src="{{site.url}}{{site.baseurl}}/assets/images/1_think_of_javascript_protypes_as_blueprints.jpeg">

