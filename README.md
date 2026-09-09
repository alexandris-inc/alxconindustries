# ALXCON Website Project

**Brand:** ALXCON  
**Full name:** Alexandris Technical Constructions

## Visual direction
- Premium black / white / charcoal
- Minimal architectural / engineering aesthetic
- Strong electrical + MEP identity
- Final logo: `assets/alxcon-logo.png`
- Current Facebook cover: `assets/facebook-cover.png`

## Pages
- `index.html` — homepage
- `projects.html` — starter projects page
- `project-detail.html` — reusable album template, opened with `?project=slug`
- `contact.html` — starter contact page

## Services
- Ηλεκτρολογικές Εγκαταστάσεις
- Μηχανολογικά Έργα
- EV Chargers
- Ανακαινίσεις Κατοικιών & Επαγγελματικών Χώρων
- Τεχνικός Ασφαλείας & Πιστοποιήσεις
- Μελέτες & Συμβουλευτική

## Product goal
The owner is not a coder. The final site should let them:
- create a new project from a simple admin,
- upload multiple photos,
- have the project appear automatically in Projects,
- mark a project/photo as featured for the homepage,
- avoid editing HTML/CSS manually.

## Simplest CMS setup

Use **Decap CMS** with the existing static site and a GitHub repository. It gives the owner a browser admin at `/admin/`, stores project entries as Markdown files, and works well with GitHub Pages or Netlify hosting.

Create one `projects` collection with these fields:

- `title` — project name
- `slug` — URL key used by `project-detail.html?project=slug`
- `category`, `location`, `service`, `year` — album metadata
- `description` — project summary
- `featured` — boolean for the homepage
- `cover` — the card image
- `gallery` — multiple project photos with captions

The next implementation step would be to move the current JavaScript project object into CMS content files, add a small build step that generates the project cards and album data, and add Decap's `config.yml` plus the `/admin/` login. This keeps hosting inexpensive and lets the owner create projects, upload photos, and choose featured work without editing HTML or CSS.

## Suggested Codex prompt
Continue this ALXCON website from the existing files. Preserve the current premium dark visual identity. First make navigation consistent across Home / Projects / Contact, then create a reusable project-detail album page and propose the simplest CMS setup for a non-coder. Do not redesign the brand.
