# TotoPy
Let's learn Python for CP and Problem-Solving...🐍


TotoPy is a repository aimed at comparing solutions across multiple programming languages, with a primary focus on Python3. 

The repository includes implementations of common programming tasks and challenges in languages like C++, JavaScript, and Python3, providing insights into different approaches to solving programming problems. 

Contributors are encouraged to add content related to their favourite languages, such as Java, Rust, Go, or any other fostering a diverse collection of solutions and learning across various programming Languages.


## Table of Contents
- [Problem 1: Swapping Two Variables](#problem-1-swapping-two-variables)
- [Problem 2: Using HashMap](#problem-2-using-hashmap)
- [Problem 3: Converting String to List](#problem-3-converting-string-to-list)
- [Problem 4: Converting List to String](#problem-4-converting-list-to-string)
- [Problem 5: Reversing List or String](#problem-5-reversing-list-or-string)
- [Problem 6: Sorting](#problem-6-sorting)
- [Problem 7: Ternary Operator](#problem-7-ternary-operator)
- [Problem 8: Declaring a List of Predefined Size](#problem-8-declaring-a-list-of-predefined-size)
- [Problem 9: Reverse Range for Array Iteration](#problem-9-reverse-range-for-array-iteration)
- [Problem 10: Getting Length of a Map](#problem-10-getting-length-of-a-map)
- [Problem 11: Erasing Elements from a Map](#problem-11-erasing-elements-from-a-map)

## 🟣 Problem 1: How to swap two variables in Python3 <a name="problem-1-swapping-two-variables"></a>
#### ✅ Best Method: Using Tuple Unpacking
```python
# Initial values
a = 10
b = 20

# Swapping using tuple unpacking
a, b = b, a

print("After swapping:")
print("a =", a)
print("b =", b)
```
#### ♻ How do we do it in other languages?
1) C++:
```cpp
int a = 10;
int b = 20;

swap(a,b)

court<<"a: "<<a<<" "<<"b: "<<b<<endl;
```
2) JavaScript
```javascript
let a = 10, b = 20;

// Swapping using array destructuring (no temporary variable needed)
[a, b] = [b, a];

console.log("After swapping:");
console.log("a =", a);
console.log("b =", b);
```

## 🟣 Problem 2: How to declare and use HashMap? <a name="problem-2-using-hashmap"></a>
Solution 1: Using dict
```python
# Declaring and using a HashMap in Python
hash_map = {}
hash_map['key1'] = 'value1'
hash_map['key2'] = 'value2'

# Accessing values
print(hash_map['key1'])  # Output: value1
print(hash_map.get('key2'))  # Output: value2

# Iterating over key-value pairs
for key, value in hash_map.items():
    print(key, value)
```

Solution 2: Using defaultdict
In Python is also a valid and efficient approach for managing key-value pairs, especially in cases where you want default values for keys that haven't been explicitly set. However, for the purpose of competitive programming and simplicity, using a standard dictionary (dict) is often preferred because it requires less code and is easier to understand at a glance.

```python
from collections import defaultdict

# Declaring and using a defaultdict in Python
hash_map = defaultdict(lambda: 'default_value')
hash_map['key1'] = 'value1'
hash_map['key2'] = 'value2'

# Accessing values
print(hash_map['key1'])  # Output: value1
print(hash_map['key3'])  # Output: default_value

# Iterating over key-value pairs
for key, value in hash_map.items():
    print(key, value)
```
#### ♻ How do we do it in other languages?
1) C++
```cpp
unordered_map<string, string> hash_map;
hash_map["key1"] = "value1";
hash_map["key2"] = "value2";

// Accessing values
cout << hash_map["key1"] << endl;  // Output: value1
cout << hash_map["key2"] << endl;  // Output: value2

// Iterating over key-value pairs
for (auto& pair : hash_map) {
  cout << pair.first << " " << pair.second << endl;
}
```

2) JavaScript
```js
// Declaring and using a HashMap in JavaScript
let hash_map = {};
hash_map['key1'] = 'value1';
hash_map['key2'] = 'value2';

// Accessing values
console.log(hash_map['key1']);  // Output: value1
console.log(hash_map['key2']);  // Output: value2

// Iterating over key-value pairs
for (let key in hash_map) {
    if (hash_map.hasOwnProperty(key)) {
        console.log(key, hash_map[key]);
    }
}
```

## 🟣 Problem 3: Converting string to list <a name="problem-3-converting-string-to-list"></a>
In Python strings are immutable so to use and make changes in them we need to convert it to a list. 

1) Converting character by character:  **Using list comprehension**
```python
# String to be converted to a list
string = "Hello, world!"

# Using list comprehension to convert string to list of characters
char_list = [char for char in string]

# Method 2 list() method
char_list = list(string)

print(char_list)  # Output: ['H', 'e', 'l', 'l', 'o', ',', ' ', 'w', 'o', 'r', 'l', 'd', '!']
```

2) Splitting based on separator: **Using `split()` method**
```python
# String to be converted to a list
string = "Hello, world! This is a string."

# Using split() method to convert string to list based on space delimiter
word_list = string.split()
print(word_list)  # Output: ['Hello,', 'world!', 'This', 'is', 'a', 'string.']

# Using split() with a custom delimiter (comma in this case)
custom_list = string.split(',')
print(custom_list)  # Output: ['Hello', ' world! This is a string.']
```

#### ♻ How do we do it in other languages?
1) C++
```cpp
string str = "Hello, world!";
vector<char> charArray(str.begin(), str.end());

// Print the array of characters
for (char ch: charArray) {
    cout << ch << " ";
}
cout << endl;
```

2) JavaScript
```js
// String to Array of Characters
let str = "Hello, world!";
let charArray = Array.from(str);

// Print the array of characters
console.log(charArray);

// String to Array of Words (splitting by space)
let wordsArray = str.split(' ');

// Print the array of words
console.log(wordsArray);
```

## 🟣 Problem 4: Converting a list to a string <a name="problem-4-converting-list-to-string"></a>
In Python, converting a list of elements into a single string can be done using the `join()` method. 
```py
# List of elements
my_list = ['Hello', 'world', 'this', 'is', 'a', 'list']

# Convert list to string using join() method
my_string = ' '.join(my_list)

print(my_string)
```
#### ♻ How do we do it in other languages?
1) C++
```cpp
vector<string> v = {"hello", "world"};
string str = "";
for(auto i: v){
    str += i;
}
cout<<str<<endl;
```

2) JavaScript
```js
// Converting an array to a string in JavaScript
let my_array = ['Hello', 'world', '2024'];

// Using join() method to concatenate array elements into a string
let my_string = my_array.join(' ');

console.log(my_string);  // Output: Hello world 2024
```

## 🟣 Problem 5: Reverse list or String <a name="problem-5-reversing-list-or-string"></a>

1) **Using Slicing**
```py
my_list = [1, 2, 3, 4, 5]
reversed_list = my_list[::-1]

print(reversed_list)  # Output: [5, 4, 3, 2, 1]
```

2) **Using `reversed()` method**
```py
my_list = [1, 2, 3, 4, 5]
reversed_list = list(reversed(my_list))

print(reversed_list)  # Output: [5, 4, 3, 2, 1]
```

> __Note__
> The same applies to strings

#### ♻ How do we do it in other languages?
1) C++
```cpp
vector<int> arr = {1,2,3,4,5};
reverse(arr.begin(), arr.end());
for(auto i: arr){
    cout<<i<<" ";
}
```

2) JavaScript
```js
let myString = "Hello, world!";
let reversedString = myString.split('').reverse().join('');

console.log(reversedString);  // Output: "!dlrow ,olleH"
```

## 🟣 Problem 6: Sorting <a name="problem-6-sorting"></a>
The `sort()` method sorts the list ascending by default.
```py
list.sort(reverse=True|False, key=myFunc)
```
> __Note__
> The same applies to strings

#### ♻ How do we do it in other languages?
1) C++
```cpp
vector<int> arr = {1,2,3,4,5};
sort(arr.begin(), arr.end()); OR sort(arr.begin(), arr.end(), greater<int>());
for(auto i: arr){
    cout<<i<<" ";
}
```

2) JavaScript
```js
let myString = "Hello, world!";
let sortedString = myString.sort();

console.log(sortedString);
```

> __Note__
> The sort() method overwrites the original array

## 🟣 Problem 7: Ternary operator <a name="problem-7-ternary-operator"></a>
Python has a ternary operator syntax that allows you to write conditional expressions concisely. The syntax is:
```py
x if condition else y
```
```py
age = 20
message = "You are eligible" if age >= 18 else "You are not eligible"
print(message)
```

#### ♻ How do we do it in other languages?
1) C++
```cpp
int age = 20;
string message = (age >= 18) ? "You are eligible": "You are not eligible";
cout << message << endl;
```

2) JavaScript
```js
let age = 20;
let message = (age >= 18) ? "You are eligible": "You are not eligible";
console.log(message);
```

## 🟣 Problem 8: Declare a list of predefined size n <a name="problem-8-declaring-a-list-of-predefined-size"></a>
```py
n = 10
list = [0] * n
# This will create a list of size n filled with 0s
```

#### ♻ How do we do it in other languages?
1) C++
```cpp
vector<int> list(n,0);
```

2) JavaScript
```js
var n = 5; // Or any other desired size
var list = new Array(n).fill(0);
```
OR
```js
var n = 5; // Or any other desired size
var list = [];
for (var i = 0; i < n; i++) {
    list.push(0);
}
```

## 🟣 Problem 9: Reverse range to iterate over an array <a name="problem-9-reverse-range-for-array-iteration"></a>
```py
array = [1, 2, 3, 4, 5]

# Iterate over the array in reverse order
for i in range(len(array) - 1, -1, -1):
    print(array[i])
```

OR
```py
for n in reversed(range(5)):
    print(n)
 
# output:
# 4
# 3
# 2
# 1
# 0
```

## 🟣 Problem 10: Get length of map <a name="problem-10-getting-length-of-a-map"></a>
```py
unorderedMap = defaultdict(lambda: 0)
length = len(unorderedMap)
```
#### ♻ How do we do it in other languages?
1) C++
```cpp
unordered_map<int, int>unorderedMap;
length = unorderedMap.size()
```

2) JavaScript
```js
let unorderedMap = {};
let length = Object.keys(unorderedMap).length;
```
OR
```js
let unorderedMap = new Map();
let length = unorderedMap.size;
```


## 🟣 Problem 11: Erase element from the map <a name="problem-11-erasing-elements-from-a-map"></a>
```py
unorderedMap = defaultdict(lambda: 0)
unorderedMap[10] += 2
unorderedMap.pop(10)
```
#### ♻ How do we do it in other languages?
1) C++
```cpp
unordered_map<int, int>unorderedMap;
unorderedMap[10] += 2
unorderedMap.erase(10
```

2) JavaScript
```js
let unorderedMap = {};
unorderedMap[10] = (unorderedMap[10] || 0) + 2;
delete unorderedMap[10];
```
OR
```js
let unorderedMap = new Map();
unorderedMap.set(10, (unorderedMap.get(10) || 0) + 2);
unorderedMap.delete(10);
```
