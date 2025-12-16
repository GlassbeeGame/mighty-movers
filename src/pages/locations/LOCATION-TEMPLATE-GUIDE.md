# Location Page Template Guide

This guide explains exactly what props the `LocationTemplate` component expects when creating a new location page.

## Quick Reference: Required Props

When creating a new location page, copy from `alpine.astro` (or any working location page) and update these props:

### ✅ Required Props (Must Include)

```astro
<LocationTemplate
  title="[Location] Moving Services"
  description="Professional moving services in [Location], San Diego."
  noindex={true}
  locationBadge="[Location Name]"
  heroTitle="Professional Movers in [Location]"
  heroDescription="Reliable moving services for [Location]."
  introHeading="Moving Services in [Location]"
  introText="Mighty Movers provides professional moving services throughout [Location]."
  mainContentHeading="Professional [Location] Moving Services"
  mainContent="[Your main content paragraph here - can be multiple paragraphs separated by \n\n]"
  servicesHeading="Our Moving Services"
  services={[
    {title:"Local Moving", description:"Local services in [Location]"},
    {title:"Residential Moving", description:"Home moves throughout [Location]"},
    {title:"Commercial Moving", description:"Business moves in [Location]"},
    {title:"Packing Services", description:"Professional packing assistance"}
  ]}
  whyHeading="Why Choose Mighty Movers"
  benefits={[
    {title:"Licensed & Insured", description:"Fully licensed and insured"},
    {title:"Experienced Team", description:"Professional movers"},
    {title:"Competitive Rates", description:"Fair pricing"},
    {title:"Same-Day Service", description:"Fast service"}
  ]}
  neighborhoodsHeading="Other Areas We Serve"
  neighborhoods={[
    {title:"La Jolla", description:"Coastal moves"},
    {title:"Downtown", description:"Urban solutions"},
    {title:"Pacific Beach", description:"Beach services"},
    {title:"Del Mar", description:"North County"}
  ]}
  faqHeading="Frequently Asked Questions"
  faqs={[
    {question:"Do you serve [Location]?", answer:"Yes! We serve all of San Diego County."},
    {question:"What services?", answer:"Local moving, packing, commercial, and more."},
    {question:"Same-day service?", answer:"Yes, based on availability."},
    {question:"Licensed?", answer:"Yes, fully licensed and insured."},
    {question:"How to get quote?", answer:"Contact us by phone or website."}
  ]}
  ctaCards={[
    {title:"Get Your Free Quote", description:"Request a free quote today.", buttonText:"Get Free Quote", buttonHref:"/contact", isDark:false},
    {title:"Call Us Today", description:"Speak with a specialist.", buttonText:"(619) 555-MOVE", buttonHref:"tel:6195556683", isDark:true}
  ]}
  infoCards={[
    {title:"Service Hours", items:["Mon-Fri: 7AM-7PM", "Sat: 8AM-6PM", "Sun: 9AM-5PM", "Same-day available"]},
    {title:"Service Area", content:"Serving [Location] and San Diego County."}
  ]}
  bottomCTAHeading="Ready to Move?"
  bottomCTADescription="Get started with San Diego's trusted movers."
  bottomCTAPrimaryText="Get Free Quote"
  bottomCTAPrimaryHref="/contact"
  bottomCTASecondaryText="Call (619) 555-MOVE"
  bottomCTASecondaryHref="tel:6195556683"
/>
```

## ⚠️ Common Mistakes to Avoid

### ❌ DON'T Use These (They Don't Exist in Template):
- `contentCards` - This prop doesn't exist! Use `mainContent` instead.
- `serviceLinks` - Wrong! Use `services` instead.
- `number` field in `neighborhoods` - The template auto-generates numbers, just use `{title, description}`

### ✅ DO Use These:
- `mainContent` - Required! This is the main paragraph content.
- `mainContentHeading` - Optional heading for main content section.
- `services` - Array of `{title, description}` objects (NOT `serviceLinks` with `href`).
- `neighborhoods` - Array of `{title, description}` objects (NO `number` field).

## Prop Details

### Page Metadata
- **`title`** (string, required): Page title for SEO
- **`description`** (string, required): Meta description
- **`noindex`** (boolean, optional): Set to `true` for location pages

### Hero Section
- **`locationBadge`** (string, required): Badge text (e.g., "Alpine", "Carlsbad")
- **`heroTitle`** (string, required): Main hero heading
- **`heroDescription`** (string, required): Hero subtitle

### Intro Section
- **`introHeading`** (string, required): Section heading
- **`introText`** (string, required): Lead paragraph

### Main Content
- **`mainContentHeading`** (string, optional): Heading for main content section
- **`mainContent`** (string, optional but recommended): Main content text. Use `\n\n` to separate paragraphs.

### Services
- **`servicesHeading`** (string, required): Section heading
- **`services`** (array, optional): Array of service objects:
  ```typescript
  {title: string, description: string}
  ```

### Why Choose Us
- **`whyHeading`** (string, required): Section heading
- **`benefits`** (array, required): Array of benefit objects:
  ```typescript
  {title: string, description: string}
  ```

### Neighborhoods
- **`neighborhoodsHeading`** (string, required): Section heading
- **`neighborhoods`** (array, required): Array of neighborhood objects:
  ```typescript
  {title: string, description: string}
  ```
  ⚠️ **Note**: Do NOT include a `number` field - the template auto-generates numbers!

### FAQ
- **`faqHeading`** (string, required): Section heading
- **`faqs`** (array, required): Array of FAQ objects:
  ```typescript
  {question: string, answer: string}
  ```

### Sidebar CTAs
- **`ctaCards`** (array, optional): Array of CTA card objects:
  ```typescript
  {
    title: string,
    description: string,
    buttonText: string,
    buttonHref: string,
    isDark?: boolean
  }
  ```

### Sidebar Info Cards
- **`infoCards`** (array, optional): Array of info card objects. Each card can have:
  ```typescript
  {
    title: string,
    items?: string[],  // For list items
    content?: string    // For paragraph content
  }
  ```

### Bottom CTA
- **`bottomCTAHeading`** (string, required): CTA heading
- **`bottomCTADescription`** (string, required): CTA description
- **`bottomCTAPrimaryText`** (string, required): Primary button text
- **`bottomCTAPrimaryHref`** (string, required): Primary button link
- **`bottomCTASecondaryText`** (string, required): Secondary button text
- **`bottomCTASecondaryHref`** (string, required): Secondary button link

## Example: Creating a New Location Page

1. **Copy an existing working page** (like `alpine.astro`):
   ```bash
   cp src/pages/locations/alpine.astro src/pages/locations/your-location.astro
   ```

2. **Replace all instances of the location name** with your new location

3. **Update the mainContent** with location-specific information:
   ```astro
   mainContent="Mighty Movers San Diego provides comprehensive moving services throughout [Your Location]. Our experienced team understands the unique characteristics of this [community type] and delivers reliable, professional moving services for residential customers."
   ```

4. **Customize services** if needed (usually keep the same 4 services)

5. **Update neighborhoods** to show other areas you serve

6. **Update FAQs** to be location-specific

## Quick Checklist

Before saving your new location page, verify:

- ✅ No `contentCards` prop (doesn't exist)
- ✅ No `serviceLinks` prop (use `services` instead)
- ✅ No `number` field in `neighborhoods` array
- ✅ `mainContent` prop is included (even if optional, it's recommended)
- ✅ All required props are present
- ✅ Location name is replaced throughout
- ✅ File name matches location (e.g., `carlsbad.astro` for Carlsbad)

## Need Help?

If you're unsure about a prop, check the working examples:
- `alpine.astro` - Simple example
- `chula-vista.astro` - More detailed content example
- `la-jolla.astro` - Full-featured example

Or check the template file itself: `_location-page-template.astro` - the interface at the top shows all available props.

