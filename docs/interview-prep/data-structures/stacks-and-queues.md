# Stacks and Queues

## Overview
Similarities
- Linear data structures
- Flexible size
  
Differences
 - Stacks are LIFO (last in, first out)
 - Queues are FIFI (first in, first out)

## Implementation
### Queue
```java
  public static class Queue {
    private static class Node {
      private int data;
      private Node next;
      private Node(int data) {
        this.data = data;
      }
    }

    private Node head; // remove from the head
    private Node tail; // add things here

    public boolean isEmpty() {
      return head == null;
    }

    public int peek() {
      return head.data;
    }

    public void add(int data) {
      Node node = new Node(data);
      if (tail != null) {
        tail.next = node;
      }
      tail = node;
      if (head == null) {
        head = node;
      }
    }

    public int remove() {
      int data = head.data;
      head = head.next;
      if (head == null) {
        tail = null;
      }
      return data;
    }
  }
```

### Stack
```java
  public static class Stack {
    private static class Node {
      private int data;
      private Node next;
      private Node(int data) {
        this.data = data;
      }
    }

    private Node top; // add and remove

    public boolean isEmpty() {
      return top == null;
    }
    public int peek() {
      return top.data;
    }
    public void push(int data) {
      Node node = new Node(data);
      node.next = top;
      top = node;
    }
    public int pop() {
      int data = top.data;
      top = top.next;
      return data;
    }
```
