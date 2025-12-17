# ⚖️ Lex Redline

![Python](https://img.shields.io/badge/Python-3.9-blue?style=for-the-badge&logo=python&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=Streamlit&logoColor=white)
![Status](https://img.shields.io/badge/Status-Prototype-orange?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

### **Intelligent Legal Document Comparison Engine**

**🔴 Live Demo:** *[ 🚀 Deployment In Progress... Check back in 5 minutes! ]*

---

### 🎯 The Problem
In high-stakes M&A and corporate law, "Version Control" is a critical risk factor.
* **Format Friction:** Comparing a "clean" PDF from opposing counsel against an internal Word draft is a manual, high-risk process.
* **Hidden Liability:** Subtle changes (e.g., changing "shall" to "may") in 100+ page documents can be missed by the human eye.
* **Structure Loss:** Standard diff tools often mangle legal formatting, making the output unreadable for attorneys.

### 💡 The Solution
**LexRedline** is a format-agnostic comparison engine. It ingests documents (PDF or Docx), performs a semantic difference analysis, and rebuilds a fully formatted Word document with "Track Changes" style highlighting.

### 🚀 Key Features
* **Multi-Format Support:** Drag-and-drop comparison for `.pdf` and `.docx`.
* **Smart Redlining:** Uses NLP-based logic to ignore formatting noise and focus on content changes.
* **Direct Export:** Generates a professional `.docx` file ready for client distribution.
* **Privacy by Design:** Stateless architecture. No documents are stored on the server; RAM is cleared post-session.

---

### 🛠 Technical Architecture
This tool uses a custom **Recursive HTML-to-DOCX Parser**.
1.  **Ingestion:** Extracts text using `pypdf` and `python-docx`.
2.  **Normalization:** Cleans OCR artifacts using Regex.
3.  **Diffing:** `Redlines` library calculates semantic differences.
4.  **Reconstruction:** A custom algorithm traverses the HTML tree, mapping `<ins>` and `<del>` tags to Microsoft Word `Run` properties (Color, Strikethrough, Bold) while preserving paragraph structure.

### 💻 Tech Stack
* **Core:** Python 3.9
* **Frontend:** Streamlit
* **Parsers:** BeautifulSoup4, Regex
* **Document Handling:** PyPDF, Python-Docx

---

### ⚖️ Disclaimer
*This tool is a prototype developed for educational purposes. It does not constitute legal advice.*

---

### 👨‍💻 About the Developer
Built by **Poorna Chand Ballarapu**, a dual-degree student bridging the gap between Law and Technology.
* **Law:** 3rd Year B.A. LL.B (Hons) at **NALSAR University of Law**.
* **Tech:** B.S. in Data Science & Applications at **IIT Madras**.
* **Focus:** Leveraging Computational Law and NLP to automate complex legal workflows in M&A and Finance.
