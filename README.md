# The Debug Lab

Static pages for The Debug Lab's software development and STEM workshop programs.

## Run locally

The pages fetch the shared navigation and footer at runtime, so serve the repository over HTTP instead of opening the HTML files directly.

From the repository root, run this in PowerShell:

```powershell
py -m http.server 8000
```

Then open either page:

- Software Development: <http://localhost:8000/frontend%20code/SD%20page.html>
- STEM Workshops: <http://localhost:8000/frontend%20code/STEM%20page.html>

Stop the server with `Ctrl+C`. Python 3 is required for the local server. No package installation or build step is needed.

## Tech stack

- HTML for page structure and content
- Tailwind CSS via its CDN for responsive styling
- A small shared `styles.css` file for the hero entrance animation and reduced-motion handling
- Vanilla JavaScript `fetch` for loading `nav.html` and `footer.html`
- Google Fonts Material Symbols for interface icons
- GitHub Pages for static hosting

## Project layout

```text
frontend code/
  SD page.html       Software Development page
  STEM page.html     STEM Workshops page
  nav.html           Shared responsive navigation
  footer.html        Shared contact and links footer
  styles.css         Shared animation styles
img/                 Page imagery
```

## Key decisions and assumptions

- Kept the existing page filenames and image names to avoid breaking links to the current content.
- Kept the existing page copy, program details, and contact information while improving markup and navigation behavior.
- Routed links without a dedicated destination to the contact section until their intended pages or URLs are available. Trial contact actions use the published email address.
- Used native HTML `details` elements for dropdowns and the mobile menu so they remain usable without adding a JavaScript menu dependency.
- Added a short hero entrance animation and disabled motion effects for visitors who prefer reduced motion.

## What I would improve with more time

- Confirm and wire the real destinations for events, coaches, student resources, and trial bookings.
- Replace CDN styling and fonts with locally managed, versioned assets and add a production build step.
- Extract the duplicated component-loading code into one shared script and add automated checks for broken links and missing images.
- Add browser-based checks for mobile navigation, keyboard interaction, and responsive layouts.
- Review the copy and course destinations with the Debug Lab team, and optimize image formats and sizes for faster loading.
