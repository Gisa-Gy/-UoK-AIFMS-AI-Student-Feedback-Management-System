<div align="center">

# 🎓 UoK AIFMS — AI Student Feedback Management System

### University of Kigali · A single-file web platform for submitting, routing, and resolving student complaints with AI assistance.

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![Chart.js](https://img.shields.io/badge/Chart.js-FF6384?style=flat&logo=chartdotjs&logoColor=white)
![Status](https://img.shields.io/badge/status-prototype-B57B0A?style=flat)
![No Build](https://img.shields.io/badge/build-none%20required-560606?style=flat)

</div>

---

## 📖 Overview

**AIFMS** gives every University of Kigali student a single, transparent channel to submit complaints and feedback, and gives the university a structured, accountable way to route, resolve, and learn from that feedback. Each complaint is read by a natural-language pipeline that classifies it by **department, sentiment, and priority**, so urgent cases reach the right office quickly.

The whole application ships as **one self-contained HTML file** — no framework, no build step, no server. Open it in a browser and it just runs.

## ✨ Key Features

### 👩‍🎓 Student portal
- Guided complaint submission with category, priority, subject, and description
- **Named or anonymous** submission modes
- Live AI routing hint and detected-tone (sentiment) preview
- **Submitted complaints are saved locally and persist across page reloads**
- Searchable, filterable complaint list (status **and** category filters combined)
- Notifications, profile, and settings

### 🏛️ Administrator dashboard (Deans & Heads of Department)
- Institution-wide overview with trend, category split, and recent cases
- Complaints workspace with combined search / status / category filtering and one-click resolve or escalate
- Analytics, AI insights, and emerging-theme detection
- Staff directory, email rules, and a report builder

### 🛡️ System Administrator dashboard
- **User accounts management** — add, edit, suspend, delete, filter (with audit logging)
- **Database management** — health tiles, live row counts for 9 core tables, manual backups
- **Security & maintenance** — audit log, failed-login watchlist, maintenance mode, two-step login
- **AI Models comparison** — Logistic Regression vs Naïve Bayes vs BERT (accuracy, precision, recall, F1, latency)
- **NLP pipeline** — animated, stage-by-stage view of how a complaint becomes a routing decision
- **Training dataset** — statistics, category distribution, geographic spread, import / export / backup

### 📤 Reporting & exports
- Download real **PDF**, **Excel (.xlsx)**, **CSV**, and **JSON** reports
- Report types: Complaint Summary, Resolution Performance, Category Breakdown, Satisfaction
- Automatic offline fallbacks (print-to-PDF and CSV) when export libraries can't load

## 🤖 AI & Data (summary)

| Model | Type | Accuracy | F1 | Latency |
|-------|------|:--------:|:---:|:-------:|
| Logistic Regression | TF-IDF baseline | 88.4% | 85.4 | 8 ms |
| Naïve Bayes | Probabilistic | 85.9% | 85.5 | 5 ms |
| **BERT (fine-tuned)** | Transformer · **active** | **94.8%** | **94.8** | 142 ms |

Pipeline: **Raw complaint → Cleaning → Tokenization → Stop-word removal → Lemmatization → Feature extraction → Classification** (category · sentiment · priority).

## 🔑 Demo Accounts

Pick one from the **Quick Access** panel on the sign-in screen, or type the credentials.

| Role | Email | Password |
|------|-------|----------|
| 🎓 Student | `student@uok.ac.rw` | `password123` |
| 🏛️ Administrator | `admin@uok.ac.rw` | `admin123` |
| 🛡️ System Administrator | `sysadmin@uok.ac.rw` | `sysadmin123` |

## 🚀 Live Demo

Once deployed with GitHub Pages, your app will be available at:

```
https://<your-username>.github.io/<your-repo-name>/
```

## 🖥️ Run Locally

No installation is required.

1. Download or clone this repository.
2. Double-click the HTML file, or open it in any modern browser.

```bash
git clone https://github.com/<your-username>/<your-repo-name>.git
cd <your-repo-name>
# then open the HTML file in your browser
```

> Chart and export libraries load from a CDN when you are online; core features still work offline.

## 🌐 Deploy to GitHub Pages

1. **Rename the HTML file to `index.html`** so GitHub Pages serves it automatically:
   ```bash
   git mv "AI_Student_Feedback_Management_System_Final_Build.html" index.html
   git commit -m "Rename app to index.html for GitHub Pages"
   git push
   ```
2. In your repository, go to **Settings → Pages**.
3. Under **Build and deployment → Source**, choose **Deploy from a branch**.
4. Select the **`main`** branch and the **`/ (root)`** folder, then click **Save**.
5. Wait about a minute, then open the published URL shown on that page.

> Prefer to keep the original filename? You can, but then visitors must open
> `https://<your-username>.github.io/<your-repo-name>/AI%20Student%20Feedback%20Management%20System%20Final%20Build.html`.
> Renaming to `index.html` is strongly recommended.

## 💾 Data & Persistence

Student complaints are saved to the browser's **`localStorage`** (key `aifms_complaints_v1`), so submissions survive page reloads on the same browser and device. All other demo data (users, audit log, analytics) lives in memory for the session. This is a **frontend prototype**: authentication and AI outputs are simulated in the browser, and there is no shared backend yet — those are the intended next steps.

## 📂 Suggested Repository Structure

```
├── index.html      # the entire application (rename from the build file)
├── README.md       # this file
└── docs/           # optional: place the system documentation here
```

## 🗺️ Roadmap

- [ ] Connect a secure backend and relational database
- [ ] Deploy the trained BERT model behind an inference API
- [ ] Real-time email and in-app notifications
- [ ] University single sign-on and persistent shared storage
- [ ] Multilingual support (English, Kinyarwanda, French)

## ⚠️ Disclaimer

This is an academic prototype built for demonstration. It is not connected to real University of Kigali systems, stores no real personal data, and should not be used for actual complaint handling without a production backend and security review.

## 📜 License

Released for educational use. You are free to study, adapt, and build on it. Add a `LICENSE` file (for example the MIT License) if you want to make the terms explicit.

## 🙌 Credits

Built for the **University of Kigali** as an AI Student Feedback Management System.
Charts by [Chart.js](https://www.chartjs.org/) · PDF by [jsPDF](https://github.com/parallax/jsPDF) · Excel by [SheetJS](https://sheetjs.com/).

<div align="center">

**⭐ If this project helps you, consider starring the repository.**

</div>
