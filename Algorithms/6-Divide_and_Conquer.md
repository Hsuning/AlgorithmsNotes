#DivideandConquer #DaC
- Description:
	- Break a problem down into a smaller pieces
	- If you’re using D&C on a list, the base case is probably an empty array or an array with one element.
	- Figure out the base case. This should be the simplest possible case.
	- Divide or decrease your problem until it becomes the base case.
```
def divide_and_conquer(h, w):
    # Simple case: one side is a multiple of the other side
    if w > h:
        h, w = w, h
    h = h%w 
    # divide until no remainder
    if h == 0: 
        return w
    
    return divide_and_conquer(h, w)

def binary_search(arr, target):
    if not arr:
        return -1
    elif len(arr) == 1:
        return -1 if arr[0] != target else target
    
    mid = len(array) // 2
    
    if arr[mid] == target:
        return target
    elif arr[mid] > target:
        return binary_search(arr[:mid], target)
    else:
        return binary_search(arr[mid+1:], target)
```
