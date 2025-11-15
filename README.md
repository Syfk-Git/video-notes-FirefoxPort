# Video Notes

Video Notes is a lightweight YouTube companion that ships two pieces from this repo:

- `extension/` &mdash; a Manifest V3 Chrome/Chromium extension that injects an inline note workspace, timeline markers, and a popup dashboard for searchable, timestamped annotations.
- `landing/` &mdash; a static marketing page (HTML/CSS/JS only) used for sharing the feature tour and installation instructions.

## Quick start

### Extension
1. Open `chrome://extensions`, enable **Developer mode**, and choose **Load unpacked**.
2. Select the `extension` folder. The content script activates automatically on `youtube.com/watch`.
3. For a deeper dive into storage, popup behavior, and helper scripts, see `extension/README.md`.

### Landing page
1. `cd landing`
2. Serve the folder with any static server, e.g. `npx serve .` or `python3 -m http.server`.
3. Deploys cleanly to any static host (GitHub Pages, Netlify, etc.) because it has no build step or dependencies.

## Development notes
- No project-wide dependencies: linting/formatting/tooling is opt-in per directory.
- Keep DOM/storage keys in uppercase snake case to match the extension code style.
- When contributing, describe UI-visible changes and manual test steps in PRs to keep reviews fast.
