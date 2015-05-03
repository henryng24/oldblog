---
layout: post
title: The Event Loop
---

As you dive deeper into JavaScript, you'll start hearing that JavaScript is single-threaded, and you might be wondering --- "What exactly does that mean?"

The concept of single-threadedness is quite simple actually. It just means that each line of JavaScript is interpreted one line at a time. Where things might get confusing is when JavaScript meets your browser.

Here's an image that may be helpful to your understanding.

![_config.yml]({{ site.baseurl }}/images/EventLoop.png)

When JavaScript is run on your browser, the environment completely changes. No longer are we dealing with the single Call Stack, as we normally would be with just JavaScript, we are now dealing with Web APIs, the Callback Queue, and also the Event Loop.

Functions like Set Timeout fall under Web APIs, your Callback Queue is where are your Callbacks go, and the Call Stack is your regular JavaScript Call Stack.

Here's an example for illustrative purposes:

var boom = function(name, callback){
    callback();
    setTimeout(function timer() {
        console.log('Hello ' + name);    
    }, 5000);
}

boom("Henry", function() { console.log("BOOM")});

1. boom("Henry", function() { console.log("BOOM")}); enters the Call Stack and is invoked.
2. function() { console.log("BOOM")} enters the Call Stack and is and console.logs "BOOM"
3. setTimeout(function timer() { console.log('Hello ' + name); }, 5000); enters the Call Stack and is invoked and calls timer() to happen in 5 seconds in the Web APIs.
4. After 5 seconds, timer() enters into the Callback Queue
5. The Event Loop sees that nothing is running in the CallStack and places timer() into the CallStack and invokes it.