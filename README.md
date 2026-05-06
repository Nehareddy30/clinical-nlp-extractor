# 🏥 Clinical NLP Extractor

An NLP pipeline that extracts **ICD-10 diagnosis codes**, **CPT procedure codes**, and **PHI** from unstructured clinical notes — with HIPAA-compliant de-identification.

## 🔍 What This Project Does

Electronic Health Records (EHRs) contain unstructured physician notes with critical billing and diagnostic information buried in free text. This pipeline automatically extracts and structures that information.

1. **PHI Extraction** — Detects patient names, provider names, dates, and locations using spaCy NER + regex
2. **ICD-10 Extraction** — Extracts diagnosis codes (M51.16, E11.65, I24.9...)
3. **CPT Extraction** — Extracts procedure codes (72148, 83036, 93306...)
4. **De-identification** — Replaces PHI with HIPAA Safe Harbor placeholder tags
5. **Export** — Saves structured results to CSV and JSON

## 📊 Accuracy Results

| Extraction Type | Correct | Total | Accuracy |
|---|---|---|---|
| ICD-10 Codes | 8 | 8 | **100%** |
| CPT Codes | 6 | 6 | **100%** |
| Patient Names | 5 | 5 | **100%** |

## 💬 Sample Output

**Input (raw clinical note):**

## ⚙️ Setup

```bash
pip install spacy scikit-learn pandas
python -m spacy download en_core_web_sm
```

Then open `clinical_nlp_extractor.ipynb` and run cells top to bottom.

## 🛠️ Tech Stack

| Component | Technology |
|---|---|
| Named Entity Recognition | spaCy en_core_web_sm |
| Code Pattern Matching | Python regex |
| Data Export | pandas CSV + JSON |
| De-identification | HIPAA Safe Harbor method |

## 🏥 Healthcare Context

- ICD-10 codes extracted: M51.16, M54.42, E11.65, I10, I24.9, E78.5, M23.201, J18.9
- CPT codes extracted: 72148, 83036, 84484, 93306, 73721, 71046
- De-identification follows HIPAA Safe Harbor standard
- Mirrors real EHR clinical note processing workflows

## 👩‍💻 Author

Neha Pannala — AI Engineer | Healthcare & Consulting Domain  
[LinkedIn](https://linkedin.com/in/neha-pannala) · [GitHub](https://github.com/Nehareddy30)
