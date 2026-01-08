# Mental Model Webpage Template - Implementation Plan

## Overview
Create a visually impressive, student-friendly webpage template for displaying mental model images. The template will use a cosmic/space theme inspired by the GitHub-Setup-Starmap webpage, with particle background effects, but kept simple for easy student use.

## Design Decisions

**User Requirements:**
- ✅ Particle background (tsParticles) for visual impact
- ✅ Keep it simple - no theme toggle or font toggle
- ✅ Hero/full-width image display as focal point
- ✅ Placeholder content (sample title, description, example image)
- ✅ Single content area for description
- ✅ Similar styling to GitHub-Setup-Starmap (cosmic theme, glowing effects, gradient text)

**Key Simplifications from Reference:**
- No theme toggle (dark/light) - single cosmic theme only
- No font toggle (OpenDyslexic) - accessibility via semantic HTML
- No complex navigation or nodes
- No separate JavaScript file - particle init embedded in HTML
- Focus: showcase the mental model image beautifully

## Files to Create

### 1. `index.html`
**Purpose:** Main webpage structure with placeholder content

**Key Components:**
- HTML5 doctype with responsive viewport meta tag
- Links to Google Fonts: Press Start 2P (display) and JetBrains Mono (body)
- Link to tsParticles library via CDN: `https://cdn.jsdelivr.net/npm/tsparticles@2.12.0/tsparticles.bundle.min.js`
- Link to styles.css
- Particle container div (`#tsparticles`)
- Main content sections:
  - **Hero**: Title with gradient text animation
  - **Image Section**: Full-width mental model image display
  - **Description Section**: Content area for thinking process
  - **Footer**: Simple credit line
- Embedded JavaScript for particle initialization (80 particles, stars/circles, interactive grab on hover)
- **Clear HTML comment markers** (must match README exactly):
  - Comment before `<title>` and `<h1>` to indicate these should be updated
  - `<!-- INSERT IMAGE HERE -->` comment before the `<img>` tag
  - Comment before description `<p>` to indicate this should be updated

**Placeholder Content:**
- Title: "My Mental Model - [Your Topic Here]"
- Heading: "My Mental Model Title"
- Image: `images/sample-mental-model.png`
- Description: 2 sample paragraphs explaining what should go here

### 2. `styles.css`
**Purpose:** Cosmic theme styling with easy customization

**CSS Organization (with section comments):**
1. **CSS Custom Properties (Variables)**
   - Colors: Dark backgrounds (#0a0a1a, #12122a), light text (#e8e8ff, #a8a8d8)
   - Accents: Pink (#ff6b9d), Purple (#a855f7), Cyan (#06b6d4)
   - Typography: Press Start 2P for titles, JetBrains Mono for body
   - Spacing: sm, md, lg, xl values
   - Border radius: md, lg values

2. **Base Styles**
   - Box-sizing reset
   - Smooth scrolling
   - Body background and font settings

3. **Particle Background**
   - Fixed position, full viewport
   - z-index: -1 (behind content)
   - pointer-events: none (except where interactive)

4. **Main Container**
   - Max-width: 1200px
   - Centered with auto margins
   - Responsive padding

5. **Hero Section**
   - Centered text
   - Gradient animated title (.glowing-title)
   - Animation: gradientShift 8s infinite
   - Responsive font sizing with clamp()

6. **Image Section**
   - Flexbox centering
   - Max-width: 100% for responsiveness
   - Border-radius for rounded corners
   - Glowing box-shadow (purple/pink)
   - Hover effect: scale(1.02) + enhanced glow

7. **Description Section**
   - Semi-transparent background card
   - Purple border
   - Max-width: 900px for readability
   - Centered with auto margins
   - Proper line-height for readability

8. **Footer**
   - Centered, muted text

9. **Responsive Design**
   - Mobile breakpoints: 768px, 480px
   - Reduced padding and font sizes on mobile
   - Maintains layout integrity

### 3. `images/` Folder + Placeholder
**Purpose:** Directory for student mental model images with example

**Create:**
- Folder: `images/`
- Placeholder image: `sample-mental-model.png`

**Placeholder Image Options:**
- **Option A (Recommended):** Create a simple placeholder PNG/JPG showing:
  - Dimensions: 1200x800px (16:9 aspect ratio)
  - Cosmic gradient background
  - Centered text: "Replace with Your Mental Model"
  - Some decorative shapes/nodes to suggest what a mental model looks like
- **Option B:** Simple colored rectangle with text (if image generation not available)
- **Option C:** SVG with embedded text (lightweight, scalable)

## Implementation Sequence

1. **Create `images/` folder**
   ```bash
   mkdir images
   ```

2. **Create `index.html`**
   - Full HTML5 structure
   - All CDN links (Google Fonts, tsParticles)
   - Complete particle initialization script
   - Clear TODO comments
   - Placeholder content

3. **Create `styles.css`**
   - CSS custom properties section
   - All styling sections (base, particles, hero, image, description, footer)
   - Responsive breakpoints
   - Gradient and glow animations
   - Well-commented for student understanding

4. **Create placeholder image**
   - Save as `images/sample-mental-model.png`
   - Demonstrate proper image placement and aspect ratio

## Technical Details

### tsParticles Configuration
```javascript
{
    particles: {
        number: { value: 80 },
        color: { value: ["#ffffff", "#a855f7", "#ff6b9d", "#06b6d4"] },
        shape: { type: ["circle", "star"] },
        opacity: { value: { min: 0.1, max: 0.8 }, animation: true },
        size: { value: { min: 1, max: 4 }, animation: true },
        move: { speed: 0.8, direction: "none", random: true },
        links: { enable: true, distance: 150, color: "#a855f7", opacity: 0.2 }
    },
    interactivity: {
        events: { onHover: { enable: true, mode: "grab" } },
        modes: { grab: { distance: 140 } }
    }
}
```

### Color Palette (Cosmic Theme)
- Background: `#0a0a1a` (very dark blue-black)
- Cards: `#12122a` (dark purple-blue)
- Text: `#e8e8ff` (light lavender)
- Accents: `#ff6b9d` (pink), `#a855f7` (purple), `#06b6d4` (cyan)

### Typography
- Display (titles): Press Start 2P - retro/pixel style
- Body (content): JetBrains Mono - monospace, readable

### Responsive Breakpoints
- Desktop: > 768px (full layout)
- Tablet: 481px - 768px (reduced padding)
- Mobile: ≤ 480px (smallest fonts, minimal padding)

## Alignment with README Instructions

The template MUST support these student actions from README.md:

### README Section: "1. Add Your Image"
- ✅ Students export mental model as `.png` or `.jpg`
- ✅ Students save file into `images/` folder
- **Template must have:** `images/` folder with placeholder image

### README Section: "2. Edit the HTML"
Students will:
1. ✅ **Open `index.html` in VS Code** - File must exist
2. ✅ **Update `<title>` tag and main `<h1>` header** - Add clear comments before these elements
3. ✅ **Find comment `<!-- INSERT IMAGE HERE -->`** - EXACT comment must appear before `<img>` tag
4. ✅ **Update `src` attribute of `<img>` tag** - Example in README: `<img src="images/my-diagram.png" alt="Mental Model of Systems">`
5. ✅ **Update paragraph text `<p>`** - Add clear comment before description paragraph(s)

### README Section: "3. Customize the Design (Optional)"
Students can:
- ✅ **Edit `styles.css` manually** - CSS must exist with clear organization
- ✅ **Change `background-color` in `body` selector** - CSS must have body section
- ✅ **Change font styles in `h1` or `p` selectors** - CSS must have h1 and p sections
- ✅ **Use AI to help write code** - Comments should guide what can be customized

### Critical Comment Requirements
The HTML comments must match README EXACTLY:
- Before image: `<!-- INSERT IMAGE HERE -->` (not "STUDENT TODO" or anything else)
- Other comments can be more descriptive but should guide students clearly

## Verification Steps

After implementation, verify:

1. **File Structure:**
   ```
   tier-3-template/
   ├── .gitignore
   ├── README.md
   ├── index.html          ← NEW
   ├── styles.css          ← NEW
   └── images/             ← NEW
       └── sample-mental-model.png  ← NEW
   ```

2. **Open index.html in browser:**
   - Particle background animates with stars/circles
   - Title has animated gradient effect
   - Placeholder image displays with glow effect
   - Image has hover effect (scale + glow)
   - Description section visible with sample text
   - Footer displays at bottom
   - Page is responsive (test at 375px, 768px, 1200px widths)

3. **Test Student Workflow:**
   - Find TODO markers easily in HTML
   - Change title text → reflects in browser
   - Change image src → new image displays properly
   - Change description → new text displays properly
   - Modify CSS variables → colors/fonts update

4. **Browser Console:**
   - No JavaScript errors
   - tsParticles loads successfully
   - Fonts load from Google Fonts CDN

5. **Performance:**
   - Page loads in < 2 seconds on average connection
   - Smooth particle animation (no lag)
   - Smooth hover effects

## Critical Considerations

### Accessibility
- Semantic HTML (header, main, section, footer)
- Alt text on image (with instruction to update)
- Readable font sizes and line heights
- Good color contrast (light text on dark background)
- Smooth scroll behavior

### Student-Friendliness
- Minimal files (3 files + 1 folder)
- Clear TODO markers in HTML
- No complex JavaScript editing needed
- CSS variables for easy customization
- Comments explain what each section does

### Browser Compatibility
- Modern browsers (Chrome, Firefox, Safari, Edge)
- No IE support needed (tsParticles requires modern JS)
- Fallback: if particles don't load, page still looks good

### Maintenance
- No dependencies to update (CDN links are versioned)
- Simple structure, easy to debug
- No build process required

## Potential Issues & Solutions

**Issue:** Students don't know what image dimensions to use
**Solution:** Placeholder demonstrates 16:9 ratio; could add HTML comment suggesting 1200x800px

**Issue:** Image file has spaces in name (e.g., "my model.png")
**Solution:** Placeholder uses hyphenated name as example; README could mention avoiding spaces

**Issue:** Particle background is distracting
**Solution:** Conservative opacity (0.1-0.8) and particle count (80); students can adjust in script

**Issue:** Page looks different on mobile
**Solution:** Responsive design maintains layout; test on common viewport sizes

**Issue:** Student wants different colors
**Solution:** CSS variables at top of stylesheet; add comment with alternative color schemes

## Success Criteria

Implementation is successful if:
1. ✅ Students can update content in < 5 minutes
2. ✅ Page looks impressive out-of-the-box
3. ✅ All external resources load via CDN
4. ✅ Mobile responsive (tested at 375px, 768px, 1200px)
5. ✅ Clear TODO comments guide edits
6. ✅ CSS variables enable easy customization
7. ✅ Matches README instructions exactly
8. ✅ No console errors
9. ✅ Works in modern browsers
10. ✅ Lightweight and fast

## Notes for Implementation

- Embed particle JavaScript in HTML (not separate file) for simplicity
- Use extensive HTML comments for student guidance
- CSS variables make customization accessible
- Keep particle config simple but visually impressive
- Ensure placeholder content demonstrates final result
- Test responsive design at multiple breakpoints
