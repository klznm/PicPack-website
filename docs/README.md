# RePack Website - GitHub Pages Setup Guide

This folder contains the website files for RePack, including the landing page, privacy policy, and terms of service.

## 📋 Before You Deploy - Replace Placeholders

**IMPORTANT:** Before deploying to GitHub Pages, you MUST replace these placeholders:

### In `index.html`:
- [ ] Line 251: Replace `href="#"` with your actual Play Store URL
- [ ] Line 268: Replace `TODO_REPLACE_WITH_YOUR_EMAIL@gmail.com` with your support email
- [ ] Line 270: Replace `Developer Name` with your actual name

### In `privacy-policy.html`:
- [ ] Line 25: Update `Last updated` date to current date
- [ ] Line 112: Replace `TODO_REPLACE_WITH_YOUR_EMAIL@gmail.com` with your support email

### In `terms.html`:
- [ ] Line 25: Update `Last updated` date to current date
- [ ] Line 82: Replace `Developer Name` with your name (appears multiple times)
- [ ] Line 126: Replace `[Your Country/State]` with your jurisdiction
- [ ] Line 145: Replace `TODO_REPLACE_WITH_YOUR_EMAIL@gmail.com` with your support email

---

## 🚀 Deployment Steps

### Step 1: Prepare Your Repository

1. **Go to your GitHub repository** (https://github.com/KaluznyM/repack)
2. Make sure you're on the `master` or `main` branch
3. Create a new commit with the `docs/` folder:

```bash
cd /mnt/d/RePack
git add docs/
git commit -m "Add website files for GitHub Pages"
git push origin master
```

### Step 2: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click **Settings** (top menu)
3. Scroll down to **Pages** (left sidebar)
4. Under **Source**, select:
   - Branch: `master` (or `main`)
   - Folder: `/docs`
5. Click **Save**

### Step 3: Wait for Deployment

- GitHub will automatically deploy your website
- This usually takes 1-5 minutes
- You'll see a message: "Your site is published at https://kaluzynym.github.io/repack/"

### Step 4: Verify Your Website

Visit these URLs to confirm everything works:

- **Landing Page:** https://kaluzynym.github.io/repack/
- **Privacy Policy:** https://kaluzynym.github.io/repack/privacy-policy.html
- **Terms:** https://kaluzynym.github.io/repack/terms.html

---

## 📱 Update Android App URLs

After your website is live, update these files in your Android app:

### `AboutFragment.kt` (lines 18-26):

```kotlin
// Replace these with your actual URLs:
private val PRIVACY_POLICY_URL = "https://kaluzynym.github.io/repack/privacy-policy.html"
private val TERMS_URL = "https://kaluzynym.github.io/repack/terms.html"
private val PLAY_STORE_URL = "https://play.google.com/store/apps/details?id=com.example.repack"
```

---

## 🎯 For Play Store Submission

When submitting RePack to Google Play Console:

1. **Privacy Policy URL:** Enter `https://kaluzynym.github.io/repack/privacy-policy.html`
2. **Website (optional):** Enter `https://kaluzynym.github.io/repack/`
3. **Support Email:** Enter the email you replaced in the HTML files

---

## 🛠️ Making Updates

To update your website after deployment:

1. Edit the HTML files in the `docs/` folder
2. Commit and push changes:

```bash
git add docs/
git commit -m "Update website content"
git push origin master
```

3. GitHub Pages will automatically redeploy (takes 1-5 minutes)

---

## ✅ Checklist Before Going Live

- [ ] Replaced ALL `TODO_REPLACE_WITH_YOUR_EMAIL` placeholders
- [ ] Replaced ALL `Developer Name` placeholders with your actual name
- [ ] Updated `Last updated` dates in Privacy Policy and Terms
- [ ] Added your Play Store URL in `index.html` (can do later)
- [ ] Tested all 3 pages load correctly
- [ ] Verified links between pages work
- [ ] Updated `AboutFragment.kt` with correct URLs

---

## 🎨 Customization (Optional)

### Change Colors

Both pages use these CSS variables (in `<style>` tags):

```css
--primary: #6750A4;        /* Purple - matches your app */
--background: #FFFBFE;     /* Off-white background */
```

You can change these to match your app's branding.

### Add Features to Landing Page

You can:
- Add screenshots of your app
- Add a demo video
- Add user testimonials
- Add download statistics

Just edit `index.html` and add content between the `<section>` tags.

---

## 📧 Need Help?

If GitHub Pages doesn't work:

1. **Check repository is public** (GitHub Pages requires public repos for free hosting)
2. **Verify branch name** (should be `master` or `main`)
3. **Check Pages settings** (Settings → Pages)
4. **Wait 5-10 minutes** for initial deployment

If you get a 404 error, make sure:
- The `docs/` folder is in the repository root
- Files are named exactly `index.html`, `privacy-policy.html`, `terms.html`

---

## 🔒 Important Notes

- **Privacy Policy is MANDATORY** for Play Store approval
- **Must be publicly accessible** before submitting to Play Store
- **Update dates** whenever you make significant changes
- **Keep URLs consistent** across app and Play Console

---

## 📂 File Structure

```
docs/
├── README.md              ← This file
├── index.html             ← Landing page (minimalist, modern)
├── privacy-policy.html    ← Privacy Policy (REQUIRED for Play Store)
└── terms.html             ← Terms of Service (recommended)
```

---

**Ready to deploy?** Follow Step 1 above! 🚀
