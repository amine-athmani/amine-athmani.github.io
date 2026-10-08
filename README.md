# Amine Athmani: personal site and resume

Static landing page (`index.html`) plus an ATS-friendly LaTeX resume (`resume/`).

## Publish on GitHub Pages

1. Create a public repo named `amine-athmani.github.io` (the site will be served at https://amine-athmani.github.io).
   Any other repo name works too; it will be served at `https://amine-athmani.github.io/<repo-name>/`.
2. Push this folder to the `main` branch.
3. In the repo: Settings > Pages > Build and deployment > Source: "Deploy from a branch", Branch: `main`, folder `/ (root)`.

`.nojekyll` tells GitHub Pages to serve the files as-is.

## Update the resume

```sh
cd resume
pdflatex Amine_Athmani_Resume.tex
cp Amine_Athmani_Resume.pdf ..   # the site links to the copy at the repo root
```

Only base LaTeX packages are used (geometry, hyperref, xcolor, lmodern), so it also compiles on Overleaf.
