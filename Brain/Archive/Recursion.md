I know what recursion is pretty well no need to go into much detail about what it is but just in case he drops some good knowledge on how recursion commonly works for problem solving then I will note that here.

## Common Recursion Pitfalls

- No base case / base case is wrong
- Forgetting to return or returning the wrong thing
- Stack overflow error i.e. infinite loop

## Helper method recursion

Involves two functions. The outer function that gets called by the developer and an inner recursive function that calls itself. This is useful when you need to store the data that is processed during recursive calls. This is because if you define a data structure within a recursive function the values will be reset with every function call.

Note: I remember having to use this for one of the leetcode questions that I solved back in the day.