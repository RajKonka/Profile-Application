# Raj Kumar Konka - Professional Portfolio Website

A modern, responsive portfolio website showcasing my work as a Software Developer, AI/ML Engineer, and Data Scientist.

![Portfolio Preview](https://img.shields.io/badge/Status-Live-success)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)

## 🌐 Live Website

Visit my portfolio: **https://rajkonka.github.io/Profile-Application/**

##  Features

- **Modern Design**: Clean, professional UI with smooth animations
- **Fully Responsive**: Works perfectly on desktop, tablet, and mobile devices
- **Interactive Elements**: Smooth scrolling, hover effects, and dynamic content
- **Performance Optimized**: Fast loading with optimized assets
- **Accessibility**: Semantic HTML and ARIA labels for better accessibility
- **SEO Friendly**: Meta tags and structured data for better search visibility

##  Project Structure

```
Profile-Application/
├── index.html          # Main HTML file
├── styles.css          # CSS styles and animations
├── script.js           # JavaScript for interactivity
├── README.md           # This file
├── DEPLOYMENT.md       # Detailed deployment guide
├── QUICKSTART.md       # Quick start guide
└── .gitignore          # Git ignore rules
```

##  Sections

1. **Hero/Home** - Eye-catching introduction with key stats
2. **About** - Professional summary and highlights
3. **Experience** - Timeline of work history with 4 positions
4. **Projects** - Featured projects with descriptions and tech stacks
5. **Skills** - Technical skills organized by category
6. **Contact** - Contact information and social links

## 💼 Experience Highlighted

- **Vantive Inc.** - AI/ML Engineer (Current)
- **University of Houston** - Research Assistant
- **NTT DATA** - Software Developer
- **Wipro (StackRoute)** - Data & Software Engineer

##  Featured Projects

1. **Intelligent Chatbot with RAG and LLaMA2 on AWS**
   - RAG pipeline with AWS Bedrock
   - ChromaDB for vector storage
   - Multiple LLM integration

2. **Scalable Face Recognition System on AWS Cloud**
   - Real-time face recognition
   - Auto-scaled architecture
   - ~80 seconds for 100 concurrent requests

3. **Predictive Analytics for Student Graduation**
   - Neural Networks (MLP & LSTM)
   - 85% to 92% accuracy improvement
   - SHAP interpretability

4. **Powerball Pattern Analysis & Number Generator**
   - Statistical modeling
   - 6 different generation models
   - Pattern recognition analysis

## 🛠️ Technologies Used

### Languages
- Java, Python, SQL, C++, JavaScript

### Backend & APIs
- RESTful APIs, Spring Boot, Flask, Microservices

### Frontend
- HTML5, CSS3, JavaScript, Responsive Design

### Cloud & DevOps
- AWS (EC2, S3, Lambda, RDS), Docker, Jenkins, CI/CD

### Databases
- MySQL, PostgreSQL, MongoDB, ChromaDB

### AI/ML & Data
- Machine Learning, Neural Networks, RAG Pipelines
- Kafka, Spark Streaming

### Analytics & Visualization
- Power BI, Tableau, Matplotlib, Folium

## 🔧 Local Development

### Prerequisites
- A modern web browser (Chrome, Firefox, Safari, Edge)
- Text editor (VS Code recommended)

### Running Locally

1. Clone the repository:
```bash
git clone https://github.com/RajKonka/Profile-Application.git
cd Profile-Application
```

2. Open `index.html` in your browser:
```bash
# On Mac
open index.html

# On Windows
start index.html

# On Linux
xdg-open index.html
```

That's it! No build process needed.

## 🎨 Customization

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

**Popular color schemes:**
- **Blue Tech**: `--primary: #0ea5e9;`
- **Purple Modern**: `--primary: #a855f7;`
- **Green Fresh**: `--primary: #10b981;`
- **Orange Bold**: `--primary: #f97316;`

### Adding Your Photo

1. Get a professional photo (400x500px recommended)
2. Create an `assets` folder:
   ```bash
   mkdir assets
   ```
3. Add your photo to the assets folder
4. Update line 177 in `index.html`:
   ```html
   <img src="assets/your-photo.jpg" alt="Raj Kumar Konka">
   ```

### Adding Project Screenshots

1. Create a projects subfolder:
   ```bash
   mkdir -p assets/projects
   ```
2. Add your project images
3. Update the image sources in project cards (lines ~434, 457, 480, 503):
   ```html
   <img src="assets/projects/project-name.png" alt="Project Name">
   ```

### Adding Your Resume

1. Add resume PDF to assets folder:
   ```bash
   cp ~/Desktop/your-resume.pdf assets/Raj_Kumar_Konka_Resume.pdf
   ```
2. The download button will automatically work (it's already configured in the HTML)

## 🔄 Making Updates

When you make changes to your portfolio:

```bash
# 1. Make your changes to files

# 2. Stage changes
git add .

# 3. Commit changes
git commit -m "Update: describe your changes"

# 4. Push to GitHub
git push
```

Your changes will be live on GitHub Pages in 1-2 minutes!

## 📱 Responsive Breakpoints

- **Desktop**: 1200px and above
- **Tablet**: 968px - 1199px
- **Mobile**: 640px - 967px
- **Small Mobile**: Below 640px

## ⚡ Performance Features

- Lazy-loaded images
- CSS-based animations (no heavy libraries)
- Optimized JavaScript (vanilla JS, no frameworks)
- Intersection Observer for scroll animations
- Efficient CSS Grid and Flexbox layouts

## 🌟 Optional Enhancements

### Add Contact Form

Integrate with services like:
- [Formspree](https://formspree.io/) - Free contact forms
- [Netlify Forms](https://www.netlify.com/products/forms/) - If you move to Netlify
- [EmailJS](https://www.emailjs.com/) - Send emails via JavaScript

### Add Google Analytics

Track your visitors:

```html
<!-- Add before closing </head> tag in index.html -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-XXXXXXXXXX');
</script>
```

### Custom Domain

To use a custom domain:

1. Buy a domain (Namecheap, GoDaddy, Google Domains)
2. Create a `CNAME` file in your repository:
   ```bash
   echo "yourdomain.com" > CNAME
   git add CNAME
   git commit -m "Add custom domain"
   git push
   ```
3. Configure DNS with your domain provider:
   ```
   Type: A, Host: @, Value: 185.199.108.153
   Type: A, Host: @, Value: 185.199.109.153
   Type: A, Host: @, Value: 185.199.110.153
   Type: A, Host: @, Value: 185.199.111.153
   Type: CNAME, Host: www, Value: rajkonka.github.io
   ```
4. Update GitHub Pages settings with your domain

## 🐛 Troubleshooting

### Portfolio Not Loading on GitHub Pages

**Solution:**
1. Go to Settings → Pages
2. Ensure branch is set to **main** and folder is **/ (root)**
3. Wait 2-3 minutes after enabling
4. Clear browser cache (Cmd/Ctrl + Shift + R)

### Images Not Showing

**Solution:**
- Check file paths are correct and case-sensitive
- Ensure images are in the correct folder
- Verify image file names match exactly

### Mobile Menu Not Working

**Solution:**
- Ensure `script.js` is linked correctly
- Check browser console for errors (F12)
- Verify JavaScript file is on the same branch

### Changes Not Appearing

**Solution:**
1. Verify changes were pushed: `git log`
2. Wait 2-3 minutes for GitHub Pages to rebuild
3. Clear browser cache: Cmd/Ctrl + Shift + R
4. Try incognito/private browsing mode

## 📈 Deployment Status

This portfolio is deployed using GitHub Pages and is automatically updated with each push to the main branch.

**Repository:** https://github.com/RajKonka/Profile-Application
**Live Site:** https://rajkonka.github.io/Profile-Application/

## 📄 License

This project is open source and available under the MIT License.

## 📞 Contact

**Raj Kumar Konka**

- 📧 Email: konkarajkumar74@gmail.com
- 💼 LinkedIn: [linkedin.com/in/rajkumark1](https://www.linkedin.com/in/rajkumark1/)
- 🐙 GitHub: [github.com/RajKonka](https://github.com/RajKonka)
- 📱 Phone: +1 (682) 405-3943
- 📍 Location: Houston, Texas


---

**Built with ❤️ by Raj Kumar Konka**


---

### 🌟 Star This Repository

If you found this portfolio helpful or inspiring, please give it a star! ⭐

### 🔗 Quick Links

- [View Live Site](https://rajkonka.github.io/Profile-Application/)
- [Report an Issue](https://github.com/RajKonka/Profile-Application/issues)
- [Deployment Guide](DEPLOYMENT.md)
- [Quick Start Guide](QUICKSTART.md)
