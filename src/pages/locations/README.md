# Location Pages Template

This directory contains the location detail pages for the Mighty Movers website.

## Template File

**`_location-page-template.astro`** - Use this as a starting point for all new location pages.

## How to Create a New Location Page

### Step 1: Copy the Template
```bash
cp src/pages/locations/_location-page-template.astro src/pages/locations/your-location-name.astro
```

### Step 2: Update the Layout Props
```astro
<Layout
  title="[Location Name] Moving Services"
  description="Professional moving services in [Location Name], San Diego. Local movers serving [neighborhoods] and surrounding areas."
>
```

### Step 3: Customize the Content
Replace all `[Placeholder...]` text with your actual content:

- **Hero Section**
  - Update `location-badge` text (e.g., "Pacific Beach")
  - Replace hero title and description
  - Optionally change the `hero-background` image URL

- **Main Content**
  - Intro section with title and description
  - 3 SEO content cards (100-150 words each for 500+ total)
  - Services links section (update service titles and links)
  - Why Choose Us section (4 benefit items with titles and descriptions)
  - Other Neighborhoods section (4 related neighborhoods)
  - FAQ section with 5 questions and answers

- **Sidebar**
  - 2 CTA cards with titles, descriptions, and button text
  - 2 info cards with headings and content

- **Bottom CTA**
  - Heading, description, and button labels

### Step 4: Add to Locations Page

Add your new location to `/src/pages/locations.astro` as a clickable card:

```astro
<a href="/locations/your-location-name" class="location-card location-link">
  <div class="location-icon">09</div>
  <h3>Your Location Name</h3>
  <p>Brief description of neighborhoods and areas served</p>
</a>
```

## Existing Location Pages

- **la-jolla.astro** - La Jolla location page (template example)

## Design Features

All location pages include:

- ✅ Responsive design (mobile, tablet, desktop)
- ✅ Interactive FAQ dropdowns (accordion-style)
- ✅ Sticky sidebar on desktop
- ✅ Services links section with clean list design
- ✅ SEO-focused content cards
- ✅ Bottom CTA section
- ✅ Black/yellow/white artistic design system
- ✅ Hover effects with yellow glow
- ✅ Border accents and clip-paths
- ✅ Smooth animations and transitions

## Location vs Service Pages

**Key Differences:**

| Feature | Location Pages | Service Pages |
|---------|---------------|---------------|
| Hero | Left-aligned, location badge | Centered, service badge |
| Focus | Where/neighborhoods/areas | What/how the service works |
| Content Cards | Location & area SEO content | Service features & process |
| Services Links | Clean list with arrows | Feature grid cards |
| Benefits | Location-specific advantages | Service-specific benefits |
| Neighborhoods | "Other Neighborhoods" section | N/A |

**Shared Elements:**

- FAQ structure (exact match)
- CTA buttons (exact match)
- Headers (same sizing/weight)
- Sidebar structure
- Bottom CTA section

## Hero Image Options

Popular Unsplash images for San Diego locations:

- **Beach/Coastal**: `photo-1581368087049-e82c8f0e2a6f`
- **San Diego Skyline**: `photo-1550102220-32cc085ed0eb`
- **La Jolla Cove**: `photo-1580655653885-65763b2597d0`
- **Downtown SD**: `photo-1449844908441-8829872d2607`
- **Neighborhood**: `photo-1487958449943-2429e8be8625`

Usage:
```css
background: url('https://images.unsplash.com/photo-ID?w=1920&q=80') center/cover no-repeat;
```

## SEO Best Practices

- Write 500+ words across the 3 content cards
- Include location-specific keywords naturally
- Reference local landmarks and neighborhoods
- Link to relevant service pages in the services links section
- Use location name in FAQ questions and answers
- Add schema markup for local business (future enhancement)

## Questions?

The template includes detailed comments at the top explaining the structure and customization points.
