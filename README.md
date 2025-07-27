
# TaskWebsite (Tailwind + Supabase)

This is a simple task management front-end using **Tailwind CSS**, **Supabase Auth**, and deployed via **GitHub Pages** using **GitHub Actions**.

## 🌐 Live Demo
 
Once deployed, your site will be live at:

```
https://<your-username>.github.io/<repo-name>/
```

## 📁 Project Structure

```
.
├── src/        # Source HTML + Tailwind input
├── dist/       # Built HTML + output.css
├── .github/workflows/tailwind.yml  # GitHub Actions config
├── tailwind.config.js
├── postcss.config.js
└── package.json
```

## 🛠 Setup Instructions

### 1. Install Dependencies

```bash
npm install
```

### 2. Run Build Locally

```bash
npm run build
```

This will:
- Compile Tailwind CSS from `src/input.css` → `dist/output.css`
- Copy HTML files from `src/*.html` → `dist/`

### 3. Deploy with GitHub Actions

Every push to the `main` branch triggers the GitHub Action to build your CSS and commit `dist/` changes automatically.

## 🌍 GitHub Pages Setup

Go to:
- `Repo Settings` → `Pages`
- Source: **Deploy from a branch**
- Branch: `main`, Folder: `/dist`

## 🔐 Supabase Auth

Login and registration handled via:

```js
supabase.auth.signInWithPassword({ email, password });
supabase.auth.signUp({ email, password });
```

The Logout button is wired to:
```js
supabase.auth.signOut();
```

## 🧠 TODO

- [ ] Add dynamic user display in navbar
- [ ] Add dark mode toggle
- [ ] Deploy on a custom domain (optional)

---

Crafted with care by [Kiernan DiMeglio](https://www.linkedin.com/in/kiernan-dimeglio/)
