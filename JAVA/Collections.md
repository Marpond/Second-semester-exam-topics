## Arrays
**Array references**
In this case, scores does not hold any value itself but it's a reference to the array to the right. That array is stored elsewhere.
```java
int[] scores = { 10, 9, 7, 4, 5 };
```

**Partially filled arrays**
In a typical program run, only a part of the array will be occupied by actual elements.

## Collections framework
![](Pasted%20image%2020220620012114.png)
All collections implement the Collection interface so they have access to all of it's methods.

**List**
Remembers the order of it's elements.
- **ArrayList**
Adapts it's size.
- **Stack**
You can only add elements at the top.
```java
Stack<Integer> stack = new Stack<>();  
stack.push(1);  
stack.push(2);  
stack.push(3);
```

**Queue**
You can only add items to the tail and remove them from the head.
```java
Queue<Integer> priorityQueue = new LinkedList<>();  
priorityQueue.add(1);  
priorityQueue.add(2);  
priorityQueue.add(3);  
priorityQueue.remove();  
System.out.println(priorityQueue.peek());
```
- **LinkedList**
It's a sequence of nodes. When inserting or removing an element, only the neighboring node instances need to be updated. Accessing however is slow.
- **PriorityQueue**
Does not maintain the first-in first-out discipline. Elements are retrieved according to their priority. Elements must belong to a class that implements the *Comparable* interface.
```java
PriorityQueue<WorkOrder> q = new PriorityQueue<>();
q.add(new WorkOrder(3, "Shampoo carpets"));
q.add(new WorkOrder(1, "Fix broken sink"));
q.add(new WorkOrder(2, "Order cleaning supplies"));
```

**Set**
Doesn't allow duplicates.
- **Hash**
Provides set implementations with hash table. Set elements are grouped into smaller collections that share the same characteristics.
To use a hash set the elements inside need a *hashCode* and *equals* method. If all elements are distinct they can inherit the methods from the *Object* class. 
- **Tree**
Elements are kept in sorted order, and in nodes, in a tree shape. It must be possible to *compare* elements and determine which one is *larger*, because of binary search.

**Map**
Manages associations between keys and values.

- **Hashmap**
- **Treemap**

## Implementing the LinkedList
```java
public class LinkedList {

	private Node first;

	public LinkedList() {
		first = null; 
	}
	
	public Object getFirst() {
		if (first == null) { 
			throw new NoSuchElementException();
		}
		return first.data;
	}

	public void addFirst(Object element) {
		Node newNode = new Node();
		newNode.data = element;
		newNode.next = first;
		first = newNode;
	}

	public Object removeFirst() {
		if (first == null) { 
			throw new NoSuchElementException(); 
		}
		Object element = first.data;
		first = first.next;
		return element;
	}
}
```