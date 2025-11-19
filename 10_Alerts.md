

---

## **Alert in Selenium WebDriver**

**Definition:**
An **Alert** is a small pop-up message box in the browser used to **notify, confirm, or collect input** from the user.

* Usually JavaScript-based
* Can be **modal** (blocks interaction) or **non-modal** (HTML-based, like Sweet Alerts)

**Why Alerts Are Used:**

1. **Notify users** – show warnings or info
2. **Confirm actions** – OK/Cancel before proceeding
3. **Collect input** – get user data

---

### **Types of Alerts**

| Type                        | Description                                                 |
| --------------------------- | ----------------------------------------------------------- |
| **Simple Alert**            | Info message with **OK** button                             |
| **Confirmation Alert**      | **OK/Cancel** buttons to accept/reject                      |
| **Prompt Alert**            | Input field + OK/Cancel for user input                      |
| **Sweet Alert (Non-Modal)** | HTML-based, customizable, can be inspected as a web element |

---

### **Handling Alerts in Selenium**

**Switching Focus:**

```java
Alert alert = driver.switchTo().alert();
```

* Returns an **Alert interface**
* Implemented via **RemoteAlert** class

**Alert Actions:**

| Method             | Description                      |
| ------------------ | -------------------------------- |
| `accept()`         | Click **OK**                     |
| `dismiss()`        | Click **Cancel**                 |
| `getText()`        | Get alert message                |
| `sendKeys(String)` | Enter input in **prompt alerts** |

**Special Case – Sweet Alerts:**

* Handled like **regular web elements** using standard Selenium methods

---

### **Exceptions Related to Alerts**

| Exception                 | Cause                                              |
| ------------------------- | -------------------------------------------------- |
| `NoAlertPresentException` | No alert is present when an operation is attempted |
| `UnhandledAlertException` | Alert exists but Selenium cannot handle it         |

---


