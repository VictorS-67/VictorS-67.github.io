# Victor's Academic Portfolio

A minimal Astro-based academic portfolio website with Tailwind CSS.

## 🚀 Project Structure

```
src/
├── components/         # Reusable UI components
│   ├── Header.astro    # Navigation bar with dark mode toggle
│   ├── Footer.astro    # Site footer with social links
│   └── SocialLinks.astro
├── content/            # Markdown content (Astro Collections)
│   ├── config.ts       # Content collection schemas
│   ├── publications/   # Your research papers
│   └── projects/       # Your projects
├── data/
│   └── author.json     # Your personal info, education, experience
├── layouts/
│   └── Base.astro      # Main page template
├── pages/              # Route pages
│   ├── index.astro     # Homepage
│   ├── experience.astro # CV/Resume page
│   ├── publications.astro
│   └── projects/
├── styles/
│   └── global.css      # Tailwind + custom styles
```

## 📝 How to Edit Content

### Personal Info
Edit `src/data/author.json` to update:
- Name, role, bio
- Social links
- Education history
- Work experience
- Skills

### Publications
Add Markdown files to `src/content/publications/`:

```md
---
title: "Your Paper Title"
authors: ["You", "Co-author"]
venue: "Conference Name"
year: 2025
type: conference  # or 'journal', 'preprint'
featured: true
doi: "10.1000/example"
code: "https://github.com/..."
---

Paper description here...
```

### Projects
Add Markdown files to `src/content/projects/`:

```md
---
title: "Project Name"
description: "Short description"
tags: ["Python", "ML"]
github: "https://github.com/..."
featured: true
date: 2024-06-15
---

Project details here...
```

## 🧞 Commands

| Command        | Action                                      |
| :------------- | :------------------------------------------ |
| `pnpm install` | Install dependencies                        |
| `pnpm dev`     | Start dev server at `localhost:4321`        |
| `pnpm build`   | Build for production to `./dist/`           |
| `pnpm preview` | Preview production build locally            |

## 🎨 Customization

### Colors
Edit `src/styles/global.css` to change the primary color palette.

### Dark Mode
Dark mode is automatic based on system preference, with a manual toggle in the header.

### Adding Pages
Create new `.astro` files in `src/pages/` - they automatically become routes.

## 📦 Deployment

Build the site:
```bash
pnpm build
```

The `dist/` folder can be deployed to:
- **GitHub Pages**: Push to `gh-pages` branch
- **Netlify/Vercel**: Connect repo, build command is `pnpm build`
- **Any static host**: Upload the `dist/` folder
