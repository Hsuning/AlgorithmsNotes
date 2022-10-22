
#MapReduce #DistributedAlgorithm
- Speed up the time requires to a lot of work by using more machines.
- #Map:
	- if you had 100 machines, map could automatically spread out the work across all the items, so you would be processing 100 items at a time, and the work would be ~(N/100) faster
	- it takes an array and applies the same function to each item in the array
	- ```arr2 = map(lambda x: 2 * x, arr1)```
- #Reduce:
	- reduce a whole list of items down to one item
	- transform an array to a single item


