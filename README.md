# Regie Canlas — 3D Artist Portfolio

A single-page portfolio site (hero, about, skills, featured projects, gallery, footer) built to match the provided reference design. Fully responsive (mobile/tablet/desktop), auto light/dark theme, and your uploaded "RC" logo wired in.

## Files
- `index.html` — the entire site (HTML + CSS + JS). No build step needed.
- `assets/logo-dark.png` — white version of your logo, shown on dark backgrounds.
- `assets/logo-light.png` — black version of your logo, shown on light backgrounds.

Keep `index.html` and the `assets` folder together — the logo won't load if `assets/` is missing.

## What's new in this version
- **Your logo** is used in the nav bar and footer, and automatically swaps between the white and black version depending on the active theme.
- **Light/dark mode**: the site follows the visitor's browser/OS preference automatically on first visit. The moon/sun button in the nav lets them override it manually, and that choice is remembered on their next visit (via `localStorage`).
- **Mobile responsive**: below ~980px width a hamburger menu replaces the nav links; layout reflows to a single column on phones, with smaller type and tighter spacing under ~640px.
- **All buttons are functional**:
  - `View Portfolio` / `Contact Me` / nav links — smooth-scroll to their sections, with the nav highlighting the active section as you scroll.
  - Social icons — open GitHub/ArtStation/Instagram/LinkedIn in a new tab, mail icon opens your email client.
  - `Download Resume` — actually downloads a placeholder text resume (swap this for your real PDF, see below).
  - Gallery tabs (`ALL`/`CHARACTERS`/`PRODUCTS`/`ENVIRONMENTS`/`PROPS`) — filter the grid live.
  - `View Full Gallery` — expands the grid to reveal 5 additional pieces, and toggles back to "Show Less".
  - `Get In Touch` — opens a pre-addressed email.

## Publish it on GitHub Pages
1. Create a new repository on GitHub, e.g. `regiecanlas.github.io` (for a user site) or any name like `portfolio` (for a project site).
2. Upload `index.html` to the repo root (drag-and-drop on the GitHub website works, or via git):
   ```bash
   git init
   git add index.html README.md
   git commit -m "Initial portfolio"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<repo-name>.git
   git push -u origin main
   ```
3. In the repo, go to **Settings → Pages**, set **Source** to `Deploy from a branch`, branch `main`, folder `/ (root)`, then Save.
4. Your site will be live at `https://<your-username>.github.io/<repo-name>/` within a minute or two.

## Customize
- Swap the placeholder images (currently from `picsum.photos`) for your actual renders — just replace each `<img src="...">` with a path to your own image files (e.g. `assets/renders/hero.jpg`).
- Update the email and social links (search for `regie.canlas@example.com`, `github.com/regiecanlas`, etc.) in the hero, footer, and JS sections.
- To use your real resume: replace the `resumeText` JS variable's content with a link to an actual PDF, e.g. change the `Download Resume` button to `<a href="assets/resume.pdf" download>` instead of the JS-generated text file.
- Colors and fonts are defined as CSS variables at the top of the `<style>` block — dark theme values in `:root`, light theme overrides in `html[data-theme="light"]`.
