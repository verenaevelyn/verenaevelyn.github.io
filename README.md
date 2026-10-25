# Verena Evelyn — Portfolio Website

A single-page, static portfolio (HTML + CSS + vanilla JavaScript). No build step, no backend, no frameworks. Works on GitHub Pages.

## 1. Folder structure

```
portfolio/
├── index.html                 ← the whole website
├── README.md
├── images/
│   ├── verena-hero.jpg        ← your puzzle portrait (included)
│   ├── project-01.jpg  …  project-10.jpg   ← your 10 projects
│   └── placeholder-project.svg  ← shown when an image is missing
└── files/
    └── verena-cv.pdf          ← your CV (YOU MUST ADD THIS)
```

Important:
- `placeholder-project.svg` is already inside the `images` folder.
- Your puzzle portrait is already included as `images/verena-hero.jpg`. To swap it, replace that file and keep the name.
- The 10 project images and the CV are not included yet: until you add them, projects show labelled placeholders and the CV button explains that the PDF is missing.
- File names are **case-sensitive** on GitHub Pages: `Project-01.JPG` is not `project-01.jpg`.

## 2. Replace images

1. Open the local `images` folder.
2. Replace the file (e.g. `project-01.jpg`) with your new image.
3. Keep the **same filename**. If you must rename it, update `image:` for that project in `index.html`.
4. Commit and push (or re-upload) to GitHub.

Suggested export sizes (about 1600–2400 px on the long edge, JPG/PNG/WebP, under ~800 KB each):

| `layout` | Shape | Ratio |
|---|---|---|
| wide | landscape | 16:10 |
| wideL | big landscape | 16:10 |
| portrait | tall | 4:5 |
| slim | tall | 3:4 |
| square | square | 1:1 |
| banner | panoramic | 21:9 |

By default whole artwork is shown (nothing cropped). To fill frames instead, set `imageFit: "cover"` in `siteConfig`.

If an image is missing or misspelled, a designed **Placeholder** tile shows that file path. It never loops or shows a broken icon.

## 3. Edit text

Open `index.html` in Notepad and search for these comments:

- `EDIT YOUR PERSONAL INFORMATION HERE` → name, headline, bio, interests (`siteConfig`)
- `EDIT YOUR CONTACT DETAILS HERE` → email, LinkedIn, Instagram, CV path
- `EDIT YOUR PROJECTS HERE` → the 10 project records (`projects`)

Only change text between the quotation marks; keep commas and brackets. Selected Works and All Projects both read from the same `projects` list. Set `featured: true` on up to four projects to show them in **Selected Works**.

Notes:
- Email, LinkedIn and Instagram are empty on purpose. Buttons stay disabled (with a short note) until you add real values. LinkedIn/Instagram must start with `https://`.
- Placeholder titles, categories and descriptions are examples, not claims about your work. Replace them.

## 4. Replace the CV

Save your PDF as `files/verena-cv.pdf` (or change `cvPath`). When the site is published and the file is missing, the CV button turns into a disabled button with a note.

## 5. Preview locally (Windows)

Double-click `index.html`. It opens in your browser. (The CV-missing check only runs once the site is published.)

## 6. Publish with GitHub Pages

1. Create a folder (e.g. `portfolio`) and put `index.html`, `images/` and `files/` inside.
2. Go to github.com → **New repository**. Name it e.g. `portfolio`, set **Public**, click **Create repository**.
3. Click **uploading an existing file**, drag in `index.html` and the `images` and `files` folders, then **Commit changes**.
4. Open **Settings → Pages**. Under **Build and deployment**, choose **Deploy from a branch**, branch `main`, folder `/ (root)`, then **Save**.
5. Wait 1–3 minutes. The URL appears at the top of the Pages screen.

URLs:
- Repository named `username.github.io` → `https://username.github.io/`
- Any other repository (e.g. `portfolio`) → `https://username.github.io/portfolio/`

All links and assets are relative, so both work.

## 7. Update after publishing

Open the repository → **Add file → Upload files** (same filename replaces the old one) → **Commit changes**. Edit text: click `index.html` → pencil icon → edit → commit. Updates may take a minute or two; refresh with Ctrl+F5.

## 8. Testing checklist

- [ ] Nav links scroll to About, Selected Works, All Projects, Contact (heading not hidden under the bar)
- [ ] Mobile menu opens, closes (link tap or Esc)
- [ ] Hero portrait loads from `images/verena-hero.jpg`
- [ ] Exactly 10 projects in All Projects; featured ones appear in Selected Works
- [ ] Missing images show placeholders, not broken icons
- [ ] Clicking a project opens the viewer; Esc closes it; arrows move between projects
- [ ] After adding email: Email Me opens your mail app
- [ ] CV button downloads `files/verena-cv.pdf`
- [ ] LinkedIn/Instagram links appear only when set
- [ ] Layout is good at phone, tablet, laptop widths; no sideways scrolling
- [ ] Tab key shows visible focus everywhere
- [ ] With OS "reduce motion" on, animations are off
- [ ] Back-to-top button works; footer year is current
- [ ] File names match exactly (lowercase) after upload
