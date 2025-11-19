
---

## **Abstraction in Java**

**Definition:**
Hides complex implementation details and shows only essential features. Focuses on **what an object does**, not **how it does it**.

**Advantages:**

* **Simplicity:** Easier to use objects without knowing inner details.
* **Reusability:** Abstract classes/interfaces can be reused in multiple subclasses.

**Keywords:** `abstract` (class), `implements` (interface)

**Types:**

1. **Interface:** Full abstraction, no implementation. Example: `WebDriver`, `WebElement`, `Alert`.
2. **Abstract Class:** Partial abstraction with some implemented methods. Example: `AbstractList`, `AbstractCollection`, `By`.
3. **Concrete Class:** Full implementation. Example: `RemoteWebDriver`.

---

## **List Interface in Java**

**Definition:**
An **ordered collection** that allows duplicates and dynamic resizing. Part of Java Collections Framework.

**Why Use List:**

* When order matters
* Frequent additions/removals
* Unknown number of elements

**Common Implementations:**

* **ArrayList:** Fast access, good for large collections
* **LinkedList:** Efficient for frequent insertions/deletions

**Key Methods & Real-time Use Cases:**

| Method                     | Usage                       | Example                      |
| -------------------------- | --------------------------- | ---------------------------- |
| `add(element)`             | Add an item                 | Add a new employee name      |
| `add(index, element)`      | Insert at specific position | Insert a task at position 2  |
| `addAll(list)`             | Merge lists                 | Combine two customer lists   |
| `get(index)`               | Access element              | Retrieve a specific order    |
| `remove(index)`            | Remove element              | Delete discontinued product  |
| `removeAll(collection)`    | Remove all matching         | Filter outdated items        |
| `size()`                   | Number of elements          | Count students in a course   |
| `clear()`                  | Remove all elements         | Empty shopping cart          |
| `System.out.println(list)` | Print all elements          | Display list of participants |

**Tip:** Use **ArrayList** for fast random access and **LinkedList** for frequent insertions/deletions.

---

