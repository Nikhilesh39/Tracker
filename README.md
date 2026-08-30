# Routine — Daily Companion V3

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

## What changed in V3
- Fixed the Add Habit modal not closing: it previously mixed three
  separate visibility mechanisms (`hidden` attribute, an `is-hidden`
  class, and an inline `style.display`) that could get out of sync.
  It now uses a single `.open` class, and the panel scrolls
  internally so its close button stays reachable even with a mobile
  keyboard open.
- Redesigned the "at a glance" hero as a ritual ring: the circular
  fill shows overall completion, and the four dots around it mark
  Morning / Office / After office / Evening, so you can see where in
  the day you stand, not just a percentage.
- Refined type (serif headings + sans body + monospace for timers),
  color, spacing, added a delete option for custom habits, and
  accessibility touches (visible focus states, reduced-motion support).
- Bumped the service worker cache to `routine-v3` so installed PWAs
  pick up the new files instead of serving the old cached version.

## Notes
- Data is stored locally in the browser using localStorage.
- No login, backend, analytics, or external API is used.
- Browser notification support is intentionally not wired into V3 yet; the reminder architecture can be added next.
