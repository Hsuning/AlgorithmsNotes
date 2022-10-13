
#LinkedLIst 
- Elements are strewn all over, and one element stores the address of the next one
- Each item stores the address of the next item in the list. A bunch of random memory addresses are linked together
- Insertion: O(1), stick new item anywhere in memory and store the address with the previous item.
- Deletion: O(1) for already found item
- Reading: O(n), you don't know the address until you read all the items
- Better: inserting into the middle of a list, delete an element
- #SequentialAccess	

![[Pasted image 20221007225649.png]]
