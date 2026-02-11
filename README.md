# Med-Phar

**Med-Phar** is a prototype medical decision support system that applies structured rule-based logic to classify symptoms, reason about possible conditions, and relate them to pharmacological information.

This project explores how deterministic rule engines can be used to assist in preliminary medical reasoning and structured health data modeling.

---

##  Project Overview

Med-Phar aims to:

- Classify medical symptoms by category and relevance  
- Apply rule-based reasoning to generate preliminary condition insights  
- Link symptom patterns to pharmacological or clinical concepts  
- Provide a framework for structured health data modeling  

It is designed as a **prototype** and is not intended for clinical use.

---

##  Repository Structure

- `server.js` — Backend API server (Node.js)  
- `regression.py` — Script for medical data regression analysis  
- `test.py` — Test cases for rule logic and data handling  
- `bdd_med&phar.sql` — SQL schema for symptom / pharmacology datasets  
- `package-lock.json` — Dependency lockfile for the Node.js environment  

---

##  Getting Started

### Requirements

- Node.js (v16+)  
- Python 3.10+  
- SQL database (e.g., MySQL or SQLite compatible with the provided schema)  

---

### Installation

```bash
git clone https://github.com/MDMM02/Med-Phar.git
cd Med-Phar
```

---

### Backend Setup

```bash
npm install
node server.js
```

---

### Python Environment Setup

```bash
python3 -m venv venv
source venv/bin/activate   # On Windows: venv\Scripts\activate
pip install -r requirements.txt
python regression.py
```

---

##  Example Usage

Example API call:

```javascript
fetch("http://localhost:3000/analyze", {
  method: "POST",
  headers: { "Content-Type": "application/json" },
  body: JSON.stringify({ symptoms: ["headache", "nausea"] })
})
.then(res => res.json())
.then(console.log);
```

---

##  Testing

Run the test script:

```bash
python test.py
```

This verifies that the core classification and reasoning logic behave as expected.

---

##  Architecture Notes

- Structured symptom input
- Deterministic rule engine (if/else logic)
- Separation between data layer (SQL schema) and reasoning layer
- Extendable architecture for additional rules and datasets

The current implementation is rule-based. Future versions may introduce probabilistic or ML-based reasoning.

---

##  Future Improvements

- Add weighted decision logic  
- Introduce symptom severity scoring  
- Develop a front-end interface  
- Store and retrieve patient sessions  
- Integrate real-world clinical datasets  
- Implement explainability output for each decision  

---

##  Disclaimer

This project is for educational and experimental purposes only.  
It does **not** provide medical advice and must not be used for real diagnostic decisions.

---

##  Author

Developed as a health-tech exploration project focused on translating clinical reasoning into structured, transparent code.
