# Fold

Also called reduce in some languages, a fold goes through elements of a list and returns a single value. Folds require a function passed to it, which will be applied to each element of the list. This function can be a named, or an anonymous function. Anonymous functions are also called lambda functions. Key to learning to use folds is thinking of what the function you will pass to fold takes as and argument, and what it should return. You can fold from left to right through a list, `List.foldl`, or from right to left, `List.foldr`. In general you should prefer `foldl `over `foldr `because it is more efficient.

## Problems to solve using List.foldl
[Problem 5](../p/p05.md) - Use `List.foldl` to reverse a list. Think about the function you want to pass to `foldl`. Its first argument will be the same type as the elements of the list you folding. The second argument will be the same type that we want to return. So, what do we want to return? In this case our goal is to arrive as a List, so let's return a List.
Now we know the form of the function we want to pass to `List.foldl`, it should be of this type.

`foo : a -> List a - > List a`

Before you can write a function that will build our reversed list, is there a built in function you can use? What functions do we know that have this type? (Remember, operators are functions too!)

[Problem 1](../p/p01.md) - Use `foldl` to find the last element of a list.  

[Problem 4](../p/p04.md) - Count the elements of a list. 

[Problem 8](../p/p08.md) - Remove duplicates from a list.

[Problem 14](../p/p14.md) - Duplicate list elements.

[Problem 57](../p/p57.md) - Construct a binary search tree.



