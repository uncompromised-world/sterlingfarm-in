# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Static HTML website for Sterling Farm Research & Services Pvt. Ltd., an agricultural products company based in India. No build process or package manager is used.

## Development

To preview the site locally, serve the directory with any static file server:
```bash
python3 -m http.server 8000
# or
npx serve .
```

## Architecture

### Page Structure
- **Main pages**: index.html, about.html, products.html, gallery.html, contact.html
- **Product category pages**: bio_organicmanure.html, bio_pesticides.html, bio_stimulant.html, botanical_fertilizers.html, coir_products.html, control_agents.html, fertilizers.html, organic_manure.html, ready_tospray.html, soil_applications.html
- **Error pages**: 400.shtml, 401.shtml, 403.shtml, 404.shtml, 413.shtml, 500.shtml

### Assets Organization
```
assets/
├── css/style-starter.css   # Main stylesheet (includes Font Awesome 4.7)
├── js/                     # jQuery, Bootstrap, Owl Carousel, Lightbox
├── fonts/                  # FontAwesome webfonts
└── images/                 # Product photos, gallery images, logos
```

### Frontend Stack
- Bootstrap 4 (grid, navbar, components)
- jQuery 3.3.1
- Owl Carousel (homepage slider)
- Lightbox Plus jQuery (gallery)
- Font Awesome 4.7 (icons)
- Google Fonts: Poppins, Hind

### Code Patterns
- Each page duplicates the full header/navbar and footer markup
- Navigation highlights current page via inline `style="color:#007520; font-weight: bold;"`
- Product pages follow identical layout template with category-specific content

### Contact Form (contact.html)
The enquiry form at line 389 is currently non-functional:
```html
<form action="#" method="post">
```
Form fields: w3lName, w3lPhone, w3lSender (email, required), w3lSubject, w3lMessage (required)

To enable form submissions, replace `action="#"` with a backend endpoint (e.g., Formspree, Netlify Forms, or custom server).
