
#BigO
- Express the runtime of an algorithm
	- How fast an algorithm is in a worst case scenarios
	- How quickly the run time of an algorithm increases as the size of the input increases.
	- Algo speed is in growth of the number of operations
- Constant: 
	- O(n) is actually O(c x n), c is some fixed amount of time that the algorithm takes, called  a constant. 
	- If two algorithms have different Big O times, the constant doesn’t matter
	- Sometimes the constant can make a difference. Quicksort has a smaller constant than merge sort. So if they’re both O(n log n) time, quicksort is faster.
- Type: 
	- $O(log n)$, logarithm time or log time. The flip of exponentials. $log_{10} 100$ = How many 10s do we multiply together to get 100. The answer is 2: 10x10. Example: Binary search. 
	- $O(n)$, linear time. The maximum number of guesses is the same as the size of the list. Example: Simple search.
	- $O(n * log n)$. Example: A fast sorting algorithm, like quicksort
	- $O(n^2)$. Example: A slow sorting algorithm, like selection sort
	- $O(n!)$. Example: A really slow algorithm, like the traveling salesperson
	- O(1): constant time, It means the time taken will stay the same, regardless of how big the hash table is.
![[Pasted image 20221008131037.png]]
- You usually ignore that constant, because if two algorithms have different Big O times, the constant doesn’t matter. But sometimes the constant can make a difference.
![[Pasted image 20221008131706.png]]