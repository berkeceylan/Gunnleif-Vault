### **Definition:**
- Rainbow Crack (Rainbow Table attack) is a type of cryptographic attack that's used to crack password hashes.
- It's an advanced version of a [Dictionary Attack](Dictionary%20Attack.md) 
- Effective against systems that use unsalted cryptographic hash functions for password storage.
- Based on Rainbow Tables:
	-  Large precomputed tables containing hash values for every possible combination of characters in a password
	- Use and try to reverse [Cryptographic Hash Functions](Cryptographic%20Hash%20Functions.md)
### How Rainbow Crack Works:
1. **Pre-computation**: 
	- Rainbow Tables are generated for a specific hash function and character set.
		- Hashing every possible password combination and storing the results in a table
2. **Storage Optimization**: 
	- Use a chain reduction method to reduce the size of the table.
	- Create chains of alternate hash and plaintext values
3. **Attack Execution**: 
	- If a matching hash is found, the original password can be deduced.
### Cons:
- **Large Storage Requirement**: 
	- Rainbow Tables are enormous in size, especially for complex and long passwords. 
	- This makes them impractical for some applications.
- **Use of Salts**: 
	- Salting passwords counteracts Rainbow Table attacks. 
	- Precomputed tables like Rainbow Tables become ineffective.
