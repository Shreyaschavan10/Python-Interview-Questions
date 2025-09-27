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
