

---

# **📌 Inheritance — Short & Clear Notes**

### **🔹 What is Inheritance?**

Inheritance is an OOP concept where one class **inherits** properties and methods from another class using the **`extends`** keyword.
It helps in **code reusability, readability**, and creating **class hierarchies**.

---

# **⭐ Advantages**

* **Reusability:** No need to rewrite common code.
* **Easy Maintenance:** Clear parent–child structure.
* **Less Code, More Clarity:** Reduces duplication.
* **Supports OOP Hierarchy:** Helps achieve clean architecture.

---

# **🌳 Types of Inheritance**

| Type             | Meaning                                                                     |
| ---------------- | --------------------------------------------------------------------------- |
| **Single**       | One child inherits one parent                                               |
| **Multilevel**   | A → B → C chain                                                             |
| **Hierarchical** | One parent → many children                                                  |
| **Multiple**     | One class inherits multiple parents (achieved using **interfaces** in Java) |
| **Hybrid**       | Combination of multiple + multilevel/hierarchical                           |

---

# **🟦 Real Java Examples**

* `Integer extends Number`
* `RuntimeException extends Exception`
* `ArrayList implements List`
* `List extends Collection`

---

# **🟩 Selenium Examples**

* `ChromeDriver extends ChromiumDriver`
* `EdgeDriver extends ChromiumDriver`
* `ChromiumDriver extends RemoteWebDriver`
* `RemoteWebDriver implements WebDriver`

---

# **🧑‍💻 Real-Time Example (Framework Usage)**

### **Where do we use inheritance in a Selenium Framework?**

✔ **Base Test Class**
Contains: driver setup, teardown, waits, screenshot methods
→ All test classes **extend** this class.

**Example:**

```java
public class BaseClass {
    WebDriver driver;
    // setup, teardown, utilities
}

public class LoginTest extends BaseClass {
   @Test
   public void runLogin() {
       driver.findElement(...);
   }
}
```

✔ **Page Object Model (POM)**
Reusable methods stored in a parent class → child page classes inherit them.

✔ **Utility Classes**
Base utility class → extended by multiple modules.

---

# **🎤 Interview Answer (Perfect 20–30 sec)**

**“Inheritance in Java allows one class to acquire properties and methods of another class using the `extends` keyword. It improves code reusability, readability, and creates a clear hierarchy. Java supports single, multilevel, hierarchical, and hybrid inheritance—while multiple is achieved through interfaces.
In real-time, Selenium classes like ChromeDriver extend ChromiumDriver. In my framework, I used Inheritance in the BaseClass, where all test classes extend the BaseClass to reuse driver setup, teardown, and utility methods.”**

---

