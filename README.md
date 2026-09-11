# Applied & Bayesian Reading Group website

This repository contains the official website for the **Applied & Bayesian Reading Group** in the Department of Statistical Sciences at the University of Toronto. It is a static [Quarto](https://quarto.org/) website published with GitHub Pages.

## Work on the site locally

1. [Install Quarto](https://quarto.org/docs/get-started/).
2. Clone this repository and open its directory.
3. Start a local development server:

   ```bash
   quarto preview
   ```

To render the complete site without starting a server, run:

```bash
quarto render
```

Rendered files are written to `_site/` and are not committed.

## Update the content

- Edit `index.qmd` for the homepage.
- Edit `schedule.qmd` to add meetings. Copy one of the empty week blocks and fill it in when details are confirmed.
- Edit `readings.qmd` to add main and optional readings.
- Edit `_quarto.yml` to change navigation, site-wide settings, or footer content.
- Edit `assets/styles.css` for visual styling.

The master Reading List Google Sheets URL is configured in three places: the navbar in `_quarto.yml`, the homepage button in `index.qmd`, and the link on `readings.qmd`. Update each occurrence if the spreadsheet changes.

## Deployment

A push to `main` runs `.github/workflows/deploy-pages.yml`. The workflow renders the site, uploads `_site/` as a GitHub Pages artifact, and deploys it through GitHub Actions.

The expected public URL is:

<https://user-jiyichen.github.io/UofT-DoSS-Reading-Group/>

The deployment workflow enables GitHub Pages automatically on its first run. If repository policy prevents Actions from enabling Pages, set **Settings → Pages → Source** to **GitHub Actions** manually and rerun the workflow.
