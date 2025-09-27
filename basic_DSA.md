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
