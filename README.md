# PriceCompare - Grocery Price Comparison PWA

A Progressive Web App for comparing grocery prices between Coles and Foodland.

## Features

✅ **3 Smart Baskets** - Organize your shopping into Weekly Shop, Quick Essentials, and Meal Prep
✅ **Real-time Price Comparison** - See which store is cheaper instantly
✅ **Advanced Filters** - Filter by store, category (Fruit, Vegetables, Salad & Greens)
✅ **Smart Sorting** - Sort by name or price (low to high, high to low)
✅ **Savings Calculator** - Know exactly how much you save at each store
✅ **32 Products** - Real data from Coles and Foodland scrapers
✅ **Offline Support** - Works without internet after first load

## Files Included

- `price-compare-app.html` - Main application file
- `manifest.json` - PWA manifest
- `service-worker.js` - Service worker for offline support

## Converting to PWA

### Option 1: Deploy to a Web Server

1. Upload all files to your web hosting:
   - price-compare-app.html (rename to index.html)
   - manifest.json
   - service-worker.js

2. **Important**: You need HTTPS for PWA to work
   - Use services like Netlify, Vercel, GitHub Pages (all free with HTTPS)

3. Add app icons (optional but recommended):
   - Create icon-192.png (192x192 pixels)
   - Create icon-512.png (512x512 pixels)
   - Place in same directory as index.html

### Option 2: Quick Deploy with Netlify (Free)

1. Go to https://app.netlify.com/drop
2. Drag and drop all your files
3. Get instant HTTPS URL
4. Visit on mobile → "Add to Home Screen"

### Option 3: GitHub Pages (Free)

1. Create GitHub repository
2. Upload files
3. Go to Settings → Pages
4. Enable GitHub Pages
5. Visit your-username.github.io/repo-name

## Creating App Icons

Use any of these free tools:
- https://realfavicongenerator.net/
- https://www.pwabuilder.com/imageGenerator
- Canva (export as 192x192 and 512x512 PNG)

Design tips:
- Use blue theme color (#2563eb) to match app
- Simple icon works best (shopping cart, price tag, etc.)
- Transparent background or solid color

## Testing PWA Features

### On Mobile (iOS/Android):

**Android:**
1. Open in Chrome
2. Look for "Add to Home Screen" popup
3. Or tap menu → "Install app"

**iOS:**
1. Open in Safari
2. Tap Share button
3. Tap "Add to Home Screen"

### PWA Checklist:
- ✅ HTTPS enabled
- ✅ manifest.json present
- ✅ Service worker registered
- ✅ Icons included (192x192, 512x512)
- ✅ Works offline

## Local Development

To test locally with PWA features:

```bash
# Install a simple HTTPS server
npm install -g http-server

# Run with HTTPS (generates self-signed cert)
http-server -S -C cert.pem -K key.pem

# Or use Python
python3 -m http.server 8000
```

Note: Service workers require HTTPS except on localhost

## Browser Support

- ✅ Chrome (Android/Desktop)
- ✅ Safari (iOS/Mac)
- ✅ Edge (Desktop)
- ✅ Firefox (Desktop)
- ⚠️ Samsung Internet (partial)

## Data

The app currently includes 32 products with real scraped data:
- Coles: 30 products
- Foodland: 28 matched products

To add more products, edit the `parseData()` function in the HTML file.

## Customization

### Update Products:
Edit lines starting around line 100 in the HTML (inside `parseData()` function)

### Change Colors:
- Theme color: Edit `theme_color` in manifest.json
- App colors: Edit Tailwind classes in HTML

### Add Categories:
Edit the `categorizeProduct()` function around line 160

## Support

For issues or questions:
1. Check browser console for errors
2. Verify HTTPS is enabled
3. Clear browser cache and try again
4. Make sure all files are in same directory

## License

Free to use and modify for personal projects.

---

Built with React, Tailwind CSS, and Lucide Icons.
