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

<details>
  <summary>C++</summary>
</details>


<details>
  <summary>JAVA</summary>
  
</details>


# Second Question

<details>
    <summary>Python Code</summary>
  ```
  class Solution:
    def minProcessingTime(self, pT: List[int], tasks: List[int]) -> int:
        maxi = 0
        pT.sort()
        sortedTasks = sorted(tasks)
        j = len(sortedTasks) - 1
        count = 0
        ptIdx = 0
        maxinFour = 0
        num = pT[ptIdx]
        while j>=0:
            if count == 4:
                ptIdx += 1
                num = pT[ptIdx]
                count = 0
                if maxi <= maxinFour:
                    maxi = maxinFour
                maxinFour = 0
            maxinFour = max(maxinFour, num + sortedTasks[j])
            count += 1
            j-=1
        return max(maxinFour, maxi)
  ```
</details>


<details>
  <summary>C++</summary>
</details>


<details>
  <summary>JAVA</summary>
  
</details>


# Third Question

<details>
    <summary>Python Code</summary>

</details>


<details>
  <summary>C++</summary>

</details>


<details>
  <summary>JAVA</summary>

</details>



# Fourth Question

<details>
    <summary>Python Code</summary>

    class Solution:
    def maxSum(self, n: list[int], k: int) -> int:
        mod = 10**9 + 7
        binaryArr = [0] * 31
        for x in n:
            for i in range(31):
                if x & (1 << i):
                    binaryArr[i] += 1
        r = 0
        while sum(binaryArr) and k:
            c = 0
            k -= 1
            for i in range(31):
                if binaryArr[i]:
                    binaryArr[i] -= 1
                    c += 1 << i
            r += c * c
            r %= mod
        return r

</details>


<details>
  <summary>C++</summary>

</details>


<details>
  <summary>JAVA</summary>

</details>
