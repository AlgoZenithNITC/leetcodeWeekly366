# leetcodeWeekly366

# First Question
<details>

  <summary>Python CODE</summary>
METHOD ONE 

```
class Solution:
    def differenceOfSums(self, n: int, m: int) -> int:
        intList = [i for i in range(1, n+1)]
        divisible = notDivisible = 0
        for num in intList:
            if num%m == 0:
                divisible += num
            else:
                notDivisible += num
        return notDivisible - divisible
```
METHOD 2

```

class Solution:
    def differenceOfSums(self, n: int, m: int) -> int:
        totalSum = n*(n+1)//2
        loop = n//m
        mSum = 0
        while loop:
            totalSum -= loop*m
            mSum += loop*m
            loop-= 1
        return totalSum - mSum
```

</details>
