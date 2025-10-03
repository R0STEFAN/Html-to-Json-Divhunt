# 🚀 DivHunt HTML/CSS JSON Converter


**Stop Manual CSS Migration — Convert Any Raw HTML/CSS to DivHunt JSON Instantly!**

This tool is designed to simplify the migration of custom components and external code into the DivHunt platform by transforming standard HTML and CSS into the platform's required JSON format.

---

## ✨ Key Features (Stable v15.2)

| Feature | Benefit for the Community |
| :--- | :--- |
| **Full Structure Conversion** | Recursively converts all elements (`<section>`, `<div>`, `h1`, etc.) into the DivHunt JSON tree. |
| **Full CSS Support** | Parses **Raw CSS** (including `linear-gradient` and vendor prefixes) and applies it to the correct element's `css` field. |
| **Robust Pseudo-Selector Support** | Correctly imports and formats styles for **`:hover`**, **`::before`**, **`::after`** as separate keys within your class styles. |
| **NEW: Advanced Combinator Handling** | Automatically transfers styles from CSS combinators (e.g., `.about-text p`) and applies them as local styles to the parent class, ensuring styles don't get ignored. |
| **NEW: Zero-Style Class Assurance** | Uses a reliable method to give every class from your HTML (even those without any CSS) a unique identity, **preventing DivHunt from replacing it** with a generic class. |
| **ID & Inline Style Support** | Correctly imports `id` attributes and parses inline `style` attributes, applying them as local styles (highest specificity). |

---

## 🛠️ How to Use (Local Installation)

This converter is a single-file, browser-based utility, making it extremely easy to run.

1.  **Download:** Clone this repository or save the `index.html` file.
2.  **Open:** Open `index.html` directly in your web browser.
3.  **Paste & Convert:** Paste your HTML into the top input and your CSS into the bottom input.

---

[Переглянути відео](demo.mp4)


## ⚠️ Critical Notes & Limitations

Please be aware of the following technical details for successful import:

### 1. Code Cleanliness (Crucial)

The converter uses a simplified parser. **Ensure your HTML and CSS inputs are clean:**

*   **Remove all comments** (`/* ... */`) before pasting your CSS.
*   **Remove all empty CSS rules** (`.class {}`).

### 2. Responsiveness Caveat

*   This converter does **NOT** correctly interpret full `@media (max-width)` logic for DivHunt's breakpoint system.
*   All imported styles will be applied to **all breakpoints** (defaulting to the desktop/1920px view).
*   **Action Required:** You will need to manually adjust mobile and tablet styles within the DivHunt builder after import.

### 3. JSON Import Limits

*   **Avoid:** Do not attempt to convert an entire, multi-screen HTML page at once (DivHunt has JSON payload limits).
*   **Recommendation:** Convert your content in chunks of **1-2 sections** at a time.
*   **Tip:** If you are importing large chunks, consider using a JSON Minifier to reduce the file size before pasting it into DivHunt.

---

## 💬 Feedback & Contributions

This tool was created to solve a community workflow challenge. Feedback, bug reports, and contributions are highly welcome!

**Happy coding!**
