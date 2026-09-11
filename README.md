# 🎓 Student Grade Calculator

A full-stack mini project that calculates a student's per-subject grades, overall
percentage, GPA, and pass/fail result — with a Node/Express backend, a vanilla
HTML/CSS/JS frontend, and a saved history of past calculations.

Built as a college mini-project reference implementation: simple enough to explain
in a viva, complete enough to actually run and demo.

---

## ✨ Features

- Add any number of subjects with marks and max marks
- Calculates, per subject: percentage, letter grade, pass/fail
- Calculates overall percentage, letter grade, GPA (10-point scale), and final result
- Saves every calculation to a history log (JSON file on the backend)
- View, and delete, past calculations from the UI
- Clean, responsive UI — works on mobile and desktop
- Zero external database required (JSON file storage) — runs anywhere Node runs

## 🏗️ Tech stack

| Layer     | Technology                          |
|-----------|--------------------------------------|
| Frontend  | HTML5, CSS3, vanilla JavaScript (fetch API) |
| Backend   | Node.js, Express.js                  |
| Storage   | JSON file (`backend/data/history.json`) |
| Testing   | Plain Node `assert` scripts          |

## 📁 Project structure
Got it — you're on GitHub creating README.md directly via the browser. Just paste this whole thing into that empty editor box (where it says "Enter file contents here"), then scroll down and click Commit changes.
Markdown
grade-calculator/
├── backend/
│   ├── server.js                 # Express app entry point
│   ├── routes/gradeRoutes.js      # API route definitions
│   ├── controllers/gradeController.js  # Request handlers
│   ├── utils/gradeLogic.js        # Pure grading logic (validation + calculation)
│   ├── tests/gradeLogic.test.js   # Unit tests for grading logic
│   ├── data/history.json          # Saved calculation history
│   └── package.json
├── frontend/
│   ├── index.html
│   ├── style.css
│   └── script.js
├── presentation/
│   └── Student_Grade_Calculator.pptx   # Project presentation slides
└── README.md
The server starts on http://localhost:5000 and also serves the frontend
directly, so opening that URL in your browser gives you the full app —
no separate frontend server needed.
Prefer to run the frontend on its own (e.g. VS Code Live Server)? Open
frontend/index.html directly, and update API_BASE at the top of
frontend/script.js to http://localhost:5000/api.
3. Run the tests (optional)
Bash
🔌 API reference
Method
Endpoint
Description
POST
/api/calculate
Calculate a result and save it to history
GET
/api/history
Get all saved calculations
DELETE
/api/history/:id
Delete one saved calculation
DELETE
/api/history
Clear all history
GET
/api/health
Health check
