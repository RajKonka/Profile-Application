# 🚀 Complete Deployment Guide - GitHub Pages

This guide will walk you through deploying your portfolio website to GitHub Pages step-by-step.

## 📋 Prerequisites

- [x] Git installed on your computer
- [x] GitHub account created
- [x] Personal Access Token (from earlier setup)

## 🎯 Deployment Steps

### Step 1: Prepare Your Portfolio Files

Make sure you have all these files in your portfolio folder:

```
portfolio/
├── index.html
├── styles.css
├── script.js
├── README.md
├── .gitignore
└── assets/
    └── Raj_Kumar_Konka_Resume.pdf
```

### Step 2: Navigate to Portfolio Folder

```bash
cd /Users/rajkumarkonka/Desktop/portfolio
```

Or wherever you saved the portfolio files.

### Step 3: Initialize Git Repository

```bash
# Initialize git in the portfolio folder
git init

# Check status
git status
```

You should see all your files listed as "Untracked files".

### Step 4: Add All Files

```bash
# Add all files to staging
git add .

# Verify files are staged
git status
```

Now files should show as "Changes to be committed".

### Step 5: Commit Your Files

```bash
git commit -m "Initial commit: Professional portfolio website"
```

### Step 6: Create GitHub Repository

**Option A: Create via GitHub Website**

1. Go to https://github.com/new
2. Repository name: **Choose one:**
   - `portfolio` (URL will be: username.github.io/portfolio)
   - `RajKonka.github.io` (URL will be: rajkonka.github.io) **← RECOMMENDED**
3. Description: "Professional portfolio website - Software Developer & AI/ML Engineer"
4. Select **Public**
5. **DO NOT** check "Initialize with README" (we already have one)
6. Click **Create repository**

**Option B: Create via Command Line (Advanced)**

```bash
# Install GitHub CLI if you haven't
# Then run:
gh repo create portfolio --public --source=. --remote=origin
```

### Step 7: Connect Local Repository to GitHub

After creating the repository on GitHub, you'll see setup instructions. Use these commands:

```bash
# Add remote repository
git remote add origin https://github.com/RajKonka/portfolio.git

# Or if you named it RajKonka.github.io:
git remote add origin https://github.com/RajKonka/RajKonka.github.io.git

# Verify remote was added
git remote -v
```

### Step 8: Push to GitHub

```bash
# Push to main branch
git branch -M main
git push -u origin main
```

You'll be prompted for:
- **Username**: `RajKonka`
- **Password**: Use your **Personal Access Token** (not your GitHub password)

### Step 9: Enable GitHub Pages

1. Go to your repository: `https://github.com/RajKonka/portfolio`
2. Click **Settings** (⚙️ icon)
3. Scroll down to **Pages** in the left sidebar
4. Under "Source":
   - Select branch: **main**
   - Select folder: **/ (root)**
5. Click **Save**

### Step 10: Wait for Deployment

- GitHub will show a message: "Your site is ready to be published at..."
- Wait 2-5 minutes for the first deployment
- Refresh the Settings → Pages page
- You should see: "Your site is live at https://rajkonka.github.io/portfolio/"

### Step 11: Visit Your Live Website! 🎉

Open your browser and go to:
- https://rajkonka.github.io/portfolio/ (if repo name is "portfolio")
- https://rajkonka.github.io/ (if repo name is "RajKonka.github.io")

---

## 🔄 Making Updates

After your initial deployment, use this workflow for updates:

```bash
# 1. Make changes to your files

# 2. Check what changed
git status

# 3. Add changes
git add .
# Or add specific files:
# git add index.html styles.css

# 4. Commit changes
git commit -m "Update: Description of your changes"

# 5. Push to GitHub
git push

# 6. Wait 1-2 minutes for GitHub Pages to rebuild
```

---

## 📸 Adding Your Photo

### Step 1: Add Photo to Assets Folder

```bash
# Copy your photo to the assets folder
cp ~/Desktop/your-photo.jpg /Users/rajkumarkonka/Desktop/portfolio/assets/raj-konka.jpg
```

### Step 2: Update HTML

Open `index.html` and find line ~177:

```html
<!-- Change this: -->
<img src="https://via.placeholder.com/400x500/1a1a2e/00d4ff?text=Your+Photo" alt="Raj Kumar Konka">

<!-- To this: -->
<img src="assets/raj-konka.jpg" alt="Raj Kumar Konka">
```

### Step 3: Commit and Push

```bash
git add assets/raj-konka.jpg index.html
git commit -m "Add professional photo"
git push
```

---

## 🖼️ Adding Project Screenshots

### Step 1: Add Screenshots to Assets

```bash
# Create a projects folder
mkdir -p assets/projects

# Copy your project images
cp ~/Desktop/project1.png assets/projects/
cp ~/Desktop/project2.png assets/projects/
```

### Step 2: Update Project Cards

In `index.html`, update the project image sources (lines ~434, 457, 480, 503):

```html
<!-- Change placeholder images to your screenshots -->
<img src="assets/projects/rag-chatbot.png" alt="RAG Chatbot">
<img src="assets/projects/face-recognition.png" alt="Face Recognition">
<img src="assets/projects/student-prediction.png" alt="Predictive Analytics">
<img src="assets/projects/powerball.png" alt="Powerball Analysis">
```

### Step 3: Commit and Push

```bash
git add assets/projects/
git add index.html
git commit -m "Add project screenshots"
git push
```

---

## 🎨 Customizing Your Portfolio

### Change Color Scheme

Edit `styles.css` (lines 7-16):

```css
:root {
    --primary: #00d4ff;        /* Change to your preferred color */
    --secondary: #7b2cbf;      /* Secondary color */
    --accent: #ff006e;         /* Accent color */
    /* ... */
}
```

Common color schemes:
- **Blue Tech**: `--primary: #0ea5e9;`
- **Purple Modern**: `--primary: #a855f7;`
- **Green Fresh**: `--primary: #10b981;`
- **Orange Bold**: `--primary: #f97316;`

### Add/Remove Sections

To remove a section:
1. Delete the section from `index.html`
2. Remove the corresponding nav link
3. Commit and push

To add a section:
1. Copy an existing section structure
2. Customize the content
3. Add a nav link
4. Style if needed in `styles.css`

---

## 🐛 Common Issues & Solutions

### Issue 1: "Permission denied (publickey)"

**Solution**: Use HTTPS instead of SSH:
```bash
git remote set-url origin https://github.com/RajKonka/portfolio.git
```

### Issue 2: Images Not Showing on GitHub Pages

**Solution**: Check file paths are correct and case-sensitive:
```html
<!-- Wrong (case mismatch) -->
<img src="Assets/photo.jpg">

<!-- Correct -->
<img src="assets/photo.jpg">
```

### Issue 3: Changes Not Appearing

**Solution**: 
1. Clear browser cache (Ctrl/Cmd + Shift + R)
2. Wait 2-3 minutes for GitHub Pages to rebuild
3. Check if changes were pushed: `git log`

### Issue 4: "Your site is having problems building"

**Solution**:
1. Check GitHub Pages settings
2. Look for build errors in Settings → Pages
3. Ensure all HTML tags are properly closed
4. Validate HTML at: https://validator.w3.org/

---

## 📊 Adding Analytics (Optional)

### Google Analytics

1. Create account at: https://analytics.google.com/
2. Get your Measurement ID (G-XXXXXXXXXX)
3. Add to `index.html` before `</head>`:

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-XXXXXXXXXX');
</script>
```

---

## 🌐 Custom Domain (Optional)

### Step 1: Buy a Domain

Purchase from:
- Namecheap.com
- GoDaddy.com
- Google Domains

### Step 2: Configure DNS

Add these DNS records:

```
Type: A
Host: @
Value: 185.199.108.153

Type: A
Host: @
Value: 185.199.109.153

Type: A
Host: @
Value: 185.199.110.153

Type: A
Host: @
Value: 185.199.111.153

Type: CNAME
Host: www
Value: rajkonka.github.io
```

### Step 3: Add CNAME File

Create `CNAME` file in your repository:

```bash
echo "yourdomain.com" > CNAME
git add CNAME
git commit -m "Add custom domain"
git push
```

### Step 4: Configure in GitHub

Settings → Pages → Custom domain: Enter your domain

---

## ✅ Deployment Checklist

Before going live, verify:

- [ ] All links work (test each one)
- [ ] Images load correctly
- [ ] Resume PDF is accessible
- [ ] Mobile responsive (test on phone)
- [ ] Contact information is correct
- [ ] Social links point to right profiles
- [ ] No console errors (F12 → Console)
- [ ] Spelling and grammar checked
- [ ] Meta tags are updated
- [ ] Favicon added (optional)

---

## 🎉 You're Live!

Congratulations! Your portfolio is now live on the internet.

### Share Your Portfolio:

- 📧 **Email signature**: Add your portfolio URL
- 💼 **LinkedIn**: Add to "Featured" section and contact info
- 📱 **Twitter/X**: Pin a tweet with your portfolio
- 📄 **Resume**: Add portfolio URL at the top
- 🔍 **Job applications**: Include in cover letters

### Next Steps:

1. Share on LinkedIn
2. Add to resume
3. Submit to job applications
4. Keep updating with new projects
5. Monitor analytics
6. Get feedback from peers

---

## 📞 Need Help?

If you run into issues:

1. Check this guide again
2. Search the error on Google
3. Check GitHub Pages documentation
4. Ask on GitHub Discussions
5. Reach out to me!

**Good luck! 🚀**
