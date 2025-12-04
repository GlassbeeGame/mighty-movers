# Images Directory

Upload your custom images here to replace the placeholder images used throughout the site.

## Hero Images

Upload hero images (recommended size: 1920x1080 or larger) and update the following files:

### Services Page
**File:** `src/pages/services.astro`
**Line:** ~146
**Current:** `background: url('https://images.unsplash.com/photo-1600880292203-757bb62b4baf?w=1920&q=80')`
**Replace with:** `background: url('/images/hero-services.jpg')`

### Locations Page
**File:** `src/pages/locations.astro`
**Line:** ~136
**Current:** `background: url('https://images.unsplash.com/photo-1449844908441-8829872d2607?w=1920&q=80')`
**Replace with:** `background: url('/images/hero-locations.jpg')`

### About Page
**File:** `src/pages/about.astro`
**Line:** ~130
**Current:** `background: url('https://images.unsplash.com/photo-1556742049-0cfed4f6a45d?w=1920&q=80')`
**Replace with:** `background: url('/images/hero-about.jpg')`

### Contact Page
**File:** `src/pages/contact.astro`
**Line:** ~141
**Current:** `background: url('https://images.unsplash.com/photo-1516455590571-18256e5bb9ff?w=1920&q=80')`
**Replace with:** `background: url('/images/hero-contact.jpg')`

## Recommended Image Names

- `hero-services.jpg` - Services page hero image
- `hero-locations.jpg` - Locations page hero image
- `hero-about.jpg` - About page hero image
- `hero-contact.jpg` - Contact page hero image
- `logo.png` - Company logo (if needed)

## Image Optimization Tips

1. **Format:** Use JPG for photos, PNG for logos/graphics
2. **Size:** Keep file sizes under 500KB for fast loading
3. **Dimensions:** 1920x1080 minimum for hero images
4. **Compression:** Use tools like TinyPNG or ImageOptim before uploading

## How to Update

1. Upload your images to this `/public/images/` directory
2. Open the corresponding page file in `src/pages/`
3. Find the `.hero-image` background URL
4. Replace the Unsplash URL with `/images/your-image-name.jpg`
5. Save the file - changes will reflect immediately in dev mode
