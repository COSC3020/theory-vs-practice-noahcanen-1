# Theory vs. Practice

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.

Speed depends on many things besides the asymptotic analysis; it is based on hardware,  Other processes running besides the program that you are testing the performance of, and Asymptotic analysis only focuses on an algorithm's growth rate, disregarding constant factors that can significantly impact performance, especially for smaller input sizes; an algorithm with a lower order of complexity might still be slower in practice due to larger constants.



- Suppose finding a particular element in a binary search tree with 1,000
  elements takes 5 seconds. Given what you know about the asymptotic complexity
  of search in a binary search tree, how long would you guess finding the same
  element in a search tree with 10,000 elements takes? Explain your reasoning.

  7 seconds

The typical time complexity of a binary search tree function is log n, so take log 1000 times it by your hardware and load you get out five seconds. Then you keep constant variables of the operating system and load increase the size of your tree to 10000, and you get out 6.6667 or rounding up 7 seconds

Here is how I did it mathematically

ln (1000) * x = 5 

x = 5/  ln (1000)

x = .723824

ln (10000) *  .723824 = 6.6667


- You measure the time with 10,000 elements and it takes 100 seconds! List 3
  reasons why this could be the case, given that reasoning with the asymptotic
  complexity suggests a different time.

1 you are using different hardware than you used on the 1st test. 2; you have increased the load on your hardware compared to the first Test.
3 Your tree is not balanced, so it does not correspond to the typical time complexity of a binary search tree. In the worst case of an unbalanced tree, you turned it into a linked list with a search time complexity of n. Assuming you have the same hardware and load as last time, it would take you 7238.24 seconds to search through all of the elements. Thus, you most likely have a somewhat balanced tree, or the thing you were looking for is near the top of your linked list tree.

I got how long it would take with a linked list by

n = 10000

10000 * .723824  = 7238.24 seconds


Add your answers to this markdown file.

I was able to do this assignment entirely on my own with help from Google AI because I just couldn't find an explanation you were happy with.

"I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice."
