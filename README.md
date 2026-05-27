# CV Website

This repository keeps the CV in LaTeX and publishes it as a GitHub Pages website.

## How it works

1. Edit `CV.tex` or files inside `Sections/`.
2. Push to the `main` branch.
3. GitHub Actions compiles `CV.tex` into `CV.pdf`.
4. GitHub Pages displays the updated `CV.pdf` through `index.html`.

## GitHub Pages setup

In the GitHub repository:

1. Go to **Settings → Pages**.
2. Set **Build and deployment → Source** to **GitHub Actions**.
3. Push to `main`.

Your website will be available at:

```text
https://YOUR-GITHUB-USERNAME.github.io/YOUR-REPOSITORY-NAME/
```

For example, if your repository is named `CV`, it will usually be:

```text
https://YOUR-GITHUB-USERNAME.github.io/CV/
```

## Main files

```text
CV.tex                         Main LaTeX file
Sections/                      CV section files
index.html                     Webpage that embeds CV.pdf
.github/workflows/deploy.yml   GitHub Actions workflow
CV.pdf                         Local preview PDF; GitHub rebuilds this automatically
```

## Local compile

```bash
pdflatex CV.tex
```

or:

```bash
latexmk -pdf CV.tex
```
