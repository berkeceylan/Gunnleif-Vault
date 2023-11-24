### Definition:
- Method used to break into a password-protected system or decrypt a file by systematically entering every word in a predefined list of potential passwords (a "dictionary").
- Its like a brute force attack
- Advanced implementation = [[Rainbow Crack]]
### Operation:
1. **Creating a Dictionary** 
2. **Hash Generation**: 
	- The attacker hashes each word in the dictionary using the same [[Cryptographic Hash Functions]] as the system.
3. **Matching Hashes**: 
4. **Password Discovery**:
### Use of Salt in Defending Against Attacks:
- **Salting**: 
	- A robust defense against dictionary attacks is the use of a unique salt for each password.
	- A salt is random data added to the password before hashing. 
	- Increase the table size 
- **Effect of Salting**: 
	- Salting drastically increases the number of possible hashes, as each password-salt combination needs a unique entry in the dictionary. 
	- This makes the attack much more resource-intensive and time-consuming, especially when large or unique salts are used.
