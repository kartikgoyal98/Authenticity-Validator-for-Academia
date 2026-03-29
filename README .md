# 🎓 Authenticity Validator for Academia — CertiValidate

> **ET Gen AI Hackathon | Smart Education Theme**
> Team: **The Decoders**

[![Live Demo](https://img.shields.io/badge/Live%20Demo-Available-brightgreen)](./complete.html)
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](#license)
[![Tech Stack](https://img.shields.io/badge/Stack-HTML%20%7C%20JS%20%7C%20Python%20%7C%20Blockchain-orange)](#tech-stack)

---

## 📌 Problem Statement

Academic credential fraud is a growing crisis across India. Manual verification processes take **4–6 weeks**, are prone to human error, and cannot scale. With a rise in sophisticated forgery tools, institutions and employers face an uphill battle verifying the authenticity of degrees, certificates, and marksheets.

**Key Statistics:**
- 📅 4–6 weeks average manual verification time
- 📈 ~75% estimated rise in document forgery with digital editing tools
- 💸 Millions in economic loss from bad hires and fraudulent admissions

---

## 💡 Our Solution

**CertiValidate** is a secure, scalable, and fully digital platform that automates academic credential verification in seconds — not weeks.

It combines:
- **OCR** (Optical Character Recognition) to extract data from legacy documents
- **AI/ML** to detect tampered images, invalid fonts, and layout anomalies
- **Blockchain (Hyperledger Fabric)** to provide an immutable audit trail for newly issued certificates
- **A real-time admin dashboard** for monitoring fraud trends

---

## 🔄 How It Works

```
1. UPLOAD    →  Institutions securely upload academic records to build a trusted data pool
2. VERIFY    →  Employers/agencies submit a certificate via the secure web portal
3. AUTOMATCH →  AI + OCR + Blockchain pipeline cross-validates the document
4. RESULT    →  Instant, trustworthy verification result is returned
```

---

## 🗂️ Repository Structure

```
📦 authenticity-validator-academia/
├── 📄 complete.html              # Full frontend demo (single-file deployment)
├── 🖼️ fack_document1.jpg         # Sample forged document (for demo testing)
├── 🖼️ real_document.jpg          # Sample authentic document (for demo testing)
├── 📊 Complete_presentation.pptx # Full project presentation (SIH submission)
└── 📖 README.md                  # You are here
```

---

## 🚀 Quick Start (Frontend Demo)

No installation required for the demo. Just open the HTML file in a browser:

```bash
# Clone the repository
git clone https://github.com/<your-username>/authenticity-validator-academia.git

# Navigate to the project
cd authenticity-validator-academia

# Open the demo in your browser
open complete.html
# OR on Linux/Windows:
# xdg-open complete.html
# start complete.html
```

### Running the Demo

1. Open `complete.html` in any modern browser (Chrome, Firefox, Edge)
2. Navigate to the **Validator** section
3. Upload either of the provided sample documents:
   - `fack_document1.jpg` → Triggers **Forgery Alert** ❌
   - `real_document.jpg` → Returns **Certificate Verified** ✅
4. Observe the step-by-step verification log

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| **Frontend** | HTML5, CSS3, JavaScript, Tailwind CSS, Chart.js |
| **Backend (Planned)** | Python (Flask / Django), Node.js with Express |
| **Database** | PostgreSQL (structured records), NoSQL (metadata) |
| **OCR Engine** | Tesseract OCR / Google Cloud Vision API |
| **Blockchain** | Hyperledger Fabric (private permissioned chain) |
| **AI / ML** | Custom models for forgery detection (photo, signature, layout) |

---

## 🧠 Core Features

### ✅ Document Verification Pipeline
- OCR-based data extraction from scanned/uploaded certificates
- AI-powered layout and font anomaly detection
- Cross-reference against institutional database (PostgreSQL)
- Blockchain hash verification for tamper-proof validation

### 📊 Admin Dashboard
- Real-time verification and forgery trend charts (Chart.js)
- Animated live statistics (total verifications, forgeries detected)
- Monthly bar chart for institutional reporting

### 🔍 Verification Result Output
For each document, the system returns:
- ✅ / ❌ Authenticity verdict
- Extracted fields: Name, ID, DOB, Issuer
- Step-by-step verification log with pass/fail per check

---

## 📸 Demo Screenshots

### Verified Document Result
> Upload `real_document.jpg` — system confirms authenticity via all 4 checks:
> OCR ✅ | AI Layout Check ✅ | Database Match ✅ | Blockchain Hash ✅

### Forgery Alert Result
> Upload `fack_document1.jpg` — system flags multiple red flags:
> Invalid Issue Date (61 Jan) ⚠️ | Demo Watermarks Detected ❌ | ID not in DB ❌ | No Blockchain Hash ❌

---

## 📐 Architecture Overview

```
┌─────────────────────────────────────────┐
│              User / Employer            │
└──────────────────┬──────────────────────┘
                   │ Upload Certificate
                   ▼
┌─────────────────────────────────────────┐
│           CertiValidate Portal          │
│         (React.js / HTML Frontend)      │
└──────────────────┬──────────────────────┘
                   │
          ┌────────┴────────┐
          ▼                 ▼
┌──────────────┐   ┌─────────────────┐
│  OCR Engine  │   │   AI/ML Model   │
│  (Tesseract/ │   │ (Forgery Detect)│
│  GCV API)    │   └────────┬────────┘
└──────┬───────┘            │
       └────────┬───────────┘
                ▼
┌─────────────────────────────────────────┐
│          Backend API (Flask/Django)     │
└──────────┬──────────────────┬───────────┘
           ▼                  ▼
┌──────────────────┐  ┌───────────────────┐
│   PostgreSQL DB  │  │ Hyperledger Fabric│
│ (Institution     │  │ (Blockchain Ledger│
│  Records)        │  │  Hash Verification│
└──────────────────┘  └───────────────────┘
```

---

## 🌍 Impact & Benefits

| Stakeholder | Benefit |
|------------|---------|
| 🎓 **Students** | Degree is protected; fair merit-based competition |
| 🏢 **Employers** | Faster, reliable hiring; reduced fraud risk |
| 🏛️ **Government** | Real-time fraud monitoring dashboard; reduced systemic fraud |
| 🏫 **Institutions** | Reduced administrative burden; enhanced reputation |

---

## 📅 Roadmap

- [x] Frontend UI prototype with mock AI pipeline
- [x] Forgery vs. authentic demo with sample documents
- [x] Impact dashboard with Chart.js visualizations
- [ ] Backend API integration (Flask)
- [ ] OCR pipeline (Tesseract / Google Cloud Vision)
- [ ] PostgreSQL schema and seed data
- [ ] Hyperledger Fabric smart contract deployment
- [ ] Pilot rollout with one partnering institution in Jharkhand

---

## 🤝 Team — The Decoders

Built for the **ET Gen AI Hackathon** under the **Smart Education** theme.

> *"Empowering Trust in Education"*

---

## 📄 License

This project is licensed under the MIT License. See [LICENSE](./LICENSE) for details.

---

## 🙏 Acknowledgements

- [Tailwind CSS](https://tailwindcss.com/) — Utility-first CSS framework
- [Chart.js](https://www.chartjs.org/) — Data visualization
- [Hyperledger Fabric](https://www.hyperledger.org/projects/fabric) — Enterprise blockchain
- [Tesseract OCR](https://github.com/tesseract-ocr/tesseract) — Open-source OCR engine
- Smart India Hackathon (SIH) template and submission format
