# Arrays

Arrays are the simplest data structure type. </br>

The data are stored adjacent to each other in the array. </br>

Arrays operations. </br>


There are two types of arrays Static and Dynamic arrays. </br>
In language like C/C++, static arrays are used and </br>
JS, python uses dynamic arrays.


#### Static arrays
* Need to decide ahead of time the number of items that can hold inside arrays.
* More control over memory.
* Faster 
* Can be found in lower level languages like C 

``` C
int arrys[3] = {1,2,3};
```

#### Dynamic arrays
* Dynamic arrays allow us to rebuild and copy the arrays at a new location with more memory if we want to add more items inside.
* They automatically allocate the memory location when adding more items cause of automatic resizing.
* The machine take care off everything for you
* So it take more 
* Can be found in higher level languages like python, JS
* Slower.

**Append operation can be  0(n) in some case. Because it has to loop over all item inside array, copy it and resize the original arrays.**


##### How this append(push) operation work?

```
In case of a four block of array, adding with 4 more items .
(0x1) [1, 2, 3, 4]

(0x1) [1, 2, 3, 4]  << loop all over each of array
(0x1) [1, 2, 3, 4]  << Copy it and move to a different location.
\/
(0x4)  [1, 2, 3, 4,  ,  ,  ,  ]  << moved it to a different location. Now it become 8 block of space and can add more item. 
(question: what happened to the original memory stored location? Space?)
```

``` python
array = [1,2,3]
array.append(4) # << adding more items

array
>>> [1,2,3,4]  << the result that copy and store at a new location.

[1,2,3]  << copy

[1,2,3] + 4  << add new item into original array

[1,2,3,4]  << store at a new location (new area of memory)

Array is now [1,2,3,4]
```

### Big O analysis
|Operations| Time Complexity|
|----------|------|
|Look up   | 0(1) |
|Push      | 0(1)* |
|Insert    | 0(n) |
|Delete    | 0(n) |



In JS
Arrays operations such as unshift which added items from front are 0(n).

### Fun facts
Python: List.
JS: Objects
Java: 
C/C++/ C#:


