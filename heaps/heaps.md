# HEAPS

# THEORY

+ [Video explanation of HEAP Watch Until 3. minute, ](https://www.youtube.com/watch?v=t0Cq6tVNRBA)
+ [Written explanation of HEAP + implementation in Python](https://www.askpython.com/python/examples/min-heap)

## COMPLEXITY

+ Removing operation O(log n)
+ Adding operation O(log n)
+ Heapifying n elements has complexity **n** not n log n
    + [Heap tutorial lecture](http://www.cs.umd.edu/~meesh/351/mount/lectures/lect14-heapsort-analysis-part.pdf)
    + [Heap explanation stack questions](https://stackoverflow.com/questions/9755721/how-can-building-a-heap-be-on-time-complexity)
    + [Overview](https://www.geeksforgeeks.org/time-complexity-of-building-a-heap/)


## MOVEMENT


+ left child = 2 * parent_idx 
+ right child = 2 * parent_idx + 1
+ parent_idx = child_idx // 2  # for 4,5 this is 2 , for 6,7 this is 3 


![](heaps.png)

# PROBLEMS

## PROBLEM https://leetcode.com/problems/kth-largest-element-in-an-array/

+ [Great - All Solutions in Video](https://www.youtube.com/watch?v=XEmy13g1Qxc&ab_channel=NeetCode)
+ [All Solution](https://www.interviewbit.com/blog/kth-largest-element-of-array/)
### FIRST SOLUTION

I need to hold only the K largest elements in this datastructure. 

1. Create maxHeap 
2. Add all elements 
3. Retrieve k elements 

Complexity of this this is n + k log n


### SIMPLER SOLUTION

1. Choose random element from list 
2. Partition based on it 
3. Is this element the k-th element (Yes)=> Finish 
4. No. 
   + If its index is less, then continue the algorithm in the larger side
   + If its index is less, then continue the algorithm in the smaller side 

Average complexity of this solution is n (Not log n as we have to compare the pivot with n elements) . 
Max can be n2


