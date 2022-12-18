# 2498 Frog Jump II
[链接](https://leetcode.com/problems/frog-jump-ii/)

### Problem
You are given a 0-indexed integer array stones sorted in strictly increasing order representing the positions of stones in a river.

A frog, initially on the first stone, wants to travel to the last stone and then return to the first stone. However, it can jump to any stone at most once.

The length of a jump is the absolute difference between the position of the stone the frog is currently on and the position of the stone to which the frog jumps.

More formally, if the frog is at `stones[i]` and is jumping to `stones[j]`, the length of the jump is `|stones[i] - stones[j]|`.
The cost of a path is the maximum length of a jump among all jumps in the path.

Return the minimum cost of a path for the frog.


### Examples

![image](https://assets.leetcode.com/uploads/2022/11/14/example-1.png)

$$ \sum_{i=1}^{n}i=\frac{n(n+1)}{2} $$

### 日本語説明


### code
```python
class Solution:
    def maxJump(self, stones: List[int]) -> int:
        ans = 0
        last_stone = 0
        for i in range(1, len(stones), 2):
            ans = max(ans, stones[i] - last_stone)
            last_stone = stones[i]
        last_stone = 0
        for i in range(0, len(stones), 2):
            ans = max(ans, stones[i] - last_stone)
            last_stone = stones[i]
        return ans
```

# code

```python
print("hello")
```
[test link](#2498-Frog-Jump-II)