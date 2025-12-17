LexRedline is a specialized Legal Tech tool designed to solve the "Version Control" crisis in corporate law. It allows legal professionals to instantly identify discrepancies between disparate document formats (PDF vs. Word) and generates a compliant .docx redline report.

🎯 The Problem
In high-stakes M&A and regulatory compliance, "Track Changes" is insufficient:

Format Friction: Comparing a "clean" PDF from opposing counsel against an internal Word draft is a manual, high-risk process.

Hidden Liability: Subtle changes (e.g., "shall" to "may") in large documents can be missed by the human eye.

Structure Loss: Standard diff tools often mangle legal formatting, making the output unreadable for attorneys.

💡 The Solution
LexRedline acts as a format-agnostic comparison engine. It ingests documents, normalizes the text, performs a semantic difference analysis, and—crucially—rebuilds a fully formatted Word document with "Track Changes" style highlighting.

🛠 Technical Architecture
This is not a simple wrapper around a library. It features a custom-built parsing engine:

Recursive HTML-to-DOCX Parser: A custom algorithm traverses the semantic tree of the difference analysis. It detects nested tags (<ins>, <del>, <span>) and recursively applies identifying logic to map them to Microsoft Word Run properties (Color, Strikethrough, Bold).

Structure Preservation: Uses a token-based injection strategy (BREAKTOKEN) to "freeze" paragraph structures during the diff process and "thaw" them during reconstruction, ensuring the final report retains readability.

Regex-Based Cleaning: Implements "Vacuum" logic to sanitize inputs from OCR-based PDFs, removing artifact line breaks while preserving paragraph integrity.

🚀 Features
Multi-Format Support: Drag-and-drop support for .pdf and .docx.

Smart Redlining: Ignores formatting noise; focuses on content changes.

Direct Export: One-click generation of a .docx file ready for client distribution.

Privacy by Design: Stateless architecture. No documents are stored on the server; RAM is cleared post-session.

💻 Tech Stack
Core: Python 3.9

Frontend: Streamlit

NLP/Diffing: Redlines, Difflib

Parsing: BeautifulSoup4, Regex (re)

Document Handling: PyPDF, Python-Docx

⚖️ Disclaimer
This tool is a prototype for educational and productivity purposes. It does not constitute legal advice and should not be the sole reliance for critical due diligence.
