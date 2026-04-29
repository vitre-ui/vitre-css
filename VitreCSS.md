# Vitre CSS Documentation

## 💎 Brand Identity
*   **Name:** Vitre
*   **Concept:** A "glass-like" finish for raw HTML. 
*   **Philosophy:** Classless styling that honors semantic tags without polluting the markup.
*   **Market Fit:** Designed as a visual companion to the modern, fast "Vite" ecosystem.

---

## 🛠 Core CSS Principles
Vitre targets elements directly to improve the look of standard HTML by default.

### 1. The Global "Glass" Variables
```css
:root {
  --vitre-primary: #3b82f6;
  --vitre-bg: #ffffff;
  --vitre-text: #1f2937;
  --vitre-border: rgba(0, 0, 0, 0.1);
  --vitre-glass-border: rgba(255, 255, 255, 0.2);
  --vitre-radius: 10px;
  --vitre-shadow: 0 4px 12px rgba(0, 0, 0, 0.05);
}
```

### 2. Classless Element Styling
```css
/* Auto-styling buttons without .btn */
button {
  appearance: none;
  background: var(--vitre-bg);
  border: 1px solid var(--vitre-border);
  border-radius: var(--vitre-radius);
  padding: 0.5em 1.2em;
  font-family: inherit;
  font-weight: 500;
  cursor: pointer;
  box-shadow: var(--vitre-shadow);
  transition: transform 0.1s ease, border-color 0.2s ease;
}

button:hover {
  border-color: var(--vitre-primary);
  background-color: #f9fafb;
}

/* Auto-styling inputs without .form-control */
input[type="text"], 
input[type="email"], 
textarea {
  width: 100%;
  padding: 0.75em;
  border: 1px solid var(--vitre-border);
  border-radius: var(--vitre-radius);
  background: rgba(255, 255, 255, 0.8);
  backdrop-filter: blur(5px);
}
```

---

## 📢 Positioning
*   **Tagline A:** "The transparent style layer."
*   **Tagline B:** "Classless CSS with a high-end finish."
*   **Tagline C:** "Clear. Light. Vitre."

---

## 💡 Next Steps
*   [ ] Build the Typography scale (h1-h6).
*   [ ] Design the classless `<table>` styles.
*   [ ] Create a "Glass" theme for code blocks `<pre><code>`.
