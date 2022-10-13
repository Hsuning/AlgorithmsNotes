#CallStack #Recursion 
- when you call a function from another function, the calling function is paused in a partially completed state.
- All the values of the variables for that function are still stored in memory.
- A stack has two operations: push and pop.
```
def greet(name):   # 1. allocate a box of memory for this function
	print “hello, “ + name + “!”
	greet2(name)  # 2. allocat another box for this function, add on the top of 1
				  # return result, the stack get popped off, back to greet
	print “getting ready to say bye...”  
	bye() # 3. a box of this function is added on the top of the stack greet
		  # same as 2
	# nothing to do, pop off greet function
```
- you don’t have to keep track of a pile of boxes yourself—the stack does it for you
- but there’s a cost: saving all that info can take up a lot of memory
- The call stack can get very large, which takes up a lot of memory.