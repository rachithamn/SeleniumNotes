

---

## **Polymorphism in Java**

**Definition:**
Polymorphism is the ability in Java to perform a single action in different ways.

* Derived from Greek: **“poly” = many**, **“morphs” = forms**.
* It allows objects of different classes to be treated as objects of a common superclass, enabling flexible and maintainable code.

**Types of Polymorphism:**

1. **Compile-Time Polymorphism (Method Overloading)**
2. **Runtime Polymorphism (Method Overriding)**

---

### **1. Compile-Time Polymorphism (Overloading)**

**Definition:**
Method overloading allows a class to have multiple methods with the same name but different **parameters (number, type, or both)**.

* The compiler determines which method to call based on the method signature.

**Java Examples:**

```java
class Calculator {
    int add(int a, int b) { return a + b; }
    double add(double a, double b) { return a + b; }
    int add(int a, int b, int c) { return a + b + c; }
}
```

* `substring()` in the `String` class is overloaded to accept different start and end indices.
* `println()` in `System.out` is overloaded for different data types (int, String, char, etc.).

**Selenium WebDriver Examples:**

* `frame()` method is overloaded:

  ```java
  driver.switchTo().frame(0);          // by index
  driver.switchTo().frame("frameName");// by name or ID
  driver.switchTo().frame(WebElement);// by WebElement
  ```

**Advantages of Overloading:**

* **Flexibility:** Handles different argument types and numbers.
* **Readability:** Same method name for similar actions on different inputs.
* **Reduces Complexity:** Simplifies code maintenance and organization.

---

### **2. Runtime Polymorphism (Overriding)**

**Definition:**
Method overriding occurs when a subclass provides a **specific implementation** of a method already defined in its superclass.

* Key feature of runtime polymorphism.
* The **method in the subclass** is called at runtime, allowing dynamic behavior.

**Rules for Overriding:**

1. Same method name, return type, and parameters.
2. Cannot reduce the visibility of the inherited method.
3. Can throw fewer or narrower exceptions.

**Java Examples:**

```java
class Parent {
    void display() { System.out.println("Parent display"); }
}

class Child extends Parent {
    @Override
    void display() { System.out.println("Child display"); }
}
```

* `equals()` and `toString()` in `String` class override methods from `Object` class.

**Selenium WebDriver Example:**

* `quit()` in `ChromiumDriver` overrides `quit()` in `RemoteWebDriver` to provide specific behavior.

**Advantages of Overriding:**

* Supports **dynamic method dispatch**.
* Enables **runtime flexibility**.
* Promotes **code reusability and abstraction**.

---

**Summary:**

| Feature               | Compile-Time (Overloading)             | Runtime (Overriding)               |
| --------------------- | -------------------------------------- | ---------------------------------- |
| **When resolved**     | Compile time                           | Runtime                            |
| **Method signature**  | Must differ (parameters)               | Must be same                       |
| **Polymorphism type** | Static                                 | Dynamic                            |
| **Example**           | `add()` methods, `frame()` in Selenium | `toString()`, `quit()` in Selenium |

---


