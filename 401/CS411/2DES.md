#### Double Data Encryption Standard (Double DES )
### Description:
* Also known as Double DES
* Derived from the Data Encryption Standard ([[DES]]) block cipher
* Double DES applies the DES algorithm twice, with two different keys = $K_{1}$ and $K_{2}$
* Effective key length = 57 bits
* If there are N keys the storage requirement is 2N
### Procedure:
1. **Encryption**:
    - Take plaintext block -> encrypt it using the first DES key ($K_{1}$)
    - Take output from the first encryption -> encrypt it again using the second DES key ($K_{2}$)
2. **Decryption**:
    - Take ciphertext block -> decrypt it using the second DES key ($K_{2}$)
    - Take  output from the first decryption -> decrypt it again using the first DES key ($K_{1}$)
### Security:
* The key bits may seem as 112 bits but because of [[Meet-in-the-middle Attack]] effective key size is 57 bits.
* Not considered as secure Therefore [[3DES]] introduced.