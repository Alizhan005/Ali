# StudenKZ Quick Reference Guide
## Essential Information at a Glance

---

## 🎨 Design Tokens

### Colors (CSS Variables)

```css
/* Primary Colors */
--primary: #1FB8CD;           /* Bright Cyan - Main accent */
--primary-dark: #13343B;      /* Dark Teal - Text & contrasts */
--accent: #5D878F;            /* Muted Gray-Teal - Secondary */

/* Semantic Colors */
--success: #34D399;           /* Green - Success states */
--warning: #F59E0B;           /* Orange - Warnings */
--error: #EF4444;             /* Red - Errors */
--info: #3B82F6;              /* Blue - Information */

/* Backgrounds */
--background: #FCFCF9;        /* Cream White - Main BG */
--surface: #FFFFFF;           /* Pure White - Cards */
--surface-gray: #F3F4F6;      /* Light Gray - Subtle BG */

/* Text */
--text-primary: #13343B;      /* Primary text */
--text-secondary: #6B7280;    /* Secondary text */
--text-tertiary: #9CA3AF;     /* Placeholder/disabled */

/* Dark Mode */
--dm-background: #0F1419;
--dm-surface: #1A1F25;
--dm-primary: #1FB8CD;
--dm-text: #E7EBF0;
--dm-text-secondary: #8B97A4;
--dm-border: #2F3740;
```

---

## 📏 Spacing Scale

```css
--space-xxs: 2px;    /* Tight elements */
--space-xs: 4px;     /* Icon padding */
--space-sm: 8px;     /* Compact spacing */
--space-md: 12px;    /* Default gap */
--space-lg: 16px;    /* Section padding */
--space-xl: 24px;    /* Card padding */
--space-2xl: 32px;   /* Section margin */
--space-3xl: 48px;   /* Large separation */
--space-4xl: 64px;   /* Hero spacing */
```

---

## 🔤 Typography

```css
/* Font Family */
font-family: 'FK Grotesk Neue', 'Inter', 'SF Pro Display', 
             'Montserrat', -apple-system, BlinkMacSystemFont, sans-serif;

/* Type Scale */
--font-h1: 32px;     /* H1: 700 weight, -0.02em spacing */
--font-h2: 28px;     /* H2: 700 weight, -0.02em spacing */
--font-h3: 24px;     /* H3: 700 weight, -0.01em spacing */
--font-h4: 20px;     /* H4: 600 weight, -0.01em spacing */
--font-h5: 18px;     /* H5: 600 weight */
--font-body-lg: 16px;    /* Body Large: 400 weight */
--font-body: 14px;       /* Body: 400 weight */
--font-body-sm: 12px;    /* Body Small: 400 weight */
--font-caption: 10px;    /* Caption: 500 weight, 0.02em */

/* Line Heights */
--line-height-tight: 1.25;
--line-height-normal: 1.5;
--line-height-loose: 1.75;
```

---

## 🔘 Border Radius

```css
--radius-sm: 8px;       /* Small elements, tags */
--radius-md: 12px;      /* Inputs, buttons */
--radius-lg: 16px;      /* Cards */
--radius-xl: 24px;      /* Modals, large cards */
--radius-full: 9999px;  /* Pills, circles */
```

---

## ⏱️ Animation Timing

```css
/* Durations */
--duration-instant: 100ms;   /* Instant feedback */
--duration-fast: 200ms;      /* Quick transitions */
--duration-normal: 300ms;    /* Standard animations */
--duration-slow: 400ms;      /* Deliberate animations */

/* Easing */
--ease-out: cubic-bezier(0.4, 0, 0.2, 1);      /* Entrances */
--ease-in: cubic-bezier(0.4, 0, 1, 1);         /* Exits */
--ease-in-out: cubic-bezier(0.4, 0, 0.6, 1);   /* Both */
```

---

## 📐 Component Sizes

### Buttons
```css
/* Small */
height: 32px;
padding: 0 16px;
font-size: 12px;

/* Medium (Default) */
height: 44px;
padding: 0 24px;
font-size: 14px;

/* Large */
height: 56px;
padding: 0 32px;
font-size: 16px;
```

### Input Fields
```css
height: 48px;
padding: 12px 16px;
border-radius: 12px;
border: 1px solid #E5E7EB;
font-size: 14px;
```

### Touch Targets
```css
min-width: 44px;
min-height: 44px;
gap: 8px; /* Between targets */
```

---

## 🎯 Shadows

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

---

## 🌈 Gradients

```css
/* Primary Gradient (Cyan → Purple) */
background: linear-gradient(135deg, #1FB8CD 0%, #8B5CF6 100%);

/* Success Gradient */
background: linear-gradient(135deg, #34D399 0%, #10B981 100%);

/* Warm Gradient (Orange → Red) */
background: linear-gradient(135deg, #F59E0B 0%, #EF4444 100%);

/* Glassmorphism */
background: rgba(255, 255, 255, 0.8);
backdrop-filter: blur(10px);
border: 1px solid rgba(255, 255, 255, 0.2);
```

---

## 📱 Breakpoints

```css
/* Mobile (Primary Focus) */
@media (min-width: 320px) and (max-width: 428px) { }

/* Tablet */
@media (min-width: 768px) and (max-width: 1024px) { }

/* Desktop */
@media (min-width: 1280px) { }
```

---

## ♿ Accessibility Standards

### Contrast Ratios (WCAG AA)
- **Normal text:** 4.5:1 minimum
- **Large text (18px+):** 3:1 minimum  
- **UI components:** 3:1 minimum

### Touch Targets
- **Minimum:** 44×44px
- **Spacing:** 8px between targets

### Focus Indicators
```css
:focus-visible {
  outline: 2px solid var(--primary);
  outline-offset: 2px;
}
```

---

## 🎬 Common Animations

### Button Press
```css
transform: scale(0.98);
transition: transform 100ms ease-out;
```

### Card Hover
```css
transform: scale(1.02) translateY(-2px);
box-shadow: 0 8px 24px rgba(0, 0, 0, 0.12);
transition: all 250ms ease-out;
```

### Page Transition
```css
/* Enter */
transform: translateX(100%);
opacity: 0;

/* Enter Active */
transform: translateX(0);
opacity: 1;
transition: all 300ms ease-out;
```

### Modal Appear
```css
@keyframes modal-scale {
  from {
    transform: scale(0.9);
    opacity: 0;
  }
  to {
    transform: scale(1);
    opacity: 1;
  }
}
animation: modal-scale 300ms ease-out;
```

---

## 🔤 Icon Sizes

```css
--icon-xs: 16px;   /* Inline icons */
--icon-sm: 24px;   /* UI elements */
--icon-md: 32px;   /* Feature icons */
--icon-lg: 48px;   /* Hero sections */
```

**Stroke Width:** 2px  
**Style:** Outline (optionally filled for active state)

---

## 👤 Avatar Sizes

```css
--avatar-xs: 24px;   /* Comments, mentions */
--avatar-sm: 32px;   /* Chat list */
--avatar-md: 48px;   /* Cards, profiles */
--avatar-lg: 64px;   /* Profile headers */
--avatar-xl: 120px;  /* Full profile */
```

---

## 🏷️ Badge Specifications

### Notification Badge
```css
min-width: 20px;
height: 20px;
padding: 0 6px;
border-radius: 10px;
background: var(--error);
color: white;
font-size: 11px;
font-weight: 600;
```

### Status Badge
```css
height: 24px;
padding: 4px 12px;
border-radius: 12px;
font-size: 11px;
font-weight: 600;
```

---

## 📊 Z-Index Scale

```css
--z-base: 0;
--z-dropdown: 1000;
--z-sticky: 1100;
--z-fixed: 1200;
--z-modal-backdrop: 1300;
--z-modal: 1400;
--z-popover: 1500;
--z-tooltip: 1600;
--z-notification: 1700;
```

---

## 🔄 Loading States

### Skeleton Loader
```css
background: linear-gradient(
  90deg,
  #f0f0f0 0%,
  #f8f8f8 50%,
  #f0f0f0 100%
);
background-size: 1000px 100%;
animation: shimmer 2s infinite;

@keyframes shimmer {
  0% { background-position: -1000px 0; }
  100% { background-position: 1000px 0; }
}
```

### Spinner
```css
width: 32px;
height: 32px;
border: 3px solid rgba(31, 184, 205, 0.2);
border-top-color: var(--primary);
border-radius: 50%;
animation: spin 800ms linear infinite;

@keyframes spin {
  to { transform: rotate(360deg); }
}
```

---

## 📝 Form Validation

### Error State
```css
border-color: var(--error);
/* + Error message below */
color: var(--error);
font-size: 11px;
```

### Success State
```css
border-color: var(--success);
/* + Checkmark icon on right */
```

### Focus State
```css
border-color: var(--primary);
box-shadow: 0 0 0 3px rgba(31, 184, 205, 0.1);
outline: none;
```

---

## 🎯 Common Patterns

### Card Pattern
```css
background: white;
border-radius: 16px;
padding: 24px;
box-shadow: 0 2px 8px rgba(0, 0, 0, 0.06);
transition: all 250ms ease-out;

/* Hover */
&:hover {
  transform: scale(1.02);
  box-shadow: 0 4px 16px rgba(0, 0, 0, 0.08);
}
```

### Input Pattern
```css
height: 48px;
padding: 12px 16px;
border-radius: 12px;
border: 1px solid #E5E7EB;
font-size: 14px;
transition: all 200ms;

&:focus {
  border-color: var(--primary);
  box-shadow: 0 0 0 3px rgba(31, 184, 205, 0.1);
}
```

### Button Pattern
```css
height: 44px;
padding: 0 24px;
border-radius: 12px;
font-size: 14px;
font-weight: 600;
transition: all 150ms;

&:active {
  transform: scale(0.98);
}
```

---

## 🌓 Dark Mode Toggle

```css
/* Light Mode (Default) */
body {
  background: var(--background);
  color: var(--text-primary);
}

/* Dark Mode */
body.dark {
  background: var(--dm-background);
  color: var(--dm-text);
}

/* Respect System Preference */
@media (prefers-color-scheme: dark) {
  body:not(.light) {
    background: var(--dm-background);
    color: var(--dm-text);
  }
}
```

---

## 🔔 Notification Types

### Toast (Top Center)
```css
max-width: 360px;
padding: 16px;
border-radius: 12px;
animation: slide-down 300ms ease-out;
/* Auto-dismiss after 3-5 seconds */
```

### Badge (Icon Overlay)
```css
position: absolute;
top: -4px;
right: -4px;
min-width: 16px;
height: 16px;
background: var(--error);
border-radius: 8px;
```

---

## 📦 Export Specifications

### Icons
- **Format:** SVG (preferred) or PNG
- **Sizes:** 16px, 24px, 32px, 48px
- **Color:** Single color (tinted via CSS)

### Images
- **Formats:** JPG (photos), PNG (graphics), WebP
- **Densities:** @1x, @2x, @3x
- **Optimization:** <200KB per image

### App Icons
- **iOS:** 180×180, 167×167, 152×152, 120×120
- **Android:** 512×512, 192×192, 144×144, 96×96
- **Format:** PNG with transparency

---

## 🚀 Performance Targets

- **App Launch:** <2s
- **Screen Navigation:** <300ms
- **API Response:** <500ms
- **Image Load:** <1s (progressive)
- **Animation FPS:** 60 FPS
- **App Size:** <50MB

---

## 📞 Quick Contacts

**Project Lead:** Alizhan Bizhan  
**Email:** alizhan695@gmail.com  
**Telegram:** @alizhan006

---

## 📚 Full Documentation

For complete specifications, see:
- [Design System Overview](./DESIGN_SYSTEM_OVERVIEW.md)
- [Brand Guidelines](./BRAND_GUIDELINES.md)
- [Component Library](./design-system/COMPONENTS.md)
- [Screen Specifications](./screens/SCREEN_SPECIFICATIONS.md)
- [UX Guidelines](./UX_GUIDELINES.md)
- [Developer Handoff](./DEVELOPER_HANDOFF.md)

---

**Version:** 1.0  
**Last Updated:** November 8, 2025
