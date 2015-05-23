---
layout: post
title: Callbacks
---

Callbacks literally perform how they're named, though not entirely the easiest concept to grasp nor explain.

To give us some context, pretend we're making a salad:

![_config.yml]({{ site.baseurl }}/images/Callbacks.png)

Because we have to make many different salads for people, we don't want to forget tossing the salad each time we make a new salad. The callback passed to our makeSalad function allows us to do this, and it can be anything we want it to be. I won't write out the toss salad function, but imagine that what it does is tosses the salad.

On line 11, we invoke our function, and if we walk through how make salad works, a callback is the ingredients will appear on the console, and our tossSalad function will happen when line 4 completes running.

Callbacks are very powerful when you want something to be performed asynchronously. To illustrate, you can be making many, many, many salads, and the time you take one salad could restrict your output and "block" the production of the other salads. In our function, when we want to make many salads, it's similar to having multiple salad-makers all happening whenever it needs to happen, thus our production is "non-blocking". The callback passed through ensures that each salad produced is tossed before each salad is complete.

