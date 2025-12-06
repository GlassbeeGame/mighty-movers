# Service Pages Template

This directory contains the service detail pages for the Mighty Movers website.

## Template File

**`_service-page-template.astro`** - Use this as a starting point for all new service pages.

## How to Create a New Service Page

### Step 1: Copy the Template
```bash
cp src/pages/services/_service-page-template.astro src/pages/services/your-service-name.astro
```

### Step 2: Update the Layout Props
```astro
<Layout
  title="Your Service Name Services"
  description="SEO-friendly description of your service"
>
```

### Step 3: Customize the Content
Replace all `[Placeholder...]` text with your actual content:

- **Hero Section**
  - Update `hero-badge` text (e.g., "Commercial Moving")
  - Replace hero title and description
  - Optionally change the `hero-image` background URL

- **Main Content**
  - Section header with title and description
  - 3 content cards with titles and paragraphs
  - 4 feature cards with icons, titles, and descriptions
  - FAQ section with 5 questions and answers

- **Sidebar**
  - 2 CTA cards with titles, descriptions, and button text
  - 2 info cards with headings and content

- **Bottom CTA**
  - Heading, description, and button labels

### Step 4: Add to Services Page

Add your new service to `/src/pages/services.astro` as a clickable card:

```astro
<a href="/services/your-service-name" class="service-large service-link">
  <div class="service-number">08</div>
  <div class="service-content">
    <h2>Your Service Name</h2>
    <p class="service-intro">Brief description of the service</p>
    <div class="service-features">
      <div class="feature-item">✓ Feature 1</div>
      <div class="feature-item">✓ Feature 2</div>
      <div class="feature-item">✓ Feature 3</div>
      <div class="feature-item">✓ Feature 4</div>
      <div class="feature-item">✓ Feature 5</div>
      <div class="feature-item">✓ Feature 6</div>
    </div>
  </div>
</a>
```

## Existing Service Pages

- **local-moving.astro** - Local moving services (template example)

## Design Features

All service pages include:

- ✅ Responsive design (mobile, tablet, desktop)
- ✅ Interactive FAQ dropdowns (accordion-style)
- ✅ Sticky sidebar on desktop
- ✅ Bottom CTA section
- ✅ Black/yellow/white artistic design system
- ✅ Hover effects with yellow glow
- ✅ Angled corners and clip-paths
- ✅ Smooth animations and transitions

## Hero Image Options

Popular Unsplash images for moving services:

- **General Moving**: `photo-1600880292203-757bb62b4baf`
- **Boxes/Packing**: `photo-1600880292089-90a7e086ee0c`
- **Moving Truck**: `photo-1464207687429-7505649dae38`
- **Office/Commercial**: `photo-1497366216548-37526070297c`
- **Storage**: `photo-1600585152220-90363fe7e115`

Usage:
```css
background: url('https://images.unsplash.com/photo-ID?w=1920&q=80') center/cover no-repeat;
```

## Questions?

The template includes detailed comments at the top explaining the structure and customization points.
