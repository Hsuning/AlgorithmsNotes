#BinarySearch #Array 
- Input: sorted array => something we can compare
- Output: position where it's located or null if not found
- Description: Guess the middle number and eliminate half the remaining numbers every time, until you're left with only one.
- Ex: 100 -> 50 -> 25 -> 13 -> 7 -> 4 -> 2 -> 1
- Space complexity: $O(log_2 N)$

```
def binary_search(sorted_array, target):
    # take a sorted array and an item
    
    # low and high keep track of which part of the list you'll search in.
    low, high = 0, len(sorted_array)-1
    
    while low <= high:
        mid = (low+high)//2 # rounded down to when the sum is not an even number
        guess = sorted_array[mid]
        if target == guess:
            return mid # return position if the item is in the array
        if target > guess:
            low = mid + 1 # update low when guess is too low
        elif target < guess:
            high = mid - 1 # update high when guess is too high
        
    return None # return None if the tiem is not in the array
```
