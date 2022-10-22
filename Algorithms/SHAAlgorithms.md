#SHAAlgorithms
- Given a string, SHA generates a hash for that string. The hash is just a short string
- **locality insensitive**: if you change one word in the string, the hash would be totally different
- Algorithms: SHA-0, SHA-1, SHA-2, and SHA-3. The first 2 have some weakness, so use the last two. However, they are not secure enough, need to consider bcrypt/scrypt/PBKDF2
	- If computationally efficient, a hash algorithm such as SHA-512 would be inappropriate for a password hash
	- Bcrypt is intentionally hard to calculate in terms of CPU cycles
	- scrypt is difficult in terms of memory needed.
- #HashTable : from string to string
- Use cases:
	- whether two files are the same
	- checking passwords: compare strings without revealing what the original string was. You get a string with hash, but you can't get the origin string from the hash

#Simhash
- **locallity sensitve** 
- If you make a small change to a string, Simhash generates a hash that’s only a little different.
- Use cases:
	- compare hashes and see how similar two strings are, which is pretty useful
	- detect duplicates while crawling the web
	- see whether a student was copying an essay from the web