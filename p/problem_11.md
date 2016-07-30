# Problem 11
Write a function to run length encode a list, but instead of using a tuple as in problem 10, use a union data type. Define to represent either a single element or a run of multiple identical element.

##Example
```
rleEncode ['a', 'a', 'a', 'b', 'c', 'c', 'd', 'e', 'e', 'e', 'e', 'e']
```
Result

[Run 4 'a', Single 'b', Run 2 'c', Single d', Run 6 'e']

#Unit Test
```
import Html exposing (text)
import List 


type RleCode a = -- define the type here


rleEncode : List a -> List RleCode a
rleEncode list =
    -- your implementation here
    []
            

main =
    text
        (if (test) then
            "Your implementation passed all tests."
         else
            "Your implementation failed at least one test."
        )



test : Bool
test =
    List.all (\(result, expect) -> result == expect)
        [ ( rleEncode [1, 1, 1, 1, 2, 5, 5, 2, 1], 
            [Run 4 1, Single 2, Run 2 5, Single 2, Single 1]
          )
        , ( rleEncode [2, 1, 1, 1], [Single 2, Run 3 1] )
        , ( rleEncode [2, 2, 2, 1, 1, 1], [Run 3 2, Run 3 1])
        , ( rleEncode [1], [Single 1] )
        , ( rleEncode [], [])
        ]
        && List.all (\(result, expect) -> result == expect)
            [ ( rleEncode [ "aa", "aa", "aa" ], [ Run 3 "aa" ] )
            , ( rleEncode [ "aab", "b", "b", "aa" ], 
                [ Single "aab", Run 2 "b", Single "aa" ] 
              )
            ]

```