# 🐍 The Python Dojo: Path of the Code Warrior

> *"A journey of a thousand lines begins with a single import."*

**The Python Dojo** is a gamified, browser-based learning environment designed to take a student from almost zero knowledge to Data Science proficiency. It runs entirely in the browser using **Pyodide** (WebAssembly), meaning no backend server is required.

The curriculum is wrapped in a martial arts narrative, where the user progresses from a wandering White Belt to a Grandmaster of the Dojo.

## 🌟 Features

* **100% Client-Side Python:** Powered by [Pyodide](https://pyodide.org/), allowing real Python code (including Numpy, Pandas, and Scikit-Learn) to run directly in the browser.
* **30-Level Story Arc:** A complete curriculum divided into 4 Acts.
* **Persistent Progress:** Uses `localStorage` to save your code and unlock status automatically.
* **Live Visualization:** Renders `matplotlib` charts directly in the chat output.
* **Interactive Validator:** A "Sensei" logic engine that checks variable types, output values, and specific syntax usage to provide custom feedback.
* **Reward System:** Generates a downloadable, high-quality SVG **Certificate of Mastery** upon completion.

## 📜 The Syllabus

The Dojo is divided into four distinct acts of mastery:

### Act I: The Katana of Logic (Basics)

* **Levels 1-5:** Variables, Math, Strings, Lists.
* **Levels 6-9:** Loops (For/While), Dictionaries, Functions.
* **Levels 10-13:** Modules (`random`), Classes & OOP, Error Handling (`try/except`).
* **Boss Battle:** *The Shadow Ronin* (Logic & OOP).

### Act II: The Archive (Data Engineering)

* **Levels 14-16:** Numpy Arrays (Vectorization), Pandas DataFrames.
* **Levels 17-18:** Data Cleaning (`dropna`, `isnull`), Indexing (`.loc`).

### Act III: The Oracle's Vision (Statistics & Viz)

* **Levels 19-22:** Descriptive Stats (`.describe`), Std Dev, Z-Scores, Correlation matrices.
* **Level 23:** *The High Priestess* (Data Cleaning + Visualization).

### Act IV: The Prophecy (Machine Learning)

* **Level 24:** Hypothesis Testing (T-Tests/P-Values).
* **Level 25:** Linear Regression (Predicting values).
* **Level 26:** NLP Basics (CountVectorizer).
* **Level 27:** Classification (Logistic Regression).
* **Level 28:** Clustering (K-Means).
* **Level 29 (FINAL BOSS):** *The Grandmaster's Prophecy* (End-to-end Data Science project).

---

## 🛠️ Customization

**Structure of a Level:**

```javascript
101: {
    title: "Lesson Name",
    description: "The story text goes here.",
    tasks: ["Task 1", "Task 2"],
    initialCode: "# Starter code",
    success: "Message shown when passed.",
    validate: (pyodide, output) => {
        // Access Python variables
        let x = pyodide.globals.get('x');
        
        // Return logic
        if (x === 10) return { passed: true, feedback: "Good job!" };
        return { passed: false, errors: ["x must be 10"] };
    }
}
```

---

*“Discipline will take you places motivation cannot.”* ⛩️