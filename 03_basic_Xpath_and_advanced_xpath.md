

---

# ⭐ **XPath Basics (Short & Clear Notes)**

## 📌 **Absolute XPath**

* Starts from root → `/html/...`
* Long, fragile, not recommended
  ✔ Example:
  `/html/body/div[1]/form/input[1]`

---

## 📌 **Relative XPath**

* Starts with `//` → can begin anywhere in DOM
* Flexible, widely used
  ✔ Example:
  `//input[@id='username']`

---

# 🔥 **Types of Basic XPath**

## 1️⃣ **Attribute-based XPath**

```
//tag[@attribute='value']
```

✔ `//input[@id='password']`

---

## 2️⃣ **Text-based XPath**

```
//tag[text()='textvalue']
```

✔ `//span[text()='Hello, sign in']`

---

## 3️⃣ **Partial Attribute XPath**

```
//tag[contains(@attribute,'partial')]
```

✔ `//input[contains(@id,'twotab')]`

---

## 4️⃣ **Partial Text XPath**

```
//tag[contains(text(),'partialtext')]
```

✔ `//a[contains(text(),'SFA')]`

---

## 5️⃣ **Index-based XPath**

```
(//tag[@attribute='value'])[2]
```

✔ `(//a[contains(text(),'Lead')])[3]`

---

---

# **Advanced XPath Cheatsheet**

### **1) Parent → Child**

**Syntax:**
`//parentTag[@attr='value']/childTag`
**Example:**

```xpath
//p[@class='top']/input
```

---

### **2) Grandparent → Grandchild**

**Syntax:**
`//grandParentXPath//grandChildTag`
**Example:**

```xpath
(//form[@id='login']//input)[1]
```

---

### **3) Child → Parent**

**Syntax:**
`//childTag[@attr='value']/parent::parentTag`
**Example:**

```xpath
//input[@id='password']/parent::p
```

---

### **4) Grandchild → Grandparent**

**Syntax:**
`//grandChildTag[@attr]/ancestor::grandParentTag`
**Example:**

```xpath
//input[@class='decorativeSubmit']/ancestor::form
```

---

### **5) Elder Cousin → Younger Cousin**

**Syntax:**
`//elderCousinTag[condition]/following::youngerCousinTag`
**Example:**

```xpath
(//span[text()='Company Name']/following::input)[1]
```

---

### **6) Younger Cousin → Elder Cousin**

**Syntax:**
`//youngerCousinTag/preceding::elderCousinTag`

---

### **7) Elder Sibling → Younger Sibling**

**Syntax:**
`//elderSibling/following-sibling::youngerSiblingTag`
**Example:**

```xpath
//label[text()='Username']/following-sibling::input
```

---

### **8) Younger Sibling → Elder Sibling**

**Syntax:**
`//youngerSibling/preceding-sibling::elderSiblingTag`

---


