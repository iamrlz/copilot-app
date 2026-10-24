# copilot-app

A responsive, dependency-free student portfolio in `student-portfolio/`, built with HTML, CSS, and JavaScript.

## Preview locally

Open `student-portfolio/index.html` directly in a modern browser. No installation or build step is needed.

Alternatively, from the repository root, run `python3 -m http.server 8000` and open
`http://localhost:8000/student-portfolio/`. Stop the preview server with Ctrl+C.
This optional static file server is only for previewing; the website has no backend.

## Publish to GitHub Pages

The deployment workflow publishes `student-portfolio/` directly as the site root.
It does not use or update the old `gh-pages` branch, so there is no separate copy
of the website to keep in sync.

1. In repository **Settings → Pages → Build and deployment**, select **GitHub Actions**
   as the source instead of deploying from `gh-pages`.
2. Merge the deployment workflow and portfolio changes into `main`. Changes to
   `student-portfolio/` or the deployment workflow on `main` automatically deploy.
   If the workflow is already merged, use **Actions → Deploy portfolio to GitHub Pages
   → Run workflow** and select `main`.
3. Wait for that workflow's **deploy** job to succeed, then open
   <https://iamrlz.dev/copilot-app/> and verify that **Light mode** switches the page
   to the light theme and **Dark mode** switches it back. Hard-refresh if the browser
   still shows cached assets.

Only `main` can deploy. If the `github-pages` environment restricts deployment
branches, allow `main` in **Settings → Environments → github-pages**.
Keep the existing custom domain and DNS configuration unchanged.
No package installation, build command, or personal access token is required.

## Customize

- Edit `student-portfolio/index.html` to replace the fictional student, skills, and illustrative projects with your own content.
- Adjust the blue and purple palettes for both themes in `student-portfolio/styles.css`.
- `student-portfolio/script.js` provides the dark/light theme toggle, mobile navigation, active-section highlighting, expandable project descriptions, and the footer year.
- Contact is intentionally an informational placeholder, not a form. No personal information is requested or collected, and no external fonts, libraries, APIs, or analytics are used.

Project cards lift and highlight on hover or keyboard focus. The layout adapts to mobile and desktop, supports smooth anchor navigation, keyboard navigation, and reduced-motion preferences, and keeps the main content accessible without JavaScript.