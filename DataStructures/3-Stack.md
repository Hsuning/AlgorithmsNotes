#Stack #Recursion 
- LIFO data structure: Last In, First Out
- Item that are added to the list last will be poped first.
	- push: add item
	- pop: get item

#CallStack
- When you call a function from another function, the calling function is paused in a partially completed state. All the values of the variables for that function are still stored in memory.

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
- Advantage: You don’t have to keep track of a pile of boxes yourself—the stack does it for you
- Disadvantage: saving all that info can take up a lot of memory. The call stack can get very large, which takes up a lot of memory.