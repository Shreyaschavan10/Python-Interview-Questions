
# Python Pattern Questions with Solutions

## 1. Right-Angled Triangle (Stars)
```
*
* *
* * *
* * * *
* * * * *
```
**Code:**
```python
n = 5
for i in range(1, n+1):
    print("* " * i)
```

---

## 2. Inverted Right-Angled Triangle
```
* * * * *
* * * *
* * *
* *
*
```
**Code:**
```python
n = 5
for i in range(n, 0, -1):
    print("* " * i)
```

---

## 3. Pyramid Pattern
```
    *    
   ***   
  *****  
 ******* 
*********
```
**Code:**
```python
n = 5
for i in range(n):
    print(" " * (n-i-1) + "*" * (2*i+1))
```

---

## 4. Diamond Pattern
```
    *    
   ***   
  *****  
   ***   
    *    
```
**Code:**
```python
n = 3
for i in range(n):
    print(" " * (n-i-1) + "*" * (2*i+1))
for i in range(n-2, -1, -1):
    print(" " * (n-i-1) + "*" * (2*i+1))
```

---

## 5. Number Triangle
```
1
1 2
1 2 3
1 2 3 4
```
**Code:**
```python
n = 4
for i in range(1, n+1):
    for j in range(1, i+1):
        print(j, end=" ")
    print()
```

---

## 6. Inverted Number Triangle
```
1 2 3 4 5
1 2 3 4
1 2 3
1 2
1
```
**Code:**
```python
n = 5
for i in range(n, 0, -1):
    for j in range(1, i+1):
        print(j, end=" ")
    print()
```

---

## 7. Floyd’s Triangle
```
1
2 3
4 5 6
7 8 9 10
```
**Code:**
```python
n = 4
num = 1
for i in range(1, n+1):
    for j in range(i):
        print(num, end=" ")
        num += 1
    print()
```

---

## 8. Binary Triangle
```
1
0 1
1 0 1
0 1 0 1
```
**Code:**
```python
n = 4
for i in range(n):
    for j in range(i+1):
        print((i+j) % 2, end=" ")
    print()
```

---

## 9. Hollow Square
```
*****
*   *
*   *
*   *
*****
```
**Code:**
```python
n = 5
for i in range(n):
    for j in range(n):
        if i == 0 or i == n-1 or j == 0 or j == n-1:
            print("*", end="")
        else:
            print(" ", end="")
    print()
```

---

## 10. Pascal’s Triangle
```
      1
     1 1
    1 2 1
   1 3 3 1
  1 4 6 4 1
```
**Code:**
```python
from math import comb

n = 5
for i in range(n):
    print(" " * (n-i), end="")
    for j in range(i+1):
        print(comb(i, j), end=" ")
    print()
```
