<p>
    <a href="https://sprucecss.com/">
        <br>
        <picture>
            <source media="(prefers-color-scheme: light)" srcset="./.github/spruce-logo-dark.svg">
            <source media="(prefers-color-scheme: dark)" srcset="./.github/spruce-logo-light.svg">
            <img alt="Spruce CSS" width="140" src="./.github/spruce-logo-dark.svg">
        # Wplugged Documentation

        This repository hosts the documentation site for wplugged.com. It's based on the Spruce Docs Eleventy template and contains the Eleventy source files, styles and build scripts.

        This repo is configured to automatically build and deploy to GitHub Pages (using GitHub Actions). A custom domain `wplugged.com` is set during the deployment step.

        Quick links

        - Site: https://wplugged.com
        - Repo: https://github.com/Sotiris-k/wplugged

        Prerequisites

        - Node.js 18+ and npm

        Local development

        1. Install dependencies:

        ```bash
        npm ci
        ```

        2. Start the dev server (Eleventy + Sass watcher):

        ```bash
        npm start
        ```

        3. Build production output (the workflow publishes the `dist` folder):

        ```bash
        npm run prod
        ```

        Deployment

        - A GitHub Action (`.github/workflows/deploy.yml`) builds the site on `main` and deploys the `dist` folder to GitHub Pages. The workflow writes a `CNAME` file with `wplugged.com` into `dist` before deployment so Pages serves the custom domain.
        - After push, go to the repository Settings → Pages to confirm the Pages configuration and the custom domain.

        DNS notes

        - To use `wplugged.com` with GitHub Pages, configure your DNS provider:
          - Add an A record for the apex (wplugged.com) pointing to GitHub Pages IPs, or use an ALIAS/ANAME if your provider supports it.
          - Add a CNAME record for `www` pointing to `<username>.github.io` or configure the apex as above.

        If you'd like, I can add a short `CNAME` file to the repo root (not strictly required because the workflow writes one to `dist`).

        More

        The site uses Eleventy and Spruce CSS. The relevant scripts are in `package.json`.
