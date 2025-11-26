# CIS 376 – FINAL DEV PROFILE PROJECT

**Thuan Nguyen** – Web Developer Portfolio  
A modern, data-driven single-page developer portfolio showcasing my journey, projects, achievements, and technical reflection.

---

## Project Information

**Student Name:** THUAN NGUYEN  
**Course**: CIS 376 – Web Development  
**Instructor**: Dr. Barry Cumbie  
**Project Type**: Final Developer Profile

---

## Product Overview

**Product Name:** *Thuan Nguyen | Web Developer Portfolio*  
**Description:**  
A clean, fast, fully responsive single-page application that dynamically loads projects and achievements from JSON using the Fetch API. Features live search/filter, Markdown-based reflection rendered with zero-md, and a professional design built with modern web standards.

Live Site: https://kise1205.github.io/Kise1205/  
Source Code: https://github.com/Kise1205/Kise1205

---

## User Story & Scenario

> **As a** potential employer, recruiter, or peer developer,  
> **I want** to quickly understand Thuan’s skills, personality, and body of work,  
> **so that** I can evaluate his fit for opportunities or collaboration — all from one beautiful, fast-loading page.

---

## Validation Results

| Validator              | Status                          | Link |
|------------------------|----------------------------------|------|
| **Nu HTML Checker**    | 100% Passed – No errors         | [Nu Report](https://validator.w3.org/nu/?doc=https%3A%2F%2Fkise1205.github.io%2FKise1205%2F) |
| **WAVE Accessibility** | 100% Passed – Zero errors       | [WAVE Report](https://wave.webaim.org/report#/https://kise1205.github.io/Kise1205/) |
| **Lighthouse (Bonus)** | 100/100 Performance & Accessibility | Chrome DevTools |

---

## Code Base Overview

Built with **HTML5, CSS3, Bootstrap 5, vanilla JavaScript (ES6+), JSON data files**, and **zero-md** for Markdown rendering.

- **index.html** – Single page with semantic structure and dynamic content areas  
- **data/data.json & achievements.json** – All content isolated from markup
- **script/script.js** – Fetch API, live search/filter, DOM manipulation, console debugging  
- **styles/style.css** – Custom responsive design + modern hover effects  
- **reflection.md** – Knowledge reflection rendered directly in-browser via zero-md

---

## Architecture & Data Flow

```
Local Development
     ↓ (git commit)
GitHub Repository
     ↓ (GitHub Pages)
Automatic Deploy → https://kise1205.github.io/Kise1205/
     ↓ (on load)
Fetch API → projects.json + achievements.json → Render cards dynamically
     ↓
zero-md → Renders reflection.md as beautiful HTML
```

Agile workflow using GitHub Issues as user stories and milestones.

---

## Effectiveness & Features

| Feature                    | Implementation                              |
|----------------------------|---------------------------------------------|
| **Single-Page App**        | One HTML file – faster load, better UX      |
| **Data-Driven Content**    | Projects & achievements from JSON           |
| **Live Search & Filter**   | Instant client-side filtering (Bonus +10)   |
| **Markdown Reflection**    | zero-md renders reflection.md beautifully   |
| **Mobile-First Responsive**| Bootstrap 5 + custom CSS                    |
| **Accessibility**          | Semantic HTML, alt text, high contrast      |

---

## Code Snippets (Key Highlights)

### Dynamic Project Loading + Search (main.js)
```js
fetch("data/projects.json")
  .then(res => res.json())
  .then(projects => {
    const renderProjects = (list) => { /* renders cards */ };
    renderProjects(projects);

    // Live search bonus
    searchInput.addEventListener("input", (e) => {
      const term = e.target.value.toLowerCase();
      const filtered = projects.filter(p => 
        p.title.toLowerCase().includes(term) || 
        p.description.toLowerCase().includes(term) ||
        p.tags.some(t => t.toLowerCase().includes(term))
      );
      renderProjects(filtered);
    });
  });
```

### Zero-MD Reflection Rendering (index.html)
```html
<zero-md src="reflection.md"></zero-md>
<!-- Renders Markdown as clean, styled HTML in-browser -->
```

---

## Tech Stack

| Component          | Tool / Library |
|--------------------|----------------|
| **Languages**      | HTML5, CSS3, JavaScript (ES6+) |
| **Framework**      | Bootstrap 5 |
| **IDE**            | Visual Studio Code |
| **AI Assistance**  | Grok (xAI) – code architecture and polish |

---

## Attribution

- Bootstrap 5 Documentation  
- MDN Web Docs – Fetch API & modern JavaScript  
- zero-md by zerodevx – https://github.com/zerodevx/zero-md  
- Font Awesome & Google Fonts  
- Grok (xAI) – code refinement and final polish
- My brother

---

## Conclusion

This final developer profile is not just a project — it’s my **digital business card**, my **resume**, and my **proof of growth** throughout CIS 376.  
It showcases clean code, modern architecture, user-centered design, and a commitment to accessibility and performance.

From Saigon to Florence, Alabama — this is who I am as a developer today.  
And I’m just getting started.

**Thank you, Dr. Cumbie, for an amazing semester.**  
Let’s build the future.

— Thuan Nguyen  
2025

--- 