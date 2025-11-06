# PDF-OCR-System-Pro
Engineered an Intelligent OCR Framework for document digitization. The system employs advanced Format Detection (invoices, tables), Image Filtering via PIL to boost Tesseract accuracy, and utilizes Pandas/SQLite for historical tracking and an integrated Analytics Dashboard.

# 🚀 PDF OCR System Pro: Enterprise-Grade Text Extractor

## 🌟 Project Summary

**PDF OCR System Pro** is a comprehensive, enterprise-grade application for converting text from scanned, image-based PDF documents into structured, searchable digital data. This project goes far beyond standard OCR, incorporating **batch processing**, **AI-driven format detection**, a robust **SQLite database** for tracking history and performance metrics, and advanced export options (DOCX, JSON, Excel).

Built as a dedicated portfolio piece, this system demonstrates proficiency across full-stack Python development, data engineering (SQLite/Pandas), and sophisticated machine learning utility (Tesseract OCR).

## ✨ Advanced Features & Portfolio Highlights

This project showcases expertise in several complex domains:

| Feature Category | Component | Description | Technologies |
| :--- | :--- | :--- | :--- |
| **Core Processing** | **Intelligent OCR Pipeline** | Utilizes **pytesseract** with configurable language, DPI, and Page Segmentation Mode (PSM). | Tesseract, Pytesseract |
| **Data Quality** | **Image Preprocessing** | Applies **Contrast Enhancement, Sharpness, and Median Filtering** to poor-quality scans before OCR to boost accuracy. | Pillow (PIL) |
| **Data Engineering** | **Extraction History** | Persistent data storage using **SQLite** to log every extraction, including metadata and quality scores. | SQLite3, Pandas |
| **Advanced Analytics** | **Dashboard** | Dedicated **Analytics Mode** provides charts (using Pandas) on activity over time, language distribution, and processing performance. | Streamlit, Pandas |
| **Intelligent Detection** | **Format Detection** | Uses **Regex Pattern Matching** to identify common document types like **Invoices, Tables, and Forms**, and extracts key data (emails, phones, dates). | Regex (re) |
| **Export Flexibility** | **Multi-Format Export** | Exports results to standard **TXT** and specialized formats: **DOCX** (for editable documents), **JSON** (for structured data), and **Excel** (with separate text/stats sheets). | `docx`, `json`, `openpyxl` |
| **Scalability** | **Batch Mode** | Efficiently processes multiple PDF files simultaneously, tracking success/failure for each file. | Python `zipfile`, Streamlit |
| **Metrics** | **Quality Scoring** | Calculates a simple **Quality Score** based on alphanumeric ratio and text length to assess OCR confidence. | Python |

## ⚙️ Tech Stack

| Category | Technology | Purpose |
| :--- | :--- | :--- |
| **Web Framework** | **Streamlit** | Fast application prototyping and creation of the clean, multi-mode UI. |
| **Backend / Logic** | **Python 3.10+** | Primary language. |
| **OCR / Vision** | **Tesseract OCR** & **Pillow** | The underlying engine for text recognition and image manipulation. |
| **Data Persistence** | **SQLite3** | Lightweight database for persistent storage of extraction records (`ocr_history.db`). |
| **Data Analysis** | **Pandas** | Used extensively for history viewing, filtering, and generating analytics charts. |
| **Export Utilities** | **`docx`, `openpyxl`, `zipfile`** | Libraries enabling complex file exports and batch ZIP archiving. |

# 🚀 PDF OCR System Pro: Enterprise-Grade Text Extractor

## 🌟 Project Summary

**PDF OCR System Pro** is a comprehensive, enterprise-grade application for converting text from scanned, image-based PDF documents into structured, searchable digital data. This project goes far beyond standard OCR, incorporating **batch processing**, **AI-driven format detection**, a robust **SQLite database** for tracking history and performance metrics, and advanced export options (DOCX, JSON, Excel).

Built as a dedicated portfolio piece, this system demonstrates proficiency across full-stack Python development, data engineering (SQLite/Pandas), and sophisticated machine learning utility (Tesseract OCR).

## ✨ Advanced Features & Portfolio Highlights

This project showcases expertise in several complex domains:

| Feature Category | Component | Description | Technologies |
| :--- | :--- | :--- | :--- |
| **Core Processing** | **Intelligent OCR Pipeline** | Utilizes **pytesseract** with configurable language, DPI, and Page Segmentation Mode (PSM). | Tesseract, Pytesseract |
| **Data Quality** | **Image Preprocessing** | Applies **Contrast Enhancement, Sharpness, and Median Filtering** to poor-quality scans before OCR to boost accuracy. | Pillow (PIL) |
| **Data Engineering** | **Extraction History** | Persistent data storage using **SQLite** to log every extraction, including metadata and quality scores. | SQLite3, Pandas |
| **Advanced Analytics** | **Dashboard** | Dedicated **Analytics Mode** provides charts (using Pandas) on activity over time, language distribution, and processing performance. | Streamlit, Pandas |
| **Intelligent Detection** | **Format Detection** | Uses **Regex Pattern Matching** to identify common document types like **Invoices, Tables, and Forms**, and extracts key data (emails, phones, dates). | Regex (re) |
| **Export Flexibility** | **Multi-Format Export** | Exports results to standard **TXT** and specialized formats: **DOCX** (for editable documents), **JSON** (for structured data), and **Excel** (with separate text/stats sheets). | `docx`, `json`, `openpyxl` |
| **Scalability** | **Batch Mode** | Efficiently processes multiple PDF files simultaneously, tracking success/failure for each file. | Python `zipfile`, Streamlit |
| **Metrics** | **Quality Scoring** | Calculates a simple **Quality Score** based on alphanumeric ratio and text length to assess OCR confidence. | Python |

## ⚙️ Tech Stack

| Category | Technology | Purpose |
| :--- | :--- | :--- |
| **Web Framework** | **Streamlit** | Fast application prototyping and creation of the clean, multi-mode UI. |
| **Backend / Logic** | **Python 3.10+** | Primary language. |
| **OCR / Vision** | **Tesseract OCR** & **Pillow** | The underlying engine for text recognition and image manipulation. |
| **Data Persistence** | **SQLite3** | Lightweight database for persistent storage of extraction records (`ocr_history.db`). |
| **Data Analysis** | **Pandas** | Used extensively for history viewing, filtering, and generating analytics charts. |
| **Export Utilities** | **`docx`, `openpyxl`, `zipfile`** | Libraries enabling complex file exports and batch ZIP archiving. |


## 📦 Installation and Setup

### 1. System Dependencies (Tesseract and Poppler)

The core OCR functionality requires system-level libraries.

#### **Mac (Homebrew)**

```bash
# Install Tesseract OCR
brew install tesseract

# Install Poppler (required by pdf2image)
brew install poppler
Windows
Follow the links provided in the original documentation to install Tesseract and Poppler and ensure they are added to your system's PATH environment variable.

2. Python Packages
Navigate to your project directory and install the required Python dependencies:

Bash

pip install streamlit pytesseract pdf2image Pillow pandas docx openpyxl
3. Running the Application
Launch the application from your terminal:

Bash

streamlit run app.py
The application will automatically open in your web browser (http://localhost:8501).

🎯 Usage Modes
The system operates in four distinct modes, selectable via the sidebar:

🔍 Single PDF: Upload one file, run full analytics (format detection, key data extraction), and choose from multiple export formats (TXT, DOCX, JSON).

📚 Batch Processing: Upload multiple files, track progress individually, and download all successful extractions as a single ZIP file.

📜 History: View a searchable, sortable table of all past extractions saved in the SQLite database, with options to download or delete records.

📊 Analytics: Visualize key performance metrics and data distribution (activity over time, language use, average quality) using interactive Streamlit charts powered by Pandas.

✅ Next Step: Deployment
This project is highly deployable. To showcase it to recruiters, I recommend deploying it on a free hosting platform like Streamlit Community Cloud (share.streamlit.io).

To successfully deploy, ensure your repository contains:

app.py (The main code).

requirements.txt (Listing all necessary Python packages: streamlit, pytesseract, pdf2image, Pillow, pandas, docx, openpyxl).

README.md (This file).

🧑‍💻 
Author: Janvi Baghel

GitHub: https://github.com/Janvibaghel

LinkedIn: https://www.linkedin.com/in/janvibaghel/
