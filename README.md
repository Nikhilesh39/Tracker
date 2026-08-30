# Routine — Daily Companion V1

A mobile-first, offline PWA for tracking daily routines.

## Run locally
You can preview with any static server. For example:
`python -m http.server 8000`
Then open `http://localhost:8000`.

## GitHub Pages
1. Create a new GitHub repository.
2. Upload everything inside this folder to the repository root.
3. Go to Settings → Pages.
4. Under Build and deployment, choose "Deploy from a branch".
5. Select the `main` branch and `/ (root)`.
6. Save and wait for the Pages URL.
7. Open it on your phone.
8. Use your browser's "Add to Home Screen" / "Install" option.

## Notes
- Data is stored locally in the browser using localStorage.
- No login, backend, analytics, or external API is used.
- Browser notification support is intentionally not wired into V1 yet; the reminder architecture can be added next.
