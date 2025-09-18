# Huffman-Shannon_fano
# Aim:
Consider a discrete memoryless source with symbols and statistics {0.55,0.15,0.15,0.1,0.05} for its output. 
Apply the Huffman and Shannon-Fano to this source. 
Show that by drawing the tree diagram, and 
Calculate the average code word length, entropy, variance, redundancy, and efficiency.
# Tools Required:
Google Colab

Laptop

# Program:
```
p = [0.55,0.15,0.15,0.1,0.05]
# Corresponding Huffman/Shannon-Fano code lengths
lk = [1,3,3,3,3]
n = len(p)

# Average Codeword Length
L = sum(p[k] * lk[k] for k in range(n))

# Entropy
hs = sum(p[k] * math.log(1 / p[k], 2) for k in range(n))
hs = round(hs, 3)

# Efficiency
eff = round(hs / L, 3)

# Redundancy
red = round(1 - eff, 3)

# Variance
var = sum(p[k] * (lk[k] - L) ** 2 for k in range(n))
var = round(var, 3)

# Output
print(f"Average Codeword Length is : {L}")
print(f"Entropy is : {hs}")
print(f"Efficiency is : {eff * 100}%")
print(f"Redundancy is : {red}")
print(f"Variance is : {var}")

```
# Calculation:

 Practical Calculation:
 
<img width="869" height="835" alt="image" src="https://github.com/user-attachments/assets/d8cf38fd-1019-4a75-9fdf-70ca7e93e368" />

 Theortical Calculation:

<img width="1075" height="825" alt="image" src="https://github.com/user-attachments/assets/be964117-8e80-4f8b-b15a-f7d85956d8d8" />

<img width="502" height="833" alt="image" src="https://github.com/user-attachments/assets/e3a8cc96-4f7b-482e-a6c4-cad5881c3bc9" />

# Output

<img width="869" height="835" alt="image" src="https://github.com/user-attachments/assets/3bda15cf-6016-47d0-ae4a-f9f05237417e" />

# Results:
Thus the discrete memoryless source with symbols and statistics {0.55,0.15,0.15,0.1,0.05} for its output was successfully calculated
