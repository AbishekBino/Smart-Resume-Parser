# Smart Resume Parser & Skill Search System

A Python-based Smart Resume Parser that automatically extracts structured information from resumes in PDF and DOCX formats. The system supports batch resume processing, skill-based candidate search, ranking, and exporting results to JSON/CSV.

Live App: [Smart Resume Parser Demo](https://smart-resume-parser-cd7xhxdhjrexa39qhtsera.streamlit.app/?utm_source=chatgpt.com)

---

# Features

* Parse PDF and DOCX resumes
* Extract:

  * Email
  * Phone number
  * Skills
  * Education
  * Experience
* Batch processing of multiple resumes
* Skill-based resume search
* Resume ranking based on matched skills
* Export results to JSON and CSV
* Error handling for invalid/corrupted files
* Modular and scalable architecture
* Streamlit-based web interface

---

# Project Architecture

```text
Resume Files (PDF/DOCX)
          ↓
Text Extraction Layer
(PyMuPDF / python-docx)
          ↓
Text Cleaning & Normalization
          ↓
Information Extraction Engine
(Regex + Rule-based NLP)
          ↓
Structured Resume Data
(JSON Format)
          ↓
Batch Processing & Search
          ↓
CSV Export / UI Display
```

---

# Technologies Used

| Technology     | Purpose                        |
| -------------- | ------------------------------ |
| Python         | Core programming language      |
| PyMuPDF (fitz) | PDF text extraction            |
| python-docx    | DOCX text extraction           |
| Regex          | Email, phone, skill extraction |
| JSON           | Structured data storage        |
| CSV            | Exporting analysis results     |
| Streamlit      | Web interface                  |

---

# Project Structure

```text
resume-parser/
│
├── app.py
├── streamlit_app.py
├── resumes/
│   ├── sample1.pdf
│   ├── sample2.docx
│
├── parsed_resume.json
├── resume_results.csv
├── requirements.txt
└── README.md
```

---

# Installation

## Clone Repository

```bash
git clone https://github.com/your-username/resume-parser.git
cd resume-parser
```

---

## Create Virtual Environment

### Windows

```bash
python -m venv venv
venv\Scripts\activate
```

### Mac/Linux

```bash
python3 -m venv venv
source venv/bin/activate
```

---

## Install Dependencies

```bash
pip install -r requirements.txt
```

---

# Running the Project

## Run CLI Version

```bash
python app.py
```

---

## Run Streamlit Web App

```bash
streamlit run streamlit_app.py
```

---

# Live Streamlit Application

[Open Smart Resume Parser Web App](https://smart-resume-parser-cd7xhxdhjrexa39qhtsera.streamlit.app/?utm_source=chatgpt.com)

---

# Supported Resume Formats

* PDF
* DOCX

---

# How It Works

## Resume Reading

The system reads PDF and DOCX resumes using:

* PyMuPDF
* python-docx

---

## Text Cleaning

The extracted text is cleaned using:

* Whitespace normalization
* Line-preserving preprocessing

---

## Information Extraction

### Contact Information

* Email extraction using Regex
* Phone number extraction using Regex

### Skills Extraction

* Predefined skill dictionary
* Regex-based word-boundary matching
* Multi-word skill detection

### Education & Experience

* Keyword-based section identification

---

## Batch Processing

Multiple resumes inside a folder can be processed automatically.

---

## Skill Search & Ranking

Recruiters can search candidates by skill.
The system ranks resumes based on:

* Number of matched skills
* Relevance

---

## Export Results

Results can be exported into:

* JSON
* CSV

---

# Example Output

```json
{
  "contact": {
    "email": "candidate@gmail.com",
    "phone": "9876543210"
  },
  "skills": [
    "python",
    "sql",
    "machine learning"
  ],
  "education": [
    "B.Tech in Computer Science"
  ],
  "experience": [
    "Software Intern at XYZ Company"
  ]
}
```

---

# Example Skill Search

```text
Search Skill: Python

Matched Resumes:
1. Asha.pdf
2. Meena.pdf
```

---

# Current Limitations

* Rule-based extraction may miss unknown skills
* No semantic understanding of skills
* Scanned image PDFs are not supported
* Resume formatting inconsistencies may affect extraction

---

# Future Improvements

* Named Entity Recognition using spaCy
* Machine Learning-based skill extraction
* OCR support for scanned resumes
* Resume classification by job role
* Database integration
* Advanced ATS ranking algorithms
* Deployment enhancements

---

# Learning Outcomes

This project helped in understanding:

* File handling
* Text preprocessing
* Regex-based NLP
* Batch processing
* Search and ranking systems
* Modular software architecture
* Data export and reporting

---

# Author

Abishek Bino

---

# License

This project is for educational and learning purposes.



