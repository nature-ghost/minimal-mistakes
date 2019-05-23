---
title: "Post: JavaScript Prototypal Inheritance: Constructors vs. OLOO"
date: 2019-05-24T01:00:00:00+09:00
categories:
  - Blog
tags:
  - Javascript
  - OLOO
  - Prototypal
link: https://medium.com/predict/javascript-prototypal-inheritance-constructors-vs-oloo-d90c482aaa55
---

One of the first things you learn about when you study JavaScript Object Oriented Programming is Prototypal Inheritance. It can be a confusing subject to learn, especially if you're accustomed to other object oriented languages. In this piece, I'm going to focus on constructors and "Object Linking to Other Objects"(OLOO) prototypal inheritance and how each works behind the scenes.

However, before I go too much into constructors and ```Object.create```, I'm going to give a brief (and rough) overview of prototypal inheritance just so we're all on the same page.

## Prototypal Inheritance Overview
While prototypal inheritance is unique to JavaScript, it is not so special that it can't be compared to inheritance in other programming languages. In Ruby, for example, there are classes; subclasses inherit form superclasses. When a method is called on an object, the program will first look to see if that object has the method that is being called. If it does not, the program will then look up into it's ancestry to see if any of the classes it inherits from has that method. The program will either find the method and call it or not find it and throw an error.

JavaScript works in a somewhat similar fashion. Prototypes can be thought of as blueprints that detail the properties and behaviors any descendent object will inherit.


![1_think_of_javascript_protypes_as_blueprints.jpeg]({{site.url}}{{site.baseurl}}/assets/images/1_think_of_javascript_protypes_as_blueprints.jpeg){:class="img-responsive"}
*Think of JavaScript Prototypes as blueprints*

When a new object is created, it is created using that blueprint. If you want to find the the blueprint from which a new object inherits, you can find it is its ```__proto__``` property.

```javascript
var obj = new Object();
obj.__proto__

// returns

Object {__defineGetter__: function, __defineSetter__: function, 
hasOwnProperty: function, __lookupGetter__: function,
__lookupSetter__: function,,,}
```


Each object in JavaScript has a ```__proto__``` property, or prototype chain, that the program uses to look up any methods that are called on that object. Similar to Ruby, if a method is called on an object in JavaScript, the program will first look to the object to see if it has that method. If it doesn't, it will look up into it's ```__proto__``` property to see if it is there.

## Constructors

Constructor functions are one of the most common methods for creating objects that you will see in the wild. They are the more classical approach to OOP, using "classes" (Constructors) to define a group of objects. Constructors will have a structure similar to this:

```javascript
funciton Persion(first, last) {
  this.firstName = first;
  this.lastName = last;
  
  this.fullName = function() {
    console.log(this.firstName + ' ' + this.lastName); 
  }
}

var sunny = new Persion('Sun-Li', 'Beatteay');

sunny.fullName()        // 'Sun-Li Beatteay'
```

So what exactly is going on here? How does ```new Persion()``` actually create a new object and how does it affect prototypal inheritance?

When ```new Persion``` is invoked, a new object is created and the value of ```this``` is set to the object. Additionally, the ```constructor``` property is changed to the constructor function and ```__proto``` is set to the constructor's prototype. If there is no return value set at the end of the constructor function, the function will return ```this```, which is the object itself.


In other words, you can rewrite,

```var sunny = new Persion('Sun-Li', 'Beatteay')```

to this:

```javascript
var sunny = {
  firstName: 'Sunny',
  lastName: 'Beatteay',
  fullName: function() {
    console.log(this.firstName + ' ' + this.lastName);
  },

  constructor: Person,
  __proto__: Person.prototype
};
```

In regards to prototypal inheritance, ```sunny``` is an instance of a ```Person``` object and ```Person``` is now in the prototype chain for ```sunny```.

```javascript
  sunny instanceof Person           // true
  sunny.__proto__                   // Object {constructor: functon...}
  sunny.__proto__ === Person.prototype    // true
```



























