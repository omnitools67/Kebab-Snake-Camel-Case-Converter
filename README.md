# Kebab, Snake & Camel Case Converter 🖋️

A lightweight, zero-dependency, client-side web utility to instantly convert text strings into **Kebab-case**, **Snake_case**, and **CamelCase**. Designed specifically for SEO specialists, web developers, and database managers.

---

## 🚀 Live Demo
Try the live working tool online:  
👉 **[Case Converter Studio on Omni Tools](https://www.omnitools.pk/kebab-case/)**

---

## ✨ Features
* **Real-time Conversion:** Formats text instantly as you type[cite: 2].
* **Three Popular Cases:**
  * **Kebab-case:** Ideal for SEO-friendly URL slugs (e.g., `my-new-post`)[cite: 2].
  * **Snake_case:** Perfect for Python variables and database column naming (e.g., `my_new_post`)[cite: 2].
  * **CamelCase:** Tailored for JavaScript, Java, and class properties (e.g., `myNewPost`)[cite: 2].
* **100% Client-side & Privacy-Focused:** All logic runs locally in the browser. Zero data transmission to any external server[cite: 2].
* **One-Click Copy:** Fast clipboard copying with instant visual feedback[cite: 2].
* **Zero Dependencies:** Pure HTML5, CSS3, and Vanilla JavaScript—no frameworks required[cite: 2].

---

## 💻 Code Snippet (Core Logic)

Here is the underlying JavaScript string formatting logic used in this tool:

```javascript
// Kebab-case (URL Friendly)
const kebab = str.toLowerCase().trim()
    .replace(/[^\w\s-]/g, '')
    .replace(/[\s_-]+/g, '-');

// Snake_case (Database/Python)
const snake = str.toLowerCase().trim()
    .replace(/[^\w\s-]/g, '')
    .replace(/[\s-]+/g, '_');

// CamelCase (JavaScript/Java)
const camel = str.replace(/(?:^\w|[A-Z]|\b\w)/g, (word, index) => {
    return index === 0 ? word.toLowerCase() : word.toUpperCase();
}).replace(/\s+/g, '').replace(/[^\w]/g, '');