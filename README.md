# MTH 102: Calculus and Analytic Geometry II

## Chapter 0: Mathematical Induction
This chapter explains **mathematical induction**, a proof technique used to prove statements for all natural numbers.

---

### What is Mathematical Induction?
- Mathematical induction proves a sequence of statements \( S_1, S_2, S_3, \dots \) for all natural numbers \( n \).
- Think of it as a row of dominoes:
  - Prove the first domino falls (\( S_1 \)).
  - Prove that if one domino falls (\( S_k \)), the next one falls (\( S_{k+1} \)).

#### Key Steps:
1. **Basis Step**:
   - Verify the first statement (e.g., \( S_1 \)) is true.
2. **Inductive Step**:
   - Assume \( S_k \) is true (inductive hypothesis).
   - Prove \( S_k \implies S_{k+1} \).

---

### Example Proofs

#### Example 1: Sum of the First \( n \) Odd Natural Numbers
**Statement:** \( 1 + 3 + 5 + \dots + (2n-1) = n^2 \)

**Proof:**
1. **Basis Step**:
   - For \( n = 1 \):
     \[ 1 = 1^2 \]
     - The statement is true for \( n = 1 \).
2. **Inductive Step**:
   - Assume \( 1 + 3 + 5 + \dots + (2k-1) = k^2 \) (inductive hypothesis).
   - Prove \( 1 + 3 + 5 + \dots + (2(k+1)-1) = (k+1)^2 \).
     \[
     1 + 3 + 5 + \dots + (2k-1) + (2(k+1)-1)
     = k^2 + (2(k+1)-1)
     = k^2 + 2k + 1
     = (k+1)^2
     \]
   - Therefore, the statement is true for \( k+1 \).

By induction, \( 1 + 3 + 5 + \dots + (2n-1) = n^2 \) for all \( n \in \mathbb{N} \).

---

#### Example 2: Sum of Powers of 2
**Statement:** \( 2^1 + 2^2 + 2^3 + \dots + 2^n = 2^{n+1} - 2 \)

**Proof:**
1. **Basis Step**:
   - For \( n = 1 \):
     \[
     2^1 = 2^{1+1} - 2 = 4 - 2 = 2
     \]
     - The statement is true for \( n = 1 \).
2. **Inductive Step**:
   - Assume \( 2^1 + 2^2 + \dots + 2^k = 2^{k+1} - 2 \) (inductive hypothesis).
   - Prove \( 2^1 + 2^2 + \dots + 2^k + 2^{k+1} = 2^{k+2} - 2 \):
     \[
     (2^1 + 2^2 + \dots + 2^k) + 2^{k+1} = (2^{k+1} - 2) + 2^{k+1}
     = 2 \cdot 2^{k+1} - 2
     = 2^{k+2} - 2
     \]
   - Therefore, the statement is true for \( k+1 \).

By induction, \( 2^1 + 2^2 + \dots + 2^n = 2^{n+1} - 2 \) for all \( n \in \mathbb{N} \).

---

#### Example 3: Divisibility Proof
**Statement:** \( 5 \mid (n^5 - n) \) for all non-negative integers \( n \).

**Proof:**
1. **Basis Step**:
   - For \( n = 0 \):
     \[ n^5 - n = 0^5 - 0 = 0 \]
     - Clearly, \( 5 \mid 0 \).
2. **Inductive Step**:
   - Assume \( 5 \mid (k^5 - k) \) (inductive hypothesis), i.e., \( k^5 - k = 5a \) for some \( a \in \mathbb{Z} \).
   - Prove \( 5 \mid ((k+1)^5 - (k+1)) \):
     \[
     (k+1)^5 - (k+1) = k^5 + 5k^4 + 10k^3 + 10k^2 + 5k + 1 - (k + 1)
     = (k^5 - k) + 5(k^4 + 2k^3 + 2k^2 + k)
     \]
     - Since \( k^5 - k = 5a \), \( 5 \mid ((k+1)^5 - (k+1)) \).

By induction, \( 5 \mid (n^5 - n) \) for all \( n \geq 0 \).

---

#### Example 4: Factorial Inequality
**Statement:** \( n! > 2^n \) for all integers \( n \geq 4 \).

**Proof:**
1. **Basis Step**:
   - For \( n = 4 \):
     \[
     4! = 24 > 2^4 = 16
     \]
2. **Inductive Step**:
   - Assume \( k! > 2^k \) (inductive hypothesis).
   - Prove \( (k+1)! > 2^{k+1} \):
     \[
     (k+1)! = (k+1) \cdot k! > (k+1) \cdot 2^k
     \]
     - Since \( k \geq 4 \), \( k+1 \geq 5 \), so:
       \[
       (k+1) \cdot 2^k > 2 \cdot 2^k = 2^{k+1}
       \]

By induction, \( n! > 2^n \) for all \( n \geq 4 \).

---

### Exercises
Prove the following assertions using mathematical induction:
1. \( 1 + 2 + 3 + \dots + n = \frac{n(n+1)}{2} \) for \( n \geq 1 \).
2. \( 1^2 + 2^2 + 3^2 + \dots + n^2 = \frac{n(n+1)(2n+1)}{6} \) for \( n \geq 1 \).
3. \( 1 + 2 \cdot 2 + 3 \cdot 2^2 + \dots + n \cdot 2^{n-1} = (n-1) \cdot 2^n + 1 \) for \( n \geq 1 \).
4. \( 1^3 + 2^3 + 3^3 + \dots + n^3 = \left( \frac{n(n+1)}{2} \right)^2 \) for \( n \geq 1 \).
5. \( 2^n > n^2 \) for \( n \geq 5 \).

---
