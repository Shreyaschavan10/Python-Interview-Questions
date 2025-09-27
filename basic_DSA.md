1. Reverse an array
``` python
def reverse_array(arr):
    left, right = 0, len(arr) - 1
    while left < right:
        arr[left], arr[right] = arr[right], arr[left]
        left += 1
        right -= 1
    return arr

print(reverse_array([1, 2, 3, 4, 5]))
```

2. Find the maximum element in an array
``` python
def find_max(arr):
    max_val = arr[0]
    for num in arr:
        if num > max_val:
            max_val = num
    return max_val

print(find_max([3, 7, 2, 9, 5]))
```

3. Find the minimum element in an array
``` python
def find_min(arr):
    min_val = arr[0]
    for num in arr:
        if num < min_val:
            min_val = num
    return min_val

print(find_min([3, 7, 2, 9, 5]))
```

4. Find the second largest element
``` python
def second_largest(arr):
    first = second = float('-inf')
    for num in arr:
        if num > first:
            second = first
            first = num
        elif num > second and num != first:
            second = num
    return second

print(second_largest([10, 20, 4, 45, 99]))
```

5. Check if an array is sorted
``` python
def is_sorted(arr):
    for i in range(len(arr) - 1):
        if arr[i] > arr[i+1]:
            return False
    return True

print(is_sorted([1, 2, 3, 4, 5]))
print(is_sorted([3, 2, 1]))
```

6. Implement linear search
``` python
def linear_search(arr, target):
    for i in range(len(arr)):
        if arr[i] == target:
            return i
    return -1

print(linear_search([10, 20, 30, 40], 30))
```

7. Implement binary search
``` python
def binary_search(arr, target):
    left, right = 0, len(arr) - 1
    while left <= right:
        mid = (left + right) // 2
        if arr[mid] == target:
            return mid
        elif arr[mid] < target:
            left = mid + 1
        else:
            right = mid - 1
    return -1

print(binary_search([1, 2, 3, 4, 5, 6], 4))
```

8. Find the sum of elements in an array
``` python
def array_sum(arr):
    total = 0
    for num in arr:
        total += num
    return total

print(array_sum([1, 2, 3, 4, 5]))
```

9. Count frequency of elements in an array
``` python
def frequency_count(arr):
    freq = {}
    for num in arr:
        if num in freq:
            freq[num] += 1
        else:
            freq[num] = 1
    return freq

print(frequency_count([1, 2, 2, 3, 3, 3, 4]))
```

10. Rotate an array by k steps
``` python
def rotate_array(arr, k):
    n = len(arr)
    k = k % n
    result = [0] * n
    for i in range(n):
        result[(i + k) % n] = arr[i]
    return result

print(rotate_array([1, 2, 3, 4, 5], 2))
```

11. Find missing number in range 1…n
``` python
def missing_number(arr, n):
    total = n * (n + 1) // 2
    sum_arr = 0
    for num in arr:
        sum_arr += num
    return total - sum_arr

print(missing_number([1, 2, 4, 5], 5))
```

12. Check if a string is palindrome
``` python
def is_palindrome(s):
    left, right = 0, len(s) - 1
    while left < right:
        if s[left] != s[right]:
            return False
        left += 1
        right -= 1
    return True

print(is_palindrome("madam"))
print(is_palindrome("hello"))
```

13. Reverse a linked list (iterative)
``` python
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None

def reverse_linked_list(head):
    prev = None
    current = head
    while current:
        nxt = current.next
        current.next = prev
        prev = current
        current = nxt
    return prev

# Example
head = Node(1)
head.next = Node(2)
head.next.next = Node(3)

reversed_head = reverse_linked_list(head)
while reversed_head:
    print(reversed_head.data, end=" ")
    reversed_head = reversed_head.next
```
14. Implement stack using list
``` python
class Stack:
    def __init__(self):
        self.stack = []

    def push(self, item):
        self.stack.append(item)

    def pop(self):
        if not self.is_empty():
            return self.stack.pop()
        return None

    def is_empty(self):
        return len(self.stack) == 0

s = Stack()
s.push(10)
s.push(20)
print(s.pop())
```
15. Implement queue using list
``` python
class Queue:
    def __init__(self):
        self.queue = []

    def enqueue(self, item):
        self.queue.append(item)

    def dequeue(self):
        if not self.is_empty():
            return self.queue.pop(0)
        return None

    def is_empty(self):
        return len(self.queue) == 0

q = Queue()
q.enqueue(10)
q.enqueue(20)
print(q.dequeue())
```

# 30 Basic DSA Questions with Answers (Python - No Inbuilt Functions)

### 1. Find the index of the first occurrence of an element in an array
```python
def first_occurrence(arr, target):
    for i in range(len(arr)):
        if arr[i] == target:
            return i
    return -1

print(first_occurrence([1, 2, 3, 2, 5], 2))
```
---

### 2. Find the index of the last occurrence of an element
```python
def last_occurrence(arr, target):
    index = -1
    for i in range(len(arr)):
        if arr[i] == target:
            index = i
    return index

print(last_occurrence([1, 2, 3, 2, 5], 2))
```
---

### 3. Count the number of even and odd numbers in an array
```python
def count_even_odd(arr):
    even, odd = 0, 0
    for num in arr:
        if num % 2 == 0:
            even += 1
        else:
            odd += 1
    return even, odd

print(count_even_odd([1, 2, 3, 4, 5, 6]))
```
---

### 4. Merge two sorted arrays
```python
def merge_sorted(arr1, arr2):
    i = j = 0
    merged = []
    while i < len(arr1) and j < len(arr2):
        if arr1[i] < arr2[j]:
            merged.append(arr1[i])
            i += 1
        else:
            merged.append(arr2[j])
            j += 1
    while i < len(arr1):
        merged.append(arr1[i])
        i += 1
    while j < len(arr2):
        merged.append(arr2[j])
        j += 1
    return merged

print(merge_sorted([1, 3, 5], [2, 4, 6]))
```
---

### 5. Remove duplicates from a sorted array
```python
def remove_duplicates(arr):
    if not arr:
        return []
    result = [arr[0]]
    for i in range(1, len(arr)):
        if arr[i] != arr[i-1]:
            result.append(arr[i])
    return result

print(remove_duplicates([1, 1, 2, 2, 3, 4, 4]))
```
---

### 6. Implement bubble sort
```python
def bubble_sort(arr):
    n = len(arr)
    for i in range(n):
        for j in range(0, n-i-1):
            if arr[j] > arr[j+1]:
                arr[j], arr[j+1] = arr[j+1], arr[j]
    return arr

print(bubble_sort([5, 2, 9, 1, 5, 6]))
```
---

### 7. Implement selection sort
```python
def selection_sort(arr):
    n = len(arr)
    for i in range(n):
        min_index = i
        for j in range(i+1, n):
            if arr[j] < arr[min_index]:
                min_index = j
        arr[i], arr[min_index] = arr[min_index], arr[i]
    return arr

print(selection_sort([64, 25, 12, 22, 11]))
```
---

### 8. Implement insertion sort
```python
def insertion_sort(arr):
    for i in range(1, len(arr)):
        key = arr[i]
        j = i - 1
        while j >= 0 and arr[j] > key:
            arr[j+1] = arr[j]
            j -= 1
        arr[j+1] = key
    return arr

print(insertion_sort([12, 11, 13, 5, 6]))
```
---

### 9. Implement quicksort
```python
def quicksort(arr):
    if len(arr) <= 1:
        return arr
    pivot = arr[-1]
    left, right = [], []
    for i in range(len(arr)-1):
        if arr[i] < pivot:
            left.append(arr[i])
        else:
            right.append(arr[i])
    return quicksort(left) + [pivot] + quicksort(right)

print(quicksort([10, 7, 8, 9, 1, 5]))
```
---

### 10. Implement merge sort
```python
def merge_sort(arr):
    if len(arr) <= 1:
        return arr
    mid = len(arr)//2
    left = merge_sort(arr[:mid])
    right = merge_sort(arr[mid:])
    return merge(left, right)

def merge(left, right):
    result = []
    i = j = 0
    while i < len(left) and j < len(right):
        if left[i] < right[j]:
            result.append(left[i])
            i += 1
        else:
            result.append(right[j])
            j += 1
    result.extend(left[i:])
    result.extend(right[j:])
    return result

print(merge_sort([12, 11, 13, 5, 6, 7]))
```
---

### 11. Find GCD of two numbers (Euclidean algorithm)
```python
def gcd(a, b):
    while b:
        a, b = b, a % b
    return a

print(gcd(48, 18))
```
---

### 12. Find LCM of two numbers
```python
def gcd(a, b):
    while b:
        a, b = b, a % b
    return a

def lcm(a, b):
    return (a * b) // gcd(a, b)

print(lcm(4, 6))
```
---

### 13. Print Fibonacci sequence up to n terms
```python
def fibonacci(n):
    a, b = 0, 1
    for _ in range(n):
        print(a, end=" ")
        a, b = b, a + b

fibonacci(10)
```
---

### 14. Find nth Fibonacci number (recursion)
```python
def fib(n):
    if n <= 1:
        return n
    return fib(n-1) + fib(n-2)

print(fib(7))
```
---

### 15. Factorial using recursion
```python
def factorial(n):
    if n == 0:
        return 1
    return n * factorial(n-1)

print(factorial(5))
```
---

### 16. Factorial using iteration
```python
def factorial_iter(n):
    result = 1
    for i in range(1, n+1):
        result *= i
    return result

print(factorial_iter(5))
```
---

### 17. Count vowels in a string
```python
def count_vowels(s):
    vowels = "aeiouAEIOU"
    count = 0
    for ch in s:
        if ch in vowels:
            count += 1
    return count

print(count_vowels("hello world"))
```
---

### 18. Reverse a string
```python
def reverse_string(s):
    chars = list(s)
    left, right = 0, len(chars) - 1
    while left < right:
        chars[left], chars[right] = chars[right], chars[left]
        left += 1
        right -= 1
    return "".join(chars)

print(reverse_string("hello"))
```
---

### 19. Find the longest word in a sentence
```python
def longest_word(sentence):
    words = sentence.split(" ")
    longest = ""
    for word in words:
        if len(word) > len(longest):
            longest = word
    return longest

print(longest_word("Python is a powerful programming language"))
```
---

### 20. Find first repeating character in a string
```python
def first_repeating(s):
    seen = {}
    for ch in s:
        if ch in seen:
            return ch
        seen[ch] = True
    return None

print(first_repeating("programming"))
```
---

### 21. Find first non-repeating character
```python
def first_non_repeating(s):
    for i in range(len(s)):
        repeat = False
        for j in range(len(s)):
            if i != j and s[i] == s[j]:
                repeat = True
                break
        if not repeat:
            return s[i]
    return None

print(first_non_repeating("swiss"))
```
---

### 22. Implement stack using linked list
```python
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None

class Stack:
    def __init__(self):
        self.top = None

    def push(self, data):
        new_node = Node(data)
        new_node.next = self.top
        self.top = new_node

    def pop(self):
        if self.top is None:
            return None
        val = self.top.data
        self.top = self.top.next
        return val

s = Stack()
s.push(10)
s.push(20)
print(s.pop())
```
---

### 23. Implement queue using linked list
```python
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None

class Queue:
    def __init__(self):
        self.front = self.rear = None

    def enqueue(self, data):
        new_node = Node(data)
        if self.rear is None:
            self.front = self.rear = new_node
            return
        self.rear.next = new_node
        self.rear = new_node

    def dequeue(self):
        if self.front is None:
            return None
        val = self.front.data
        self.front = self.front.next
        if self.front is None:
            self.rear = None
        return val

q = Queue()
q.enqueue(10)
q.enqueue(20)
print(q.dequeue())
```
---

### 24. Depth of a binary tree
```python
class TreeNode:
    def __init__(self, data):
        self.data = data
        self.left = None
        self.right = None

def max_depth(root):
    if root is None:
        return 0
    return 1 + max(max_depth(root.left), max_depth(root.right))

root = TreeNode(1)
root.left = TreeNode(2)
root.right = TreeNode(3)
root.left.left = TreeNode(4)

print(max_depth(root))
```
---

### 25. Inorder traversal of binary tree
```python
def inorder(root):
    if root:
        inorder(root.left)
        print(root.data, end=" ")
        inorder(root.right)

inorder(root)
```
---

### 26. Preorder traversal of binary tree
```python
def preorder(root):
    if root:
        print(root.data, end=" ")
        preorder(root.left)
        preorder(root.right)

preorder(root)
```
---

### 27. Postorder traversal of binary tree
```python
def postorder(root):
    if root:
        postorder(root.left)
        postorder(root.right)
        print(root.data, end=" ")

postorder(root)
```
---

### 28. Level order traversal (BFS)
```python
from collections import deque

def level_order(root):
    if not root:
        return
    q = deque([root])
    while q:
        node = q.popleft()
        print(node.data, end=" ")
        if node.left:
            q.append(node.left)
        if node.right:
            q.append(node.right)

level_order(root)
```
---

### 29. Check if two strings are anagrams
```python
def are_anagrams(s1, s2):
    if len(s1) != len(s2):
        return False
    count = {}
    for ch in s1:
        count[ch] = count.get(ch, 0) + 1
    for ch in s2:
        if ch not in count or count[ch] == 0:
            return False
        count[ch] -= 1
    return True

print(are_anagrams("listen", "silent"))
```
---

### 30. Find peak element in an array
```python
def find_peak(arr):
    n = len(arr)
    for i in range(n):
        if (i == 0 or arr[i] >= arr[i-1]) and (i == n-1 or arr[i] >= arr[i+1]):
            return arr[i]
    return None

print(find_peak([1, 3, 20, 4, 1, 0]))
```

