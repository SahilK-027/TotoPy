# TotoPy
Let's learn Python for CP and Problem-Solving...🐍


TotoPy is a repository aimed at comparing solutions across multiple programming languages, with a primary focus on Python3. 

The repository includes implementations of common programming tasks and challenges in languages like C++, JavaScript, and Python3, providing insights into different approaches to solving programming problems. 

Contributors are encouraged to add content related to their favourite languages, such as Java, Rust, Go, or any other fostering a diverse collection of solutions and learning across various programming Languages.

## 🟣 Problem 1: How to swap two variables in Python3
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
#### ♻ Solutions in other languages
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

## 🟣 Problem 2: How to declare and use HashMap?
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
#### ♻ Solutions in other languages
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
