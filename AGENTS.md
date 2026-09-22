# Project Guidelines & Agent Permissions

## File Operations & Editing Permissions
* **Full Autonomous Editing:** The agent is explicitly authorized to **always create, edit, modify, move, rename, and organize** HTML, CSS, JavaScript, asset, and config files in this repository without pausing for manual confirmation.
* **Proactive Execution:** Proactively write, update, and test game files and directory structures to fulfill user requests immediately.

## Architecture Guidelines
* **Multi-Game Directory Layout:**
  * Root `index.html` is the mobile-first arcade portal hub.
  * Every game lives in its own dedicated sub-path: `games/<game-id>/index.html`.
  * Games can have their own `assets/` subfolder created on-demand only when external assets (images, sounds, sprites) are needed (no empty placeholder folders).
* **Mobile-First Standard:**
  * Ensure touch-friendly controls, proper viewport scaling (`viewport-fit=cover`), and prevent accidental zoom/scroll issues (`touch-action: manipulation` or `none` on canvas).
  * Use Web Audio API for lightweight sound effects where applicable.
* **Naming Conventions:**
  * Always use kebab-case (no spaces) for filenames and directories (e.g., `math-grade-2`, `super-speed`).
* **Localization:**
  * Maintain Hebrew RTL support and ensure mathematical equations maintain proper LTR formatting via `math-ltr-box` / `dir="ltr"` isolation.

## Git Commit Guidelines
* **Commit Message Format:**
  * Brief, clear subject line (imperative mood, e.g. `feat: add ...`, `fix: ...`).
  * Followed by a blank line and a brief body description when possible, highlighting key rationale or details without repeating the subject line.
