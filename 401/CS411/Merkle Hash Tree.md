## Merkle Trees

### Definition:
- Named after Ralph Merkle
- Used to efficiently summarize and verify the integrity of large sets of data.
- The tree is constructed using [Cryptographic Hash Functions](Cryptographic%20Hash%20Functions.md) 
	- Rely on cryptographic hash functions, such as MD5, SHA-1, SHA-2, or SHA-3, to hash the data blocks and non-leaf nodes.
### Properties:
- **Hierarchical Structure**:
	- It is a binary tree 
- **Hash-Based**: 
	- Each leaf node is a hash of a data block, while each non-leaf node is a hash of its children's hashes.
- **Efficient Verification**:
	- Allows for efficient and quick verification of large data sets.
- **Tamper-Evident**: 
	- Any change in the data alters the root hash, signaling data modification.
### Operation:
1. **Data Segmentation**: 
	- Data is divided into blocks.
2. **Hashing Leaves**: 
	- Each block of data is hashed using a cryptographic hash function, forming the leaf nodes.
3. **Building the Tree**: 
	- Non-leaf nodes are created by hashing the concatenation of their children's hashes. This process is repeated up the tree.
4. **Merkle Root**: 
	- The root of the tree is a single hash that uniquely represents all of the data in the tree.
![](MerkleHashTree.png)
