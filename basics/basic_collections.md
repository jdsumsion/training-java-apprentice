# Basic Collections

Here are the basic collection types:

- `ArrayList` (backed by `Object[]`)
- `LinkedList` (backed by per-item node with next/prev pointers)
- `HashMap` (backed by hash bucket array with lists for collisions)
- `HashSet` (backed by hash bucket array with lists for collisions)

More advanced types are here:
- `LinkedHashMap`
- `TreeSet`
- etc.

Here is how the basic types are implemented:
- `ArrayList` (backed by `Object[]`)
- `LinkedList` (backed by per-item node with next/prev pointers)
- `HashMap` (backed by hash bucket array with lists for collisions)
- `HashSet` (backed by hash bucket array with lists for collisions)

Order of execution the basic types (Big-O notation):
- `ArrayList`
  - get by index: O(1)
  - set by index: O(1) unless expansion is needed, O(n) if expansion occurs
  - traverse: O(1) per item
- `LinkedList`
  - get by index: O(n)
  - set by index: O(n)
  - traverse: O(1) per item
  - NOTE: extra memory required for each item
- `HashMap`
  - get: O(1) unless hash collision
  - put: O(1) unless hash collision
  - traverse: O(1) per item
  - hash collisions can cause O(n) access in the worst case
- `HashSet`
  - get: O(1) unless hash collision
  - put: O(1) unless hash collision
  - traverse: O(1) per item
  - implemented as a `HashMap` with the set values as keys and with unused null values

---

Collections quiz

What is the difference between order of execution of `ArrayList.get(100)` and `LinkedList.get(100)`?
- [ ] there is no difference
- [ ] `ArrayList` is O(n) and `LinkedList` is O(1)
- [ ] `ArrayList` is O(log(n)) and `LinkedList` is O(n)
- [x] `ArrayList` is O(1) and `LinkedList` is O(n)

> Think about how `LinkedList` is implemented.  Ask yourself how it finds the 100th element.  Is `ArrayList` any different?

What is the worst case `HashMap` order of execution for `get` and `put`?
- [ ] O(1)
- [ ] O(log(n))
- [x] O(n)

> What happens when all keys hash to the same hash code?  How is `HashMap` implemented in that case?

What statements are true about how `LinkedList` and `ArrayList` use memory?
- [ ] `LinkedList` is more expensive to grow
- [x] `LinkedList` is more expensive per item
- [x] `ArrayList` takes more memory than just the size of the items
- [ ] `ArrayList` takes more memory than `LinkedList` per item
- [x] `ArrayList` memory size is proportional to the its capacity

> Think about how `ArrayList` and `LinkedList` are implemented.

What is the difference between order of execution of `HashMap.get()` and `HashSet.get()`?
- [x] there is no difference
- [ ] `HashMap` is more expensive than `HashSet` because it has to keep track of values
- [ ] `HashSet` is faster because it has to keep track of less data

> Think about how `HashSet` is implemented.  Ask yourself how it differs from `HashMap`.

---
