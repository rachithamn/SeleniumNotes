
---

# ✨ String Creation & Comparison in Java

## 🔹 **String Creation**

### **1️⃣ String Literal**

* Example: `String name = "TestLeaf";`
* Stored in the **String Pool**.
* If another literal has the same value, Java **reuses** the same object.
* ✔️ **Memory efficient**

```java
String name1 = "TestLeaf";
String name2 = "TestLeaf"; // Reused from String Pool
```

---

### **2️⃣ Using `new` Keyword**

* Example: `String str = new String("TestLeaf");`
* Always creates a **new object** in Heap (outside Pool).
* Even identical values ➝ **different objects**

```java
String str1 = new String("TestLeaf");
String str2 = new String("TestLeaf"); // New object again
```

---

## 🔹 **String Comparison**

### **👉 Using `==` (Reference Check)**

* Checks if both references point to **same object**.
* Literal vs new ➝ **not equal**

```java
name1 == str1  // false
```

---

### **👉 Using `.equals()` (Value Check)**

* Compares **contents** of strings.
* Even if objects are different, values match.

```java
str1.equals(str2); // true
```

---

### **👉 Using `.equalsIgnoreCase()`**

* Compares **values ignoring case**.

```java
"TestLeaf".equalsIgnoreCase("testleaf"); // true
```

---

## 🔹 **Important Notes**

* **String are Immutable** → any change creates a new object.
* **String Pool improves memory usage**.
* **Comparisons are case-sensitive** unless using `equalsIgnoreCase()`.

---

