#### Please add your answers to the ***Analysis of  Algorithms*** exercises here.

## Exercise I

a) Since there is one loop, it is O(n). 


b) This pseudocode contains a nested loop. We need to multiply O(n) * O(n) which results in O(n^2).


c) This is a recursive call. It resembles a loop. I think it is O(n) because it will eventually reach the base case.

## Exercise II

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