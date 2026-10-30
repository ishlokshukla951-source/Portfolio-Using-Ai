# Premium Full-Stack Developer Portfolio — Ishlok Shukla

A premium, modern, responsive personal portfolio website designed and developed exclusively with **pure semantic HTML5 and modern CSS3** (zero external frameworks like Bootstrap or Tailwind, and zero JavaScript dependencies).

---

## 📁 1. Project File Structure

```text
portfolio/
│
├── index.html                  # Main semantic HTML5 document
│
├── css/
│   └── style.css               # Complete responsive CSS3 stylesheet & design tokens
│
├── images/
│   ├── profile.jpg             # High-res developer portrait
│   ├── about.jpg               # Developer workspace & code editor visual
│   ├── project-1.jpg           # Inkloom AI platform preview image
│   ├── project-2.jpg           # Personal Profile Card UI preview
│   ├── project-3.jpg           # Personal Portfolio preview
│   └── background.jpg          # Subtle ambient background texture
│
├── assets/
│   └── icons/                  # Scalable Vector Graphics (SVG) icon library
│       ├── html5.svg
│       ├── css3.svg
│       ├── javascript.svg
│       ├── java.svg
│       ├── git.svg
│       ├── github.svg
│       ├── vscode.svg
│       └── linkedin.svg
│
└── README.md                   # Comprehensive documentation & setup guide
```

---

## 🎨 2. Design System & Color Palette (Light Theme)

Designed around a crisp, modern light aesthetic with porcelain backgrounds, vibrant indigo & sky-blue accents, and sharp typography:

| Token | Hex / Value | Role / Usage |
|---|---|---|
| **Background Primary** | `#F8FAFC` | Clean Porcelain Slate 50 root background |
| **Background Secondary** | `#FFFFFF` | Pure White for elevated cards & surfaces |
| **Card Surface** | `rgba(255, 255, 255, 0.92)` | Frosted glass card surface with backdrop blur |
| **Primary Accent** | `#6366F1` | Vibrant Indigo for gradients, buttons & nodes |
| **Secondary Accent** | `#0284C7` | Ocean Sky Blue for highlights & badges |
| **Main Text** | `#0F172A` | Deep Slate 900 for ultra-crisp readable headings |
| **Secondary Text** | `#475569` | Balanced Slate 600 for body text & descriptions |
| **Borders** | `rgba(15, 23, 42, 0.08)` | Subtle hairline borders on cards |
| **Glow Aura** | `rgba(99, 102, 241, 0.25)` | Indigo radiance on avatar frame & button hovers |

### Typography Stack
- **Display & Headings:** `Space Grotesk` (Google Fonts, weights: 500, 600, 700, 800)
- **Body & UI:** `Inter` (Google Fonts, weights: 300, 400, 500, 600, 700)
- **Code & Tags:** `JetBrains Mono` (Google Fonts, weights: 400, 500, 600)

---

## 🖼️ 3. Image Assets & Download Instructions

If setting up this portfolio from scratch, save the following images into your `images/` directory with their exact specified filenames:

1. **`images/profile.jpg`**
   - **Description:** Professional developer portrait.
   - **Direct URL:** `https://images.unsplash.com/photo-1539571696357-5a69c17a67c6?w=800&auto=format&fit=crop&q=85`
   - **Recommended Dimensions:** 800x800px (1:1 square crop).

2. **`images/about.jpg`**
   - **Description:** Modern developer workstation with code editor and ambient glow.
   - **Direct URL:** `https://images.unsplash.com/photo-1555066931-4365d14bab8c?w=900&auto=format&fit=crop&q=85`
   - **Recommended Dimensions:** 900x600px.

3. **`images/project-1.jpg`**
   - **Description:** Inkloom AI platform interface showcase.
   - **Direct URL:** `https://images.unsplash.com/photo-1618005182384-a83a8bd57fbe?w=900&auto=format&fit=crop&q=85`
   - **Recommended Dimensions:** 900x500px.

4. **`images/project-2.jpg`**
   - **Description:** Responsive Personal Profile Card UI component preview.
   - **Direct URL:** `https://images.unsplash.com/photo-1507238691740-187a5b1d37b8?w=900&auto=format&fit=crop&q=85`
   - **Recommended Dimensions:** 900x500px.

5. **`images/project-3.jpg`**
   - **Description:** Personal Portfolio website preview.
   - **Direct URL:** `https://images.unsplash.com/photo-1460925895917-afdab827c52f?w=900&auto=format&fit=crop&q=85`
   - **Recommended Dimensions:** 900x500px.

6. **`images/background.jpg`**
   - **Description:** Deep midnight navy gradient mesh backdrop.
   - **Direct URL:** `https://images.unsplash.com/photo-1550745165-9bc0b252726f?w=1600&auto=format&fit=crop&q=85`
   - **Recommended Dimensions:** 1600x900px.

---

## 🚀 4. How to Run in VS Code Using Live Server

Follow these 4 simple steps to run the portfolio locally:

### Step 1: Install VS Code and the Extension
1. Open **Visual Studio Code**.
2. Press `Ctrl + Shift + X` (or `Cmd + Shift + X` on macOS) to open the **Extensions** panel.
3. Search for **"Live Server"** (by *Ritwick Dey*).
4. Click **Install**.

### Step 2: Open the Project Folder
1. Click **File** > **Open Folder...**
2. Select the `portfolio` folder on your computer.

### Step 3: Launch Live Server
- **Method A:** Right-click on `index.html` in the file explorer and select **"Open with Live Server"**.
- **Method B:** Open `index.html` and click the **"Go Live"** button in the blue status bar at the bottom right corner of VS Code.

### Step 4: View the Portfolio
Your default browser will automatically open:
```text
http://127.0.0.1:5500/index.html
```
Any edits you make to `index.html` or `css/style.css` will instantly refresh the page without needing any build tools!

---

## 💡 5. HTML5 & CSS3 Architectural Explanations

### A. Semantic Document Hierarchy
- `<header class="navbar">`: Sticky navigation bar containing the logo, links, and mobile drawer.
- `<main>`: Encloses the core page content, improving accessibility and screen-reader parsing.
- `<section>`: Divides the portfolio into discrete thematic landmarks (`#home`, `#about`, `#skills`, `#projects`, `#education`, `#contact`).
- `<article class="project-card">`: Represents self-contained project units.
- `<footer>`: Contains brand notes, back-to-top anchors, and copyright credentials.

### B. Pure CSS Responsive Mobile Navigation (Checkbox Hack)
Instead of relying on JavaScript, the mobile drawer uses the CSS checkbox hack:
```html
<input type="checkbox" id="nav-toggle" class="nav-toggle-input" />
<label for="nav-toggle" class="nav-toggle-label">
  <span class="nav-toggle-bar"></span>
  <span class="nav-toggle-bar"></span>
  <span class="nav-toggle-bar"></span>
</label>
<ul class="nav-menu">...</ul>
```
When clicked, `:checked` triggers CSS sibling combinators:
- Transforms the 3 hamburger lines into an animated 'X' via `transform: rotate(45deg)`.
- Transitions the navigation drawer into view (`transform: translateY(0); opacity: 1;`).

### C. Glassmorphism & Visual Polish
Glass cards are crafted using:
```css
background: rgba(17, 24, 39, 0.75);
backdrop-filter: blur(14px);
-webkit-backdrop-filter: blur(14px);
border: 1px solid rgba(255, 255, 255, 0.10);
box-shadow: 0 10px 25px -5px rgba(0, 0, 0, 0.5);
```

### D. Mailto Contact Solution
Because the portfolio is strictly HTML and CSS without a server-side backend, the form uses the native HTML5 `mailto:` protocol:
```html
<form action="mailto:ishlok.bcs2026100@invertisuniversity.ac.in" method="POST" enctype="text/plain">
```
Submitting this form opens the user's native email client (e.g. Gmail, Apple Mail, Outlook) with their name, email, subject, and message pre-populated.

---

## 👨‍💻 Author

**Ishlok Shukla**  
Aspiring Full-Stack Developer  
B.Tech Computer Science & Engineering — Invertis University  
Shahjahanpur, Uttar Pradesh, India  
- **GitHub:** [ishlokshukla951-source](https://github.com/ishlokshukla951-source)  
- **LinkedIn:** [Ishlok Shukla](https://linkedin.com/in/ishlok-shukla)  
- **Email:** ishlok.bcs2026100@invertisuniversity.ac.in
