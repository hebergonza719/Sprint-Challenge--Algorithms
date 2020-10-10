# Analysis of Algorithms

## Exercise I

Give an analysis of the running time of each snippet of
pseudocode with respect to the input size n of each of the following:

```python
a)  a = 0
    while (a < n * n * n):
      a = a + n * n
```


```
b)  sum = 0
    for i in range(n):
      j = 1
      while j < n:
        j *= 2
        sum += 1
```

```
c)  def bunnyEars(bunnies):
      if bunnies == 0:
        return 0

      return 2 + bunnyEars(bunnies-1)
```

## Exercise II

Suppose that you have an n-story building and plenty of eggs. Suppose also that an egg gets broken if it is thrown off floor f or higher, and doesn't get broken if dropped off a floor less than floor f. Devise a strategy to determine the value of f such that the number of dropped + broken eggs is minimized.

Write out your proposed algorithm in plain English or pseudocode AND give the runtime complexity of your solution.

1. determine half of the amount of floors
2. check if egg breaks in half
2a.
if egg breaks
  go down a level
  check if breaks
    if it breaks
      go to half of current floor and bottom floor
    if it doesn't break
      return floor
  repeat loop
2b.
if egg doesn't break
  go up to half of current floor and top
  check if egg breaks
    if it breaks
      go down a level
      if it breaks
        go to half of current floor and previous floor
      if it doesn't break
        return floor
    repeat loop

The runtime complexity is Θ(log(n)). In my planning, I noticed it had similarities to a binary search tree which has a runtime complexity of Θ(log(n)).
