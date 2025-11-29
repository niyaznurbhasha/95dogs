# Deployment Instructions for 95 Dogs Website

## GitHub Pages Setup

Your website will be live at: **https://niyaznurbhasha.github.io/95dogs**

### Step 1: Create GitHub Repository

1. Go to GitHub: https://github.com/niyaznurbhasha
2. Click the **"+"** button (top right) → **New repository**
3. Repository name: **95dogs**
4. Make it **Public**
5. **DO NOT** initialize with README (we already have files)
6. Click **Create repository**

### Step 2: Push Your Code

Open your terminal in the portfolio folder and run:

```bash
# Initialize git (if not already done)
git init

# Add all files
git add .

# Commit
git commit -m "Initial commit - 95 Dogs website"

# Add remote (replace with your actual repo URL)
git remote add origin https://github.com/niyaznurbhasha/95dogs.git

# Push to GitHub
git branch -M main
git push -u origin main
```

### Step 3: Enable GitHub Pages

1. Go to your repository: https://github.com/niyaznurbhasha/95dogs
2. Click **Settings** tab
3. Click **Pages** in the left sidebar
4. Under **Source**, select **GitHub Actions**
5. The GitHub Action will automatically build and deploy your site

### Step 4: Wait for Deployment

1. Go to the **Actions** tab in your repository
2. Watch the deployment workflow run (takes 1-2 minutes)
3. Once complete (green checkmark ✓), your site is live!

### Step 5: Visit Your Website

Open: **https://niyaznurbhasha.github.io/95dogs**

---

## Important Notes

### Logo Image
- Make sure your logo image is at `static/img/funny.png`
- Or update the path in `layouts/index.html` line 49

### Contact Form Setup
To make the contact form work:
1. Go to https://formspree.io/ and create a free account
2. Create a new form
3. Copy your form ID
4. Edit `layouts/_default/contact.html` line 118
5. Replace `YOUR_FORM_ID` with your actual Formspree form ID
6. Commit and push the changes

### Videos
Make sure all your video files are in the `static/videos/` folder:
- 01_robot1_crouchToStand_out.mp4
- 02_slowedRobotScream.mp4
- 03_gasmask_sneaking_out.mp4
- 04_dunegune_parkour_out.mp4
- 05_final_trim.mp4

---

## Making Updates

After making changes to your website:

```bash
git add .
git commit -m "Description of your changes"
git push
```

The site will automatically rebuild and deploy (takes 1-2 minutes).

---

## Troubleshooting

**Site not showing up?**
- Check the Actions tab for build errors
- Make sure GitHub Pages is set to "GitHub Actions" in Settings → Pages

**Images/videos not loading?**
- All files must be in the `static/` folder
- Check file paths are correct (case-sensitive!)

**Animation not working?**
- Clear your browser cache (Ctrl+F5 or Cmd+Shift+R)
- Make sure JavaScript is enabled

---

## Need Help?

- GitHub Pages docs: https://docs.github.com/en/pages
- Hugo docs: https://gohugo.io/documentation/
- Check the Actions tab for build logs if something goes wrong

