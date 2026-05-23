# ETHERNET - frame

## Information
> Difficulty: Easy <br>
> Date: 22-05-2026
---
### Objective
Find the confidential data hidden in the ethernet frame.

---

### Explanation

### Step 1 : Analyze the binary data

**The ethernet frame payload contained binary data.**
<br>

![binary code](<images/Captura de tela 2026-05-22 215148.png>)

### Step 2: Convert binary to hexadecimal.
**Using CyberChef, the binary data was converted into hexadecimal format.**
<br>

![binary to hex](<images/Captura de tela 2026-05-22 215033.png>)

### Step 3: Decode the Base64.
**Using the Base64 decode operation in CyberChef, the original plaintext data/flag was recovered successfully.**
<br>

![hex to base64](<images/Captura de tela 2026-05-22 215115.png>)

![solveda](<images/Captura de tela 2026-05-22 215142.png>)
