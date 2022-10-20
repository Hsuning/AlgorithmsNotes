#DynamicProgramming
- Start by solving subproblems and builds up to solving the big problem
- Used to solve #knapsackproblem
- useful when you’re trying to optimize something given a constraint
- when the problem can be broken into discrete subproblems
- no single formula for calculating a dynamic-programming solution
- Every dynamic-programming algorithm starts with a grid
	- rows are the items and columns are conditions (like wieghts)
	- The values in the cells are usually what you’re trying to optimize. Like in knapsack proble, the value is the value of items that we can fit in under condition, like the grid can only contain item within 3 lb.
	- Each cell is a subproblem, so think about how you can divide your problem into subproblems.
	- we loop all the items and weights to fill in the value
	- the value that we filled in would be the max of 1) the previous max (row-1, same column) and value of current item + value of the remaing space (grid = 3, current item =2, find another item = 1 and add with current item)
	- At every iteration, we are storing the current max estimate, so the estimate can never get worse
- Condition
	- the order of the rows doesn't matter
	- fill in column-wise could make a difference for some problem
	- we can only choose to take an item or not. if we want to take a fraction of item, we have to use #GreedyAlgorithm 
	- only works when each subproblem is discrete—when it doesn’t depend on other subproblems
- Use
	- when you’re trying to optimize something given a constraint
	- when the problem can be broken into discrete subproblems, and they don’t depend on each other

#longestcommonsubsequence 
The number of letters in a sequence that the two words have in common
	- Find similarities in DNA strands
	- git diff
	- Levenshtein distance measures how similar two strings are
	- word wrap: figure out where to wrap so that the line length stays consistent