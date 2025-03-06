# Theory vs. Practice

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.

Speed depends on many things besides the asymptotic analysis; it is based on hardware,  Other processes running besides the program that you are testing the performance of, and the secondary processes inside the program that are ignored in asymptotic analysis. For instance

T(n)= 3T(n/3) + 3

      3(3T(n/9) + 3) + 3
      
      9T(n/9) + 6
      
      27T(n/27) + 9
      
      ...
      
      3^iT(n/3^i) + i*3
    
for i = lg n

      nT(1) + lgn*3 = n + lgn*3 ∈ Θ(n)


This is the asymptotic analysis for a program. However, inside the asymptotic bounds Θ(n), the asymptotic complexity is n. To get to that, we must ignore the secondary process of lgn*3. However, that process still factors into the program's runtime.

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

For this assignment, I was able to do it entirely on my own.

"I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice."
