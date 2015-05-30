---
layout: post
title: Time and Space
---

...Complexity.

If you're learning about software engineering, time complexity may be one of the topics that you initially dive into. But sometimes when you're introduced to time complexity, you may not be introduced to its other pair: space complexity. There may also be some confused as to how they're both calculated and why the calculation works as it does.

To start off, time complexity and space complexity are described using Big O Notation represented as such: O(N), O(1), O(logn), meaning linear, constant, and logarithmic respectively. This list is not exhaustive.

Let's break down a single for loop that we're all familiar with:

for (var i = 0; i < input; i ++) {
  console.log(i);
}

Notice that when we first declare our variable, "i = 0" is declared once and will never run again in this for loop, representing one operation:

1

The second part of the for loop, "i < input" would run "input" + 1 times as the operation will continue checking to see if "i" is less than input, thus running as many times depending on:

input + 1

The third part of the for loop, "i ++" would run input times as "i" will only be incremented when "i" is less than the input. The number of times this executes will vary depending on:

input

Now let's put all that together: 1 + input + 1 + input. We can simply refactor this as:

2(input) + 2

Here's where many people get caught up - "I follow up to this point - but shouldn't our Big O notation be O(2N +2)?"

When it comes to time and space complexity as the input becomes large. In the grand scheme of things, if your input is 1,000,000 apples, how does the "+2" portion of the algorithm have on the run time based on the input? If you thought inconsequential, then you're right!

On the same note, we don't care whether if it's 2,000,000 (2X) apples or 3,000,000 (3X) apples as the input is still large. Focusing on those constant factors are equally inconsequential since our input has no impact on the multiplier.

Space complexity can be approached the same way!

Try it yourself! What do you think the Big O notation of one for loop and another for loop nested within that for loop is?

