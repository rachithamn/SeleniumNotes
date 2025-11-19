

---

## **Window Handling in Selenium**

**What is a Window Handle?**

* A **unique identifier (String)** assigned by Selenium to each open browser window or tab.
* Acts like an **address**, allowing WebDriver to control a specific window.

**Why Window Handles Are Important:**

* Web apps can open **multiple windows/tabs**.
* Selenium needs a unique ID to interact with elements in the correct window.

---

### **Methods to Handle Windows**

| Method                            | Description                                          |
| --------------------------------- | ---------------------------------------------------- |
| `getWindowHandle()`               | Returns the **ID of the current window**             |
| `getWindowHandles()`              | Returns a **Set of IDs** of all open windows         |
| `switchTo().window(windowHandle)` | Switches control to the **window with the given ID** |

---

### **Handling Multiple Windows**

**Steps:**

1. Retrieve all window handles:

```java
Set<String> handles = driver.getWindowHandles();
```

2. Convert the set to a list (if needed for sequential access):

```java
List<String> windows = new ArrayList<>(handles);
```

3. Switch to the desired window:

```java
driver.switchTo().window(windows.get(1)); // switch to second window
```

**Tip:** Always **switch back** to the original window if needed:

```java
driver.switchTo().window(windows.get(0));
```

---
