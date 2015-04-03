---
layout: post
title: Data Structures
---

Would you rather: Have a very fast potato chip-making machine that takes up the size of half your house, or a very slow potato chip-making machine that takes up a quarter of your house?

The concept of optimizing data structures typically come with a tradeoff, like every decision we make in life. For data structures, it is time and space. I'll explain below how a few data structures were optimized. Data structures could go hand-in-hand to explain time complexity: the amount of time taken by an algorithm to run for a given input.

Linked Lists

The optimization that linked lists achieve is the efficient insertion and removal of elements in the list. As you can see below, each "node" contains two fields: one is the value of the particular node, and the other is a pointer to another value. You can tell how much more efficient it would be to remove the value 99 in a linked list, as opposed to a regular array of values when you actually start to think how you achieve this in a regular array. In a regular array, in order to remove 99 potato chips, you need to first iterate over the array to find where the 99 potato chips are, and then remove them, and combine the array from the point where the 99 potato chips were removed. In a linked list, all you would need to do is point reference for value 12, to 37.

![_config.yml]({{ site.baseurl }}/images/LinkedLists.png)

Binary Search Tree

In this binary search tree, only values that are greater than the current value can be placed on the right side, whereas the lower values can only be placed on the left. It may not be initially intuitive how this makes looking for something particularly easier, but you'll soon realize what you're looking for will be on only one side of the tree, saving you the time that you would need to take looking on the other side. Also notice that in this large tree, there are small sub-trees, that you can also completely ignore. Try looking for 1, for example. As the tree gets larger and larger, the binary search tree makes our lives easier and easier.

![_config.yml]({{ site.baseurl }}/images/BinarySearchTree.png)

Hash Tables

Out of the all the data structures I mentioned above, hash tables is the most difficult to grasp. As the diagram below depicts, hash tables are created by associating the particular key of a key value pair to an index number of an array, the value is placed in that particular index. How this works is that the key is put through a "hasher function". The hasher function involves putting the key through processes, and a modulo operator of the size of the array. In the below example, we would put John Smith through a hasher function (let's say the hasher function converts the string to a number, 23) and performs a modulo operation on it based on the number of buckets we specify (7 in this case). 20 % 6 gets us a value of 2, which then places John Smith's phone number in that particular bucket. I'll leave it to your curiousity to look up hash table collisons, resizing, and its contribution to the creation of Objects in JavaScript.

![_config.yml]({{ site.baseurl }}/images/HashTable.png)