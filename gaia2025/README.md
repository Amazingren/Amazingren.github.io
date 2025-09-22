# GAIA 2025 Symposium Booklet

A professional symposium booklet for "GAIA 2025: Geospatial AI and Applications with Foundation Models", created using modern web technologies and optimized for PDF generation.

## 📁 Files Structure

```
workshop_booklet/
├── index.html          # Main HTML booklet content
├── styles.css          # Professional CSS styling  
├── generate_pdf.sh     # PDF generation script
├── generate_pdf.py     # Python PDF generation helper
├── image_setup.py      # Image management script
├── preview.py          # Browser preview script
├── README.md          # This file
├── images/            # Logo and image assets
│   ├── insait-logo.svg
│   ├── ellis-logo.svg
│   └── [other images...]
└── output/            # Generated PDF output (created automatically)
```

## 🌟 Features

- **Professional Design**: Modern, clean layout with typography optimized for print
- **Complete GAIA Content**: All symposium information, speakers, and schedule
- **Image Integration**: Support for logos, speaker photos, and venue images
- **Responsive Layout**: Works on both screen and print media
- **High-Quality PDF**: Optimized for PDF generation with proper page breaks
- **Detailed Schedule**: Complete 2-day program with times and breaks
- **Interactive Elements**: Clickable speaker links and hover effects
- **Easy Customization**: Simple HTML/CSS structure for easy modifications

## 📅 Event Details

- **Event**: GAIA 2025 Symposium - Geospatial AI and Applications with Foundation Models
- **Date**: 24-25 September 2025
- **Venue**: Grand Hotel Millennium Sofia, Bulgaria
- **Organizers**: INSAIT & ELLIS Unit Sofia
- **Website**: https://gaia.insait.ai/
- **Registration**: https://forms.gle/Lcfty4vXWoLPazDM6

## 🚀 Quick Start

### View in Browser
1. Open `index.html` in any modern web browser
2. The booklet will display with proper styling and layout

### Generate PDF

#### Method 1: Using the Script (Recommended)
```bash
cd workshop_booklet
./generate_pdf.sh
```

The script will automatically detect and use:
- Google Chrome (preferred)
- Chromium
- wkhtmltopdf (fallback)

#### Method 2: Manual Browser Print
1. Open `index.html` in Chrome/Chromium
2. Press `Ctrl+P` (or `Cmd+P` on Mac)
3. Select "Save as PDF"
4. Choose "More settings" → Set margins to "Minimum"
5. Ensure "Background graphics" is checked
6. Click "Save"

#### Method 3: Using wkhtmltopdf directly
```bash
wkhtmltopdf --page-size A4 --margin-top 0 --margin-bottom 0 --margin-left 0 --margin-right 0 index.html workshop_booklet.pdf
```

## 📝 Customization

### Adding Workshop Details
Edit the following placeholders in `index.html`:

```html
<!-- Cover page -->
<p class="date">Date: [Your Date]</p>
<p class="venue">Venue: [Your Venue]</p>
<p class="organizers">Organized by: [Your Organization]</p>

<!-- Contact information -->
<p><strong>Organizers:</strong> [Your Names]</p>
<p><strong>Email:</strong> [Your Email]</p>
<p><strong>Website:</strong> [Your Website]</p>
```

### Adding Images

The booklet supports various types of images:

#### Method 1: Use the Image Setup Script
```bash
./image_setup.py        # Setup and see requirements
./image_setup.py status # Check what's added
```

#### Method 2: Manual Addition
1. Copy images to the `images/` folder
2. Use these naming conventions:
   - **Logos**: `insait-logo.png`, `ellis-logo.png`
   - **Speakers**: `firstname-lastname.jpg` (e.g., `george-leifman.jpg`)
   - **Venue**: `venue-hotel.jpg`
   - **Banner**: `conference-banner.jpg`

#### Image Specifications
- **Logos**: PNG/SVG, transparent background, max 200x80px
- **Speaker photos**: JPG, square ratio, min 200x200px  
- **Venue images**: JPG, landscape, min 800x400px
- **File size**: Under 500KB each for best performance

### Modifying Styles
The CSS uses custom properties (CSS variables) for easy theming:

```css
:root {
    --primary-color: #2563eb;    /* Main blue color */
    --secondary-color: #1e40af;  /* Darker blue */
    --accent-color: #3b82f6;     /* Light blue */
    /* ... other variables ... */
}
```

### Adding/Removing Talks
1. Copy an existing talk section in `index.html`
2. Update the talk number, title, speaker, and content
3. Add corresponding entry in the table of contents

## 🎨 Design Features

- **Typography**: Inter font family for clean, professional text
- **Color Scheme**: Professional blue gradient with good contrast
- **Layout**: A4-optimized with proper margins and spacing
- **Print-Ready**: CSS print styles ensure colors and layout are preserved
- **Mobile-Friendly**: Responsive design works on smaller screens

## 🔧 Technical Details

### Browser Compatibility
- Chrome/Chromium (recommended for PDF generation)
- Firefox (viewing only)
- Safari (viewing only)
- Edge (viewing and PDF generation)

### Dependencies
- No external JavaScript libraries required
- Uses Google Fonts (Inter) - will fallback to system fonts if offline
- Self-contained CSS with no external dependencies

## � Booklet Contents

The booklet includes:

1. **Cover Page**: GAIA 2025 title, dates, venue, organizers
2. **Program Overview**: Complete 2-day schedule with times
3. **Detailed Schedule**: Day-by-day breakdown with coffee/lunch breaks
4. **Speaker Pages**: Each talk includes:
   - Speaker name and affiliation
   - Talk title and abstract
   - Speaker biography (where available)
   - Key projects/contributions
5. **Symposium Information**: About GAIA, contact details, registration

## 👥 Featured Speakers

The symposium features renowned experts from:
- Google Research (George Leifman)
- ServiceNow Research (Alexandre Lacoste)  
- MIT (Jeroen Audenaert)
- ETH Zurich (Thomas Zurbuchen)
- EPFL (Devis Tuia)
- QCRI/HBKU (Ferda Ofli)
- NTUA (Ioannis Papoutsis)
- Nankai University (Yimian Dai)
- MBZUAI (Salman Khan)
- TU Berlin (Begüm Demir)
- INSAIT (Danda Paudel)

## 🐛 Troubleshooting

### PDF Generation Issues
- **No PDF generator found**: Install Chrome, Chromium, or wkhtmltopdf
- **Poor print quality**: Use Chrome/Chromium for best results
- **Missing colors**: Ensure "Background graphics" is enabled
- **Page breaks**: Margins should be set to minimum in print settings

### Display Issues
- **Fonts not loading**: Check internet connection or use local fonts
- **Layout problems**: Ensure you're using a modern browser
- **Mobile display**: The design is responsive but optimized for desktop/print

## 📞 Support

For issues or questions:
1. Check this README for common solutions
2. Verify all files are in the correct location
3. Test in different browsers if having display issues
4. For PDF generation, try different methods listed above

## 📄 License

This template is provided as-is for workshop organization purposes. Feel free to modify and use for your events.