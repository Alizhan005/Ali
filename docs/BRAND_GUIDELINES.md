# StudenKZ Brand Guidelines
## Kazakhstan's First Student Super-Platform

---

## 📋 Table of Contents
1. [Brand Identity](#brand-identity)
2. [Color Palette](#color-palette)
3. [Typography](#typography)
4. [Logo Usage](#logo-usage)
5. [Visual Style](#visual-style)
6. [Illustrations](#illustrations)
7. [Photography](#photography)

---

## Brand Identity

**Product Name:** StudenKZ  
**Positioning:** First Digital Super-Platform for Students in Kazakhstan  
**Tagline:** "One App. All Student Needs."

**Brand Voice:**
- Friendly and approachable
- Energetic and youthful
- Helpful and supportive
- Tech-savvy but not intimidating

**Target Audience:**
- University students in Kazakhstan (500K+ users)
- Age: 17-25 years old
- Tech-savvy Gen Z
- Budget-conscious, socially active lifestyle

---

## Color Palette

### Primary Colors

| Color | Hex Code | Usage |
|-------|----------|-------|
| **Bright Cyan** | `#1FB8CD` | Primary accent, CTAs, active states |
| **Dark Teal** | `#13343B` | Text, contrasts, headers |
| **Muted Gray-Teal** | `#5D878F` | Secondary elements, disabled states |

### Semantic Colors

| Color | Hex Code | Usage |
|-------|----------|-------|
| **Success Green** | `#34D399` | Confirmations, successful actions, positive feedback |
| **Warning Orange** | `#F59E0B` | Warnings, caution messages |
| **Error Red** | `#EF4444` | Errors, destructive actions, alerts |
| **Info Blue** | `#3B82F6` | Information, neutral notifications |

### Background Colors

| Color | Hex Code | Usage |
|-------|----------|-------|
| **Cream White** | `#FCFCF9` | Main background |
| **Pure White** | `#FFFFFF` | Cards, surfaces, elevated elements |
| **Light Gray** | `#F3F4F6` | Subtle backgrounds, dividers |

### Text Colors

| Color | Hex Code | Usage |
|-------|----------|-------|
| **Primary Text** | `#13343B` | Main content, headlines |
| **Secondary Text** | `#6B7280` | Supporting text, metadata |
| **Tertiary Text** | `#9CA3AF` | Placeholder text, disabled text |

---

## Dark Mode Palette

| Element | Hex Code |
|---------|----------|
| **Background** | `#0F1419` |
| **Surface** | `#1A1F25` |
| **Primary** | `#1FB8CD` (unchanged) |
| **Text** | `#E7EBF0` |
| **Text Secondary** | `#8B97A4` |
| **Border** | `#2F3740` |

---

## Typography

### Primary Font Family
**FK Grotesk Neue** (modern, clean grotesque)

**Fallbacks:**
```css
font-family: 'FK Grotesk Neue', 'Inter', 'SF Pro Display', 'Montserrat', -apple-system, BlinkMacSystemFont, sans-serif;
```

### Font Weights
- **Regular (400):** Body text, descriptions
- **Medium (500):** Emphasized text, labels
- **Semibold (600):** Accents, important information
- **Bold (700):** Headings, titles

### Type Scale

| Style | Size | Weight | Line Height | Letter Spacing |
|-------|------|--------|-------------|----------------|
| **H1** | 32px | 700 | 40px | -0.02em |
| **H2** | 28px | 700 | 36px | -0.02em |
| **H3** | 24px | 700 | 32px | -0.01em |
| **H4** | 20px | 600 | 28px | -0.01em |
| **H5** | 18px | 600 | 24px | 0 |
| **Body Large** | 16px | 400 | 24px | 0 |
| **Body** | 14px | 400 | 20px | 0 |
| **Body Small** | 12px | 400 | 16px | 0 |
| **Caption** | 10px | 500 | 14px | 0.02em |

### Typography Guidelines
- Headings use 700 weight with negative letter-spacing
- Body text uses 400-500 weight
- Maintain minimum 1.5 line-height for readability
- Use sentence case for most UI elements
- ALL CAPS only for small labels/badges

---

## Logo Usage

### Logo Variants
1. **Full Logo:** Icon + "StudenKZ" wordmark
2. **Icon Only:** For app icon, favicons, small spaces
3. **Wordmark Only:** For horizontal layouts

### Clear Space
Maintain minimum clear space equal to the height of the "K" in StudenKZ around the logo.

### Minimum Sizes
- Full Logo: 120px width minimum
- Icon Only: 32px × 32px minimum
- Do not compress or distort

### Color Variations
- **Primary:** Cyan logo on white/light backgrounds
- **White:** On dark backgrounds or photos
- **Dark:** Dark teal logo on light backgrounds
- **Monochrome:** For single-color applications

### Don'ts
❌ Don't rotate the logo  
❌ Don't change logo colors arbitrarily  
❌ Don't add effects (shadows, outlines, gradients)  
❌ Don't place on busy backgrounds without contrast

---

## Visual Style

### Design Principles
1. **Modern & Youthful:** Contemporary design that resonates with Gen Z
2. **Clean & Functional:** Prioritize usability over decoration
3. **Dynamic & Energetic:** Use gradients and animations to create life
4. **Accessible:** Ensure everyone can use the platform

### Design Elements

#### Border Radius
- **Small:** 8px (buttons, tags, small cards)
- **Medium:** 12px (input fields, medium cards)
- **Large:** 16px (large cards, modals)
- **Extra Large:** 24px (hero elements, special features)

#### Shadows
```css
/* Subtle */
box-shadow: 0 2px 8px rgba(0, 0, 0, 0.06);

/* Medium */
box-shadow: 0 4px 16px rgba(0, 0, 0, 0.08);

/* Strong */
box-shadow: 0 8px 24px rgba(0, 0, 0, 0.12);

/* Floating */
box-shadow: 0 12px 32px rgba(0, 0, 0, 0.16);
```

#### Gradients
```css
/* Primary Gradient (Cyan to Purple) */
background: linear-gradient(135deg, #1FB8CD 0%, #8B5CF6 100%);

/* Success Gradient */
background: linear-gradient(135deg, #34D399 0%, #10B981 100%);

/* Warm Gradient */
background: linear-gradient(135deg, #F59E0B 0%, #EF4444 100%);
```

#### Glassmorphism
```css
background: rgba(255, 255, 255, 0.8);
backdrop-filter: blur(10px);
border: 1px solid rgba(255, 255, 255, 0.2);
```

---

## Illustrations

### Illustration Style
- **Flat design** with subtle gradients
- **Friendly, youthful characters** representing students
- **Brand color palette** throughout
- **Isometric elements** for complex concepts
- **Simple, clear metaphors** for features

### Illustration Guidelines
- Use rounded shapes (avoid sharp angles)
- Include diverse student representations
- Maintain consistent character style
- Add subtle shadows for depth
- Keep backgrounds minimal

### When to Use Illustrations
- Onboarding screens
- Empty states
- Error states
- Feature explanations
- Marketing materials
- Holiday/seasonal themes

---

## Photography

### Photo Style
- **Natural lighting** with bright, warm tones
- **Real students** in authentic university settings
- **Candid moments** over posed shots
- **Diverse representation** of Kazakhstan students
- **Campus environments** recognizable to target audience

### Photo Requirements
- **Minimum resolution:** 800×800px
- **Formats:** JPG, PNG
- **Maximum size:** 5MB
- **Aspect ratios:** 
  - 1:1 for products
  - 16:9 for banners
  - 3:4 for profiles

### Photo Processing
- Slight saturation boost for vibrancy
- Soft vignette for focus
- Consistent color grading
- Optional filters (student-friendly, not excessive)

---

## Icon System

### Icon Style
- **Outline style** with 2px stroke width
- **Optional fill** for active states
- **Rounded line caps** and corners
- **Consistent visual weight**

### Icon Sizes
- **Extra Small:** 16×16px (inline icons)
- **Small:** 24×24px (UI elements)
- **Medium:** 32×32px (feature icons)
- **Large:** 48×48px (hero sections)

### Icon Library
- Primary: Lucide Icons / Heroicons
- Custom icons for unique StudenKZ features
- Maintain consistent style when creating custom icons

---

## Spacing System

```
2px  → xxs (tight elements, fine adjustments)
4px  → xs  (icon padding, tight spacing)
8px  → sm  (compact spacing, between related elements)
12px → md  (default gap, comfortable spacing)
16px → lg  (section padding, card internal padding)
24px → xl  (card padding, component separation)
32px → 2xl (section margins, large gaps)
48px → 3xl (major section separation)
64px → 4xl (hero spacing, dramatic separation)
```

### Spacing Rules
- Use multiples of 4px for consistency
- Maintain consistent spacing across similar elements
- Increase spacing for visual hierarchy
- Respect touch target minimums (44×44px)

---

## Responsive Design

### Breakpoints
- **Mobile:** 320-428px (primary focus)
- **Tablet:** 768-1024px
- **Desktop:** 1280px+ (web version)

### Mobile-First Approach
- Design for mobile first
- Scale up for larger screens
- Maintain consistent experience across devices
- Optimize touch targets for mobile

---

## Brand Assets Checklist

### Required Assets
- [ ] Logo (SVG, PNG @1x, @2x, @3x)
- [ ] App icon (multiple sizes for iOS/Android)
- [ ] Splash screen backgrounds
- [ ] Onboarding illustrations (3)
- [ ] Empty state illustrations (6+)
- [ ] Error state illustrations (4+)
- [ ] Category icons (custom set)
- [ ] Achievement badges
- [ ] Verification badges
- [ ] Social media assets

---

## Usage Guidelines

### Do's ✅
- Use brand colors consistently
- Maintain adequate contrast ratios
- Follow typography hierarchy
- Respect spacing system
- Use illustrations meaningfully
- Test designs in both light and dark modes

### Don'ts ❌
- Don't mix font families arbitrarily
- Don't use colors outside the palette
- Don't ignore accessibility guidelines
- Don't over-animate or distract users
- Don't clutter the interface
- Don't compromise usability for aesthetics

---

## Accessibility Standards

### Color Contrast
- **Normal text:** Minimum 4.5:1 contrast ratio
- **Large text:** Minimum 3:1 contrast ratio
- **UI elements:** Minimum 3:1 contrast ratio

### Additional Requirements
- Provide text alternatives for images
- Don't rely solely on color for information
- Ensure touch targets are minimum 44×44px
- Support dynamic type sizing
- Test with screen readers

---

**Version:** 1.0  
**Last Updated:** November 8, 2025  
**Contact:** Alizhan Bizhan | alizhan695@gmail.com
