# nedko.co

Personal website for Nedko Hristov — a space for thoughtful writing, practical guides, and lessons learned from building software and teams.

**Domain:** [nedko.co](https://nedko.co)

**Description:** Building scalable technology—and sustainable teams.

## Tech Stack

- **Static Site Generator:** [Jekyll](https://jekyllrb.com/)
- **Hosting:** [GitHub Pages](https://pages.github.com/)
- **Markdown:** Kramdown
- **CI/CD:** GitHub Actions

## Project Structure

```
├── _config.yml      # Jekyll configuration
├── _layouts/        # Page templates
├── _includes/       # Reusable components
├── _posts/          # Blog posts (writing)
├── _guides/         # Guides collection
├── assets/          # CSS, images, etc.
├── index.md         # Homepage
├── about.md         # About page
├── contact.md       # Contact page
├── portfolio.md     # Portfolio page
└── writing/         # Writing index
```

## Testing Locally

### Prerequisites

- Ruby (2.7+ recommended)
- Bundler

### Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/nedkoh/nedko.co.git
   cd nedko.co
   ```

2. Install dependencies:
   ```bash
   bundle install
   ```

3. Run the local server:
   ```bash
   bundle exec jekyll serve
   ```

4. Open [http://localhost:4000](http://localhost:4000) in your browser.

### Live Reload (optional)

```bash
bundle exec jekyll serve --livereload
```

## Making Changes and Deploying

### Workflow

1. **Create a branch** for your changes:
   ```bash
   git checkout -b your-branch-name
   ```

2. **Make your changes** — edit Markdown files, add posts, update styles, etc.

3. **Test locally** to verify changes look correct:
   ```bash
   bundle exec jekyll serve
   ```

4. **Commit and push** your changes:
   ```bash
   git add .
   git commit -m "Description of changes"
   git push -u origin your-branch-name
   ```

5. **Open a Pull Request** on GitHub:
   ```bash
   gh pr create --title "Your PR title" --body "Description"
   ```

6. **Merge to main** — once the PR is approved and merged, GitHub Actions will automatically build and deploy the site to GitHub Pages.

### Adding Content

**New blog post:**
```bash
# Create a new post in _posts/
# Filename format: YYYY-MM-DD-title.md
```

```markdown
---
title: Your Post Title
---

Your content here...
```

**New guide:**
```bash
# Create a new guide in _guides/
```

```markdown
---
title: Your Guide Title
---

Your content here...
```

## Deployment

Deployment is automatic via GitHub Actions. When changes are merged to `main`:

1. The `preview.yaml` workflow triggers
2. Jekyll builds the site
3. The built site deploys to GitHub Pages
4. Changes are live at [nedko.co](https://nedko.co)

## License

All rights reserved.
