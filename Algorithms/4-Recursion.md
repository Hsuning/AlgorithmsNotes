#Recursion #RecursiveMethod 
- Use: #Stack 
- Recursion is when a function calls itself
- Description: a recursive function has two parts
	- base case: when the function doesn't call itself again. So function won't end up in an infinite loop = > RecursionError: maximum recursion depth exceeded
	- recursive case: when the function calls itself
- Loops may achieve a performance gain for your program. 
```
def countdown(i):
    if i <= 0: # Base case
        return "ok"
    else: # Recursive case
        print(i)
        return countdown(i-1)
```
- #TailRecursion: a recursive function in which the recursive call is the last statement that is executed by the function. So basically nothing is left to execute after the recursion call.
```
def fact(n):
	if n == 0:
		return 1
	return n * fact(n-1)

def fact(n, a=1):
	if n <= 1:
		return a
	return fact(n-1, n*a) #Tail Recursion
```
