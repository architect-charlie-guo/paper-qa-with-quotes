### **Experiment 1: Interactive Question-Answering with a PDF via OpenAI API**
**Objective:**  
Test the feasibility of loading a PDF file directly into a conversation thread using OpenAI API, enabling users to ask questions about the content.

**Success Criteria:**  
- The API successfully processes the PDF content.  
- Questions are answered with clear references to the document text.  
- Performance is acceptable even for larger files.

---

### **Experiment 2: Quote Searching, Highlighting, and Labeling in a PDF using PyMuPDF**  
**Objective:**  
Determine if PyMuPDF or similar PDF libraries can:  
1. Search for specific quotes in a PDF.
   * The quote may not be 100% precise, so fuzzy match need to be used.
   * A quote may fall on two pages, so it's challenge. It's acceptable to convert the PDF to HTML before highlighting and labelling quotes. 
3. Highlight the quotes.
4. Add numeric labels (e.g., 1, 2, 3) to the highlights for easier identification.  

**Success Criteria:**  
- Quotes are accurately located and highlighted.  
- Numeric labels are visually displayed and correspond correctly to the quotes.  
- The process is scalable and efficient for documents with numerous quotes.

