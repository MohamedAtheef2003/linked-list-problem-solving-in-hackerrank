# Singly Linked List in Python

This repository contains a Python implementation of a **singly linked list**. The program demonstrates basic data structure operations such as **inserting nodes dynamically** and **displaying the list elements** in order.

## Features

- Insert nodes at the end of the list
- Display all nodes in sequence
- Simple and easy to understand for learning purposes

## Code Example

```python
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None

class Solution:
    def display(self, head):
        current = head
        while current:
            print(current.data, end=' ')
            current = current.next

    def insert(self, head, data):
        new_node = Node(data)
        if head is None:
            return new_node
        current = head
        while current.next:
            current = current.next
        current.next = new_node
        return head

# Example usage
mylist = Solution()
head = None
for data in [2, 3, 4, 1]:
    head = mylist.insert(head, data)
mylist.display(head)
