---
title: Level One Algorithms
date: "2018-03-01T22:12:03.284Z"
---

1.  Simple Search (stupid search)

With each guess in the list of elements, you’re eliminating only one number. If the number is at the end of list then it could take you the length of the list - 1 tries to guess the position of the element you are trying to find.

2.  Binary Search

Whether you are searching for a person in the phone book, or a word in the dictionary. Even if a web application is searching a username in the database when the user signs, all of these problems are search problems and all of these cases use the sam algorithm to solve it, _binary search_.

Binary search is an algorithm, where the input is a sorted list of elements. If the element you are looking for is in that list, binary search returns the position of the element where it’s located. Otherwise, binary search returns _null_

3.  Example 1

I’m thinking of a number between 1 and 100.
You have to guess the number in the fewest tries possible. With every guess your algorithm will tell you if your guess is too high or too low, or correct.

**Important: Is your guess is too high or too low, or correct.**

For the example problem we should start with 50 if it is too low then you juste limited half the numbers! Now you know that 1-50 are too low, and so your next guess would be 75. With binary search you eliminate half the numbers every time. Thats is it, let me repeat it again with binary search you eliminate have the numbers every time.

4.  Example 2

Suppose you are looking for a word in the dictionary. The dictionary has 240,000 word. In the worst case, how many steps do you think binary search will take?

To solve the problem with binary search you cut the number of words in half until you’re left with only one word.

240k --> 120k --> 60k --> 30k --> 15k -->7.5k --> 3,750 --> 1,875 --> 938 --> 469 --> 235 --> 118 --> 59 -->30 --> 15 --> 8 --> 4 --> 2 --1 BINGO it will take you 18 steps.

**In general for a list of n, binary search will take you log₂n steps.**
