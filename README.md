# TotoPy
Let's learn Python...🐍


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
