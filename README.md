# 🚀 Raj Kumar Konka - Professional Portfolio Website

A modern, responsive portfolio website showcasing my work as a Software Developer, AI/ML Engineer, and Data Scientist.

![Portfolio Preview](https://img.shields.io/badge/Status-Live-success)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)

## ✨ Features

- **Modern Design**: Clean, professional UI with smooth animations
- **Fully Responsive**: Works perfectly on desktop, tablet, and mobile devices
- **Interactive Elements**: Smooth scrolling, hover effects, and dynamic content
- **Performance Optimized**: Fast loading with lazy-loaded images
- **Accessibility**: Semantic HTML and ARIA labels for better accessibility
- **SEO Friendly**: Meta tags and structured data for better search visibility

## 📂 Project Structure

```
portfolio/
├── index.html          # Main HTML file
├── styles.css          # CSS styles and animations
├── script.js           # JavaScript for interactivity
├── assets/             # Images and documents
│   └── Raj_Kumar_Konka_Resume.pdf
└── README.md           # This file
```

## 🎨 Sections

1. **Hero/Home** - Eye-catching introduction with key stats
2. **About** - Professional summary and highlights
3. **Experience** - Timeline of work history
4. **Projects** - Featured projects with descriptions
5. **Skills** - Technical skills and technologies
6. **Contact** - Contact information and social links

## 🚀 Deployment to GitHub Pages

### Step 1: Create GitHub Repository

```bash
# Navigate to portfolio folder
cd path/to/portfolio

# Initialize git (if not already done)
git init

# Add all files
git add .

# Commit
git commit -m "Initial commit: Professional portfolio website"

# Create repository on GitHub (replace YOUR_USERNAME)
# Go to https://github.com/new and create: portfolio or YOUR_USERNAME.github.io

# Add remote
git remote add origin https://github.com/YOUR_USERNAME/portfolio.git

# Push to GitHub
git branch -M main
git push -u origin main
```

### Step 2: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click **Settings** → **Pages** (left sidebar)
3. Under "Source", select **main** branch
4. Click **Save**
5. Your site will be live at: `https://YOUR_USERNAME.github.io/portfolio/`

**Pro Tip**: For a cleaner URL, name your repository `YOUR_USERNAME.github.io` and it will be accessible at `https://YOUR_USERNAME.github.io`

## 🔧 Customization

### Adding Your Photo

1. Add your photo to the `assets/` folder
2. Update line 177 in `index.html`:
   ```html
   <img src="assets/your-photo.jpg" alt="Raj Kumar Konka">
   ```

### Updating Project Images

1. Add project screenshots to `assets/` folder
2. Update the `src` attributes in the project cards (lines 434, 457, 480, 503 in `index.html`)

### Changing Colors

Edit the CSS variables in `styles.css` (lines 7-16):

```css
:root {
    --primary: #00d4ff;        /* Main accent color */
    --secondary: #7b2cbf;      /* Secondary accent */
    --background: #0a0a0f;     /* Background color */
    --surface: #1a1a2e;        /* Card/section background */
    /* ... more colors */
}
```

### Adding More Sections

To add a new section:

1. Add section to `index.html` following the existing pattern
2. Add styling in `styles.css`
3. Update navigation in the navbar

## 📱 Responsive Breakpoints

- **Desktop**: 1200px and above
- **Tablet**: 968px - 1199px
- **Mobile**: 640px - 967px
- **Small Mobile**: Below 640px

## ⚡ Performance Tips

- Images are lazy-loaded for better performance
- CSS and JS are minified for production (use build tools)
- Uses modern CSS Grid and Flexbox for layouts
- Optimized animations using CSS transforms

## 🌟 Optional Enhancements

### Add a Contact Form

You can integrate with services like:
- **Formspree**: https://formspree.io/
- **Netlify Forms**: https://www.netlify.com/products/forms/
- **EmailJS**: https://www.emailjs.com/

### Add Analytics

Add Google Analytics to track visitors:

```html
<!-- Add before closing </head> tag -->
<script async src="https://www.googletagmanager.com/gtag/js?id=YOUR-GA-ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'YOUR-GA-ID');
</script>
```

### Custom Domain

To use a custom domain with GitHub Pages:

1. Buy a domain (e.g., rajkonka.com)
2. Create a `CNAME` file in your repository with your domain
3. Configure DNS records with your domain provider
4. Update GitHub Pages settings

## 🐛 Troubleshooting

### Images Not Loading

- Check file paths are correct
- Ensure images are in the `assets/` folder
- Verify image names match exactly (case-sensitive)

### GitHub Pages Not Working

- Make sure repository is public
- Check that GitHub Pages is enabled in settings
- Verify branch name is correct (main or master)
- Wait 5-10 minutes after enabling Pages

### Mobile Menu Not Working

- Check JavaScript file is linked correctly
- Open browser console for error messages
- Ensure all closing tags are present

## 📄 License

This project is open source and available under the MIT License.

## 📞 Contact

**Raj Kumar Konka**
- Email: konkarajkumar74@gmail.com
- LinkedIn: [linkedin.com/in/rajkumark1](https://www.linkedin.com/in/rajkumark1/)
- GitHub: [github.com/RajKonka](https://github.com/RajKonka)

---

**Built with ❤️ by Raj Kumar Konka**

*Last Updated: February 2026*
