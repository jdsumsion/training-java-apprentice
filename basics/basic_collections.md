# Basic Collections

Here are the basic collection types:

- `ArrayList`
- `LinkedList`
- `HashMap`
- `HashSet`

More advanced types are here:
- `LinkedHashMap`
- `TreeSet`
- etc.

Big O notation for the basic types:
- `ArrayList` - O(1) for access, possibly O(n) for insert if array needs expansion, otherwise O(1)
- `LinkedList`- O(n) for access other than in-order traversal, O(1) for insert, memory is scattered, extra memory required for each item
- `HashMap` - O(1) for get, O(1) for put, unless hash collisions occur, then O(n)
- `HashSet` - implemented as a `HashMap` with null values

