# StudenKZ UX Guidelines
## Animations, Interactions & User Experience Patterns

---

## 📋 Table of Contents
1. [Micro-Animations](#micro-animations)
2. [Transitions & Navigation](#transitions--navigation)
3. [Gestures & Interactions](#gestures--interactions)
4. [Feedback Patterns](#feedback-patterns)
5. [Accessibility](#accessibility)
6. [Performance Guidelines](#performance-guidelines)
7. [Gamification](#gamification)
8. [Trust & Safety](#trust--safety)

---

## Micro-Animations

### Animation Principles
- **Duration:** 200-300ms for most interactions
- **Easing:** Ease-out for entrances, ease-in for exits
- **Purpose:** Every animation should serve a functional purpose
- **Performance:** 60 FPS target, GPU-accelerated when possible

---

### 1. Button Animations

#### Press Animation
```css
/* On tap/click */
transform: scale(0.98);
transition: transform 100ms ease-out;

/* Ripple effect */
/* Material Design ripple from tap point */
animation: ripple 600ms ease-out;
```

**Usage:** All interactive buttons  
**Effect:** Slight scale down + ripple from touch point  
**Duration:** 100ms scale, 600ms ripple

---

#### Loading State
```css
/* Button morphs into spinner */
.button-loading {
  pointer-events: none;
  opacity: 0.7;
}

/* Text fades out, spinner fades in */
.button-text {
  opacity: 0;
  transition: opacity 200ms;
}

.button-spinner {
  opacity: 1;
  animation: spin 800ms linear infinite;
}
```

**Usage:** After submit/action button pressed  
**Duration:** Instant state change, spinner continuous

---

### 2. Card Animations

#### Hover/Focus (Desktop/Tablet)
```css
transform: scale(1.02) translateY(-2px);
box-shadow: 0 8px 24px rgba(0, 0, 0, 0.12);
transition: all 250ms ease-out;
```

**Usage:** Product cards, service cards  
**Effect:** Slight lift and shadow increase  
**Duration:** 250ms

---

#### Tap (Mobile)
```css
/* Quick scale down then bounce back */
@keyframes tap-bounce {
  0% { transform: scale(1); }
  50% { transform: scale(0.98); }
  100% { transform: scale(1); }
}

animation: tap-bounce 200ms ease-out;
```

**Usage:** All tappable cards  
**Duration:** 200ms

---

### 3. Page Transitions

#### Slide Transition
```css
/* Forward navigation */
.page-enter {
  transform: translateX(100%);
  opacity: 0;
}

.page-enter-active {
  transform: translateX(0);
  opacity: 1;
  transition: all 300ms ease-out;
}

/* Back navigation */
.page-exit {
  transform: translateX(0);
  opacity: 1;
}

.page-exit-active {
  transform: translateX(100%);
  opacity: 0;
  transition: all 300ms ease-in;
}
```

**Usage:** Screen-to-screen navigation  
**Duration:** 300ms

---

#### Modal/Dialog
```css
/* Backdrop */
@keyframes backdrop-fade {
  from { opacity: 0; }
  to { opacity: 1; }
}

/* Modal */
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

**Usage:** Modals, dialogs, popups  
**Duration:** 300ms  
**Note:** Always include backdrop blur

---

#### Bottom Sheet
```css
@keyframes slide-up {
  from {
    transform: translateY(100%);
  }
  to {
    transform: translateY(0);
  }
}

animation: slide-up 350ms cubic-bezier(0.4, 0, 0.2, 1);
```

**Usage:** Bottom sheets, action sheets  
**Duration:** 350ms  
**Dismissal:** Swipe down or tap backdrop

---

### 4. Tab Switching

```css
/* Content fade and slide */
.tab-content-exit {
  position: absolute;
  opacity: 1;
  transform: translateX(0);
}

.tab-content-exit-active {
  opacity: 0;
  transform: translateX(-20px);
  transition: all 200ms ease-in;
}

.tab-content-enter {
  opacity: 0;
  transform: translateX(20px);
}

.tab-content-enter-active {
  opacity: 1;
  transform: translateX(0);
  transition: all 200ms ease-out;
}
```

**Duration:** 200ms  
**Effect:** Crossfade with subtle horizontal movement

---

### 5. Pull to Refresh

```css
/* Elastic bounce effect */
.pull-indicator {
  transform: translateY(var(--pull-distance));
  transition: transform 0s;
}

/* On release, snap back with bounce */
.pull-indicator-release {
  animation: elastic-bounce 400ms ease-out;
}

@keyframes elastic-bounce {
  0% { transform: translateY(var(--pull-distance)); }
  60% { transform: translateY(80px); }
  80% { transform: translateY(70px); }
  100% { transform: translateY(0); }
}
```

**Threshold:** 80px pull distance  
**Indicator:** Spinner appears at threshold  
**Duration:** 400ms return animation

---

### 6. Like/Favorite Animation

```css
/* Heart pop */
@keyframes heart-pop {
  0% {
    transform: scale(1);
  }
  25% {
    transform: scale(1.3);
  }
  50% {
    transform: scale(0.9);
  }
  75% {
    transform: scale(1.1);
  }
  100% {
    transform: scale(1);
  }
}

/* Particle burst */
@keyframes particle-burst {
  0% {
    transform: scale(0) translateY(0);
    opacity: 1;
  }
  100% {
    transform: scale(1) translateY(-20px);
    opacity: 0;
  }
}
```

**Usage:** Like buttons, favorites  
**Effect:** Heart bounces + small particles burst  
**Duration:** 500ms  
**Haptic:** Light impact feedback

---

### 7. Add to Cart Animation

```css
/* Item flies to cart icon */
@keyframes fly-to-cart {
  0% {
    transform: translate(0, 0) scale(1);
    opacity: 1;
  }
  100% {
    transform: translate(var(--cart-x), var(--cart-y)) scale(0.2);
    opacity: 0;
  }
}
```

**Usage:** Food items, products added to cart  
**Duration:** 600ms  
**Effect:** Item image flies to cart icon  
**Follow-up:** Cart icon bounces + badge updates

---

### 8. Success Animation

```css
/* Checkmark draw */
@keyframes checkmark-draw {
  0% {
    stroke-dashoffset: 100;
  }
  100% {
    stroke-dashoffset: 0;
  }
}

/* Circle expand */
@keyframes circle-expand {
  0% {
    transform: scale(0);
    opacity: 0;
  }
  50% {
    opacity: 1;
  }
  100% {
    transform: scale(1);
    opacity: 1;
  }
}

/* Confetti */
@keyframes confetti-fall {
  /* Multiple particle trajectories */
}
```

**Usage:** Order confirmation, payment success  
**Sequence:**
1. Circle expands (300ms)
2. Checkmark draws (400ms, starts at 200ms)
3. Confetti particles (800ms, starts at 400ms)

**Total duration:** 1200ms

---

### 9. Error Animation

```css
/* Shake */
@keyframes shake {
  0%, 100% { transform: translateX(0); }
  10%, 30%, 50%, 70%, 90% { transform: translateX(-8px); }
  20%, 40%, 60%, 80% { transform: translateX(8px); }
}

animation: shake 400ms ease-in-out;
```

**Usage:** Form errors, failed actions  
**Duration:** 400ms  
**Haptic:** Error vibration (if supported)

---

### 10. Loading States

#### Skeleton Shimmer
```css
@keyframes shimmer {
  0% {
    background-position: -1000px 0;
  }
  100% {
    background-position: 1000px 0;
  }
}

.skeleton {
  background: linear-gradient(
    90deg,
    #f0f0f0 0%,
    #f8f8f8 50%,
    #f0f0f0 100%
  );
  background-size: 1000px 100%;
  animation: shimmer 2s infinite;
}
```

**Usage:** Content loading  
**Duration:** 2s per cycle (infinite)

---

#### Progress Bar
```css
@keyframes progress-fill {
  from { width: 0%; }
  to { width: var(--progress-percent); }
}

animation: progress-fill 300ms ease-out forwards;
```

**Usage:** File uploads, multi-step processes  
**Update:** Smooth transitions between progress values

---

### 11. Notification Badge

```css
/* Scale pulse */
@keyframes badge-pulse {
  0%, 100% {
    transform: scale(1);
  }
  50% {
    transform: scale(1.2);
  }
}

animation: badge-pulse 1s ease-in-out infinite;
```

**Usage:** New notification indicator  
**Duration:** 1s pulse (repeating)  
**Stop:** When user views notifications

---

## Transitions & Navigation

### Navigation Stack Behavior

#### Push (Forward)
- **New screen:** Slides in from right
- **Current screen:** Slides left and scales down slightly
- **Duration:** 300ms

#### Pop (Back)
- **Current screen:** Slides out to right
- **Previous screen:** Scales back up and slides right
- **Duration:** 300ms

#### Replace
- **Fade transition:** Crossfade between screens
- **Duration:** 250ms

---

### Tab Bar Transitions

```css
/* Active indicator slide */
.tab-indicator {
  transition: transform 250ms cubic-bezier(0.4, 0, 0.2, 1);
  transform: translateX(var(--active-tab-position));
}

/* Icon morph: outline → filled */
.tab-icon {
  transition: all 200ms ease-out;
}
```

**Effect:** Smooth indicator slide + icon change  
**Color transition:** Gray → Primary color

---

### Modal Presentations

#### Full Screen Modal
- Slides up from bottom
- Navigation bar with close button
- Can be dismissed with down swipe

#### Card Modal
- Scales up from center with backdrop blur
- Rounded corners
- Dismissed by tapping backdrop or close button

#### Bottom Sheet
- Slides up from bottom
- Partial screen coverage
- Handle bar for swipe gesture
- Swipe down to dismiss

---

## Gestures & Interactions

### Swipe Gestures

#### Swipe to Delete (Lists)
```
→→→  [Item]  [🗑️ Delete]
```
- **Threshold:** 60% of screen width
- **Visual:** Red background reveals delete button
- **Haptic:** Light feedback at threshold
- **Confirmation:** Tap delete button to confirm

#### Swipe for Actions (Chat, Email)
```
← [Item] → [Archive] [Delete]
```
- **Left swipe:** Archive/Mark read
- **Right swipe:** Delete
- **Threshold:** 40% width
- **Elastic bounce:** Doesn't overextend

#### Swipe Between Tabs/Screens
- **Full screen swipe:** Horizontal pan
- **Threshold:** 30% screen width
- **Cancel:** Let go before threshold
- **Animation:** Following finger + elastic bounce

---

### Pull Down Gestures

#### Pull to Refresh
- **Activation:** Pull down from top
- **Threshold:** 80px
- **Indicator:** Spinner appears
- **Elastic:** Bounces back after release

#### Pull to Reveal Search
- **Location:** Feed/list views
- **Effect:** Search bar slides down
- **Threshold:** 40px
- **Sticky:** Stays until dismissed or scroll up

---

### Long Press

#### Context Menu
- **Duration:** 500ms hold
- **Haptic:** Medium impact when menu appears
- **Visual:** Item scales slightly (0.98)
- **Menu:** Bottom sheet or popover with actions

#### Reorder (Lists)
- **Duration:** 500ms hold
- **Visual:** Item lifts with shadow
- **Haptic:** Medium impact
- **Mode:** Drag to reorder, release to place

---

### Pinch Gestures

#### Pinch to Zoom (Images)
- **Smooth scaling:** Follows finger distance
- **Min scale:** 1x (original)
- **Max scale:** 4x
- **Snap back:** If released below 1x

#### Pinch to Collapse/Expand (Lists)
- **Alternative:** Semantic zoom
- **Usage:** Map views, calendar views

---

### Double Tap

#### Like (Images)
- **Effect:** Heart animation appears at tap point
- **Duration:** 600ms
- **Haptic:** Light impact

#### Zoom (Images)
- **First tap:** Zoom to 2x at tap point
- **Second tap:** Zoom back to 1x

---

## Feedback Patterns

### Visual Feedback

#### Tap Feedback
- **Instant:** Visual change within 16ms
- **Ripple:** Expands from tap point
- **Opacity:** Slight transparency on press

#### Active States
- **Buttons:** Darker shade or scale down
- **Links:** Underline or color change
- **Cards:** Shadow increase or lift

#### Focus States (Accessibility)
- **2px outline:** Primary color
- **Offset:** 2px from element
- **High contrast:** Visible on all backgrounds

---

### Haptic Feedback

> **Note:** iOS and Android support

#### Light Impact
- **Usage:** Tap buttons, toggle switches
- **Intensity:** Subtle

#### Medium Impact
- **Usage:** Long press, context menu, modal open
- **Intensity:** Noticeable

#### Heavy Impact
- **Usage:** Error, success, important action
- **Intensity:** Strong

#### Selection
- **Usage:** Scrubbing through pickers, sliders
- **Intensity:** Light, rapid

---

### Audio Feedback

> **Note:** Optional, user-controllable

#### Success Sound
- **Usage:** Order placed, payment confirmed
- **Duration:** <500ms
- **Tone:** Positive, uplifting

#### Error Sound
- **Usage:** Form error, failed action
- **Duration:** <300ms
- **Tone:** Alert but not harsh

#### Notification Sound
- **Usage:** New message, order update
- **Duration:** <1s
- **Tone:** Attention-getting but pleasant

---

### Loading Feedback

#### Immediate Feedback
- **<100ms:** Show loading indicator immediately
- **Don't:** Wait for data to show something

#### Optimistic Updates
- **UI updates first:** Show result immediately
- **Rollback if fail:** Undo on error
- **Usage:** Likes, follows, simple actions

#### Skeleton Screens
- **Better than spinners:** Shows layout structure
- **Matches content:** Same shape as real content
- **Shimmer effect:** Indicates loading

---

## Accessibility

### Screen Reader Support

#### Labels
- **All interactive elements:** Meaningful labels
- **Images:** Alt text descriptions
- **Icons:** Accessibility label if no text

#### Announcements
- **Dynamic content:** Announce updates
- **Form errors:** Read error messages
- **Success actions:** Confirm completion

---

### Motor Accessibility

#### Touch Targets
- **Minimum size:** 44×44px
- **Spacing:** 8px between targets
- **Padding:** Extend beyond visual bounds if needed

#### Timing
- **No time limits:** Or allow extension
- **Pause/stop:** For auto-advancing content
- **Skip repetition:** Skip to main content link

---

### Visual Accessibility

#### Color Contrast
- **Normal text:** 4.5:1 minimum
- **Large text (18px+):** 3:1 minimum
- **UI elements:** 3:1 minimum

#### Don't Rely on Color Alone
- **Icons + text:** Both convey meaning
- **Patterns:** Use shapes, not just color
- **Success/Error:** Icon + color + text

#### Text Sizing
- **Respect system settings:** Support dynamic type
- **Min size:** 12px for body text
- **Line height:** 1.5 minimum for readability

---

### Cognitive Accessibility

#### Clear Language
- **Simple words:** Avoid jargon
- **Short sentences:** Easy to parse
- **Consistent terms:** Same word for same action

#### Clear Navigation
- **Breadcrumbs:** Show where you are
- **Back button:** Always visible
- **Home button:** Escape route

#### Error Prevention
- **Confirmation:** For destructive actions
- **Undo:** Allow reversal
- **Clear instructions:** Before action

---

## Performance Guidelines

### Animation Performance

#### Use CSS Transforms
```css
/* GOOD - GPU accelerated */
transform: translateX(100px);
transform: scale(1.2);
transform: rotate(45deg);
opacity: 0.5;

/* BAD - Forces layout recalculation */
left: 100px;
width: 120%;
```

#### Will-Change Property
```css
/* For elements that will animate */
.animated-element {
  will-change: transform, opacity;
}

/* Remove after animation */
.animated-element.done {
  will-change: auto;
}
```

---

### Reduce Motion

```css
@media (prefers-reduced-motion: reduce) {
  * {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
  }
}
```

**Respect user preference:** Some users get motion sick

---

### Image Loading

#### Progressive Loading
1. **Placeholder:** Blurred low-res or solid color
2. **Load:** High-res image
3. **Crossfade:** Smooth transition (300ms)

#### Lazy Loading
- **Load on scroll:** When near viewport
- **Threshold:** 200px before visible
- **Priority:** Above-the-fold loads first

---

### Perceived Performance

#### Skeleton Screens
- **Better than spinners:** Feels faster
- **Content shape:** Matches real layout

#### Optimistic UI
- **Instant feedback:** Update UI immediately
- **Background request:** Actually save data
- **Rollback:** If request fails

#### Prefetching
- **Predict next action:** Preload likely screens
- **Link hover:** Start loading on hover (desktop)
- **Background:** During idle time

---

## Gamification

### Achievement System

#### Badge Display
```
┌─────────────────┐
│  [Badge Icon]   │
│  Achievement!   │
│  First Purchase │
└─────────────────┘
```

**Animation:**
1. Scale up from 0 (400ms)
2. Bounce effect (200ms)
3. Confetti particles (800ms)
4. Auto-dismiss after 3s or tap

---

#### Progress to Next Level
```
Level 2 → Level 3
████████████░░░░░░░░  60%
120/200 points
```

**Visual:**
- Animated progress bar fill
- Sparkle effect on milestones
- Celebration on level up

---

### Loyalty Tiers

#### Visual Indicators
- **Newbie:** Gray badge
- **Student:** Blue badge
- **Veteran:** Purple badge
- **Legend:** Gold gradient badge

**Progression:**
- Clear requirements
- Visual progress bar
- Benefits at each level

---

### Streaks & Habits

#### Daily Login Streak
```
🔥 7 Day Streak!
M T W T F S S
✓ ✓ ✓ ✓ ✓ ✓ ✓
```

**Notifications:**
- Reminder if streak at risk
- Celebration on milestones (7, 30, 100 days)

---

### Leaderboards

#### Weekly/Monthly
```
┌────────────────────────┐
│ 🏆 Top Sellers         │
│ 1. 👤 Aida K.   12 sales│
│ 2. 👤 Yerlan M. 10 sales│
│ 3. 👤 You       8 sales │
│ ...                    │
└────────────────────────┘
```

**Features:**
- Personal ranking highlighted
- Friends' rankings
- Refresh animation

---

## Trust & Safety

### Verification Badges

#### Display
- **✓ Verified Student:** Blue checkmark
- **✓ Verified Seller:** Green checkmark
- **⭐ Official Partner:** Gold star badge

**Tooltip:** Hover/tap to see verification details

---

### Ratings & Reviews

#### Star Display
```
⭐⭐⭐⭐☆ 4.2 (234 reviews)
```

**Interactive:**
- Tap stars to rate
- Animation on selection
- Optional review text

---

### Safety Features

#### Report Button
- **Location:** Three-dot menu (•••)
- **Flow:** Select reason → Optional details → Submit
- **Feedback:** "Thanks for reporting" confirmation

#### Block User
- **Confirmation:** "Are you sure?"
- **Effect:** Hide from all listings and messages
- **Reversible:** Can unblock in settings

---

### Secure Transactions

#### Escrow Indicator
```
🔒 Secure Payment
Your money is held safely until delivery
```

**Visual:**
- Lock icon
- Green color
- Trust message

---

## Content Guidelines

### Empty States

#### Friendly Tone
```
┌──────────────────┐
│  [Illustration]  │
│  Nothing here... │
│     yet!         │
│                  │
│  [Start Action]  │
└──────────────────┘
```

**Elements:**
- Relevant illustration
- Short, friendly message
- Clear call-to-action

---

### Error Messages

#### Be Helpful
```
❌ BAD:
"Error 500"

✅ GOOD:
"Something went wrong
We're working on it. Try again in a moment."
```

**Principles:**
- Explain what happened
- Suggest solution
- Provide action button

---

### Loading Messages

#### Add Personality
```
• "Fetching your books..."
• "Cooking up your order..."
• "Finding study buddies..."
• "Crunching numbers..."
```

**Principles:**
- Contextual to action
- Brief and fun
- Never too long

---

## Responsive Design

### Breakpoint Behaviors

#### Mobile (< 428px)
- Single column layouts
- Bottom sheets for actions
- Thumb-friendly navigation at bottom
- Collapsible content

#### Tablet (768px - 1024px)
- Two-column layouts where appropriate
- Side panels instead of full-screen
- Hover states enabled
- Keyboard shortcuts

#### Desktop (> 1280px)
- Multi-column layouts
- Persistent navigation
- Mouse-optimized interactions
- Keyboard navigation critical

---

### Orientation Changes

#### Portrait → Landscape
- Maintain scroll position
- Adapt layout (stack → side-by-side)
- Smooth transition (200ms)

---

## Testing Checklist

### Animation Testing
- [ ] All animations run at 60 FPS
- [ ] No janky scrolling
- [ ] Reduced motion preference respected
- [ ] Animations feel snappy, not slow

### Interaction Testing
- [ ] All touch targets minimum 44×44px
- [ ] Gestures work smoothly
- [ ] Feedback is immediate (<100ms)
- [ ] No accidental triggers

### Accessibility Testing
- [ ] Screen reader announces everything
- [ ] Keyboard navigation works
- [ ] Color contrast passes WCAG AA
- [ ] Works with system font sizes

### Performance Testing
- [ ] Fast 3G loads in <5s
- [ ] Images lazy load
- [ ] Smooth on low-end devices
- [ ] Battery-efficient animations

---

**Version:** 1.0  
**Last Updated:** November 8, 2025  
**Contact:** Alizhan Bizhan | alizhan695@gmail.com
