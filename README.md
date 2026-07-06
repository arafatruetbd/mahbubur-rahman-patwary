# Mahbubur Rahman Patwary — Portfolio

A modern, responsive personal portfolio site for **Mahbubur Rahman Patwary** built with vanilla **HTML, CSS, and Bootstrap Icons**. The site is static, dependency-free, and ready to deploy to any static host (GitHub Pages, Netlify, Vercel, Cloudflare Pages, etc.).

> Single-page layout · Full-bleed dark navy hero · Accessible semantic HTML · Mobile-first responsive design

---

## ✨ Features

- 🎨 **Premium dark theme** — navy (`#0b1d3a` → `#07142a`) with gold accents (`#d4a437`)
- 🖼️ **Full-screen hero** under the sticky navbar, edge-to-edge gradient background
- 👤 **Layered portrait composition** — dark circle backdrop + gold ring + `me.png` photo
- 📱 **Fully responsive** — desktop two-column, tablet stacked, mobile optimized
- ♿ **Accessible** — skip-link, `:focus-visible`, `prefers-reduced-motion`, semantic landmarks
- ⚡ **Zero build step** — pure HTML/CSS, no JS framework, no bundler

---

## 🛠️ Tech Stack

| Layer       | Choice                                             |
| ----------- | -------------------------------------------------- |
| Markup      | HTML5 (semantic, ARIA-labelled sections)           |
| Styling     | Vanilla CSS3 with custom properties (design tokens) |
| Icons       | Bootstrap Icons (CDN)                              |
| Fonts       | System font stack                                  |
| Interactivity | Minimal vanilla JS (mobile drawer toggle)        |

---

## 🚀 Getting Started

### Prerequisites

None — just a modern web browser. Optional: a local static server for development.

### Run Locally

**Option A — Just open the file**

Double-click `index.html` (works on all modern OSes).

**Option B — Local server (recommended for development)**

Using Python:

```bash
cd path/to/mrp-portfolio
python -m http.server 5500
# then visit http://localhost:5500
```

Using Node:

```bash
npx serve .
```

Using VS Code: install the **Live Server** extension, right-click `index.html` → *Open with Live Server*.

### Deploy

Drop the folder onto any static host. No build step required.

| Host             | Steps                                                                 |
| ---------------- | --------------------------------------------------------------------- |
| GitHub Pages     | Push to a repo, enable Pages on `main` branch, root folder             |
| Netlify          | Drag-and-drop the folder onto the Netlify dashboard                    |
| Vercel           | `vercel --prod` from inside the folder                                 |
| Cloudflare Pages | Connect repo, build command empty, output dir `.`                      |

---

## 📁 Project Structure

```
mrp-portfolio/
├── index.html          # Single-page markup with all sections
├── me.png              # Profile photo (replace with your own)
├── styles.css          # Global reset, design tokens, container, a11y helpers
├── navbar.css          # Sticky header + mobile drawer
├── hero.css            # Full-bleed hero, portrait composition, bg shapes
├── about.css           # Feature cards
├── skills.css          # Skill bars
├── stats.css           # Statistics grid
├── prefooter.css       # 3-column Resume / Gallery / Contact band
├── footer.css          # Copyright bar
└── README.md           # You are here
```

The CSS is **deliberately split per section** so you can tweak any block in isolation without hunting through one giant file.

---

## 🎨 Design Tokens

Defined in `:root` in `styles.css`:

| Token              | Value      | Purpose                          |
| ------------------ | ---------- | -------------------------------- |
| `--color-navy`     | `#0b1d3a`  | Primary dark background          |
| `--color-navy-dark`| `#07142a`  | Darker navy (gradients, footer)  |
| `--color-gold`     | `#d4a437`  | Accent color                     |
| `--color-gold-light`| `#f3c969` | Hover / highlight accent         |
| `--color-white`    | `#ffffff`  | Primary text on dark             |
| `--container-width`| `1200px`   | Max inner content width          |
| `--header-height`  | `80px`     | Sticky navbar total height       |
| `--radius-sm/md/lg`| `8/14/24px`| Border radii                     |
| `--shadow-card`    | …          | Card drop shadow                 |

---

## 🧩 Sections Overview

| Section     | Purpose                                              |
| ----------- | ---------------------------------------------------- |
| `#home`     | Hero — greeting, headline, CTAs, socials, portrait   |
| `#about`    | About-me paragraph + feature cards                   |
| `#skills`   | Skill bars with proficiency percentages              |
| `#stats`    | Quick-glance stats (projects, clients, years, etc.)  |
| `#resume`   | Prefooter column — resume download + highlights      |
| `#gallery`  | Prefooter column — thumbnail strip                   |
| `#contact`  | Prefooter column — phone, email, location, socials   |
| `footer`    | Copyright line                                       |

---

## ✏️ Customization

### Change the photo

Replace `me.png` with your own portrait (ideally a transparent-background PNG, roughly 600–800px square). The dark circle backdrop + gold ring are drawn in CSS, so no Photoshop required.

### Update social links

Open `index.html` and edit the hero `<ul class="hero__socials">` block (around line 102). The current live links are:

- **Facebook** → `https://www.facebook.com/mahbuburrahmanpatwary`
- **Email** → `mailto:mahbub@marketbangla.co`

Replace the remaining `href="#"` placeholders (Twitter/X, LinkedIn, Instagram) with your profiles.

### Edit copy

All text lives directly in `index.html`. Search for the section you want to change and edit the inner HTML — no template engine, no Markdown-to-HTML.

### Adjust colors

Override the design tokens at the top of `styles.css`:

```css
:root {
  --color-navy:      #0b1d3a;
  --color-gold:      #d4a437;
  /* … etc. */
}
```

Every section picks them up automatically.

### Tweak hero height

The hero is `calc(100vh - var(--header-height))`. Change `--header-height` in `styles.css` (e.g. `60px` for a shorter navbar) and the hero re-flows on every screen.

---

## ♿ Accessibility Notes

- Skip-link at the top jumps directly to `#main`
- All decorative icons use `aria-hidden="true"`; meaningful links have `aria-label`
- Sections use semantic `<section>` with `aria-labelledby` pointing at their headings
- `:focus-visible` outlines on all interactive elements
- `prefers-reduced-motion: reduce` disables transitions and dot-grid animation
- Color contrast ratios meet WCAG AA on body text and CTAs

---

## 📜 License

MIT © Mahbubur Rahman Patwary

Feel free to fork, customize, and deploy your own version. If this template helped you build something, a star is appreciated.

---

## 🙏 Credits

- Icons by [Bootstrap Icons](https://icons.getbootstrap.com/)
- Photo: Mahbubur Rahman Patwary
- Inspired by the classic DevFolio / Mahbubur Rahman style

---

**Happy coding!** 🚀