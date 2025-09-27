**Python Fresher Level Coding Interview Questions and Answers**

1. **Write a Python program to reverse a string.**
   - Answer 1:
   ```python
   s = 'hello'
   print(s[::-1])
   ```

2. **Write a Python program to check if a number is prime.**
   - Answer 1:
   ```python
   n = 17
   prime = True
   for i in range(2, int(n**0.5)+1):
       if n % i == 0:
           prime = False
           break
   print(prime)
   ```

3. **Write a Python program to find the factorial of a number.**
   - Answer 1:
   ```python
   def factorial(n):
       if n == 0:
           return 1
       else:
           return n * factorial(n-1)
   print(factorial(5))
   ```

4. **Write a Python program to find the largest element in a list.**
   - Answer 1:
   ```python
   lst = [3, 7, 2, 9, 4]
   print(max(lst))
   ```

5. **Write a Python program to count vowels in a string.**
   - Answer 1:
   ```python
   s = 'hello world'
   vowels = 'aeiou'
   count = sum(1 for char in s if char in vowels)
   print(count)
   ```

6. **Write a Python program to remove duplicates from a list.**
   - Answer 1:
   ```python
   lst = [1, 2, 2, 3, 4, 4]
   lst = list(set(lst))
   print(lst)
   ```

7. **Write a Python program to check if a string is palindrome.**
   - Answer 1:
   ```python
   s = 'radar'
   print(s == s[::-1])
   ```

8. **Write a Python program to merge two dictionaries.**
   - Answer 1:
   ```python
   dict1 = {'a':1, 'b':2}
   dict2 = {'c':3, 'd':4}
   dict3 = {**dict1, **dict2}
   print(dict3)
   ```

9. **Write a Python program to generate Fibonacci series.**
   - Answer 1:
   ```python
   n = 10
   a, b = 0, 1
   for _ in range(n):
       print(a, end=' ')
       a, b = b, a+b
   ```

10. **Write a Python program to find the second largest number in a list.**
    - Answer 1:
    ```python
    lst = [4, 1, 9, 7, 9]
    unique_lst = list(set(lst))
    unique_lst.sort()
    print(unique_lst[-2])
    ```

11. **Write a Python program to check if a number is even or odd.**
    - Answer 1:
    ```python
    n = 5
    print('Even' if n % 2 == 0 else 'Odd')
    ```

12. **Write a Python program to find the sum of elements in a list.**
    - Answer 1:
    ```python
    lst = [1, 2, 3, 4, 5]
    print(sum(lst))
    ```

13. **Write a Python program to find common elements in two lists.**
    - Answer 1:
    ```python
    list1 = [1, 2, 3]
    list2 = [2, 3, 4]
    print(list(set(list1) & set(list2)))
    ```

14. **Write a Python program to check if a list is empty.**
    - Answer 1:
    ```python
    lst = []
    print('Empty' if not lst else 'Not Empty')
    ```

15. **Write a Python program to sort a list of tuples by second element.**
    - Answer 1:
    ```python
    lst = [(1,3),(2,2),(3,1)]
    lst.sort(key=lambda x: x[1])
    print(lst)
    ```

16. **Write a Python program to count the occurrence of an element in a list.**
    - Answer 1:
    ```python
    lst = [1,2,2,3,2]
    print(lst.count(2))
    ```

17. **Write a Python program to flatten a nested list.**
    - Answer 1:
    ```python
    nested = [[1,2],[3,4]]
    flat = [item for sublist in nested for item in sublist]
    print(flat)
    ```

18. **Write a Python program to remove whitespace from a string.**
    - Answer 1:
    ```python
    s = '  hello  '
    print(s.strip())
    ```

19. **Write a Python program to find the GCD of two numbers.**
    - Answer 1:
    ```python
    import math
    print(math.gcd(12, 18))
    ```

20. **Write a Python program to find the LCM of two numbers.**
    - Answer 1:
    ```python
    import math
    def lcm(a,b):
        return abs(a*b)//math.gcd(a,b)
    print(lcm(12,18))
    ```

21. **Write a Python program to check Armstrong number.**
    - Answer 1:
    ```python
    n = 153
    sum = 0
    for digit in str(n):
        sum += int(digit)**3
    print(sum == n)
    ```

22. **Write a Python program to swap two numbers.**
    - Answer 1:
    ```python
    a, b = 5, 10
    a, b = b, a
    print(a, b)
    ```

23. **Write a Python program to convert a list of strings to uppercase.**
    - Answer 1:
    ```python
    lst = ['a','b']
    lst = [s.upper() for s in lst]
    print(lst)
    ```

24. **Write a Python program to find the longest word in a list.**
    - Answer 1:
    ```python
    words = ['Python','Programming','AI']
    print(max(words, key=len))
    ```

25. **Write a Python program to check if a number is a perfect square.**
    - Answer 1:
    ```python
    import math
    n = 16
    print(math.isqrt(n)**2 == n)
    ```

26. **Write a Python program to count words in a string.**
    - Answer 1:
    ```python
    s = 'Python is fun'
    print(len(s.split()))
    ```

27. **Write a Python program to print multiplication table of a number.**
    - Answer 1:
    ```python
    n = 5
    for i in range(1,11):
        print(n,'x',i,'=',n*i)
    ```

28. **Write a Python program to reverse a list.**
    - Answer 1:
    ```python
    lst = [1,2,3]
    print(lst[::-1])
    ```

29. **Write a Python program to check leap year.**
    - Answer 1:
    ```python
    year = 2024
    print(year%4==0 and (year%100!=0 or year%400==0))
    ```

30. **Write a Python program to remove punctuation from a string.**
    - Answer 1:
    ```python
    import string
    s = 'Hello, world!'
    print(s.translate(str.maketrans('', '', string.punctuation)))
    ```

# Python Fresher Level Coding Interview Questions (Set 2: Q31–Q60)

---

### 31. Write a Python program to find the largest of three numbers.
```python
a, b, c = 10, 25, 7
print(max(a, b, c))
```

### 32. Write a Python program to reverse words in a sentence.
```python
s = "Python is fun"
print(" ".join(s.split()[::-1]))
```

### 33. Write a Python program to check if two strings are anagrams.
```python
s1, s2 = "listen", "silent"
print(sorted(s1) == sorted(s2))
```

### 34. Write a Python program to find the frequency of each character in a string.
```python
s = "hello world"
freq = {}
for ch in s:
    freq[ch] = freq.get(ch, 0) + 1
print(freq)
```

### 35. Write a Python program to find the missing number in a list of consecutive numbers.
```python
lst = [1, 2, 3, 5, 6]
n = max(lst)
missing = set(range(1, n+1)) - set(lst)
print(missing)
```

### 36. Write a Python program to find the duplicate elements in a list.
```python
lst = [1, 2, 3, 2, 4, 1]
dupes = [x for x in set(lst) if lst.count(x) > 1]
print(dupes)
```

### 37. Write a Python program to find the intersection of two sets.
```python
a = {1, 2, 3}
b = {2, 3, 4}
print(a & b)
```

### 38. Write a Python program to convert a decimal number to binary.
```python
n = 10
print(bin(n)[2:])
```

### 39. Write a Python program to convert binary to decimal.
```python
b = "1010"
print(int(b, 2))
```

### 40. Write a Python program to check if a string contains only digits.
```python
s = "12345"
print(s.isdigit())
```

### 41. Write a Python program to find the sum of digits of a number.
```python
n = 1234
print(sum(int(d) for d in str(n)))
```

### 42. Write a Python program to check if two strings are rotations of each other.
```python
s1, s2 = "abcd", "cdab"
print(len(s1) == len(s2) and s2 in s1+s1)
```

### 43. Write a Python program to find the smallest element in a list without using min().
```python
lst = [3, 7, 1, 9]
smallest = lst[0]
for num in lst:
    if num < smallest:
        smallest = num
print(smallest)
```

### 44. Write a Python program to check if a number is a palindrome.
```python
n = 121
print(str(n) == str(n)[::-1])
```

### 45. Write a Python program to find the first non-repeating character in a string.
```python
s = "aabbcde"
for ch in s:
    if s.count(ch) == 1:
        print(ch)
        break
```

### 46. Write a Python program to find all pairs in a list whose sum is equal to a given number.
```python
lst = [1, 2, 3, 4, 5]
target = 6
pairs = [(x, y) for i, x in enumerate(lst) for y in lst[i+1:] if x+y == target]
print(pairs)
```

### 47. Write a Python program to count uppercase and lowercase letters in a string.
```python
s = "Hello World"
upper = sum(1 for ch in s if ch.isupper())
lower = sum(1 for ch in s if ch.islower())
print("Upper:", upper, "Lower:", lower)
```

### 48. Write a Python program to check if a substring exists inside a string.
```python
s, sub = "hello world", "world"
print(sub in s)
```

### 49. Write a Python program to find the maximum occurring element in a list.
```python
lst = [1, 2, 2, 3, 1, 2]
print(max(set(lst), key=lst.count))
```

### 50. Write a Python program to remove all occurrences of a given element from a list.
```python
lst = [1, 2, 3, 2, 4, 2]
x = 2
lst = [i for i in lst if i != x]
print(lst)
```

### 51. Write a Python program to check if two lists are identical.
```python
a, b = [1, 2, 3], [1, 2, 3]
print(a == b)
```

### 52. Write a Python program to check if two lists have the same elements regardless of order.
```python
a, b = [1, 2, 3], [3, 2, 1]
print(sorted(a) == sorted(b))
```

### 53. Write a Python program to transpose a matrix.
```python
matrix = [[1, 2, 3], [4, 5, 6]]
transpose = [[row[i] for row in matrix] for i in range(len(matrix[0]))]
print(transpose)
```

### 54. Write a Python program to find the sum of each row and column in a matrix.
```python
matrix = [[1, 2], [3, 4]]
row_sum = [sum(row) for row in matrix]
col_sum = [sum(col) for col in zip(*matrix)]
print("Row:", row_sum, "Col:", col_sum)
```

### 55. Write a Python program to flatten a dictionary.
```python
def flatten_dict(d, parent_key='', sep='.'):
    items = {}
    for k, v in d.items():
        new_key = parent_key + sep + k if parent_key else k
        if isinstance(v, dict):
            items.update(flatten_dict(v, new_key, sep=sep))
        else:
            items[new_key] = v
    return items

d = {"a": {"b": 1, "c": 2}, "d": 3}
print(flatten_dict(d))
```

### 56. Write a Python program to implement a stack using a list.
```python
stack = []
stack.append(1)
stack.append(2)
print(stack.pop())  # removes last element
print(stack)
```

### 57. Write a Python program to implement a queue using deque.
```python
from collections import deque
queue = deque([1, 2, 3])
queue.append(4)
print(queue.popleft())  # removes first element
print(queue)
```

### 58. Write a Python program to find the longest substring without repeating characters.
```python
s = "abcabcbb"
longest, temp = "", ""
for ch in s:
    if ch in temp:
        temp = temp[temp.index(ch)+1:]
    temp += ch
    if len(temp) > len(longest):
        longest = temp
print(longest)
```

### 59. Write a Python program to find the common prefix among a list of strings.
```python
words = ["flower", "flow", "flight"]
prefix = words[0]
for word in words[1:]:
    while not word.startswith(prefix):
        prefix = prefix[:-1]
print(prefix)
```

### 60. Write a Python program to generate a random password.
```python
import random, string
chars = string.ascii_letters + string.digits + string.punctuation
password = ''.join(random.choice(chars) for _ in range(10))
print(password)
```
