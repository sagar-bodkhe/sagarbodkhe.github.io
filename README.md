# Portfolio Website

A modern, responsive portfolio website built with HTML, CSS, and JavaScript. Designed to showcase your projects, skills, and experience with beautiful animations and a clean, professional design.

🔗 **Live Site**: [sagarbodkhe.github.io](https://sagarbodkhe.github.io)  
📦 **Repository**: [github.com/sagar-bodkhe/sagarbodkhe.github.io](https://github.com/sagar-bodkhe/sagarbodkhe.github.io)

## Features

- 🎨 Modern, sleek design with gradient effects
- 📱 Fully responsive (mobile, tablet, desktop)
- ✨ Smooth animations and transitions
- 🎯 Interactive navigation with active section highlighting
- 💫 Animated background orbs
- ⌨️ Typing animation for hero subtitle
- 📊 Animated statistics counters
- 🎭 Scroll-triggered animations
- 📧 Contact form (ready for backend integration)

## Tech Stack

- **HTML5** - Semantic markup
- **CSS3** - Modern styling with CSS variables, animations, and gradients
- **JavaScript (Vanilla)** - Interactive features and animations
- **Google Fonts** - Inter font family

## Project Structure

```
portfolio/
│
├── index.html              # Main HTML file
├── README.md              # Project documentation
│
└── assets/
    ├── css/
    │   └── style.css      # All styles and animations
    ├── js/
    │   └── main.js        # JavaScript functionality
    └── images/            # Placeholder for images
        └── .gitkeep       # Keep folder in git
```

## Getting Started

### Local Development

1. Clone or download this repository
2. Open `index.html` in your web browser
3. That's it! No build process required.

### Customization

#### 1. Update Personal Information

Edit `index.html` and replace:
- **Name**: Change "Your Name" in the hero section
- **Email**: Update email addresses in contact section and social links
- **Social Links**: Update GitHub, LinkedIn URLs in the hero section
- **About Section**: Modify the about text and statistics
- **Projects**: Replace project cards with your actual projects

#### 2. Customize Colors

Edit CSS variables in `assets/css/style.css`:

```css
:root {
    --primary: #6366f1;        /* Main brand color */
    --secondary: #ec4899;      /* Secondary accent */
    --accent: #f59e0b;         /* Additional accent */
    --background: #0f172a;     /* Dark background */
    /* ... more variables */
}
```

#### 3. Update Skills

Modify the skills grid in `index.html` to reflect your actual skills and technologies.

#### 4. Add Your Projects

Replace the placeholder project cards with your real projects:
- Update project titles and descriptions
- Add project images (place in `assets/images/`)
- Update GitHub and live demo links
- Modify technology tags

#### 5. Configure Contact Form

The contact form currently shows an alert. To make it functional, you can:

**Option A: Use Formspree**
1. Sign up at [formspree.io](https://formspree.io)
2. Get your form endpoint
3. Update the form action in `index.html`:
   ```html
   <form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
   ```

**Option B: Use EmailJS**
1. Sign up at [emailjs.com](https://www.emailjs.com)
2. Configure your email service
3. Update the JavaScript in `assets/js/main.js` to use EmailJS SDK

**Option C: Use Your Own Backend**
- Update the form submission handler in `main.js` to POST to your API endpoint

## Deploying to GitHub Pages

### Method 1: Using GitHub Web Interface

1. **Create a new repository** on GitHub (or use an existing one)
   - Repository name: `your-username.github.io` (for user page) or any name (for project page)

2. **Upload files**
   - Click "uploading an existing file"
   - Drag and drop all files (index.html, assets folder, README.md)
   - Commit changes

3. **Enable GitHub Pages**
   - Go to repository Settings
   - Scroll to "Pages" section
   - Under "Source", select branch (usually `main` or `master`)
   - Select folder (usually `/root`)
   - Click Save

4. **Access your site**
   - Your site will be available at: `https://sagarbodkhe.github.io`
   - Since the repository is named `sagarbodkhe.github.io`, it's automatically configured as a user page

### Method 2: Using Git Command Line

```bash
# Initialize git repository
git init

# Add all files
git add .

# Commit files
git commit -m "Initial portfolio website"

# Add remote repository
git remote add origin https://github.com/sagar-bodkhe/sagarbodkhe.github.io.git

# Push to GitHub
git branch -M main
git push -u origin main
```

Then follow steps 3-4 from Method 1 to enable GitHub Pages.

**Note**: Since this repository is named `sagarbodkhe.github.io`, it will automatically be available at `https://sagarbodkhe.github.io` once GitHub Pages is enabled.

### Method 3: Using GitHub Actions (Optional)

For more advanced deployment, you can set up GitHub Actions. Create `.github/workflows/deploy.yml`:

```yaml
name: Deploy to GitHub Pages

on:
  push:
    branches: [ main ]

jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - name: Deploy
        uses: peaceiris/actions-gh-pages@v3
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          publish_dir: ./
```

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## Performance Tips

1. **Optimize Images**: Compress images before adding them to `assets/images/`
2. **Lazy Loading**: Consider adding lazy loading for images if you add many
3. **Minify CSS/JS**: For production, minify CSS and JavaScript files
4. **CDN**: Consider hosting fonts and assets via CDN for better performance

## Future Enhancements

- [ ] Add dark/light theme toggle
- [ ] Implement blog section
- [ ] Add project filtering/search
- [ ] Integrate with GitHub API to show live stats
- [ ] Add more animation effects
- [ ] Implement smooth page transitions
- [ ] Add testimonials section
- [ ] Add resume download functionality

## License

This project is open source and available under the [MIT License](LICENSE).

## Credits

- Design inspiration from modern portfolio websites
- Icons: SVG icons embedded directly
- Fonts: [Google Fonts - Inter](https://fonts.google.com/specimen/Inter)

## Support

If you have any questions or need help customizing this portfolio, feel free to:
- Open an issue on GitHub
- Fork the repository and make your own version
- Share your portfolio once it's live!

---

**Made with ❤️ for showcasing your work**
