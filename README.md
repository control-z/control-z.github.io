# Control-Z | XR & Spatial Computing

A modern, static website showcasing XR and spatial computing content, designed for hosting on GitHub Pages.

## Features

- **Modern XR-Themed Design**: Beautiful gradient backgrounds, glassmorphism effects, and particle animations
- **Responsive Layout**: Works perfectly on desktop, tablet, and mobile devices
- **YouTube Integration**: Placeholder sections for 4 embedded YouTube videos with easy-to-follow instructions
- **Smooth Animations**: Glitch effects, floating VR frame, and fade-in animations
- **Performance Optimized**: Lightweight with no external dependencies (except YouTube embeds)

## Getting Started

### Local Development

Simply clone this repository and open `index.html` in your browser:

```bash
git clone <your-repo-url>
cd control-z.web
# Open index.html in your browser
```

Or use a local server:

```bash
# Python 3
python -m http.server 8000

# Node.js (with http-server)
npx http-server

# Then visit http://localhost:8000
```

### Adding Your YouTube Videos

1. Find your YouTube video ID from the URL (e.g., `https://www.youtube.com/watch?v=VIDEO_ID`)
2. In `index.html`, locate each video section
3. Replace the empty `src=""` in the iframe with: `src="https://www.youtube.com/embed/VIDEO_ID"`
4. Update the title and description for each video
5. Videos will automatically display once embedded

**Example:**
```html
<!-- Before -->
<iframe class="youtube-iframe" src="" ...></iframe>

<!-- After -->
<iframe class="youtube-iframe" src="https://www.youtube.com/embed/dQw4w9WgXcQ" ...></iframe>
```

**Note:** The first video is already embedded as an example.

## Deploying to GitHub Pages

### Option 1: Using GitHub Settings

1. Push your code to a GitHub repository
2. Go to **Settings** → **Pages**
3. Under **Source**, select your main branch (usually `main` or `master`)
4. Click **Save**
5. Your site will be available at `https://yourusername.github.io/control-z.web`

### Option 2: Using GitHub Actions

Create `.github/workflows/deploy.yml`:

```yaml
name: Deploy to GitHub Pages

on:
  push:
    branches: [ main ]

permissions:
  contents: read
  pages: write
  id-token: write

jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - name: Setup Pages
        uses: actions/configure-pages@v2
      - name: Upload artifact
        uses: actions/upload-pages-artifact@v1
        with:
          path: '.'
      - name: Deploy to GitHub Pages
        uses: actions/deploy-pages@v1
```

## Customization

### Colors

Edit the CSS variables in `styles.css`:

```css
:root {
    --primary-color: #6366f1;
    --secondary-color: #8b5cf6;
    --accent-color: #ec4899;
    /* ... more variables */
}
```

### Content

- **Hero Section**: Edit the main title and subtitle in `index.html`
- **About Section**: Modify the description in the about section
- **Footer**: Update copyright information

## Browser Support

- Chrome/Edge (latest)
- Firefox (latest)
- Safari (latest)
- Mobile browsers

## License

MIT License - feel free to use this for your own projects!

## Contributing

Contributions are welcome! Feel free to submit issues or pull requests.

