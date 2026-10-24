# Workout Planner

Dedicated source repository for the existing Workout Planner V3, with V2 retained as a historical release.

## Current status

Repository scaffold only. Original V2 and V3 HTML files have not yet been retrieved. No GitHub remote has been configured and nothing has been published.

V3 source reference: `/Workout-Planner-v3.html`, Library ID `libfile_be0bf22e991481919108edaff557484b`.
Original conversation: Workout Planner Integration (`6adb86ce-2dbc-83e9-8c4a-459be3b85b3a`).

## Layout

- `src/index.html`: editable application source, initially an exact copy of V3 (pending).
- `versions/v2/Workout-Planner-v2.html`: unchanged original V2 (pending).
- `versions/v3/Workout-Planner-v3.html`: unchanged original V3 (pending).
- `CHANGELOG.md`: verified version history and migration status.
- `.github/workflows/pages.yml`: validates required files, stages the site, and deploys GitHub Pages.

Do not reconstruct or overwrite historical versions. Import the actual files and record their SHA-256 hashes in `versions/README.md`. Copy V3 into `src/index.html` without changing the original archive. Include any companion assets required by either HTML file.

## Preview and maintain

Open `src/index.html` in a browser after import. If browser restrictions affect the app, serve `src/` with a local static HTTP server. Verify mobile layout, workout editing, save/reload behavior, and external resources after import. Application functionality and storage behavior have not yet been inspected.

Keep future changes in `src/`; leave `versions/` unchanged. Record meaningful changes in `CHANGELOG.md`. Create V2/V3 Git tags only after the corresponding originals have been imported and verified.

## GitHub and Pages setup

1. Authorize GitHub and choose an owner and repository (suggested name: `workout-planner`). Confirm repository visibility before creation.
2. Import and verify both original HTML files; commit the source and archives.
3. Add the chosen GitHub repository as `origin` and push branch `main`.
4. In repository **Settings > Pages**, select **GitHub Actions** as the build and deployment source.
5. Run **Deploy Workout Planner** from Actions, or push a source change to `main`.
6. Confirm a successful deployment and open the deployment URL. Verify the application on desktop and mobile before reporting it as live.

The workflow publishes only `src/` and the version HTML archives, not the README or repository metadata. V3 serves at the site root; archives serve at `versions/v2/Workout-Planner-v2.html` and `versions/v3/Workout-Planner-v3.html`. These are relative paths, not confirmed live links. Published HTML is accessible to the site's audience; review source for embedded personal data or credentials before deployment.

GitHub reference: https://docs.github.com/en/pages/getting-started-with-github-pages/using-custom-workflows-with-github-pages
