# Hashtable


## Hash functions 
* Hash functions generates the hash keys into hash value. <br/>
* Hash functions are idempotent. <br/>
* Idempotent: a properties that always return the same result for the same input. <br/>

## Hash map
* Hash function generates the hash key to hash value. <br/>
* The generated hash values become the index position in the data storage array. <br/>
* And the (key, value) pair is stored inside data structure with  hash values index position. <br/>

```python

Hash_Table = [None] * size
Address = Hash_Function(keys)
Hash_Table[Address] = []
Hash_Table[Address].append([keys, values])
```

## Hash Collision
* The hash function is based on the size of storage array. **(in case only two elements can be stored in the storage array, the hash function cannot be generated index position more than two. )**
* Therefore, same hash values key may be generated for several items **(in case store items become more than two.)**
* In that case, different values with different hash key may be stored under same `bucket` hash values index. 
* This is called hash collision. <br/>
* Hash collison are unavoidable with limited data space and resources.
* There are several methods to solve hash collision. One of the example is **Separate Chaining** method which store collided values as `linked lists` in the same index. <br/>
**Note: In most language this collided values are stored as `linked lists` a type of data strucuture. For example, an array of size(2) as below.**

```python
{["a" , 1] , [ ["b" , 2], ["c" , 3] , … , ["j" , 7] ]} 
```

## Big O analysis

#### Time Complexity
* Normally, Hashtable cost `O(1)` for most operations, `insert`, `lookup`, `delete` or `remove`, `search` or `access`.
* If there is Hash Collison, some operations, such as search become slow down and it become theoretically `O(n/k)` where k is the size of hashtable and generally can be assumed as `O(n)` .

**` Average Case: O(1)`**
**` Worst Case: O(n)`**

#### SpaceComplexity
A reasonable hashtable cost O(n) space Complexity.

**`Average Case: O(n)`**
**`Worst Case: O(n)`**


### Fun facts
* Python: Dictionary.
* JS: Objects
* Java: 
* C/C++/ C#:

### Questions
Does hash function slow down the data structure operations?

### Sets
``` python
{1, 2, 3, 4}
```
* Set:  in python, set are based on Hash tables.
* Set are unordered collections of items.
* Set items cannot be referred by index values. ``` { set[i] } ```
* Set elements are immutable, unchangeable.
* Set cannot be append new items.
* Set items are unique and don't allow duplicate items. `{1, 1, 1, 2, 2, 2, 2} >> {1, 2}`
* Set are `O(1)`.


## Hash Table with Python (Dictionary)

``` python
dictionary = { 
 -1 : "-1"
  1 : 'hello', 
  'two' : True, 
  '3' : [1, 2, 3], 
  'four' : {'fun': 'addition'}, 
  5.0 : 5.5, 
  'six' : six()
}
```
``` python
def six():
    return 6
```

Insert: ``` dictionary[7] = "seven" ```
Remove: ``` dictionary.pop('six') ```
Access: ``` dictionary[1] 
                >>> 'hello'
	``` <br/><br/>
Get: ``` dcitionary.get('two') ```
* Get method takes key as first argument and return values if it is exist. Else it return None.
* Get method takes only two arguments and the second argument is taken as optional default value.
* If first argument, key value is not existed in the dictionary, it return second argument which is default value.

` dictionary.keys() >>> return keys ` 
` dictionary.values() >>> return values ` 
` dictionary.items() >>> return items `  / `(keys, value)` pair items. <br/>
**Above three will return classes.**

### Looping : 
```python
for key, value in dictionary.items():
    print(key, value)
```

**Note: don’t confuse with `enumerate`. Which return index value and items in iteration.**


