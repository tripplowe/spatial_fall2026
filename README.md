# FANR 3800 — Lecture Site

Source and publishing workflow for the FANR 3800 lecture website.

- **Live site:** <https://tripplowe.github.io/spatial_fall2026/>
- **Repository:** `tripplowe/spatial_fall2026` (public)
- **Author:** Dr. Tripp Lowe

Lectures are written once in Markdown and published as a web page, with **PDF**
and **Word** versions generated automatically as download links. The site is
built with [Quarto](https://quarto.org) and hosted on GitHub Pages.

---

## How this works (the mental model)

There are **two independent things** happening in this repo, and keeping them
straight prevents almost every problem:

1. **Publishing the site** — done by running `quarto publish gh-pages` on your
   machine. This renders your lectures and pushes the finished website to the
   `gh-pages` branch, which is what GitHub Pages serves. **This is the only step
   that changes what visitors see.**
2. **Version-controlling the source** — done by committing and syncing in VS
   Code. This saves your `.md` sources and `_quarto.yml` to the `main` branch so
   your work is backed up and available on your other computer. **This does not
   publish anything.**

You do both for each lecture: publish to make it live, sync to save the source.

> The `_site/` folder is only a *local* render output. It changes when you run
> `quarto render` or `quarto preview`, never when you sync. Don't edit it and
> don't commit it (it's in `.gitignore`).

---

## One-time setup (per computer)

Install these on any machine you'll publish from (Windows 11):

1. **Git** — `winget install --id Git.Git -e`, then set your identity:
   ```powershell
   git config --global user.name "Tripp Lowe"
   git config --global user.email "you@uga.edu"
   ```
2. **Quarto** — install from <https://quarto.org/docs/get-started/>. Verify with `quarto check`.
3. **VS Code** — `winget install --id Microsoft.VisualStudioCode -e`, then install the **Quarto** extension from the Extensions panel.
4. **TinyTeX** (LaTeX engine for PDF output) — after Quarto is installed:
   ```powershell
   quarto install tinytex
   ```
5. **Clone the repo:**
   ```powershell
   cd C:\dev
   git clone https://github.com/tripplowe/spatial_fall2026.git
   cd spatial_fall2026
   ```

---

## Adding and publishing a lecture (the routine)

For each new lecture:

1. **Create the file** in the project root, named `WeekNN_Lecture.md`
   (e.g. `Week03_Lecture.md`). Start it with front matter:
   ```markdown
   ---
   title: "FANR 3800: Week 3 Lecture Plan"
   subtitle: "Your subtitle"
   author: "Dr. Tripp Lowe"
   date: "Fall 2026"
   ---

   # Week 3 - Title

   Your content here.
   ```

2. **Add it to the navbar** in `_quarto.yml` under `website: > navbar: > left:`,
   matching the existing indentation exactly (spaces, never tabs):
   ```yaml
       left:
         - href: index.qmd
           text: Home
         - href: Week01_Lecture.md
           text: "Lecture 1"
         - href: Week02_Lecture.md
           text: "Lecture 2"
         - href: Week03_Lecture.md
           text: "Lecture 3"
   ```

3. **(Optional) Preview locally** to check it before it goes live:
   ```powershell
   quarto preview
   ```
   Press `Ctrl+C` to stop.

4. **Publish** (this renders and deploys — no separate `quarto render` needed):
   ```powershell
   quarto publish gh-pages
   ```
   Confirm when prompted. The page is live in a minute or two.

5. **Save the source** — in VS Code's Source Control panel, stage the new file
   and the edited `_quarto.yml`, write a commit message ("Add Week 3"), commit,
   and **Sync**. This backs up the source and pushes it to your other computer.

---

## Where things end up (URLs)

GitHub Pages serves `.html` (not `.md`) and is **case-sensitive**. For a file
named `Week03_Lecture.md` the links are:

| Item        | URL                                                                    |
|-------------|------------------------------------------------------------------------|
| Home        | `https://tripplowe.github.io/spatial_fall2026/`                        |
| Web page    | `https://tripplowe.github.io/spatial_fall2026/Week03_Lecture.html`     |
| PDF         | `https://tripplowe.github.io/spatial_fall2026/Week03_Lecture.pdf`      |
| Word (DOCX) | `https://tripplowe.github.io/spatial_fall2026/Week03_Lecture.docx`     |

The PDF and Word links also appear in the **Other Formats** section in each
page's margin. Paste whichever URL you want into **eLearning Commons** once —
it updates in place each time you republish, so you never have to relink.

---

## Repository structure

```
spatial_fall2026/
├── _quarto.yml           # Site config + navbar (edit this to add lectures)
├── index.qmd             # Home page (required — the site root)
├── Week01_Lecture.md     # Lecture source files
├── Week02_Lecture.md
├── README.md             # This file
├── .gitignore
├── _publish.yml          # Created by the first `quarto publish gh-pages`
├── .github/workflows/
│   └── publish.yml        # Optional CI (see note below)
└── _site/                # Local render output — do not edit or commit
```

`.gitignore` should contain at least:
```
/.quarto/
/_site/
*.aux
*.log
*.out
*.toc
```

---

## Second-computer checklist

Publishing happens from your machine, so before publishing on the other
computer:

1. Make sure Quarto **and TinyTeX** are installed there (see setup above).
2. **Pull the latest source first** so you don't overwrite newer work:
   ```powershell
   git pull
   ```
   (or click **Sync** in VS Code)
3. Then follow the normal routine — edit, `quarto publish gh-pages`, commit, sync.

---

## Content rules (this repo is PUBLIC)

Because GitHub Pages on the free plan requires a **public** repository,
everything committed here is world-readable, including the full git history.
**Never commit:**

- Exam questions, answer keys, or solutions
- Grades, rosters, or any student data (FERPA)
- Copyrighted readings or figures you don't have rights to redistribute

Keep anything sensitive in a separate private location entirely.

---

## Troubleshooting

**A page gives a 404.**
- Did you actually run `quarto publish gh-pages`? Syncing in VS Code alone does
  **not** publish. Run the publish command.
- Check the URL: it must end in `.html` (not `.md`) and match the filename's
  capitalization exactly (`Week03_Lecture.html`, not `week03...`).
- Give a fresh deploy 30–60 seconds, then hard-refresh (`Ctrl+F5`).

**The whole site 404s / home page missing.**
- There must be an `index.qmd` (or `index.md`) in the project root. Without it
  there's no site root to serve.
- In **Settings → Pages**, Source should be **Deploy from a branch → `gh-pages` / (root)**.

**`quarto publish gh-pages` fails.**
- Read the error. A LaTeX error means the PDF format choked on something in the
  lecture — check math/special characters, or temporarily comment out `pdf:` in
  `_quarto.yml` to isolate it.
- Confirm TinyTeX is installed: `quarto install tinytex`.

**A newly added lecture doesn't show up after publishing.**
- Confirm it's referenced in `_quarto.yml` with correct indentation (spaces).
- Re-run `quarto render` locally — if `_site/WeekNN_Lecture.html` appears, the
  file is fine and you just need to `quarto publish gh-pages` again.

**Verify what's actually on GitHub.**
```powershell
git branch --show-current        # should print: main
git fetch
git log --oneline -3 origin/main # should list your latest commit
```
If your commit isn't there, your source never reached `main` — check you're on
the `main` branch (bottom-left of the VS Code status bar) and sync again.

---

## Note on the GitHub Action (optional CI)

`.github/workflows/publish.yml` was set up to publish automatically on every
push, but the workflow settled into a **manual** approach using
`quarto publish gh-pages`. The Action is not required and is not relied upon.

If idle runs send you "workflow failed" emails, you can delete
`.github/workflows/publish.yml` (commit and sync) to stop them. Leaving it in
place is harmless. If you ever want to revisit fully automatic publishing, the
Action needs **Settings → Actions → General → Workflow permissions → Read and
write permissions** enabled to work.

---

## Command cheat sheet

| Task                        | Command                          |
|-----------------------------|----------------------------------|
| Preview the site locally    | `quarto preview`                 |
| Render locally (no publish) | `quarto render`                  |
| **Publish the live site**   | `quarto publish gh-pages`        |
| Check the Quarto install    | `quarto check`                   |
| Get latest source           | `git pull` (or Sync in VS Code)  |
| Install PDF engine          | `quarto install tinytex`         |
