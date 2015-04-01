---
layout: post
title: Instantiation Patterns
---

Don't you wish that everytime your younger sibling made you a grilled cheese, it would always be the same?

This post will show you how you can make that possible... sort of.

Functional Instantiation:

![_config.yml]({{ site.baseurl }}/images/Functional.png)

You can probably already tell that this particular function constructor is very clear in what properties and methods it has... but then again, any time you make a different type of grilled cheese with a delicious method, you would need to type in that method again...


Functional - Shared Instantiation:

![_config.yml]({{ site.baseurl }}/images/Functional-Shared.png)

Here, the function contructor's properties are extended to the GrilledCheeseMethods. This is another object that contains methods so that all you need to do is extend the methods onto a particular object. Slightly more efficient than regular Functional Instantiation, but less clear.


Prototypal Instantiation:

![_config.yml]({{ site.baseurl }}/images/Prototypal.png)

Ah, now every instance of GrilledCheese will "delegate" to KingGrilledCheese's properties - or methods in this case - meaning they won't need to be rewritten and every new instance of GrilledCheese will "remember" they have properties of KingGrilled Cheese. Though, this could be easier...

Pseudoclassical Instantiation:

![_config.yml]({{ site.baseurl }}/images/Pseudoclassical.png)

Yes, younger sibling, I don't want to teach you how to make a myGrilledCheese delicious every time. Nor do I want to write extra lines of code. Just make me a fresh new GrilledCheese. However, what you don't write, leaves to the "magic" of the interpreter, and makes the function constructor a little less clear.


