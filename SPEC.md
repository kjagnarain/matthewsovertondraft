# SPEC.md — Matthews Overton Page Redesign

## Objective
Redesign the existing `index-8.html` (Matthews Overton Birmingham economic development page) to visually match the aesthetic, colors, typography, and layout patterns of https://www.overton.ventures.

## Reference Design Analysis (overton.ventures)

### Color Palette
- **Background**: Off-white / warm cream `#f6f4f0` (or very close)
- **Text**: Near-black `#1a1a1a` or `#111111`
- **Footer**: Pure black `#000000` with white text
- **Cards/Overlays**: Dark/black with white text for work items
- **Rules/Dividers**: Thin black lines (`1px solid #000` or similar)
- **No accent colors**: Monochromatic palette (remove the clay/rust accent)

### Typography
- **Headlines**: Elegant, high-contrast serif font — use **Cormorant Garamond** or **Playfair Display** from Google Fonts. Very large sizes (60px–110px+), tight letter-spacing (`-0.02em`), light to regular weight.
- **Body**: Clean, modern sans-serif — **Inter** or similar. Size 16–18px, line-height 1.5–1.6.
- **Labels/Eyebrows**: Sans-serif, uppercase, small (11–12px), wide letter-spacing (`0.15em–0.22em`), often with a thin horizontal rule above or beside.
- **Section titles**: Large serif, sentence case, sometimes with italic emphasis on key words.

### Layout Patterns
1. **Hero**: Full-viewport height (or nearly), with dark background (can be solid dark `#1a1a1a` or near-black since no video is available), white text, large serif headline at bottom-left, eyebrow label above it. Navigation is minimal, transparent, white text over dark hero.
2. **Introduction sections**: Two-column editorial layout — small eyebrow/label on left, large serif text on right. Asymmetric.
3. **Work/Content cards**: Full-width cards with dark background and white text overlay, or image backgrounds with dark gradient overlay. Grid of 2 columns.
4. **Theory/Approach sections**: Clean off-white background, large serif heading left, content right with thin horizontal rules as dividers between items.
5. **Connect/Contact**: Off-white background, two-column — label on left, large serif CTA + email on right.
6. **Footer**: Pure black background, white logo left, white nav links right, small copyright text at bottom center.

### Navigation
- Minimal: Logo (stylized mark) on left, links centered or right
- Transparent over hero, becomes solid on scroll (optional)
- Links: uppercase or title case, clean sans-serif

### Other Details
- Generous whitespace — sections are spacious
- Thin horizontal rules (1px black) as section dividers and within content
- No box shadows, no gradients (except photo overlays)
- Very editorial, magazine-like feel

---

## Implementation Requirements

### Source Files
- **Input HTML**: `/mnt/agents/upload/index-8.html`
- **Grant Image**: `/mnt/agents/upload/grant.jpg`

### Output
- Single redesigned HTML file: `/mnt/agents/output/index.html`
- Grant image should be referenced properly (can be copied to output or referenced via relative path)

### Content Preservation
Keep ALL existing content from `index-8.html`:
- Matthews Overton branding and messaging
- All sections: Hero/Intro, Practice, Scale, Focus, Approach, Principal, Contact
- All text about Grant Brigham, scale numbers, focus areas, approach commitments
- All contact information (emails, phone, office location)
- Footer copyright

### Specific Redesign Tasks

1. **Color System**
   - Replace warm paper/clay palette with overton.ventures monochromatic scheme
   - Background: `#f6f4f0` (warm off-white)
   - Text: `#111111`
   - Muted text: `rgba(0,0,0,0.5)` or `#666`
   - Footer: `#000000`
   - Remove `--clay` accent entirely (or make it near-black)

2. **Typography**
   - Replace Fraunces with **Cormorant Garamond** (Google Fonts)
   - Replace DM Sans with **Inter** (Google Fonts)
   - Headlines: Cormorant Garamond, weight 300–400, sizes 40px–80px+, tight line-height
   - Body: Inter, weight 400, 16px
   - Labels: Inter, uppercase, 11px, letter-spacing 0.18em

3. **Hero Section**
   - Dark background (`#1a1a1a` or `#111`) filling full viewport height
   - White text
   - Eyebrow label: small, uppercase, with thin rule above
   - Large serif headline at bottom-left: "Patient capital for Birmingham's next chapter."
   - Navigation transparent over hero, white text, minimal
   - Remove the "No. 01 — Birmingham Office" floating stamp

4. **Navigation**
   - White over hero, dark when scrolled past hero
   - Minimal links: Practice, Scale, Focus, Approach, Principal, Contact
   - Logo: "Matthews Overton" in serif, simplified mark
   - Remove dot accent, keep it minimal

5. **Section Layouts**
   - Each section should have thin top border (`1px solid #000` or `rgba(0,0,0,0.15)`)
   - Section headers: eyebrow label left (small, uppercase), large serif title right — TWO COLUMN
   - Remove the § numbering style, use simple labels
   - Content areas: two-column editorial layouts

6. **About/Practice Section**
   - Two-column: label "About" on left with rule above, body text on right
   - Body in clean sans-serif, not serif
   - Remove drop caps styling

7. **Scale Section**
   - Redesign to be more like overton's "Theory of Change" section
   - Three stats in a row with thin rules
   - Large serif numbers, uppercase sans labels
   - Clean horizontal layout with dividers

8. **Focus/Pillars Section**
   - Convert from 3-column grid to a more editorial layout
   - Could use a 2-column card grid with thin borders
   - Or keep 3-column but with cleaner styling (no clay color)

9. **Approach Section**
   - Similar to overton's ENVision/Build/Invest layout
   - Large serif heading left, content blocks on right with thin rule dividers
   - Numbered items with uppercase labels

10. **Principal Section**
    - Two-column: Grant's photo on left, bio on right
    - Use the actual grant.jpg image (provided at `/mnt/agents/upload/grant.jpg`)
    - Photo should be aspect-ratio 4:5, grayscale or natural (clean editorial look)
    - Bio heading in large serif
    - Contact meta below with thin rules
    - Remove placeholder text about bio

11. **Contact Section**
    - Two-column editorial: label left, large serif CTA right
    - Email prominently displayed as underlined link
    - Clean, minimal

12. **Footer**
    - Pure black background (`#000`)
    - White text
    - Logo/mark on left
    - Nav links on right
    - Copyright at bottom center, small, uppercase, wide letter-spacing

13. **Animations**
    - Keep subtle scroll reveal animations
    - Simplify entrance animations to be more understated
    - No flashy effects — understated and elegant

### Technical Requirements
- Single self-contained HTML file (inline CSS and JS, or `<style>`/`<script>` tags)
- Responsive design (mobile breakpoints at 720px and 900px)
- Google Fonts loaded via `<link>`
- Grant image referenced with relative path (`./grant.jpg`)
- Smooth scrolling

### Quality Standards
- Must look editorial, magazine-like, and premium
- Must feel visually related to overton.ventures
- Typography must be elegant and well-proportioned
- Whitespace must be generous
- Mobile responsive must work well
