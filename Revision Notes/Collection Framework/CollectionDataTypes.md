
# Collection Datatypes Key Points To Be Remembered :

| Collection Type | Key Definition | Key Points | Characteristics | Time Complexity | Space Complexity | Syntax | Use Case | Mutable | Ordered | Iterable | Methods Applicable |
|-----------------|----------------|------------|-----------------|-----------------|------------------|--------|----------|---------|---------|----------|---------------------|
| ArrayList       | List           | Dynamic array implementation | Ordered, resizable array | Insertion/Deletion: O(n), Access: O(1) | O(n) | `List<Type> list = new ArrayList<>();` | Storing and accessing elements by index | Yes | Yes | Yes | add(), remove(), get(), size(), etc. |
| LinkedList      | List           | Doubly linked list implementation | Ordered, efficient insertion/deletion | Insertion/Deletion: O(1), Access: O(n) | O(n) | `List<Type> list = new LinkedList<>();` | Manipulating large collections with frequent insertions/deletions | Yes | Yes | Yes | add(), remove(), get(), size(), etc. |
| Vector          | List           | Synchronized dynamic array | Thread-safe, resizable array | Insertion/Deletion: O(n), Access: O(1) | O(n) | `List<Type> vector = new Vector<>();` | When thread safety is required | Yes | Yes | Yes | add(), remove(), get(), size(), etc. |
| Stack           | List           | LIFO stack implementation | Last-In, First-Out behavior | Insertion/Deletion: O(1), Access: O(1) | O(n) | `Stack<Type> stack = new Stack<>();` | Handling function calls, backtracking | Yes | Yes | Yes | push(), pop(), peek(), isEmpty(), etc. |
| HashSet         | Set            | Hash table implementation | Unordered, unique elements | Insertion/Deletion: O(1), Access: O(1) | O(n) | `Set<Type> set = new HashSet<>();` | Storing unique elements, membership check | Yes | No | Yes | add(), remove(), contains(), size(), etc. |
| LinkedHashSet   | Set            | Linked hash set implementation | Ordered, unique elements | Insertion/Deletion: O(1), Access: O(1) | O(n) | `Set<Type> set = new LinkedHashSet<>();` | Maintaining insertion order, uniqueness | Yes | Yes | Yes | add(), remove(), contains(), size(), etc. |
| TreeSet         | Set            | Red-black tree implementation | Sorted, unique elements | Insertion/Deletion: O(log n), Access: O(log n) | O(n) | `Set<Type> set = new TreeSet<>();` | Storing elements in sorted order | Yes | Yes | Yes | add(), remove(), contains(), size(), etc. |
| ArrayDeque      | Queue          | Array-based deque implementation | FIFO behavior | Insertion/Deletion: O(1), Access: O(1) | O(n) | `Deque<Type> deque = new ArrayDeque<>();` | Implementing queues, stacks, double-ended queues | Yes | No | Yes | add(), remove(), peek(), size(), etc. |
| PriorityQueue   | Queue          | Priority-based heap implementation | Priority ordering | Insertion/Deletion: O(log n), Access: O(1) | O(n) | `Queue<Type> queue = new PriorityQueue<>();` | Implementing priority queues | Yes | No | Yes | add(), remove(), peek(), size(), etc. |
| HashMap         | Map            | Hash table implementation | Key-value pairs, unordered | Insertion/Deletion: O(1), Access: O(1) | O(n) | `Map<KeyType, ValueType> map = new HashMap<>();` | Associating unique keys with values | Yes | No | Yes | put(), remove(), get(), containsKey(), size(), etc. |
| LinkedHashMap   | Map            | Linked hash map implementation | Key-value pairs, ordered | Insertion/Deletion: O(1), Access: O(1) | O(n) | `Map<KeyType, ValueType> map = new LinkedHashMap<>();` | Maintaining insertion order while mapping keys to values | Yes | Yes | Yes | put(), remove(), get(), containsKey(), size(), etc. |
| TreeMap         | Map            | Red-black tree implementation | Key-value pairs, sorted | Insertion/Deletion: O(log n), Access: O(log n) | O(n) | `Map<KeyType, ValueType> map = new TreeMap<>();` | Storing key-value pairs in sorted order | Yes | Yes | Yes | put(), remove(), get(), containsKey(), size(), etc. |
| ConcurrentHashMap | Map        | Thread-safe hash map | Concurrent access | Insertion/Deletion: O(1), Access: O(1) | O(n) | `Map<KeyType, ValueType> map = new ConcurrentHashMap<>();` | High-concurrency scenarios requiring thread safety | Yes | No | Yes | put(), remove(), get(), containsKey(), size(), etc. |
| Hashtable       | Map            | Hash table implementation | Legacy, thread-safe | Insertion/Deletion: O(1), Access: O(1) | O(n) | `Hashtable<KeyType, ValueType> table = new Hashtable<>();` | Legacy code, thread-safe mapping of keys to values | Yes | No | Yes | put(), remove(), get(), containsKey(), size(), etc. |
| Properties      | Map            | Key-value pairs | Configuration data | Insertion/Deletion: O(1), Access: O(1) | O(n) | `Properties props = new Properties();` | Handling configuration data | Yes | No | Yes | getProperty(), setProperty(), load(), store(), etc. |




# HashMap vs HashTable:

| Criteria      | HashMap                                | HashTable                              |
|---------------|----------------------------------------|----------------------------------------|
| Thread Safety | Not synchronized, not thread-safe      | Synchronized, thread-safe              |
| Null Values   | Allows null key and values             | Does not allow null keys or values     |
| Performance   | Generally faster due to lack of synchronization overhead | Slower due to synchronization overhead|
| Iteration     | Fail-fast iterator                     | Enumerator (legacy)                    |
| Inheritance   | Inherits from AbstractMap              | Inherits from Dictionary              |

# ArrayList vs LinkedList:

| Criteria       | ArrayList                              | LinkedList                             |
|----------------|----------------------------------------|----------------------------------------|
| Data Structure | Resizable array                        | Doubly linked list                     |
| Random Access  | Efficient (O(1))                      | Less efficient (O(n))                  |
| Insertion/Deletion | Slower for large lists (O(n))      | Faster for large lists (O(1))          |
| Memory Usage   | Less memory overhead                  | More memory overhead                   |
| Iteration      | Faster for sequential access          | Faster for sequential and random access|


# HashSet vs TreeSet:

| Criteria      | HashSet                                | TreeSet                                |
|---------------|----------------------------------------|----------------------------------------|
| Implementation| Uses HashMap internally                | Uses Red-Black tree internally         |
| Ordering      | Unordered                              | Sorted according to natural ordering or custom comparator |
| Performance   | Generally faster (O(1) for insertion, deletion, and lookup) | Slower due to ordering overhead (O(log n) for insertion, deletion, and lookup) |
| Null Values   | Allows one null value                 | Does not allow null values             |
| Use Case      | Suitable for general-purpose use cases| Suitable when elements need to be maintained in sorted order |


# Stack vs Queue:

| Criteria       | Stack                                  | Queue                                  |
|----------------|----------------------------------------|----------------------------------------|
| Data Structure | LIFO (Last In, First Out)              | FIFO (First In, First Out)             |
| Operations     | push(), pop(), peek()                 | enqueue(), dequeue(), peek()          |
| Implementation| Can be implemented using arrays or linked lists | Can be implemented using arrays or linked lists |
| Use Cases      | Used in algorithms, backtracking, expression evaluation, etc. | Used in scheduling, task management, breadth-first search, etc. |


# PriorityQueue vs TreeMap:

| Criteria       | PriorityQueue                         | TreeMap                                |
|----------------|----------------------------------------|----------------------------------------|
| Data Structure | Heap                                   | Red-Black tree                         |
| Ordering       | Orders elements based on their natural order or a custom comparator | Orders elements based on their natural order or a custom comparator |
| Operations     | Offer(), Poll(), Peek()                | Put(), Remove(), FirstKey()           |
| Use Cases      | Used in algorithms like Dijkstra's shortest path, Huffman coding, etc. | Used when you need to maintain a key-value mapping in sorted order |


# HashSet vs LinkedHashSet:

| Criteria       | HashSet                                | LinkedHashSet                          |
|----------------|----------------------------------------|----------------------------------------|
| Ordering       | Unordered                              | Maintains insertion order              |
| Implementation| Uses HashMap internally                | Uses LinkedHashMap internally          |
| Performance   | Faster (O(1) for insertion, deletion, and lookup) | Slightly slower due to maintaining insertion order |
| Use Cases      | General-purpose usage where order is not important | When you need to maintain insertion order while still having O(1) performance |


# HashMap vs LinkedHashMap:

| Criteria       | HashMap                                | LinkedHashMap                          |
|----------------|----------------------------------------|----------------------------------------|
| Ordering       | Unordered                              | Maintains insertion order              |
| Implementation| Uses array of linked lists (buckets) internally | Extends HashMap and uses a doubly linked list to maintain insertion order |
| Performance   | Generally faster                       | Slightly slower due to maintaining insertion order |
| Use Cases      | General-purpose usage where order is not important | When you need to maintain insertion order |
