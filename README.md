[![Netlify Status](https://api.netlify.com/api/v1/badges/f05a545a-6504-4ab2-8d04-022ca82d602b/deploy-status)](https://app.netlify.com/sites/cozy-nougat-8c197b/deploys)

# Personal blog

This is the source code for my blog site: https://blog.ronnyale.com/

## Tech Stack

- **Quarto**: Static site generator for blog posts
- **Netlify**: Hosting platform
- **GitHub**: Version control

## Local Development

### Preview the site locally

```bash
quarto preview
```

This will start a local server and open the site in your browser. Changes will auto-reload.

### Build the site

```bash
quarto render
```

This generates the static site in the `docs/` folder.

## Deployment

### Deploy to Netlify

After building the site locally, deploy with:

```bash
quarto publish netlify
```

**Important Notes:**
- Always run `quarto render` before publishing to ensure the latest changes are built
- The `docs/` folder is committed to git (this is intentional)
- Deployment is manual via `quarto publish netlify`, not automatic from GitHub pushes
- Your Netlify site configuration is stored in `_publish.yml`

### First-time setup (already done)

If you need to set up a new site:

```bash
quarto publish netlify
# Follow the prompts to authorize and select/create a site
```

## Project Structure

```
.
├── _quarto.yml          # Main Quarto configuration
├── posts/               # Blog posts (one folder per post)
│   └── YYYY-MM-DD-slug/
│       └── index.qmd    # Post content
├── docs/                # Generated site (committed to git)
├── styles.scss          # Custom styles for readability
└── _publish.yml         # Netlify deployment config
```

