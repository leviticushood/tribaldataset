# Trial Tribal Dataset v1.4

An interactive web application for exploring and filtering tribal data sovereignty questions mapped against the **CARE Principles** and **UNDRIP** (United Nations Declaration on the Rights of Indigenous Peoples) frameworks.

## 🌐 Live Demo

[https://leviticushood.github.io/tribaldataset/](https://leviticushood.github.io/tribaldataset/)

---

## 📖 Overview

This tool allows researchers, policymakers, and community stakeholders to browse and filter a curated dataset of questions related to Indigenous data governance. Each question is tagged with relevant CARE and UNDRIP categories, and responses are aggregated across five anonymized tribal groups (A–E), with supporting justifications available for review.

---

## 🔍 Frameworks Used

### CARE Principles (Indigenous Data Governance)
| Code | Principle |
|------|-----------|
| C | Collective Benefit |
| A | Authority to Control |
| R | Responsibility |
| E | Ethics |

### UNDRIP (UN Declaration on the Rights of Indigenous Peoples)
| Code | Category |
|------|----------|
| I | Internal Autonomy |
| C | Collective Authority |
| E | External Participation |

---

## ✨ Features

- **Multi-dimensional filtering** — filter questions by CARE principle, UNDRIP category, and tribal group simultaneously
- **Keyword search** — search across question text, section, subsection, and question number
- **Aggregated responses** — view how many tribes answered "Yes" to each question, displayed as a fraction and percentage
- **Justifications** — expand individual tribal justifications for each question via collapsible details
- **Real-time updates** — filters apply instantly without page reloads

---

## 🛠️ Tech Stack

- **Frontend:** Vanilla HTML, CSS, JavaScript (no frameworks)
- **Backend / Database:** [Supabase](https://supabase.com/) (PostgreSQL with REST API)
- **Hosting:** GitHub Pages

---

## 📁 Project Structure

```
tribaldataset/
├── index.html      # Main application — UI, filtering logic, and Supabase integration
├── style.css       # Stylesheet
└── README.md       # Project documentation
```

---

## 🗄️ Database

The app connects to a Supabase project using an anonymous public key. It queries the `questions_long` table, which stores one row per question-tribe combination, including:

- `question_number` — unique identifier
- `section` / `subsection` — organizational hierarchy
- `question_text` — the survey/governance question
- `care_principal` — comma-separated CARE codes
- `undrip` — comma-separated UNDRIP codes
- `answer` — boolean (Yes/No)
- `tribe_code` — anonymized tribal identifier (tribe_a through tribe_e)
- `final_justification` — qualitative response text

---

## 🚀 Running Locally

No build step required. Simply clone the repo and open `index.html` in a browser:

```bash
git clone https://github.com/leviticushood/tribaldataset.git
cd tribaldataset
open index.html
```

> The app will connect to the hosted Supabase instance automatically.

---

## 🤝 Acknowledgements

This project was developed to support research into Indigenous data sovereignty and governance. The CARE Principles were developed by the Global Indigenous Data Alliance. UNDRIP was adopted by the UN General Assembly in 2007.

---

## 📄 License

This project is open source. Please use and share with respect for the communities whose data and governance frameworks it represents.
