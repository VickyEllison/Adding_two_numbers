# Adding_two_numbers
You are given two non-empty linked lists representing two non-negative integers. The digits are stored in reverse order and each of their nodes contain a single digit. Add the two numbers and return it as a linked list.

You may assume the two numbers do not contain any leading zero, except the number 0 itself.
**Solution** 

`Intuition`

Keep track of the carry using a variable and simulate digits-by-digits sum starting from the head of list, which contains the least-significant digit.
[![112121.png](https://i.postimg.cc/nhFM3VGJ/112121.png)](https://postimg.cc/qzFkRTFb)

*Figure 1. Visualization of the addition of two numbers: 342 + 465 = 807342+465=807.
Each node contains a single digit and the digits are stored in reverse order.*
**Algorithm**
Just like how you would sum two numbers on a piece of paper, we begin by summing the least-significant digits, which is the head of l1 and l2. Since each digit is in the range of 0…9, summing two digits may "overflow". For example 5 + 7 = 12. In this case, we set the current digit to 2 and bring over the *carry* = 1 to the next iteration. *carry* must be either 0 or 11 because the largest possible sum of two digits (including the carry) is 9 + 9 + 1 = 19.



