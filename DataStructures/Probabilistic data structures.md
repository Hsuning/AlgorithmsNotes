#BloomFilters
- They give you an answer that could be wrong but is probably correct:
	- False positives are possible: You’ve already even though you haven’t.
	• False negatives aren’t possible: You haven’t then you definitely haven’t
- Very little space

#HyperLogLog
- Use cases
	- count the number of unique searches performed by its users
	- count the number of unique items that users looked at today.
- approximates the number of unique elements in a set. It won’t give you an exact answer, but it comes very close and uses only a fraction of the memory a task like this would otherwise take.