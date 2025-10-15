# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is a personal e-portfolio website for David Mobolaji Abiodun, documenting his MSc in Enterprise IT Management at the University of Essex. The portfolio is a static website hosted on GitHub Pages, built with HTML, CSS, and Jekyll configuration.

## Project Structure

The repository follows a content-centric structure:

- **Root HTML files**: Main navigation pages ([index.html](index.html), [cv.html](cv.html), [university-of-essex.html](university-of-essex.html), Module1-6.html)
- **[style.css](style.css)**: Centralized stylesheet with CSS custom properties for theming
- **[assets/](assets/)**: Background images (drone photography) used across pages
- **[projects/](projects/)**: Organized by module, containing assignments, presentations, code exercises, and reports
- **Certs/**: Professional certifications
- **Risk/**: Risk management materials

### Module Organization

The portfolio documents 6 modules of the MSc program:
1. Launching into Enterprise IT Management (Merit)
2. Security and Risk Management (Distinction)
3. Information Technology Service Management (Distinction)
4. Enterprise IT Project Management (Distinction)
5. Into Data Science (Distinction)
6. Cloud Operations and Management (In Progress)

Each module has:
- A root-level HTML file (e.g., Module1.html) with unit-by-unit structure
- A corresponding projects/Module N/ directory with deliverables
- Consistent navigation linking between modules

## Styling Architecture

The codebase uses a unified styling approach across all pages:

### CSS Variables (defined in style.css and inline styles)
- `--bg-img`: Background image (easily swappable)
- `--text`, `--accent`, `--highlight`, `--success`: Color scheme
- `--card-bg`, `--overlay`, `--rule`: Layout elements

### Key CSS Classes
- `.overlay`: Full-viewport dark background overlay
- `.content`: Main content card with backdrop
- `.unit-title`: Yellow, bold unit headings
- `.activity`: Orange, bold activity/section headings
- `.reflection`: Italic body text for reflective writing
- `.grade`: Green, bold grade display
- `.reading-title`: Underlined reading section headers
- `.bottom-links`: Navigation footer

### Design Pattern
All pages follow the same structure:
1. Full-screen background image (drone photography)
2. Dark overlay (rgba(0, 0, 0, 0.7))
3. Semi-transparent content card
4. Bottom navigation links

## Common Development Tasks

### Updating Module Content
Module pages follow a strict unit-based structure. Each unit contains:
- Unit title (`.unit-title` class, yellow)
- Required/Additional Reading sections
- Activities with links to assignments
- Inline grades where applicable

### Adding New Projects
Projects are organized in [projects/](projects/) subdirectories by module. When adding new project files:
- Place in appropriate Module N/ folder
- Link from the corresponding ModuleN.html page
- Use relative paths for all internal links

### Modifying Styling
The design uses a dark theme with high contrast. When making style changes:
- Prefer editing [style.css](style.css) CSS variables for global changes
- Each module page has inline `<style>` blocks that can override defaults
- Background images are specified per-page via inline styles or CSS variables
- Maintain color consistency: yellow for titles, orange for activities, green for grades

### Jekyll Configuration
The site uses GitHub Pages with Jekyll theme "minimal" ([_config.yml](_config.yml:5)):
- Title: "David Mobolaji Abiodun"
- Theme is set but heavily overridden by custom CSS

## Navigation Structure

The navigation is hierarchical:
- [index.html](index.html) → Landing page with intro
- [university-of-essex.html](university-of-essex.html) → Module overview with grades
- Module1-6.html → Detailed unit breakdowns
- projects/Module N/ → Assignments and deliverables
- Bottom links on each page provide cross-navigation

All navigation uses text links styled with white text and hover effects (no button elements).

## Git Workflow

Recent commits show incremental updates to Module6.html and project files. The repository:
- Uses simple commit messages (e.g., "Update Module6.html")
- Main branch: `main`
- Clean working tree (no uncommitted changes at conversation start)

## Content Maintenance Notes

### Module Pages
- Units are numbered sequentially within each module
- Each unit includes required reading citations
- Activities link to external course platform (my-course.co.uk) or local project files
- Grades are displayed inline as `<span class="grade">(Grade: Distinction)</span>`

### Academic Content
The portfolio contains:
- Collaborative discussion posts
- Individual presentations and assignments
- Python programming exercises ([projects/Module 1/Program/](projects/Module 1/Program/))
- Jupyter notebooks for data science work ([projects/Think Bayes/](projects/Think Bayes/))
- BPMN/UML diagrams
- Risk management reports
- Cloud architecture diagrams

When working with academic content, maintain the reflective and professional tone established throughout the portfolio.
