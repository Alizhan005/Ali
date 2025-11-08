# StudenKZ Component Specifications
## UI Component Library

---

## 📋 Table of Contents
1. [Buttons](#buttons)
2. [Input Fields](#input-fields)
3. [Cards](#cards)
4. [Navigation](#navigation)
5. [Avatars](#avatars)
6. [Badges](#badges)
7. [Modals & Sheets](#modals--sheets)
8. [Notifications](#notifications)
9. [Loading States](#loading-states)
10. [Lists & Tables](#lists--tables)

---

## Buttons

### Primary Button
```css
background: linear-gradient(135deg, #1FB8CD 0%, #8B5CF6 100%);
color: #FFFFFF;
border-radius: 12px;
font-weight: 600;
text-align: center;
```

### Sizes

| Size | Height | Padding | Font Size |
|------|--------|---------|-----------|
| **Small** | 32px | 12px 16px | 12px |
| **Medium** | 44px | 12px 24px | 14px |
| **Large** | 56px | 16px 32px | 16px |

### Variants

#### Primary Button
- **Default:** Gradient background, white text
- **Hover:** Slight scale (1.02), increased shadow
- **Active:** Scale (0.98), pressed state
- **Disabled:** Opacity 0.5, no interaction
- **Loading:** Spinner replaces text, disabled state

```css
/* Default */
.btn-primary {
  background: linear-gradient(135deg, #1FB8CD 0%, #8B5CF6 100%);
  color: #FFFFFF;
  border: none;
  box-shadow: 0 4px 12px rgba(31, 184, 205, 0.3);
}

/* Hover */
.btn-primary:hover {
  transform: scale(1.02);
  box-shadow: 0 6px 16px rgba(31, 184, 205, 0.4);
}

/* Active */
.btn-primary:active {
  transform: scale(0.98);
}

/* Disabled */
.btn-primary:disabled {
  opacity: 0.5;
  cursor: not-allowed;
}
```

#### Secondary Button
- **Default:** Transparent background, primary color border and text
- **Style:** 1px solid border
- **Hover:** Light primary color background (10% opacity)

```css
.btn-secondary {
  background: transparent;
  color: #1FB8CD;
  border: 1px solid #1FB8CD;
  border-radius: 12px;
}

.btn-secondary:hover {
  background: rgba(31, 184, 205, 0.1);
}
```

#### Ghost Button
- **Default:** Transparent background, no border, primary color text
- **Hover:** Light background (5% opacity)

```css
.btn-ghost {
  background: transparent;
  color: #1FB8CD;
  border: none;
}

.btn-ghost:hover {
  background: rgba(31, 184, 205, 0.05);
}
```

#### Danger Button
- **Use:** Destructive actions (delete, cancel)
- **Style:** Red background or red outline

```css
.btn-danger {
  background: #EF4444;
  color: #FFFFFF;
  border: none;
}

.btn-danger-outline {
  background: transparent;
  color: #EF4444;
  border: 1px solid #EF4444;
}
```

### Icon Buttons
- Square or circular
- Icon only, no text
- Size: 40×40px (medium), 32×32px (small), 48×48px (large)
- Icon size: 20×20px (medium)

```css
.btn-icon {
  width: 40px;
  height: 40px;
  padding: 0;
  border-radius: 50%; /* or 8px for square */
  display: flex;
  align-items: center;
  justify-content: center;
}
```

### Button States

| State | Visual Change |
|-------|---------------|
| **Default** | Base styling |
| **Hover** | Scale 1.02, shadow increase |
| **Active/Pressed** | Scale 0.98 |
| **Focus** | 2px outline, primary color |
| **Disabled** | 50% opacity, no pointer |
| **Loading** | Spinner icon, disabled |

---

## Input Fields

### Text Input

```css
.input-field {
  height: 48px;
  padding: 12px 16px;
  border-radius: 12px;
  border: 1px solid #E5E7EB;
  background: #FFFFFF;
  font-size: 14px;
  color: #13343B;
}

/* Focus State */
.input-field:focus {
  border-color: #1FB8CD;
  box-shadow: 0 0 0 3px rgba(31, 184, 205, 0.1);
  outline: none;
}

/* Error State */
.input-field.error {
  border-color: #EF4444;
}

/* Success State */
.input-field.success {
  border-color: #34D399;
}
```

### Input Variants

#### With Leading Icon
```
┌─────────────────────────┐
│ 🔍  Search...          │
└─────────────────────────┘
```
- Icon: 20×20px, left padding 16px
- Text padding: 12px (after icon space)

#### With Trailing Icon/Button
```
┌─────────────────────────┐
│ Password          👁️    │
└─────────────────────────┘
```
- Icon/button on right
- Clickable for actions (show/hide password)

#### With Label
```
Email Address *
┌─────────────────────────┐
│ your@email.com         │
└─────────────────────────┘
```
- Label: 12px, 600 weight, 8px margin-bottom
- Required indicator: red asterisk

#### With Helper Text
```
┌─────────────────────────┐
│ username               │
└─────────────────────────┘
Only letters and numbers allowed
```
- Helper text: 11px, secondary color
- 4px margin-top

#### With Error Message
```
┌─────────────────────────┐
│ invalid@              │ ❌
└─────────────────────────┘
⚠️ Please enter a valid email
```
- Error icon on right
- Error message: 11px, red color
- 4px margin-top

### Text Area
- Multi-line input
- Min-height: 120px
- Resize: vertical only
- All other styles match text input

### Select / Dropdown
```css
.select {
  appearance: none;
  background: url('chevron-down.svg') no-repeat right 12px center;
  padding-right: 40px;
}
```
- Chevron icon on right
- Opens dropdown menu below
- Selected item highlighted

### Search Field
```
┌─────────────────────────┐
│ 🔍  Search StudenKZ... │
└─────────────────────────┘
```
- Search icon on left
- Clear button (×) appears when text entered
- Autocomplete suggestions below

### Toggle Switch
```
OFF ○──  or  ──●○ ON
```
- Width: 48px, Height: 28px
- Handle: 24×24px circle
- Animation: 200ms ease
- Colors: Gray (off), Primary gradient (on)

### Checkbox
```
☐ Unchecked
☑ Checked
```
- Size: 20×20px
- Border-radius: 4px
- Checkmark animation
- Indeterminate state supported

### Radio Button
```
○ Unselected
◉ Selected
```
- Size: 20×20px
- Circular
- Inner dot animation

### Date Picker
- Calendar modal opens on click
- Selected date highlighted
- Today marked with dot
- Range selection supported

---

## Cards

### Basic Card
```css
.card {
  background: #FFFFFF;
  border-radius: 16px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.06);
  padding: 24px;
}

.card:hover {
  transform: scale(1.02);
  box-shadow: 0 4px 16px rgba(0, 0, 0, 0.08);
  transition: all 200ms ease;
}
```

### Card Variants

#### Product Card
```
┌─────────────────────┐
│  [Image 16:9]       │
├─────────────────────┤
│ Product Title       │
│ Author • Year       │
│                     │
│ 🎓 KBTU • Year 2    │
│ 📊 Excellent        │
│                     │
│ 5,000 ₸    [❤️ 24] │
└─────────────────────┘
```

**Specifications:**
- Image: aspect ratio 16:9, border-radius 12px
- Title: 16px, 600 weight, 2 lines max
- Metadata: 12px, secondary color
- Price: 18px, 700 weight, primary color
- Favorite button: top-right overlay on image

#### Service Card (Home Grid)
```
┌─────────────────────┐
│ 📖                 │
│                     │
│ Marketplace        │
│ Buy & sell         │
│ textbooks          │
└─────────────────────┘
```

**Specifications:**
- Gradient background (unique per service)
- Icon: 48×48px, top-left
- Title: 18px, 700 weight
- Description: 12px, 2 lines max
- Height: 140px

#### Restaurant Card
```
┌───────────────────────┐
│ [Cover Image]         │
│ 🏷️ -20% first order  │
├───────────────────────┤
│ Restaurant Name       │
│ ⭐ 4.8 • 🕐 25-35 min │
│ 💰 500-1500₸         │
└───────────────────────┘
```

#### User/Profile Card
```
┌───────────────────────┐
│  [Avatar]             │
│  Name Surname         │
│  🎓 KBTU • Year 3     │
│  ⭐ 4.9 (23 reviews)  │
│                       │
│  [Message] [Follow]   │
└───────────────────────┘
```

#### Club Card
```
┌────────────────────────┐
│ [Cover + Avatar]       │
│                        │
│ Club Name              │
│ 👥 245 members         │
│ 📅 Meets: Fri 6PM      │
│                        │
│ [Join] [Info]          │
└────────────────────────┘
```

### Card Interactive States
- **Default:** Base shadow
- **Hover:** Scale 1.02, shadow increase
- **Active:** Scale 0.98
- **Selected:** Primary color border (2px)

---

## Navigation

### Top Navigation Bar
```
┌──────────────────────────────┐
│ [Logo]            🔔 👤      │
└──────────────────────────────┘
```

**Specifications:**
- Height: 64px
- Background: White (light mode), Dark surface (dark mode)
- Shadow: 0 2px 8px rgba(0,0,0,0.04)
- Logo: 32px height
- Icons: 24×24px
- Notification badge: 8×8px red dot

### Bottom Navigation
```
┌──────────────────────────────┐
│ 🏠    🛍️    🍔    👥    👤   │
│ Home  Shop  Food  Social  Me │
└──────────────────────────────┘
```

**Specifications:**
- Height: 72px
- 5 items evenly spaced
- Icons: 24×24px
- Labels: 10px
- Active state: Primary color + filled icon
- Inactive: Gray + outline icon
- Safe area inset for iOS devices

### Tab Bar (Horizontal Scroll)
```
┌───────────────────────────────┐
│ All • Popular • New • Sale •  │
└───────────────────────────────┘
```

**Specifications:**
- Height: 44px
- Pills with 24px horizontal padding
- Active: Primary color background, white text
- Inactive: Transparent, gray text
- Smooth scroll behavior

### Breadcrumbs
```
Home > Marketplace > Textbooks > Mathematics
```

**Specifications:**
- 12px font size
- Secondary text color
- " > " separator
- Last item: primary text color
- Clickable for navigation

---

## Avatars

### Sizes
- **XS:** 24×24px (comments, mentions)
- **SM:** 32×32px (chat list)
- **MD:** 48×48px (cards, profiles)
- **LG:** 64×64px (profile headers)
- **XL:** 120×120px (full profile)

### Variants

#### Photo Avatar
- Circular (border-radius: 50%)
- Object-fit: cover
- Border: 2px white for group overlays

#### Initials Avatar
- Gradient background (from user ID)
- Initials: 2 letters, white, centered
- Font-weight: 600

#### Icon Avatar
- Icon instead of photo
- Used for system accounts
- Solid color background

#### Status Indicator
- Online: Green dot (8×8px) bottom-right
- Away: Yellow dot
- Offline: No indicator
- Do Not Disturb: Red dot

#### Group Avatar
- Stack 2-3 avatars
- Overlap by 25%
- White border to separate

---

## Badges

### Badge Variants

#### Notification Badge
```css
.badge-notification {
  min-width: 20px;
  height: 20px;
  padding: 0 6px;
  border-radius: 10px;
  background: #EF4444;
  color: #FFFFFF;
  font-size: 11px;
  font-weight: 600;
}
```
- Displays count (1-99, then 99+)
- Position: top-right of parent element

#### Status Badge
```
✓ VERIFIED   • NEW   • -20%   • HOT
```

**Specifications:**
- Pill shape (border-radius: 12px)
- Height: 24px
- Padding: 4px 12px
- Font: 11px, 600 weight
- Variants:
  - Success: Green background
  - Info: Blue background
  - Warning: Orange background
  - Sale: Red background
  - New: Purple background

#### Text Badge
- Small label for metadata
- Transparent background
- Icon + text combination
- Examples: "🎓 KBTU", "⭐ 4.8", "🕐 25 min"

### Badge Positioning
- **Top-right:** Notification counts
- **Top-left:** Status (new, sale)
- **Inline:** Within text content
- **Overlay:** On images (promo badges)

---

## Modals & Sheets

### Modal Dialog
```
      ┌─────────────────┐
      │    [Title]   ×  │
      ├─────────────────┤
      │                 │
      │    Content      │
      │                 │
      ├─────────────────┤
      │ [Cancel] [Save] │
      └─────────────────┘
```

**Specifications:**
- Max-width: 480px (mobile: full-width minus 32px)
- Border-radius: 24px
- Backdrop: rgba(0,0,0,0.5) with blur
- Animation: Scale up + fade in (300ms)
- Close button: top-right
- Buttons: bottom, right-aligned

### Bottom Sheet
```
────────────────────────
         ━━━
┌────────────────────────┐
│                        │
│      Content           │
│                        │
└────────────────────────┘
```

**Specifications:**
- Slides up from bottom
- Handle bar: 4×32px, centered, gray
- Swipe down to dismiss
- Backdrop: rgba(0,0,0,0.3)
- Border-radius: 24px top corners only
- Max-height: 90vh

### Action Sheet
- List of action buttons
- Destructive action in red
- Cancel button separated at bottom
- Used for: Share, Delete, Edit options

### Drawer
- Slides in from left or right
- Full height
- Width: 320px (tablet: 400px)
- Used for: Filters, menus, settings
- Overlay closes drawer

---

## Notifications

### Toast Notification
```
┌────────────────────────────┐
│ ✓ Order placed successfully│
└────────────────────────────┘
```

**Specifications:**
- Appears from top with bounce
- Width: max 360px
- Padding: 16px
- Border-radius: 12px
- Auto-dismiss: 3-5 seconds
- Close button optional
- Position: top-center

**Variants:**
- **Success:** Green background, checkmark icon
- **Error:** Red background, X icon
- **Warning:** Orange background, alert icon
- **Info:** Blue background, info icon

### Snackbar
- Bottom-center positioning
- Action button on right
- Persistent until dismissed or action taken

### Banner
- Full-width at top of screen
- Used for important announcements
- Dismissible with × button
- Colorful, eye-catching

---

## Loading States

### Spinner
```css
.spinner {
  width: 32px;
  height: 32px;
  border: 3px solid rgba(31, 184, 205, 0.2);
  border-top-color: #1FB8CD;
  border-radius: 50%;
  animation: spin 800ms linear infinite;
}
```

**Sizes:**
- Small: 16×16px (inline)
- Medium: 32×32px (buttons, cards)
- Large: 48×48px (page loading)

### Progress Bar
```
━━━━━━━━━━━━━━━━━━░░░░░░  75%
```

**Specifications:**
- Height: 8px
- Border-radius: 4px
- Background: light gray
- Fill: primary gradient
- Optional percentage label

### Skeleton Loader
```
┌────────────────────────┐
│ ▓▓▓▓▓▓▓               │
│ ░░░░░░░░░░            │
│ ░░░░░░                │
│                        │
│ ░░░░░░░░  ░░░░░       │
└────────────────────────┘
```

**Specifications:**
- Gray background (shimmer effect)
- Matches layout of actual content
- Smooth pulse animation
- Used while content loads

### Pull to Refresh
- Pull down gesture
- Elastic bounce effect
- Spinner appears at threshold
- Releases to refresh

---

## Lists & Tables

### List Item
```
┌────────────────────────────┐
│ [Icon] Title               │
│        Subtitle            │
└────────────────────────────┘
```

**Specifications:**
- Height: 64-72px
- Padding: 16px
- Divider: 1px line or 8px gap
- Hover: Light background
- Tap: Ripple effect

### List with Actions
```
┌────────────────────────────┐
│ [🔔] Notification   [→]   │
└────────────────────────────┘
```
- Leading icon/avatar
- Title + subtitle
- Trailing icon/button
- Swipe for more actions

### Grid List
- 2 columns on mobile
- 3-4 columns on tablet
- Gap: 16px
- Equal height cards

### Table (Desktop)
```
┌──────┬────────┬────────┬────────┐
│ Name │ Status │ Price  │ Action │
├──────┼────────┼────────┼────────┤
│ Item │ Active │ 1,000₸ │  Edit  │
└──────┴────────┴────────┴────────┘
```

**Specifications:**
- Header: 600 weight, 12px, uppercase
- Rows: 48px height
- Striped or bordered
- Sortable columns
- Hover: light background

---

## Form Components

### Form Group
```
Label *
┌────────────────────────┐
│ Input field            │
└────────────────────────┘
Helper text here
```

**Spacing:**
- Label margin-bottom: 8px
- Input margin-bottom: 4px
- Helper text margin-bottom: 16px

### Inline Form
- Label and input on same row
- Label: 30% width
- Input: 70% width
- Aligned vertically

### Form Validation
- Validate on blur (after user leaves field)
- Show errors immediately
- Success indicator after validation
- Disable submit until valid

---

## Feedback & Ratings

### Star Rating
```
★★★★☆ 4.0
```
- Star size: 20×20px
- Filled: Primary color or gold (#F59E0B)
- Empty: Light gray
- Half stars supported
- Interactive for input

### Review Card
```
┌────────────────────────────┐
│ [Avatar] Name    ★★★★☆    │
│          Date              │
│                            │
│ Review text...             │
│                            │
│ [Photo] [Photo] [Photo]    │
│                            │
│ 👍 Helpful (24)  Report    │
└────────────────────────────┘
```

### Like Button
- Heart icon
- Outline when inactive
- Filled + animation when active
- Count displays next to icon
- Particle effect on tap

---

## Media Components

### Image Gallery
- Horizontal scroll
- Dot indicators for count
- Pinch to zoom
- Swipe between images
- Full-screen mode

### Video Player
- Standard controls
- Play/pause overlay
- Progress bar
- Volume control
- Fullscreen button

### Audio Player
- Play/pause button
- Progress bar with scrubbing
- Current time / Total time
- Volume control (desktop)

---

## Accessibility Features

### Focus Indicators
```css
:focus-visible {
  outline: 2px solid #1FB8CD;
  outline-offset: 2px;
}
```

### Screen Reader Only
```css
.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  padding: 0;
  margin: -1px;
  overflow: hidden;
  clip: rect(0,0,0,0);
  border: 0;
}
```

### Skip Links
- "Skip to main content"
- Visible on focus
- Top of page

---

## Component States Summary

| State | Visual Treatment |
|-------|------------------|
| **Default** | Base styling |
| **Hover** | Background change, scale, shadow |
| **Active/Pressed** | Scale down 0.98 |
| **Focus** | 2px outline, primary color |
| **Disabled** | 50% opacity, no pointer events |
| **Loading** | Spinner, disabled |
| **Success** | Green indicators |
| **Error** | Red indicators, shake animation |
| **Selected** | Border or background highlight |

---

**Version:** 1.0  
**Last Updated:** November 8, 2025  
**Contact:** Alizhan Bizhan | alizhan695@gmail.com
