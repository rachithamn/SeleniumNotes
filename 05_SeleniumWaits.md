

---

# **🕒 Selenium Waits — Complete Notes**

## **1️⃣ Implicit Wait**

* Applies **globally** to all elements once set.
* Selenium **exits early** if the element is found before timeout.
* If element is not found within given time →
  ❌ **Throws:** `NoSuchElementException`

**Syntax:**

```java
driver.manage().timeouts().implicitlyWait(Duration.ofSeconds(10));
```

---

## **2️⃣ Explicit Wait**

* Used for **specific elements** only (not global).
* Waits until a **certain condition** is met.
* More **customizable and reliable** than implicit wait.

**Example:**

```java
WebDriverWait wait = new WebDriverWait(driver, Duration.ofSeconds(10));
wait.until(ExpectedConditions.visibilityOfElementLocated(By.id("username")));
```

---

## **3️⃣ Fluent Wait**

* Similar to explicit wait but more flexible.
* Lets you set:

  * ⏱️ Max time
  * 🔁 Polling interval
  * ❌ Ignore exceptions

**Example:**

```java
Wait<WebDriver> wait = new FluentWait<>(driver)
    .withTimeout(Duration.ofSeconds(20))
    .pollingEvery(Duration.ofSeconds(2))
    .ignoring(NoSuchElementException.class);

wait.until(driver -> driver.findElement(By.id("username")));
```

---

# 🎯 **Quick Comparison Table**

| Wait Type         | Scope       | Early Exit | Conditions Support | Best Use                          |
| ----------------- | ----------- | ---------- | ------------------ | --------------------------------- |
| **Implicit Wait** | Global      | ✔️ Yes     | ❌ No               | Basic element load delays         |
| **Explicit Wait** | Per element | ✔️ Yes     | ✔️ Yes             | Specific elements with conditions |
| **Fluent Wait**   | Per element | ✔️ Yes     | ✔️ Yes + polling   | Slow-loading or dynamic elements  |

---

