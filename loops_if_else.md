# Python Loops and If-Else Questions with Answers

Below are 30 unique Python interview/practice questions on loops and if-else with answers.

---

### 1. Print numbers from 1 to 10 using a for loop.
```python
for i in range(1, 11):
    print(i)
```

---

### 2. Print even numbers from 1 to 20 using a while loop.
```python
i = 1
while i <= 20:
    if i % 2 == 0:
        print(i)
    i += 1
```

---

### 3. Find the sum of first 10 natural numbers.
```python
total = 0
for i in range(1, 11):
    total += i
print(total)
```

---

### 4. Check if a number is positive, negative, or zero.
```python
num = -5
if num > 0:
    print("Positive")
elif num < 0:
    print("Negative")
else:
    print("Zero")
```

---

### 5. Print the multiplication table of 5.
```python
for i in range(1, 11):
    print(f"5 x {i} = {5*i}")
```

---

### 6. Count the number of digits in a number.
```python
num = 12345
count = 0
while num > 0:
    count += 1
    num //= 10
print(count)
```

---

### 7. Reverse a number using a while loop.
```python
num = 1234
rev = 0
while num > 0:
    rev = rev*10 + num%10
    num //= 10
print(rev)
```

---

### 8. Check if a number is divisible by both 3 and 5.
```python
n = 15
if n % 3 == 0 and n % 5 == 0:
    print("Divisible by both")
else:
    print("Not divisible by both")
```

---

### 9. Print all odd numbers between 1 and 50.
```python
for i in range(1, 51, 2):
    print(i)
```

---

### 10. Calculate factorial of a number using loop.
```python
n = 5
fact = 1
for i in range(1, n+1):
    fact *= i
print(fact)
```

---

### 11. Print the Fibonacci series up to 10 terms.
```python
a, b = 0, 1
for _ in range(10):
    print(a, end=" ")
    a, b = b, a+b
```

---

### 12. Check if a number is prime.
```python
n = 13
is_prime = True
for i in range(2, int(n**0.5)+1):
    if n % i == 0:
        is_prime = False
        break
print("Prime" if is_prime else "Not Prime")
```

---

### 13. Find the largest number among three numbers.
```python
a, b, c = 5, 10, 7
if a >= b and a >= c:
    print(a)
elif b >= a and b >= c:
    print(b)
else:
    print(c)
```

---

### 14. Print squares of numbers from 1 to 10.
```python
for i in range(1, 11):
    print(i**2)
```

---

### 15. Count the number of vowels in a string.
```python
s = "hello world"
count = 0
for ch in s:
    if ch in "aeiou":
        count += 1
print(count)
```

---

### 16. Print numbers from 10 to 1 using while loop.
```python
i = 10
while i > 0:
    print(i)
    i -= 1
```

---

### 17. Check if a year is a leap year.
```python
year = 2024
if (year % 4 == 0 and year % 100 != 0) or (year % 400 == 0):
    print("Leap Year")
else:
    print("Not a Leap Year")
```

---

### 18. Calculate sum of digits of a number.
```python
num = 1234
total = 0
while num > 0:
    total += num % 10
    num //= 10
print(total)
```

---

### 19. Print first 10 odd numbers using loop.
```python
for i in range(1, 20, 2):
    print(i)
```

---

### 20. Print all multiples of 7 between 1 and 100.
```python
for i in range(7, 101, 7):
    print(i)
```

---

### 21. Find the smallest number in a list using loop.
```python
lst = [10, 5, 8, 2, 7]
smallest = lst[0]
for num in lst:
    if num < smallest:
        smallest = num
print(smallest)
```

---

### 22. Print ASCII values of characters in a string.
```python
s = "ABC"
for ch in s:
    print(ch, ord(ch))
```

---

### 23. Print factorial of numbers from 1 to 5.
```python
for i in range(1, 6):
    fact = 1
    for j in range(1, i+1):
        fact *= j
    print(f"Factorial of {i} = {fact}")
```

---

### 24. Check if a number is Armstrong number.
```python
n = 153
temp, total = n, 0
while temp > 0:
    digit = temp % 10
    total += digit**3
    temp //= 10
print("Armstrong" if total == n else "Not Armstrong")
```

---

### 25. Print the reverse of a string using loop.
```python
s = "hello"
rev = ""
for ch in s:
    rev = ch + rev
print(rev)
```

---

### 26. Check if a character is a vowel or consonant.
```python
ch = 'a'
if ch in "aeiou":
    print("Vowel")
else:
    print("Consonant")
```

---

### 27. Print sum of even numbers between 1 and 50.
```python
total = 0
for i in range(2, 51, 2):
    total += i
print(total)
```

---

### 28. Print multiplication tables from 1 to 3.
```python
for i in range(1, 4):
    for j in range(1, 11):
        print(f"{i} x {j} = {i*j}")
    print()
```

---

### 29. Check if a string is palindrome using loop.
```python
s = "madam"
rev = ""
for ch in s:
    rev = ch + rev
print("Palindrome" if s == rev else "Not Palindrome")
```

---

### 30. Find the GCD of two numbers.
```python
a, b = 36, 60
while b:
    a, b = b, a % b
print("GCD =", a)
```
