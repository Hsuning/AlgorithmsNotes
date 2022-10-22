#HashTable #Dictionary
- Search, insert, delete : O(1), instant
- #HashFunction: put in a string/int/float (any kind of data) and get back a number (index)
	- consistently maps a name to the same index
	- map different strings to different indexes
	- only returns valid indexes
- Use: 
	- create a mapping from one thing to another thing and look something up
	- filtering out duplicates
	- Caching/memorizing data instead of making your server do work
- Example: {"A":3, "B":2}
- Collision: get assigned a value to a slot that is already assigned to other value
- To avoid collisions (worst case performance): 
	- A low load factor = fewer collision, $\frac{Number Of Items}{Number Of Slots}$ estimate how many empty slots remain in your hash table, grater than 0.7 means you have more items than slots in your array => resize by creating a new array with double size and re-insert all the items
	- A good hash function: distribute values in the array evenly

#InvertedIndexed
- a #HashTable that stores a mapping (words, numbers) to its locations in a document or a set of documents
- 2 types:
	- record-level: stores the words and its list of references to documents
	- word-level: stores the positions of each word within a document
- Example: the word 'hi' is in document 1 starting at word 3, so has an entry (1, 3)
Word | (text, word within the text)
----- | -----
hi | (1, 3), (2, 12)
there | (1, 4)
here | (2, 6)
- Use cases:
	- directs you from a word to a document or a web page.
- Advantage:
	- fast full text searches, at a cost of increased processing when a document is added to the database.
	- easy to develop
	- the most popular data structure used in document retrieval systems, used on a large scale for example in search engines
- Disadvantage:
	- Large storage overhead and high maintenance costs on update, delete and insert.