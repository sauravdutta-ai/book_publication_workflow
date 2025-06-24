#  Automated Book Publication Workflow

A smart, AI-driven content pipeline that simulates the real-world publishing workflow—automating content scraping, intelligent rewriting, human-in-the-loop editing, and versioned storage of book chapters.

Developed as part of the AI Internship assignment for **Softnerve Technology**.

---

## 🚀 Key Features

- 🔍 **Web Scraping & Screenshots**  
  Automatically extracts book chapters and captures visual snapshots from [Wikisource](https://en.wikisource.org/wiki/The_Gates_of_Morning/Book_1/Chapter_1) using `Playwright`.

- ✍️ **AI-Powered Writing & Reviewing**  
  Uses **Google Gemini API** to rewrite (spin) the chapter text for clarity and engagement, followed by grammar and tone refinement via an AI reviewer.

- 🧠 **Human-in-the-Loop Interaction**  
  Seamlessly incorporates suggestions from human writers, editors, or reviewers after each AI pass to simulate a multi-iteration editorial process.

- 🗃️ **Versioned Storage & Search**  
  Saves every stage (original, AI-written, reviewed, human suggestions) in structured text format. Prepares for integration with **ChromaDB** and **RL search algorithms** for intelligent version retrieval.

---

## 🧰 Tech Stack

| Tool        | Purpose                          |
|-------------|----------------------------------|
| `Python`    | Core scripting language          |
| `Playwright`| Browser automation & scraping    |
| `Gemini API`| Large Language Model (AI writer) |
| `ChromaDB`  | Versioned vector storage (future ready) |
| `Git`       | Version control & collaboration  |

---


---

##  How It Works

1. **Scraping**  
   Fetches raw text and screenshot of the chapter page.

2. **AI Writer Agent**  
   Rewrites the content using Gemini Pro or Gemini Flash.

3. **AI Reviewer Agent**  
   Refines grammar, tone, and structure for publication-readiness.

4. **Human Suggestions**  
   Prompts the user for feedback/suggestions after each iteration.

5. **Data Storage**  
   Saves each version as a `.txt` file in the `data/` directory.

---

## ▶️ Getting Started

### ✅ Step 1: Install dependencies

```bash
pip install -r requirements.txt
```

### ✅ Step 2: Run the pipeline

```bash
python main.py
```

### 📁 Output Files

| File        | Description                          |
|-------------|----------------------------------|
| `original_chapter.txt`    | Raw scraped text          |
| `spun_chapter.txt`| AI-rewritten version    |
| `reviewed_chapter.txt`| AI-refined version |
| `suggestions.txt`  | Human input for improvement |
| `chapter1.png`       | Screenshot of the source webpage  |

### Sample Suggestion (Human Input Example)

"Use simpler vocabulary in the dialogue parts."
"Add a one-line summary at the beginning."
"Translate the final paragraph to Hindi."

### Future Scope

- 🌐 **Auto-translate chapters using multilingual mode**
- 📑 **Generate summaries and titles with LLM agents**
- 🗨️ **Allow collaborative feedback like Google Docs**
- 🧠 **Integrate ChromaDB with RL-powered search**

### License & Attribution

This project was created solely for evaluation purposes for the internship role at Softnerve Technology.
All rights are retained by the developer. No commercial use is intended or permitted.

### Acknowledgements

Special thanks to the Softnerve team for crafting such an engaging and realistic assignment that combines AI, automation, and editorial creativity.
