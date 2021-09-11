# Linked List
[HackerRank](https://www.youtube.com/watch?v=njTh_OwMljA)
[CS Dojo](https://www.youtube.com/watch?v=WwfhLC16bis)

A sequence of elements where each element is linked to the next element. They can contain any type of data, be sorted or unsorted, contain duplicates or all unique elements.

Linked lists and arrays are very similar. A difference between linked lists and arrays is that in an array, elements are indexed. For linked lists you have to start at the beginning then traverse through, which is done at linear time. 

#### Advantages
- Insertion and deletion can be quick
  - prepend: O(1)
  - append: O(n)

#### Disadvantages
- Slow to get nth element
  - O(n)

### Doubly linked list
In addition to having a link to the next element, it also has a link to the previous element.

## Implementation

```java
public class Node {
  Node next;
  int data;
  public Node(int data) {
    this.data = data;
  }
}

public class LinkedList {
  Node head;

  public void append(int data) {
    if (head == null) {
      head = new Node(data);
      return;
    }
    // pointer for the current node
    Node current = head;
    while(current.next != null) {
      current = current.next;
    }
    // create node at end of list
    current.next = new Node(data);
  }

  public void prepend(int data) {
    Node newHead = new Node(data);
    newHead.next = head;
    head = newHead;
  }

  public void deleteWithValue(int data) {
    if (head == null) return;
    if (head.data == data) {
      head = head.next;
      return;
    }

    Node current = head;
    while (current.next != null) {
      if (current.next.data == data) {
        current.next = current.next.next;
        return;
      }
      current = current.next;
    }
  }
}
```



coding then behavioral
focus
  communication!!
  complete task before interview - 24hrs
  explain solution
  during, will be asked to add a feature or update performance
  send via zip file or cloud storage
behavioral
 3 areas: 
    moments when you worked others
    how I work with feedback - positive/negative - both maybe
    project work - what I consider as a successful project
      how I work when things go wrong
  hit past experience
  assume interviewer has no idea about the company I work for

architecture part
