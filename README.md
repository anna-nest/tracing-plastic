# Tracing Plastic: A Scrollytelling Journey Through Waste

An interactive data visualization exploring humanity's 8.3 billion tonnes of plastic production and where it all goes.

## Overview

This scrollytelling experience transforms abstract statistics about plastic waste into personal understanding through progressive visualization. The narrative guides viewers from global production trends to individual impact, revealing the complex pathways of plastic waste through an animated alluvial diagram.

**Live Demo:** [View the story](https://anna-nest.github.io/tracing-plastic)

## Key Features

- **Progressive Data Revelation:** Scroll-triggered animations reveal data at a narrative pace
- **Custom Alluvial Diagram:** 15,000-pixel tall flow diagram showing waste pathways
- **Responsive Design:** Optimized for desktop, tablet, and mobile viewing
- **Interactive Elements:** Canvas-based particle systems, synchronized percentage animations
- **Accessibility:** No interaction required beyond scrolling

## Technical Stack

- **HTML5/CSS3** - Semantic structure and responsive layout
- **Vanilla JavaScript** - Custom scroll detection and animations
- **D3.js** - Production time-series visualization
- **Scrollama.js** - Scroll event detection and management
- **Canvas API** - Particle system rendering

## Data Sources

- OECD (2022), [Global Plastics Outlook](https://www.oecd.org/en/publications/global-plastics-outlook_de747aef-en.html)
- Historical production data (1950-2019)
- Waste management statistics (recycling, incineration, landfill, mismanagement rates)

## Project Structure

```
tracing-plastic/
├── index.html              # Main HTML structure
├── styles.css              # All styling and responsive design
├── js/
│   ├── scrollama-init.js   # Scroll detection and animations
│   ├── production-chart.js # D3.js production chart
│   └── debris-reveal.js    # Canvas particle effects
└── assets/
    ├── plastic-heap.webp   # Visual elements
    ├── heap-alluvial-combined.webp
    └── [other images]
```

## Key Technical Challenges

### 1. Alluvial Diagram Synchronization

The 15,000-pixel tall alluvial diagram required precise mathematical calculations to synchronize animated percentage numbers with diagram branch turning points across different viewport sizes.

### 2. Responsive Viewport Calculations

Maintaining consistent image aspect ratios and animation timing across mobile (400vh), tablet (900vh), and desktop (1220vh) using CSS custom properties and viewport-height-based calculations.

### 3. Percentage Animation System

Custom JavaScript extracts percentage numbers from sticky containers, converts them to absolute positioning, then animates them horizontally to align with text — all while preserving visual continuity across scroll directions.

### 4. Canvas Particle Systems

Two separate canvas layers simulate microplastic particles with irregular polygon shapes, realistic drift patterns, and performance optimization for smooth 60fps animation.

## Installation & Local Development

```bash
# Clone the repository
git clone https://github.com/anna-nest/tracing-plastic.git

# Navigate to directory
cd tracing-plastic

# Open in browser (requires local server for proper loading)
# Option 1: Python
python -m http.server 8000

# Option 2: Node.js
npx http-server

# Visit http://localhost:8000
```

## Browser Compatibility

- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+

Requires JavaScript enabled. Optimized for modern browsers with support for:

- CSS sticky positioning
- Canvas API
- ES6 JavaScript
- CSS custom properties

## Credits

Created by Anna Nesterova

Independent project developed in voluntary collaboration with the REUSE Foundation (no financial support).

## License

MIT License - feel free to use for educational purposes with attribution.

---

**Questions or feedback?** Open an issue or reach out via [contact method]
