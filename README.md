## Tech stack
- HTML for page structure and content
- Tailwind CSS for responsive styling
- A small shared `styles.css` file for the hero entrance animation and reduced-motion handling
- JavaScript `fetch` for loading `nav.html` and `footer.html`
- Google Fonts Material Symbols for interface icons
- GitHub Pages for static hosting

## Project layout

```text
frontend code
  SD page.html       Software Development page
  STEM page.html     STEM Workshops page
  nav.html           Shared responsive navigation
  footer.html        Shared contact and links footer
  styles.css         Shared animation styles
img                 Page imagery
```

## Key decisions and assumptions

- Kept the existing page filenames and image names to avoid breaking links to the current content.
- Kept the existing page copy, program details, and contact information while improving markup and navigation behavior.
- Routed links without a dedicated destination to the contact section until their intended pages or URLs are available. Trial contact actions use the published email address.
- Used native HTML `details` elements for dropdowns and the mobile menu so they remain usable without adding a JavaScript menu dependency.
- Added a short hero entrance animation and disabled motion effects for visitors who prefer reduced motion.

## What I would improve with more time

- Confirm and wire the real destinations for events, coaches, student resources and trial bookings.
- Extract the duplicated component-loading code into one shared script and add automated checks for broken links and missing images.
- Review the copy and course destinations with the Debug Lab team, and optimize image formats and sizes for faster loading.
- Use JSON to do control for those listing.
