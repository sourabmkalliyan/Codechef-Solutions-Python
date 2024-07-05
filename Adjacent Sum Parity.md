## Adjacent Sum Parity
### Problem Statement
Chef has an array A of length N.

Chef forms a binary array B of length N using the parity of the sums of adjacent elements in A. Formally,
- 𝐵𝑖 =(𝐴𝑖 + 𝐴𝑖+1) %  2 for 1≤i≤N−1
- 𝐵𝑁 =(𝐴𝑁+ 𝐴1) %  2

Here x%y denotes the remainder obtained when x is divided by y.

Chef lost the array A and needs your help. Given array B, determine whether there exists any valid array A which could have formed B.

### Python Solution
```python
t = int(input())

for _ in range(t):
    n = int(input())
    b = list(map(int, input().split()))
    
    if b.count(1)%2 == 0:
        print("YES")
    else:
        print("NO")
```
