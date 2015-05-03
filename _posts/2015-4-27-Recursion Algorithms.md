---
layout: post
title: Recursion Algorithms
---

A dream within a dream.

When I was first learning JavaScript and learned the idea of a recursion, I have to admit that I thought it was pretty awesome. A little part of me also felt that it should have been expected - to be able to write a function with a function. As I become more experienced with JavaScript, I' learned a few strategies to arrive at your recursion function.

First of all, here's what you're tasked with:

For a given n, find the nth Fibonacci number. If you don't recall how Fibonacci numbers work - long story short, the sum of the nth number is equivalent to the sum of the two previous Fibonacci numbers. For example:

fib(0) = 0

fib(1) = 1

fib(2) = 1

fib(3) = 2

fib(4) = 3

fib(5) = 5

1) Visualize how your function looks like in a tree diagram. Recursion problems can typically be broken down into smaller branches of an overall tree, representing the whole problem. If we were trying to find the 5th Fibonacci number, here's how the tree would look like.

![_config.yml]({{ site.baseurl }}/images/Recursion.png)

Despite how this diagram looks, I've also learned that my imagination of what I thought of recursion was proved to be incorrect - at least in this case. The branches that stem out don't happen simutaneously! What really happens is a depth search (breadth search strategy to be explained in a later blog post) of fib(4) first - so the function works through the left-most functions to the right-most functions. There is no explosion magic that makes everything happen at once!

2) Determine first how you will break the problem down into the smallest piece possible. Aim to solve just one of the branches first. Then analyze how you could adjust it to produce an end result that could be applied to every branch.

3) Establish a base case. Without this, your recursion function will go on in an infinite loop and crash your browser (you wouldn't want that would you?)! So remember that within your function, that you need to create a condition that will cause the function to stop running after its done all the work.

Well there you have it! You didn't think I was going to provide you the solution, did you?

