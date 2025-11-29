# 🌸 Nhu Tran — Front-End Developer & UI/UX Enthusiast  

Welcome to **Final Project - Echo**, A soft, elegant, single-page portfolio built with vanilla HTML, CSS, Bootstrap 5, and dynamic content loaded from JSON using the Fetch API.

---

## 👩‍💻 Project Overview

**Project Title:** *Dev Project Echo*  
**Purpose:**  
This is my final developer profile for **CIS 376 – Web Development** (Fall 2025) with Dr. Barry Cumbie.

I wanted my digital space to feel like **me** — warm, clean, intentional, and a little dreamy.  
Everything you see is hand-coded with love, no heavy frameworks, just pure HTML, CSS, and JavaScript.

---

## 💖 Acknowledgment

Course: CIS 376 – Web Development

Instructor: Dr. Barry Cumbie

Student Developer: Nhu Tran

---

## 🧠 User Story

> **As a** busy user who schedules daily plans,  
> **I want** a calendar interface that lets me pick a day, time, and note quickly,  
> **so that** I can organize events without endless scrolling.

---

## 🚀 Live Demo & Source

**Live Site:** [BetterDay Calendar – GitHub Pages](https://yourusername.github.io/betterday-calendar/)  
**Source Code:** [GitHub Repository](https://github.com/yourusername/betterday-calendar)

---

## ✅ Key Features

- Full-screen hero with personal introduction  
- Responsive navbar with working hamburger menu  
- **Projects** — dynamically loaded from `data/projects.json`  
- **Achievements & Skills** — dynamically loaded from `data/achievements.json`  
- Live "View Live" and "Source Code" buttons on every project  
- Knowledge reflection rendered with **zero-md**  
- Elegant pink footer with validation links  
- 100% Lighthouse, Nu HTML, and WAVE clean  

---

## 🧱 Architecture Overview

The project is built with **HTML, CSS, and Vanilla JavaScript (ES6)** using a clean modular structure.

### 📂 File Structure

```
nhu-tran-portfolio/
├── index.html
├── reflection.md
├── data/
│   ├── projects.json
│   └── achievements.json
├── assets/images/
├── styles/style.css
└── scripts/main.js
```



---

## 💻 Code Snippet – Event Logging

```javascript
saveNoteBtn.addEventListener("click", () => {
  userNote = noteInput.value.trim();

  if (!selectedDate || !selectedTime) {
    resultBox.classList.replace("alert-info", "alert-danger");
    resultBox.textContent = "❗ Please select both date and time before saving.";
    return;
  }

  resultBox.classList.replace("alert-warning", "alert-success");
  resultBox.innerHTML = `
    ✅ Event saved: <strong>${selectedDate}</strong> @ <strong>${selectedTime}</strong><br>
    📝 Note: ${userNote || "None"}
  `;

  console.log(
    `%c📅 Event: ${selectedDate} @ ${selectedTime} | 📝 Note: ${userNote}`,
    "color: #f48fb1; font-weight: bold;"
  );
});
```
### 🪄 Explanation

This snippet ensures that users can only save an event after both the date and time are selected.
It then logs the complete information — including note — to the browser console, and updates the confirmation box visually.

```javascript
function renderCalendar() {
  for (let i = 1; i <= 30; i++) {
    const btn = document.createElement("button");
    btn.className = "slot";
    btn.textContent = i;

    btn.addEventListener("click", () => {
      selectedDate = `${i} ${currentMonth.textContent}`;
      selectedTime = null;
      noteInput.value = "";

      document.querySelectorAll(".calendar-grid .slot").forEach(b =>
        b.classList.remove("selected")
      );
      btn.classList.add("selected");

      resultBox.classList.replace("alert-success", "alert-info");
      resultBox.innerHTML = `📅 Selected <strong>${selectedDate}</strong><br>Now choose a time.`;
    });

    calendarGrid.appendChild(btn);
  }
}
```
### 🪄 Explanation

Generates 30 interactive date buttons.
When clicked, the previous time selection is reset to prevent carry-over errors and the interface updates to guide the user to pick a time next.

---

## 🧰 Tech Stack

| Layer             | Technology Used                                      |
|-------------------|-------------------------------------------------------|
| Markup            | HTML5 (semantic)                                      |
| Styling           | CSS3 + Bootstrap 5 + Google Fonts (Playfair + Inter)  |
| Logic             | Vanilla JavaScript (ES6+) + Fetch API                 |
| Data              | JSON files (`projects.json`, `achievements.json`)     |
| Reflection        | zero-md (Markdown → HTML in-browser)                  |
| Icons             | Bootstrap Icons                                       |
| Hosting           | GitHub Pages                                          |
| Validation        | Nu HTML Checker • WAVE • Lighthouse                   |

---

## Validation & Performance

- Nu HTML Checker → [View Report](https://validator.w3.org/nu/?doc=https%3A%2F%2Fnhu-tran.github.io%2F)  
- WAVE Accessibility → [View Report](https://wave.webaim.org/report#/https://nhu-tran.github.io/)  
- Lighthouse → [View Report](https://pagespeed.web.dev/report?url=https%3A%2F%2Fnhu-tran.github.io%2F)

---

## 🤝 Attribution

- Dr. Barry Cumbie — for an inspiring semester  
- Bootstrap 5 & zero-md — for making beautiful things easy  
- Coffee, pink aesthetics, and good music — for keeping me going  

---

> “Design is not just what it looks like and feels like.  
> Design is how it works.” — Steve Jobs

Thank you for visiting my little corner of the internet  
Made with care in Florence, Alabama • 2025

— Nhu Tran