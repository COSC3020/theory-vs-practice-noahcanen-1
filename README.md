# Theory vs. Practice

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.

  Speed is dependent on a lot of things besides the complexity of code, it is based upon hardware, other processes running, and size of information

- Suppose finding a particular element in a binary search tree with 1,000
  elements takes 5 seconds. Given what you know about the asymptotic complexity
  of search in a binary search tree, how long would you guess finding the same
  element in a search tree with 10,000 elements takes? Explain your reasoning.

  7 seconds

The typical time complexity of a binary search tree function is log n so take log 1000 times it by your operating system and load you get out five seconds. Then you keep constant variables of the operating system and load increase the size of your tree to 10000, and you get out 6.6667 or rounding up 7 seconds

Here is how I did it mathematically

ln (1000) * x = 5 

x = 5/  ln (1000)

x = .723824

ln (10000) *  .723824 = 6.6667


- You measure the time with 10,000 elements and it takes 100 seconds! List 3
  reasons why this could be the case, given that reasoning with the asymptotic
  complexity suggests a different time.

1 you are using different hardware than you used on the 1st test. 2; you have increased the load on your hardware compared to the first Test.
3 Your tree is not balanced, so it does not correspond to the typical time complexity of a binary search tree.

Add your answers to this markdown file.
