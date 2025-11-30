# Google AdSense Configuration Guide

This file provides instructions for adding Google AdSense ads to your Finnish Notes website.

## Current Ad Placement

Ads are configured to appear in the **right sidebar** (Table of Contents area) on desktop view.

## Setup Instructions

### 1. Apply for Google AdSense

If you don't have an AdSense account yet:
1. Visit: https://www.google.com/adsense/
2. Sign up with your Google account
3. Add your website URL: `https://chenyicheng1998.github.io/Finnish-Notes/`
4. Wait for approval (usually takes 1-2 weeks)

### 2. Get Your Ad Code

Once approved:
1. Log in to your AdSense dashboard
2. Go to **Ads** → **By ad unit** → **Display ads**
3. Create a new ad unit:
   - **Name**: Finnish Notes Sidebar
   - **Type**: Display ad
   - **Size**: Responsive (recommended for sidebar)
4. Copy the generated ad code

### 3. Add Ad Code to Website

1. Open the file: `layouts/partials/docs/toc-after.html`
2. Find the commented section with "Example AdSense code"
3. Paste your ad code in that section
4. Remove or comment out the placeholder section
5. Commit and push your changes

Example:
```html
<!-- Remove the placeholder div -->
<!-- Add your code here -->
<script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-YOUR-ID"
     crossorigin="anonymous"></script>
<ins class="adsbygoogle"
     style="display:block"
     data-ad-client="ca-pub-YOUR-ID"
     data-ad-slot="YOUR-SLOT-ID"
     data-ad-format="auto"
     data-full-width-responsive="true"></ins>
<script>
     (adsbygoogle = window.adsbygoogle || []).push({});
</script>
```

### 4. Test Your Ads

1. Push your changes to GitHub
2. Wait for GitHub Pages to rebuild (usually 1-5 minutes)
3. Visit your website
4. Check if ads are displaying correctly
5. Use browser DevTools to check for any errors

## Ad Placement Locations

Currently configured:
- ✅ Right sidebar (Table of Contents) - Desktop only

Other possible locations (not yet configured):
- ⬜ After article content
- ⬜ Before article content
- ⬜ Footer area
- ⬜ Between sections

To add ads in other locations, you can create similar files:
- `layouts/partials/docs/inject/content-after.html` - After article
- `layouts/partials/docs/inject/content-before.html` - Before article
- `layouts/partials/docs/inject/footer.html` - In footer

## Important Notes

- **Ad Policy**: Make sure your content complies with [Google AdSense Program Policies](https://support.google.com/adsense/answer/48182)
- **Mobile View**: Sidebar ads won't show on mobile (sidebar is hidden). Consider adding ads in content area for mobile users.
- **Ad Limit**: Google recommends no more than 3 ad units per page
- **Testing**: Use AdSense's ad review center to ensure ads are appropriate for your educational content

## Troubleshooting

### Ads not showing?
1. Check browser console for errors
2. Verify your AdSense account is approved
3. Check if ad code is correct
4. Wait 24-48 hours after adding code (ads may not show immediately)
5. Disable ad blockers when testing

### Need help?
- [AdSense Help Center](https://support.google.com/adsense/)
- [AdSense Community](https://support.google.com/adsense/community)

## File Locations

- Ad template: `layouts/partials/docs/toc-after.html`
- This guide: `ADSENSE_SETUP.md`
