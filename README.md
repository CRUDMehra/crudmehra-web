# CRUD Mehra — Personal Portfolio Website

> **crudmehra.com** · Dark-themed personal portfolio for Senior Mobile App Developer.

## 🗂 File Structure

```
crudmehra/
├── index.html        ← Home page
├── portfolio.html    ← Portfolio / Projects
├── contact.html      ← Contact / Hire Me
├── favicon.svg       ← Favicon (auto-detected by browsers)
├── css/
│   └── style.css     ← All shared styles
├── js/
│   └── main.js       ← Nav toggle, scroll reveal, animations
└── README.md
```

## 🚀 Deploy to Cloudflare Pages

### Step 1 — Push to GitHub
```bash
git init
git add .
git commit -m "Initial commit — portfolio site"
git remote add origin https://github.com/CRUDMehra/<repo-name>.git
git push -u origin main
```

### Step 2 — Connect Cloudflare Pages
1. Go to [dash.cloudflare.com](https://dash.cloudflare.com) → **Pages** → **Create a project**
2. Connect your GitHub account and select the repo
3. Build settings:
   - **Framework preset:** None
   - **Build command:** _(leave empty)_
   - **Build output directory:** `/` _(root)_
4. Click **Save and Deploy**

### Step 3 — Custom Domain
1. In Cloudflare Pages → your project → **Custom domains**
2. Add `crudmehra.com`
3. Cloudflare will auto-configure DNS if your domain is on Cloudflare — done!

---

## ✏️ Customization

### Add a Profile Photo
In `index.html`, find the `.avatar-monogram` div and replace with:
```html
<img src="images/profile.jpg" alt="CRUD Mehra" />
```
Place your photo at `images/profile.jpg`.

### Add Portfolio Projects
In `portfolio.html`, copy any `.project-card` block and update:
- `project-num` (003, 004…)
- `project-icon` (emoji)
- `project-title`
- `project-desc`
- `project-tags` (use `.tag`, `.tag.green`, or `.tag.blue`)
- `project-footer` links

### Hook up the Contact Form
The form currently shows a success message without sending. To make it functional:

**Option A — Formspree (easiest):**
```html
<form action="https://formspree.io/f/YOUR_ID" method="POST">
```

**Option B — Cloudflare Pages Functions** or any backend of your choice.

---

## 🎨 Theme Colors

| Variable        | Value     | Usage               |
|-----------------|-----------|---------------------|
| `--bg`          | `#080808` | Page background     |
| `--accent`      | `#00ff88` | Green accent        |
| `--accent-2`    | `#00c8ff` | Blue accent         |
| `--text`        | `#e8e8e8` | Primary text        |
| `--text-muted`  | `#666`    | Secondary text      |

---

Made with ☕ by CRUD Mehra · [hello@crudmehra.com](mailto:hello@crudmehra.com)
