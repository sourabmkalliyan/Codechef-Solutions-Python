## TCS Examination
### Problem Statement
Two friends, Dragon and Sloth, are writing a computer science examination series. There are three subjects in this series:
DSA, TOC, and DM. Each subject carries 100 marks.

You know the individual scores of both Dragon and Sloth in all 3 subjects. You have to determine who got a better rank.

The rank is decided as follows:

- The person with a bigger total score gets a better rank
- If the total scores are tied, the person who scored higher in DSA gets a better rank
- If the total score and the DSA score are tied, the person who scored higher in TOC gets a better rank
- If everything is tied, they get the same rank.

### Python Solution
```python
t = int(input())

for _ in range(t):
    dDSA, dTOC, dDM = map(int, input().split())
    sDSA, sTOC, sDM = map(int, input().split())
    
    dTotal = dDSA + dTOC + dDM
    sTotal = sDSA + sTOC + sDM
    
    d = "DRAGON"
    s = "SLOTH"
    
    if dTotal > sTotal:
        print(d)
    elif sTotal > dTotal:
        print(s)
    else:
        if dDSA > sDSA:
            print(d)
        elif sDSA > dDSA:
            print(s)
        else:
            if dTOC > sTOC:
                print(d)
            elif sTOC > dTOC:
                print(s)
            else:
                print("TIE")
```
