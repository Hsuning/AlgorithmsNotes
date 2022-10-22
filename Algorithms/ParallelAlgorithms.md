#ParallelAlgorithms
- There’s a parallel version of quicksort that will sort an array in O(n) time.
- the time gains aren’t linear
	- Overhead of managing the parallelism: expense for divide and merge
	- load balancing: how do you distribute the work evenly so both cores are working equally hard