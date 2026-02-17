# Sara Blanco Gómez - Academic Website

My personal academic website showcasing my CV, research experience, and blog posts. Built with [Quarto](https://quarto.org) and automatically deployed to GitHub Pages.

**Live Site:** https://sara-bg.github.io/cv_bmmb531_test/

## About

This website features:
- **Home Page:** My complete academic CV including education, research experience, awards, and activities
- **Blog:** Posts about my research, experiences, and technical projects
- **Automatic Deployment:** Changes pushed to the main branch automatically rebuild and deploy the site

## Technology Stack

- **[Quarto](https://quarto.org)** - Modern scientific and technical publishing system
- **GitHub Actions** - Automated build and deployment pipeline
- **GitHub Pages** - Free hosting for the static website

## Prerequisites

To work with this site locally, you need:
- [Quarto](https://quarto.org/docs/get-started/) installed on your computer
- Git installed
- A text editor (VS Code, Sublime, etc.)

## Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/sara-bg/cv_bmmb531_test.git
cd cv_bmmb531_test
```

### 2. Preview Locally

To see the website on your computer before publishing:

```bash
quarto preview
```

This opens your browser and shows the site. Changes you make to files will automatically refresh in the browser.

### 3. Build the Site

To generate the static website files:

```bash
quarto render
```

This creates a `_site/` folder with all the HTML files.

## Project Structure

```
.
├── _quarto.yml                    # Main site configuration
├── index.qmd                      # CV/Home page
├── styles.css                     # Custom CSS styling
├── headshot.jpg                   # Profile photo
├── blog/
│   ├── index.qmd                  # Blog listing page
│   └── posts/                     # Individual blog posts
│       └── 2026-02-17-creating-this-website/
│           └── index.qmd          # First blog post
└── .github/
    └── workflows/
        └── publish.yml            # GitHub Actions deployment workflow
```

## Adding a New Blog Post

1. **Create a folder** for your post under `blog/posts/`:
   ```bash
   mkdir -p blog/posts/YYYY-MM-DD-post-title
   ```

2. **Create the post file** `blog/posts/YYYY-MM-DD-post-title/index.qmd`:
   ```markdown
   ---
   title: "Your Post Title"
   author: "Sara Blanco Gómez"
   date: "2026-02-17"
   categories: [research, chemistry, tutorial]
   description: "A brief description of your post"
   ---

   ## Introduction

   Your content goes here...
   ```

3. **Preview your post** locally:
   ```bash
   quarto preview
   ```

4. **Commit and push** when ready:
   ```bash
   git add .
   git commit -m "Add new blog post about [topic]"
   git push
   ```

The site will automatically rebuild and deploy within 2-3 minutes.

## Deployment

### How It Works

The website uses **GitHub Actions** to automatically build and deploy:

1. You push changes to the `main` branch
2. GitHub Actions workflow (`.github/workflows/publish.yml`) triggers automatically
3. Quarto renders the website
4. The built site deploys to GitHub Pages
5. Your site updates at https://sara-bg.github.io/cv_bmmb531_test/

### First-Time Setup

If deploying for the first time, enable GitHub Pages:

1. Go to repository **Settings** → **Pages**
2. Under "Build and deployment" → "Source"
3. Select **"GitHub Actions"** from the dropdown
4. Save (happens automatically)

### Monitoring Deployments

- View workflow runs: https://github.com/sara-bg/cv_bmmb531_test/actions
- Check deployment status in the Actions tab after each push

## Customization

### Updating the CV

Edit `index.qmd` to update your CV content. The file uses standard Markdown formatting.

### Changing the Theme

Edit `_quarto.yml` and change the `theme` value:
```yaml
format:
  html:
    theme: cosmo  # Try: flatly, minty, pulse, sandstone, etc.
```

See all themes: https://quarto.org/docs/output-formats/html-themes.html

### Custom Styling

Edit `styles.css` to customize colors, fonts, spacing, and other visual elements.

### Site Configuration

Edit `_quarto.yml` to modify:
- Site title
- Navigation menu items
- Social media links
- Page layout options

## Troubleshooting

**Site not updating after push?**
- Check that GitHub Pages source is set to "GitHub Actions" (not "Deploy from a branch")
- View the Actions tab to see if the workflow ran successfully
- Hard refresh your browser (Ctrl+Shift+R or Cmd+Shift+R)

**Preview not working?**
- Make sure Quarto is installed: `quarto --version`
- Check for syntax errors in your `.qmd` files

**Build errors?**
- Check the Actions tab for error messages
- Ensure all `.qmd` files have valid YAML front matter
- Make sure image paths are correct

## Resources

- [Quarto Documentation](https://quarto.org/docs/guide/)
- [Quarto Websites Guide](https://quarto.org/docs/websites/)
- [Quarto Blog Guide](https://quarto.org/docs/websites/website-blog.html)
- [GitHub Pages Documentation](https://docs.github.com/en/pages)

## License

This website is for personal use. Feel free to use the structure as a template for your own academic website.
