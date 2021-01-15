# Hashtable


## Hash functions 
* Hash function generates the hash key to hash value. <br/>
* Hash functions are idempotent. <br/>
* Idempotent: a properties that always return the same result for the same input. <br/>

## Hash map
* Hash function generates the hash key to hash value. <br/>
* The generated hash values become the index position in the data storage array. <br/>
* And the (key, value) pair is stored inside data structure with  hash values index position. <br/>

```python
Address = Hash_Function(keys)

Hash_Table[Address].append([keys, values])
```

## Hash Collision
* The hash function is based on the size of storage array. **(in case only two elements can be stored in the storage array, the hash function cannot be generated index position more than two. )**
* Therefore, same hash values key may be generated for several items **(in case store items become more than two.)**
* In that case, different values with different hash key may be stored under same hash values index. 
* This is called hash collision. 
**Note: in most language this collided data are stores as lists in the same index. For example, an array of size(2).**

```python
{["a" , 1] , [ ["b" , 2], ["c" , 3] , … , ["j" , 7] ]} 
```

## Big O analysis
* Normally, Hash map cost `O(1)` for most operations, insert, `lookup`, `delete` or `remove`, `search` or `access`.
* If there is Hash Collison, it cost `O(n)` for some operations, such as search, etc.

### Fun facts
* Python: Dictionary.
* JS: Objects
* Java: Array
* C/C++/ C#: Array

### Questions
Does hash function slow down the data structure operations?

``` python
{1, 2, 3, 4}
```
* Set:  in python, set are based on Hash tables.
* Set are unordered collections of items.
* Set items cannot be referred by index values. ``` { set[i] }. ```
* Set elements are immutable, unchangeable.
* Set cannot be append new items.
* Set items are unique allows no duplicate items. `{1, 1, 1, 2, 2, 2, 2} >> {1, 2}`
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
  'six' : <function six at 0x04046970>
}
```

Insert: ``` dictionary[7] = "seven" ```
Remove: ``` dictionary.pop('six') ```
Access: ``` dictionary[1] 
                >>> 'hello'
	```
* Get: dcitionary.get('two')
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


