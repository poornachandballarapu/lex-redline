# ⚖️ LexRedline: Intelligent Legal Document Comparison

**Live Demo:** 

### The Problem
In High-Stakes M&A and Corporate Law, "Version Control" is a massive risk. 
- "Track Changes" fails when comparing PDFs against Word Docs.
- Manual comparison of 400+ page regulatory drafts is prone to human error.
- "Clean" PDFs from opposing counsel may hide subtle liability shifts.

### The Solution
**LexRedline** is a Python-based Legal Tech tool designed to automate redlining with semantic awareness.

### Key Features
- **Format Agnostic:** Compares PDF vs. Word, Word vs. Text, etc.
- **Structure Preservation:** Uses a custom Recursive Parser to maintain paragraph integrity during analysis.
- **Diff-to-Docx Engine:** Generates a fully formatted MS Word (.docx) file with standard Legal Redlines (Green/Red) for immediate use.
- **Privacy First:** Stateless processing. No documents are stored on the server.

### Tech Stack
- **Python 3.9**
- **NLP:** Redlines library for semantic diffing.
- **Parsers:** BeautifulSoup4, PyPDF, Python-Docx.
- **Frontend:** Streamlit.
