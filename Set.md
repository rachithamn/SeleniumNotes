

---

## **Set in Java**

**Definition:**
A **Set** is an **unordered collection** that **does not allow duplicate values**.

**Key Points:**

1. **Order depends on implementation**:

   * **HashSet:** Random order (uses hashing)
   * **LinkedHashSet:** Maintains insertion order
   * **TreeSet:** Sorted in ascending (ASCII) order

2. **No duplicates:**

   * Duplicate elements are automatically ignored
   * Cannot use `get(index)` as Sets are **index-free**

**Example:**

```java
int num[] = {1,2,3,4,4,5,67,9};
List<Integer> list = Arrays.asList(num);
list.get(4); // 4 (index-based)

Set<Integer> set = new HashSet<>(list);
set; // [1, 2, 3, 4, 5, 67, 9] - duplicate 4 removed, no indexing
```

3. **Index-based retrieval is not possible** in a Set.

**Tip:** Use **Set** when **uniqueness** is required, not order or indexing.

---

