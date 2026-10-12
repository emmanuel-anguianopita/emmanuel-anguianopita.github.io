# Javier Emmanuel Anguiano Pita — Academic website

A minimalist personal academic website built using **Quarto**, with the Cosmo theme and custom Sass styling.

## Requirements

- [Quarto](https://quarto.org/docs/get-started/) for local preview and rendering.
- [Git](https://git-scm.com/downloads) or GitHub Desktop for pushing changes.
- A GitHub account. No paid hosting required for a public repository.

## Preview locally

Open a terminal in this folder and run:

```bash
quarto preview
```

Preview will open in your browser. To create the generated HTML:

```bash
quarto render
```

## Publish to GitHub Pages (automatic)

1. On GitHub, create a **public** repository, ideally `YOUR_USERNAME.github.io` to use the shortest site address. Do not initialize the repository with a README.
2. Upload/push **all files**, including the hidden `.github/workflows/publish.yml` file. GitHub Desktop is the easiest way to preserve the folder structure.
3. Open the repository's **Settings → Pages → Build and deployment → Source**, and choose **GitHub Actions**.
4. The workflow automatically builds and deploys the Quarto website after pushes to `main`. If required, run it from **Actions → Publish Quarto website → Run workflow**.
5. View the live URL under **Settings → Pages**. For repository `YOUR_USERNAME.github.io`, the address is `https://YOUR_USERNAME.github.io/`; for a normal project repository, `https://YOUR_USERNAME.github.io/REPOSITORY/`.

### Command-line push (alternative to GitHub Desktop)

```bash
git init
git branch -M main
git add .
git commit -m "Initial Quarto academic website"
git remote add origin https://github.com/YOUR_USERNAME/YOUR_USERNAME.github.io.git
git push -u origin main
```

To update:

```bash
git add .
git commit -m "Update academic website"
git push
```

### Before publishing

- Replace placeholder GitHub link in `_quarto.yml` with your own profile.
- Review affiliation and wording of research projects.
- Add confirmed publications to `publications.qmd`; do not list submitted papers as published.
- Add your downloadable CV at `assets/cv/cv.pdf` and uncomment its link in `cv.qmd`.
- Do not upload confidential data, unpublished manuscripts without permission, or copyrighted PDFs.

## File structure

- `_quarto.yml`: site settings and navigation.
- `styles.scss`: visual appearance.
- `index.qmd`: home.
- `research.qmd`, `publications.qmd`, `teaching.qmd`, `materials.qmd`, `cv.qmd`: main pages.
- `projects/`: descriptions of ongoing work.
- `examples/`: illustrative tables and figure embedding.
- `assets/`: images, CV, articles, materials.
- `.github/workflows/publish.yml`: build/deploy automation.

## Troubleshooting

If GitHub shows no website, verify **Pages → Source = GitHub Actions**, that the latest workflow run is green in **Actions**, and that the default branch is `main`. GitHub may require approving the first workflow run depending on repository security settings.
