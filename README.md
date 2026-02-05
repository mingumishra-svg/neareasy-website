# NearEasy Website

Landing page for NearEasy app - Hotels Near Me finder.

## Files
```
neareasy-website/
├── index.html          # Main landing page
├── privacy.html        # Privacy Policy
├── terms.html          # Terms & Conditions
├── .well-known/
│   └── assetlinks.json # Android App Links verification
└── README.md           # This file
```

## Hosting Options

### Option 1: GitHub Pages (Free)
1. Create repo: `neareasy-website`
2. Push these files
3. Settings > Pages > Enable
4. Custom domain: `neareasy.app`

### Option 2: Netlify (Free)
1. Drag & drop folder to netlify.com
2. Set custom domain: `neareasy.app`

### Option 3: Vercel (Free)
1. Import from GitHub
2. Set custom domain: `neareasy.app`

### Option 4: Firebase Hosting (Free)
```bash
npm install -g firebase-tools
firebase login
firebase init hosting
firebase deploy
```

## Domain Setup

1. **Buy domain:** neareasy.app (Google Domains, Namecheap, etc.)

2. **DNS Settings:**
   - For GitHub Pages:
     ```
     Type: A
     Host: @
     Value: 185.199.108.153
            185.199.109.153
            185.199.110.153
            185.199.111.153

     Type: CNAME
     Host: www
     Value: yourusername.github.io
     ```

   - For Netlify/Vercel: Use their provided DNS settings

## App Links Setup

### Get SHA256 Fingerprint
```bash
# For debug keystore
keytool -list -v -keystore ~/.android/debug.keystore -alias androiddebugkey -storepass android -keypass android

# For release keystore
keytool -list -v -keystore your-release-key.jks -alias your-alias
```

### Update assetlinks.json
Replace `YOUR_SHA256_FINGERPRINT_HERE` with your actual SHA256 fingerprint.

### Verify
After hosting, verify at:
https://digitalassetlinks.googleapis.com/v1/statements:list?source.web.site=https://neareasy.app&relation=delegate_permission/common.handle_all_urls

## Play Store Link
Update `index.html` with actual Play Store link once published:
```
https://play.google.com/store/apps/details?id=com.amit.nearesthotels
```

## SEO Checklist
- [x] Title tag with keywords
- [x] Meta description
- [x] Open Graph tags
- [x] Twitter Card
- [x] Structured data (JSON-LD)
- [x] Mobile responsive
- [ ] Add screenshots
- [ ] Add favicon.png
- [ ] Add og-image.png (1200x630)

## Assets Needed
1. **favicon.png** - 32x32 or 16x16
2. **og-image.png** - 1200x630 for social sharing
3. **App screenshots** - For showcase section
