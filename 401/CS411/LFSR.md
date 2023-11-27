## Linear Feedback Shift Registers(LFSR):
## Definition:
- Is a sequential shift register with linear feedback
	- Atomic element is Flip-Flop
- Used for key generation process in [Stream Cipher](Stream%20Cipher.md)
### Operation:
- $\large C(x)$ = Feedback Polynomial
- $\large C(x) = 1 + c_1x +c_2x^2+ \ldots + C_Lx^L$
-  $\large L$ = amount of flip-flops
- $\large2^L$ = number of sequences we can create
- If $C(x)$ is a [Primitive Polynomials](Primitive%20Polynomials.md) -> LSFR have max period of $\large 2^{L}-1$
	-  Only LSFR's with primitive polynomials yield max length sequences 
 ![](LSFR.png)
### Attack:
- By using [BMA](BMA.md) we can calculate 2 things
	- **[Linear Complexity](Linear%20Complexity.md) of the Sequence** (the length of shortest LFSR)
	- **Feedback Polynomial** ($C(x)$)
	- with these two things we can produce the sequence and break the Stream Cipher
- BMA also can validate the security of LSFR by checking it's randomness
- Cost of Correlation Attack: $\prod_{i=1}^{n} (2^{L_i} - 1)$
- Cost of Brute Force Attack: $\sum_{i=1}^{n} (2^{L_i} - 1)$
### Types:
- **Nonlinear Combination Generator**:
	- Use multiple LSFR
	- Combiner function must be:
		- Balanced
		- No statistical dependencies
		- Highly nonlinear
	- Example: $\large F(x_1, x_2, x_3, x_4, x_5) = 1 \oplus x_2 \oplus x_3 \oplus x_4 x_5 \oplus x_1 x_3 x_4 x_5$
		- nonlinear order of F is  4
	![](NCG.png)
- **Geffe Generator**:
	- Use 3 LSFR
	- $\large F(x_1, x_2, x_3) = (x_1 \land x_2) \oplus (\neg x_1 \land x_3)$
	- Correlation attack can be used to break the Stream cipher if key-stream was created by Geffe generator
		- There is a correlation between x1 and z, x2 and z, x3 and z 
		- Since correlation -> $\large P(z =x_i) = 3/4$
	![](GeffeGenrator.png)
- **Shrinking Generator**
	-  LSFR can be clocked by the output of another LSFR
	- Increase the linear complexity
	![](ShirinkingGenerator.png)