## ATM Machine
### Problem Statement
There is an ATM machine. Initially, it contains a total of K units of money. N people (numbered
1 through N) want to withdraw money; for each valid i, the i-th person wants to withdraw 𝐴𝑖 ​ units of money.

The people come in and try to withdraw money one by one, in the increasing order of their indices. Whenever someone tries to withdraw money, if the machine has at least the required amount of money, it will give out the required amount. Otherwise, it will throw an error and not give out anything; in that case, this person will return home directly without trying to do anything else.

For each person, determine whether they will get the required amount of money or not.


### Python Solution

```python
def atm_machine(n, k, a):
    result = ""
    for i in range(n):
        if a[i] <= k:
            k -= a[i]
            result += "1"
        else:
            result += "0"
    return result
    

t = int(input())
for _ in range(t):
    n,k = map(int, input().split())
    a = list(map(int, input().split()))
    print(atm_machine(n, k, a))
```
