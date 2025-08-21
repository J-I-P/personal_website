# Personal Website - Static HTML/CSS Portfolio

William Lee's personal portfolio website built with pure HTML, CSS, and external assets. This is a static website with no build system, dependencies, or compilation steps required.

Always reference these instructions first and fallback to search or bash commands only when you encounter unexpected information that does not match the info here.

## Working Effectively

### Setup and Serving
- **No installation required** - This is a static HTML/CSS website with no dependencies
- **Clone and serve immediately**:
  - `python3 -m http.server 8000` -- Starts immediately (< 1 second). NEVER CANCEL.
  - Alternative: `npx serve . -p 8001` -- Takes ~2 seconds to start. NEVER CANCEL.
- **Access website**: Open `http://localhost:8000` or `http://localhost:8001` in browser
- **Stop server**: `Ctrl+C` or `pkill -f "python3 -m http.server"`

### Development Workflow
- **Edit files directly**: No compilation step needed
- **See changes**: Refresh browser after editing HTML/CSS files
- **File structure**:
  - `index.html` - Main page content and structure
  - `style.css` - Custom styling and layout
  - `reset.css` - CSS reset (Eric Meyer's reset v2.0)
  - `README.md` - Basic project readme

## Validation

### HTML Validation
- **Command**: `npx htmlhint *.html` -- Takes ~2 seconds. NEVER CANCEL. Set timeout to 30+ seconds.
- **Known issues**: The current HTML has 2 syntax errors (unmatched `</ul>` tag on line 55) but the website functions correctly
- **Expected output**: Reports tag-pair errors but website still works in browsers

### CSS Validation  
- **Syntax check**: CSS has balanced braces and valid syntax
- **Manual validation**: Verify styles apply correctly by viewing website in browser
- **No CSS linter configured** - stylelint requires configuration not present in this repository

### Browser Testing
- **ALWAYS test manually after changes**: Load `http://localhost:8000` in browser
- **Verification checklist**:
  - Header navigation displays "WILLIAM LEE", "BASED IN TAIWAN", etc.
  - Banner section shows William's intro and image
  - Introduction section with sparkle images
  - About cards (01-04: Attention to Detail, Adaptability, Problem Solver, Team Player)
  - Contact section with social links
  - Projects section with portfolio items
  - Footer with copyright notice
- **External resources**: Images from GitHub and Google Fonts may be blocked in restricted environments but local CSS styling will work

### End-to-End Validation Scenarios
- **Basic functionality test**:
  1. Start server: `python3 -m http.server 8000`
  2. Open `http://localhost:8000` in browser
  3. Verify all sections render correctly
  4. Test responsive layout by resizing browser window
  5. Hover over "CONTACT ME" links to verify hover effects work
  6. Check browser console for any JavaScript errors (none expected)

## Common Tasks

### Repository Structure
```
.
├── .git/                 # Git repository
├── .github/             # GitHub configuration (created for instructions)
├── README.md            # Basic project description
├── index.html           # Main website file (6,084 bytes)
├── reset.css            # CSS reset file (1,107 bytes)
└── style.css            # Custom styles (3,500 bytes)
```

### Key Files Content
- **index.html**: Single-page portfolio with sections for header, banner, intro, about, contact, projects, footer
- **style.css**: Custom CSS with responsive layout, grid system (max-width: 1296px), color scheme (black/white/#00ffa3)
- **reset.css**: Eric Meyer's CSS Reset v2.0 for cross-browser consistency

### External Dependencies
- **Google Fonts**: Bruno Ace SC font family (loaded via CDN)
- **Images**: Portfolio and decoration images hosted on GitHub (hexschool training materials)
- **No JavaScript**: Pure HTML/CSS implementation
- **No build tools**: No Node.js, webpack, or other build system

## Technology Stack
- **Frontend**: HTML5, CSS3
- **Fonts**: Google Fonts (Bruno Ace SC)
- **Images**: External GitHub-hosted assets
- **Server**: Any static file server (Python SimpleHTTPServer, npx serve, nginx, etc.)
- **Browser support**: Modern browsers with CSS Grid and Flexbox support

## Performance and Timing
- **Server startup**: < 1 second (Python) or ~2 seconds (npx serve)
- **HTML validation**: ~2 seconds
- **Page load**: Instant for local files, external resources depend on network
- **No build time**: Changes are immediately visible on refresh

## Notes for Developers
- **HTML syntax**: Contains known but non-breaking errors (unmatched ul tag)
- **Images**: External resources may fail in restricted networks but layout remains intact
- **Responsive**: Uses CSS Grid and Flexbox for responsive design
- **Color scheme**: Black background (#000), white text (#fff), green accent (#00ffa3)
- **Typography**: Large heading fonts (128px, 64px, 40px) with Bruno Ace SC family