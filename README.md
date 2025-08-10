[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/vgbm4cZ0)
---
OPEN THIS COLLAB LINK TO ACESS:
[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1jmty9yRENi3zkND6PYwB11zN9NieTWky?usp=sharing)
---
Demo video:
[![Watch the video](https://img.youtube.com/vi/vsBaMhNOiuA/0.jpg)](https://www.youtube.com/watch?v=vsBaMhNOiuA)

---

# ADGM Company Compliance Checker

### AI-Powered Document Review System for ADGM Business Setup! ✨

Transform your company documents into ADGM-compliant files with smart AI annotations and suggestions! 🚀

## 📋 What This Does

*   **🎯 Main Purpose:** Check if your business documents meet ADGM (Abu Dhabi Global Market) requirements!

## ✨ Amazing Features

*   **📤 Upload documents** (`PDF`/`DOCX`) through a web interface.
*   **🤖 AI Classification** - Automatically detects document types.
*   **📋 Smart Checklist** - Compares against ADGM requirements.
*   **🔴 Red Annotations** - Adds comments directly in your `DOCX` files.
*   **📦 ZIP Download** - Get all reviewed documents at once.
*   **📊 JSON Reports** - Detailed compliance summary.

## 🚀 How to Use (Google Colab)

### 🔥 Quick Start - 3 Easy Steps:

1.  **Open Google Colab 🌐**
    *   Go to [Google Colab]([https://colab.research.google.com/](https://colab.research.google.com/drive/1jmty9yRENi3zkND6PYwB11zN9NieTWky?usp=sharing)).
    *   Upload the `valura-1.ipynb` file.
    *   Make sure GPU is enabled (`Runtime` → `Change runtime type` → `GPU`).

2.  **Install Everything 📦**
    *   Run the first cell (marked with 🎓):
    ```python
    # This installs all needed packages
    !pip install pyngrok streamlit docx python-docx chromadb pdfplumber beautifulsoup4
    !pip install -q -U google-genai
    ```

3.  **Download Sample Data 🌴**
    *   Run the second cell to get real ADGM documents:
    ```python
    # Downloads official ADGM templates and reference files
    # Creates folders: /content/user_uploads and /content/adgm_reference
    ```

### 🎬 Full Workflow:

#### Cell 3: Create Sample Data 🎯

```python
# Adds fake company info to test documents
# Makes Register_of_Directors.docx ready for testing
```

#### Cell 4: Setup AI Database 👍

```python
# Creates ChromaDB with ADGM rules
# Sets up RAG (Retrieval Augmented Generation)
```

#### Cell 5: Create Streamlit App 💻

```python
# Saves the main app code to app.py
# This is your web interface!
```

#### Cell 6: Launch Web App 🌐

```python
# Starts ngrok tunnel + Streamlit
# Gives you public URL to access your app
```

## 🎨 How the App Works

#### Stage 1: Upload Files 📤
*   **Tab 1:** Upload new documents (drag & drop).
*   **Tab 2:** Use existing files from the folder.
*   Supports: `PDF` and `DOCX` only ✅

#### Stage 2: AI Detection 🎭
*   🤖 Gemini AI reads each document.
*   📋 Classifies into types like:
    *   Articles of Association
    *   Employment Contract
    *   Register of Directors
    *   Board Resolution
    *   UBO Declaration
    *   Register of Shareholders

#### Stage 3: Checklist Matching 📋
*   ✅ Compares uploaded docs vs. required docs.
*   🚨 Shows missing documents.
*   🎉 Celebrates when all are present!

#### Stage 4: Smart Review 📝
*   🧠 AI reviews each document for compliance.
*   🔴 Adds red comments directly in `DOCX` files.
*   📊 Progress bar shows review status.
*   💡 Provides suggestions on how to fix issues.

#### Stage 5: Download Results 📥
*   📄 **Individual files** - Download each reviewed `DOCX`.
*   📦 **ZIP package** - All files in one download.
*   📊 **JSON report** - Detailed compliance summary.

## 🛠️ Setup Instructions

### 🔑 API Keys Needed:
*   **Gemini API Key** (for AI document analysis)
*   **Ngrok Auth Token** (for public web access)

### 📁 Folder Structure Created:
```text
/content/
├── user_uploads/          # 📤 Your business documents
├── adgm_reference/        # 📋 Official ADGM rules & templates  
├── reviewed_docs/         # 📝 AI-annotated output files
└── chroma_db/             # 🧠 AI knowledge database
```

## 💡 Example Usage

### 🎯 Perfect Workflow:

1.  **📤 Upload Files:**
    ```
    Articles_of_Association.docx
    Employment_Contract.docx
    Register_of_Directors.docx
    UBO_Declaration.pdf
    Board_Resolution.docx
    Register_of_Shareholders.docx
    ```

2.  **🎭 Watch AI Magic:**
    ```text
    🟦 File: Articles_of_Association.docx → Gemini detected: Articles of Association
    🟦 File: Employment_Contract.docx → Gemini detected: Employment Contract
    ✅ All 6 required documents detected!
    ```

3.  **📝 Get Smart Comments:**
    ```text
    🔥 Director Name (Severity: Medium) → Add complete address details
    🔥 Signature Date (Severity: High) → Date format should be DD/MM/YYYY
    ```

4.  **📥 Download Results:**
    ```
    Reviewed_Articles_of_Association.docx (with red comments)
    Reviewed_Employment_Contract.docx (with suggestions)
    ADGM_Reviewed_Documents.zip (all files)
    final_compliance_report.json (detailed report)
    ```

## 🎨 Tech Stack

### 🤖 AI & ML:
*   **Google Gemini 2.0** - Document classification & compliance review
*   **ChromaDB** - Vector database for ADGM rules storage
*   **RAG System** - Smart rule retrieval for document checking

### 🎨 Frontend:
*   **Streamlit** - Beautiful web interface with tabs & progress bars
*   **File Upload** - Drag & drop functionality
*   **Real-time Processing** - Live progress updates

### 📄 Document Processing:
*   **python-docx** - `DOCX` reading & red comment annotation
*   **pdfplumber** - `PDF` text extraction
*   **BeautifulSoup4** - HTML content parsing

### 🌐 Deployment:
*   **Google Colab** - Cloud notebook environment
*   **ngrok** - Public URL tunneling
*   **ZIP packaging** - Bulk file downloads

## 🚨 Important Notes

### 🔐 Security:
*   🔑 API Key is visible in code (will be secured in production).
*   📝 Free tier limits - Gemini API may hit rate limits.
*   🛡️ Local processing - Can be switched to offline LLMs.

### 📏 Limitations:
*   📄 `DOCX` annotation only - PDF comments not supported yet.
*   🎯 ADGM focus - Built specifically for ADGM compliance.
*   🤖 AI dependent - Requires internet for Gemini API.

## 🌟 Future Improvements

### 💡 Advanced Features:
*   📋 Custom checklists for different business types.
*   🏢 Multi-jurisdiction support beyond ADGM.
*   📊 Analytics dashboard for compliance trends.
*   🤝 Team collaboration features.

## 📞 Need Help?

### 🐛 Common Issues:
*   **"No files found"** → Check if files uploaded correctly.
*   **"API limit reached"** → Wait a few minutes, try again.
*   **"ngrok expired"** → Re-run the ngrok cell.

### 💬 Getting Support:
*   📧 Create a GitHub issue for bugs.
*   💡 Feature requests are welcome!
*   🤝 Contributions are appreciated.

## 🎉 Why This is Amazing

### 🚀 Business Impact:
*   **⏱️ Saves time** - No manual compliance checking.
*   **💰 Saves money** - Reduces legal review costs.
*   **🎯 Accuracy** - AI catches what humans miss.
*   **📈 Scalable** - Handle multiple companies easily.

### 🛠️ Technical Excellence:
*   **🤖 Modern AI** - Latest Gemini 2.0 model.
*   **🎨 User-friendly** - Beautiful web interface.
*   **⚡ Fast processing** - Real-time document analysis.
*   **📦 Complete solution** - Upload → Process → Download.

---
🎊 Ready to make ADGM compliance easy for everyone
