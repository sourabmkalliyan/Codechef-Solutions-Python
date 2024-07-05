## Candies
### Problem Statement
Abhi is a salesman. He was given two types of candies, which he is selling in N different cities.

For the prices of the candies to be valid, Abhi's boss laid down the following condition:
- A given type of candy must have distinct prices in all N cities.

In his excitement, Abhi wrote down the prices of both the candies on the same page and in random order instead of writing them on different pages. Now he is asking for your help to find out if the prices he wrote are valid or not.

You are given an array A of size 2N. Find out whether it is possible to split A into two arrays, each of length N, such that both arrays consist of distinct elements.

Both arrays can have distinct elements only if no element in the original array is repeated more than twice.

### Python Solution
```python
t = int(input())
for _ in range(t):
    n = int(input())
    a = list(map(int, input().split()))
    
    mymap = {}
    def candies():
        for i in range(2*n):
            if a[i] in mymap:
                if mymap[a[i]] >= 2:
                    return "NO"
                else:
                    mymap[a[i]] += 1
            else:
                mymap[a[i]] = 1
        return "YES"
                
    print(candies())
```
