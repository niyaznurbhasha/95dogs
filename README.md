# 95 Dogs Website

**Live at:** https://niyaznurbhasha.github.io/95dogs

This is a custom Hugo-based website with an animated landing page and navigation system.

## Features

### Landing Page Animation Sequence
1. **Initial Black Screen** (0.5 seconds)
2. **White Flash** - Brief white flash revealing the logo
3. **Full Brightness Navigation** (1 second) - The four corner words (MERCH, TOUR, FAQ, CONTACT) appear at full brightness
4. **Dimmed State** - Corner words fade to 5% opacity, logo remains fully visible

### Navigation
- **Logo Click** → Takes you to the filmmaker content showcase
- **MERCH** → Blank merch page (ready for future content)
- **TOUR** → Page displaying "95 DOGS IS NOT ON TOUR"
- **FAQ** → Frequently Asked Questions page
- **CONTACT** → Contact form page

## Setup Instructions

### 1. Logo Image
The landing page uses `/img/funny.png` as the logo. To use a different image:
- Place your logo image in the `static/img/` folder
- Update line 49 in `layouts/index.html` to point to your image:
  ```html
  <img id="logo" src="/img/YOUR_LOGO_IMAGE.png" alt="95 Dogs Logo">
  ```

### 2. Contact Form Setup
The contact form is currently set up to work with [Formspree](https://formspree.io/), a free form backend service.

**To activate the contact form:**
1. Go to [https://formspree.io/](https://formspree.io/) and create a free account
2. Create a new form and get your form endpoint
3. Open `layouts/_default/contact.html`
4. Replace `YOUR_FORM_ID` on line 118 with your actual Formspree form ID:
   ```html
   <form id="contactForm" action="https://formspree.io/f/YOUR_ACTUAL_FORM_ID" method="POST">
   ```
5. Uncomment line 136 and comment out the mock response on line 139

**Alternative:** You can use other form services like Netlify Forms, Basin, or build your own backend.

### 3. Running the Website Locally

```bash
# Start the Hugo development server
hugo server -D

# The site will be available at http://localhost:1313/
```

### 4. Building for Production

```bash
# Generate static files in the /public directory
hugo

# Deploy the contents of /public to your hosting service
```

### 5. Customization

#### Changing Colors
All pages use a black background (`#000`) with white text (`#fff`). To customize:
- Edit the CSS in each layout file under `layouts/` directory
- Main colors are defined in the `<style>` sections

#### Modifying Animation Timing
In `layouts/index.html`, you can adjust:
- Initial black screen: Line 129 - `setTimeout(..., 500)` (500ms = 0.5s)
- Navigation brightness duration: Line 143 - `setTimeout(..., 1000)` (1000ms = 1s)
- White flash duration: CSS animation on line 33

#### Adding Content
- **Videos**: Place video files in `static/videos/`
- **Images**: Place images in `static/img/`
- **New Pages**: Create a new `.md` file in `content/` and a corresponding layout in `layouts/_default/`

## File Structure

```
portfolio/
├── config.toml                 # Hugo configuration
├── layouts/
│   ├── index.html             # Landing page with animation
│   └── _default/
│       ├── merch.html         # Merch page layout
│       ├── tour.html          # Tour page layout
│       ├── faq.html           # FAQ page layout
│       ├── contact.html       # Contact form layout
│       └── content.html       # Filmmaker content showcase
├── content/
│   ├── merch.md               # Merch page content
│   ├── tour.md                # Tour page content
│   ├── faq.md                 # FAQ page content
│   ├── contact.md             # Contact page content
│   └── content.md             # Content showcase page
└── static/
    ├── img/                   # Images (including logo)
    └── videos/                # Video files
```

## Troubleshooting

**Logo not showing?**
- Make sure the image path in `layouts/index.html` matches your actual image location
- Check that the image is in the `static/img/` folder
- Try clearing your browser cache

**Videos not playing?**
- Ensure video files are in `static/videos/`
- Check that video file names match those referenced in `layouts/_default/content.html`
- Try different video formats (MP4 is most compatible)

**Contact form not sending emails?**
- Make sure you've set up Formspree or another form service
- Check that the form action URL is correct
- Look for errors in the browser console (F12)

## Support

For Hugo documentation: [https://gohugo.io/documentation/](https://gohugo.io/documentation/)

For Formspree help: [https://help.formspree.io/](https://help.formspree.io/)

