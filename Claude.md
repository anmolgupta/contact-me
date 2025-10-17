# Digital Visiting Card Project

## Project Overview
This repository contains a single-page digital visiting card implemented as a responsive HTML page with embedded CSS. The visiting card adapts its layout based on the viewing device - displaying horizontally on desktop screens and vertically on mobile devices.

## Technical Requirements

### File Structure
- **index.html**: Single HTML file containing all markup and styles
- **No external dependencies**: Self-contained HTML with embedded CSS
- **No inline styles**: All styling done through CSS classes

### Layout Specifications

#### Desktop View (e768px width)
- **Orientation**: Horizontal layout
- **Grid Structure**: CSS Grid with multiple columns
- **Component Arrangement**: Side-by-side placement of card sections
- **Visual Flow**: Left-to-right reading pattern

#### Mobile View (<768px width)
- **Orientation**: Vertical layout
- **Grid Structure**: CSS Grid with single column
- **Component Arrangement**: Stacked sections
- **Visual Flow**: Top-to-bottom scrolling

### Component Structure
The visiting card includes the following sections:
1. **Profile Section**: Photo/avatar and primary identification
2. **Name & Title**: Full name and professional title/role
3. **Contact Information**: Email, phone, location
4. **Social Links**: Professional social media profiles
5. **Bio Section**: Brief professional summary
6. **Skills/Expertise**: Key competencies (optional)
7. **CTA Section**: Call-to-action buttons (contact, download vCard, etc.)

### CSS Architecture

#### Naming Convention
- Use BEM-inspired class naming: `.card`, `.card__header`, `.card__content`
- Semantic class names that describe purpose, not appearance
- Prefix utility classes with `u-`: `.u-text-center`, `.u-margin-top`

#### Grid System
```css
/* Desktop: Multi-column grid */
.card {
  display: grid;
  grid-template-columns: 1fr 2fr;
  gap: 2rem;
}

/* Mobile: Single column */
@media (max-width: 767px) {
  .card {
    grid-template-columns: 1fr;
  }
}
```

#### Responsive Breakpoints
- **Mobile First Approach**
- Primary breakpoint: 768px
- Optional tablet breakpoint: 1024px for fine-tuning

### Design Principles
1. **Clean and Professional**: Minimalist design with clear typography
2. **Accessibility**: Semantic HTML, proper contrast ratios, keyboard navigation
3. **Performance**: Optimized CSS, minimal file size
4. **Cross-browser Compatible**: Works on modern browsers
5. **Print-friendly**: Optional print styles for physical cards

### Color Scheme Guidelines
- Primary color for headings and CTAs
- Secondary color for accents
- Neutral colors for text and backgrounds
- Sufficient contrast for accessibility (WCAG AA standard)

### Typography
- System font stack for fast loading
- Clear hierarchy with distinct heading sizes
- Readable body text (16px minimum)
- Consistent line-height and spacing

## Development Notes

### CSS Variables
Use CSS custom properties for maintainable theming:
```css
:root {
  --color-primary: #2563eb;
  --color-text: #1f2937;
  --spacing-unit: 1rem;
  --max-width: 1200px;
}
```

### Testing Checklist
- [ ] Responsive layout works at all viewport sizes
- [ ] No horizontal scroll on mobile
- [ ] All text is readable
- [ ] Links and buttons are easily clickable
- [ ] Images load properly and are optimized
- [ ] Print layout is clean and usable

## Future Enhancements (Optional)
- Dark mode toggle
- Animated transitions
- vCard download functionality
- QR code for easy sharing
- Multiple theme variations
- follow KISS principal while designing UX