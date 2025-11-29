
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

