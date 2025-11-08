# StudenKZ Design System & UX Specification

## 1. Product Overview
- **Product name:** StudenKZ — Kazakhstan’s first student super-platform.  
- **Mission:** Deliver a unified digital companion that simplifies, empowers, and celebrates student life.  
- **Primary audience:** Gen-Z university students (17-25) across Kazakhstan; digitally native, cost-conscious, socially active.  
- **Experience promise:** “One app. All student needs.” across commerce, services, community, and finance.

## 2. Brand Narrative & Voice
- **Personality:** Energetic, reliable, and relatable. Speaks as a trusted peer who gets campus culture and offers smart shortcuts.  
- **Tone:** Positive, solution-oriented, occasionally playful. Avoid slang that could alienate; opt for clear, inclusive language.  
- **Messaging pillars:** Save smarter, live fuller, grow together.  
- **Voice applications:**  
  - **Headlines:** punchy, aspirational (max 6 words).  
  - **Body copy:** concise, informative, 400-500 weight.  
  - **Microcopy:** actionable verbs (“Join club”, “Split bill”), avoid passive constructions.

## 3. Core Design Principles
1. **Student-first utility:** Prioritize clarity and access to high-frequency tasks (ordering food, finding materials, checking balances).  
2. **Positive friction:** Encourage safe, informed decisions (e.g., verify sellers, confirm transfers) without slowing down the experience.  
3. **Vibrant modularity:** Pair bold gradients with clean modular layouts to keep interfaces lively yet manageable at scale.  
4. **Trust by design:** Reinforce verification, safety badges, and transaction transparency visually and contextually.  
5. **Inclusive flexibility:** Seamless light/dark modes, localization-ready layouts, and keyboard/screen reader support in every flow.

## 4. Visual Language

### 4.1 Color System
| Token | Hex | Usage |
| --- | --- | --- |
| `--color-primary` | `#1FB8CD` | Primary actions, active states, progress indicators. |
| `--color-secondary` | `#13343B` | Headings, body text on light backgrounds, emphasis on light surfaces. |
| `--color-accent` | `#5D878F` | Supporting icons, dividers, secondary buttons. |
| `--color-success` | `#34D399` | Positive feedback, confirmed states, verification tick. |
| `--color-error` | `#F87171` | Validation errors, destructive actions. |
| `--color-warning` | `#FBBF24` | Cautionary notices, pending statuses. |
| `--color-background` | `#FCFCF9` | App background (light). |
| `--color-surface` | `#FFFFFF` | Cards, sheets, modals. |
| `--color-border` | `rgba(19, 52, 59, 0.12)` | Borders, separators. |

**Gradient system:**  
- Primary CTA: `linear-gradient(135deg, #1FB8CD 0%, #6C5CE7 100%)`.  
- Secondary hero: `linear-gradient(135deg, #13343B 0%, #1FB8CD 100%)`.  
- Use gradients sparingly to highlight high-value interactions (hero cards, section headers). Keep supporting UI elements flat for contrast.

**Dark mode counterparts:**  
- Background `#0F1419`, Surface `#1A1F25`, Text `#E7EBF0`, Text Secondary `#8B97A4`, Divider `#2F3740`.  
- Maintain primary cyan untouched for recognition; adjust shadows to `rgba(0, 0, 0, 0.32)`.

### 4.2 Typography
- **Primary:** FK Grotesk Neue (weights 400, 500, 600, 700).  
- **Fallback stack:** `Inter, "SF Pro Display", Montserrat, Arial, sans-serif`.  
- **Headline styling:** weight 700, letter-spacing `-0.02em`; line-height 1.15–1.2.  
- **Body text:** weight 400–500, line-height 1.5; keep paragraphs under 80 characters width on desktop.  
- **Accents & labels:** weight 600 for key-value labels, badge titles.  
- **Number styles:** tabular lining for finances and timers.  
- **Language support:** ensure Cyrillic glyph coverage; validate font licensing for app distribution.

### 4.3 Iconography & Illustration
- **Icon library:** Lucide/Heroicons outline (2px stroke). Active states can fill with primary color.  
- **Sizes:** 16/24/32/48px; maintain consistent stroke.  
- **Illustrations:** friendly students, isometric university scenes, subtle gradients. Maintain brand palette with occasional complementary purples.  
- **Photography:** Bright, authentic campus scenes. Avoid staged stock feel. Minimum 800×800px, JPG/PNG, max 5MB.  
- **Video:** Up to 30s, MP4; use for product demos, event highlights.

### 4.4 Glassmorphism
- Apply to key surfaces (hero stats, floating cards) using `rgba(255,255,255,0.72)` background, backdrop blur 20px, border `1px solid rgba(255,255,255,0.4)`.  
- Limit usage to prevent performance issues; avoid on data-heavy tables.

## 5. Layout, Grid & Spacing
- **Spacing scale:** 2, 4, 8, 12, 16, 24, 32, 48, 64px (xxs → 4xl).  
- **Mobile grid:** 4px baseline grid, 16px horizontal padding, 8pt vertical rhythm.  
- **Tablet grid:** 12-column, 24px gutters, safe-area padding 24px.  
- **Desktop grid:** 12-column, 80px margins on large screens, max width 1280px for content.  
- **Safe zones:** 44px minimum touch targets, 12px min tap spacing.  
- **Elevation:** Level 1 `0 2px 8px rgba(0,0,0,0.06)`; Level 2 `0 8px 24px rgba(19,52,59,0.16)` for modals.

## 6. Component System

### 6.1 Buttons
- **Variants:** Primary (gradient fill), Secondary (outline), Ghost, Danger (solid red), Icon-only.  
- **Sizes:** Small 32px, Medium 44px, Large 56px.  
- **States:** Default, Hover (elevate shadow + lighten gradient), Active (scale 0.98, pressed shadow), Disabled (reduce opacity to 40%, retain text legibility), Loading (spinner or progress bar).  
- **Content rules:** Sentence case labels, avoid all caps. Leading icon optional (16px with 8px gap).

### 6.2 Inputs & Form Controls
- **Structure:** 12px radius, 1px border `#E5E7EB`, padding `12px 16px`.  
- **States:** Focus (primary border + glow), Error (red border + helper text), Success (green check icon), Disabled (muted text).  
- **Supporting elements:** Left icons (email, lock, search). Helper text 12px, 60% opacity.  
- **Complex controls:** Dropdowns with bottom sheet on mobile; toggle switches radius 16px, active fill primary gradient.

### 6.3 Cards
- 16px radius, white surface, Level 1 shadow.  
- Hover (desktop): scale 1.02, shadow to `0 12px 32px rgba(19,52,59,0.12)`.  
- **Content modules:**  
  - **Service cards:** 2×3 grid (icon, title, one-line description).  
  - **Product cards:** adopt provided marketplace layout; ensure text truncates at 2 lines.  
  - **Restaurant cards:** highlight promo badge at top-left.  
  - **Club cards:** cover image with overlay gradient for readability.

### 6.4 Navigation
- **Top Bar:** 56px height, logo left, action icons right with 16px spacing. Notification badge uses success green pulse animation.  
- **Bottom Navigation:** 5 tabs, 28px icons; active tab uses filled icon + label in primary color. Bottom-safe inset on iOS accounted.  
- **Service shortcuts:** horizontal chips (8px radius) with scroll bounce.

### 6.5 Avatars & Badges
- **Avatars:** 32/48/64/120px; group avatars overlap with 2px white border. Default gradient backgrounds with initials.  
- **Verification badges:**  
  - Student: gold gradient `#F6C56A → #F59E0B`.  
  - Seller: green gradient.  
  - Partner: deep blue gradient.  
  - Place badge at lower-right of avatar; add tooltips (“Verified KBTU student”).  
- **Status badges:** pill shape, 20–24px height, uppercase short labels.

### 6.6 Overlays & Feedback
- **Bottom sheets:** 12px top radius, drag handle center, glass backdrop blur. Use for filters, quick actions.  
- **Toasts:** slide from top, 4 sec default, include icon + close.  
- **Dialogs:** 24px radius, focus on single decision; include descriptive text.  
- **Skeleton loaders:** animate shimmer left-to-right, 1.2s duration.  
- **Progress indicators:** circular spinner for background tasks, linear progress for uploads.

### 6.7 Data Visualization
- Use brand palette with clear contrast; avoid more than 5 segments per chart.  
- Animations ease-out 400ms.  
- Provide tooltips with exact values and context labels.  
- Include legends or inline labels; ensure screen reader alt text.

## 7. Interaction & Motion
- **Motion principles:** purposeful, fast (<300ms), uses cubic-bezier `(0.22, 1, 0.36, 1)` for ease-out.  
- **Micro-animations:**  
  1. Button press ripple + scale 0.98.  
  2. Card tap bounce 1.02 scale then settle.  
  3. Tab switch slide-fade between panels.  
  4. Pull to refresh elastic overshoot + spinner.  
  5. Like/heart pop with particle burst.  
  6. Add-to-cart trajectory animation to nav icon.  
  7. Success checkmark draw + confetti (light).  
  8. Error shake ±6px.  
  9. Loading shimmer pulses.  
  10. Notification badge pulse every 6s when unread.  
- **Haptics:** Use medium impact for confirmations, light tap for toggles, warning vibration for errors (iOS/Android guidelines).  
- **Gestures:** swipe to archive/mute in chat, long-press for contextual actions (save, report).

## 8. Key Experience Flows

### 8.1 Onboarding & Authentication
- **Splash:** gradient background (day/evening/holiday variants), center logo fade-in, tagline “Your Student Life, Simplified”.  
- **Onboarding carousel:** 3 slides (Save Money, All-in-One, Community) with custom illustrations and CTA “Get started”. Include skip + progress dots.  
- **Registration:** Email/phone + password, social logins (Google, Apple), optional university verification (upload/student email). Enforce password strength meter.  
- **University selection:** searchable dropdown with logos; fallback manual entry; prompt verification upload for extra trust badge.

### 8.2 Home Dashboard
- **Top bar:** compact logo left, notifications/profile right.  
- **Hero band:** greeting (“Hey, Alizhan! 👋”), weather tile (glassmorphic), quick stats (balance, active orders, messages).  
- **Services grid:** 2×3 layout with category gradients; allow reordering in settings.  
- **Featured stories:** horizontally scrollable banners, auto-rotate 5s with pause on hover/interaction.  
- **Bottom nav:** Home, Marketplace, Food, Community, Profile.

### 8.3 Marketplace
- **Top:** search with filter icon, category chips (Textbooks, Notes, Coursework, Equipment).  
- **Filter drawer:** slides from right/bottom sheet mobile with controls for university, major, year, subject, condition, price slider, transaction type. Include “Save filter preset”.  
- **Product cards:** 16:9 image, title (2 lines), author/year, context (university, year, condition), price + likes.  
- **Detail page:** gallery, metadata (author, ISBN), condition photos, seller profile with rating, actions “Message seller”, “Add to favorites”, recommended items.  
- **Selling flow:** floating “+ Sell” button. Stepper (Photos → Details → Condition → Pricing → Preview). Autosave drafts.

### 8.4 Food Delivery
- **Restaurant list:** filter chips (Cuisine, Price, Rating, Time) + featured categories (“Student Portions”, “Under 1000₸”).  
- **Restaurant card:** cover image, promo badge, rating/time, price range, cuisine.  
- **Menu page:** sticky category navigation, popular dishes pinned, dish card with photo, description, calories, price, “+” button.  
- **Cart:** floating CTA “Cart (3) • 3 500₸”, bottom sheet summary, add promo code, payment method selection, delivery address (map view), delivery time, order comments.  
- **Order tracking:** timeline (Accepted → Preparing → On the way → Delivered), live map, courier info, ETA countdown.

### 8.5 Community
- **Club directory:** category tabs (Arts, Sports, Gaming, etc.), search.  
- **Club card:** cover + avatar overlay, member count, meeting schedule, actions [Join] [Info].  
- **Details:** description, member avatars, upcoming events, media gallery, club chat, admin-only “Create event”.  
- **Events feed:** calendar toggle, list with event card (datetime, location, organizer, attendees, CTA “I’m going”).

### 8.6 Tutors & Roommates
- **Tabs:** Tutors | Roommates.  
- **Tutor cards:** avatar (80px), name, university/year, subject list, rating, hourly price, actions [Message] [Book].  
- **Filters:** subject, university, year, price, rating, format (Online/Offline).  
- **Roommates:** filter by gender, age, university, district, budget, lifestyle, interests. Profile detail includes compatibility tags and button to start chat.

### 8.7 FinTech Module
- **Dashboard:** virtual student card, balance, quick actions (Top up, Transfer, Split bill).  
- **Analytics:** pie chart for spending categories, line chart for trends, show cashback earned.  
- **Transactions:** card with merchant icon, date/time, amount, cashback. Provide receipt view and dispute option.  
- **Features:** university payments, financial planning goals, escrow status for marketplace deals.

### 8.8 Profile & Settings
- **Header:** editable cover, centered avatar (120px) with verification badges, name/university/year, “Edit profile” CTA.  
- **Stats row:** Orders, Rating, Friends.  
- **Sections:** My Listings, Order History, Favorites, Reviews, Settings, My Studies (schedule + grades), My Clubs, Savings & transactions.  
- **Settings:** personal info, security (2FA), notifications (push/email toggles), privacy, language (RU/KZ/EN), theme (Light/Dark/Auto), university link, about/support.

### 8.9 Messaging & Notifications
- **Chat list:** avatar, name, preview, timestamp, unread badge, online indicator. Swipe actions (Archive, Delete, Mute).  
- **Chat room:** bubble layout (own messages right with primary color, others left grey), grouped timestamps, read receipts (double checkmark), typing indicator, attachments (photos, video, voice notes, stickers, quick replies).  
- **Notification center:** slide from right, categories (Orders, Messages, System, Promo), mark all as read, granular notification settings.  
- **Push template:** icon, title, message, time stamp.

### 8.10 Search & Discovery
- Search bar with icon, voice input, recent and popular searches.  
- Filter chips, advanced modal, save presets, “Clear all”.  
- Results show relevance score, “Did you mean” suggestions, related searches, empty state with recommendations.

### 8.11 Gamification & Trust
- **Achievements:** badge collection (First Purchase, Seller of the Month, Active Member, Eco Student). Display in profile.  
- **Loyalty tiers:** Newbie → Student → Veteran → Legend; show progress bar and perks.  
- **Referral:** unique code, share modal with preview card, track invites.  
- **Trust & safety:** verification indicators (student, seller, partner), 5-star reviews with photos, verified purchase badge, helpful votes, report/block actions, safety guidelines.

### 8.12 Support & Emergency
- **Emergency contacts widget:** Dean’s office, dormitory, medical center, tech support; accessible from profile and quick settings.  
- **Campus mode:** auto-detect campus, surface campus-only offers and services, highlight map shortcuts.  
- **Study timer:** pomodoro with stats, integrates with schedule.  
- **Group orders:** collaborative food order flow, bill splitting, coordination chat.

## 9. Accessibility & Inclusivity
- Minimum contrast 4.5:1 for text/iconography. Validate gradients with accessible overlays.  
- Touch targets ≥44×44px; maintain spacing for gesture accuracy.  
- Provide ARIA labels and content descriptions for screen readers.  
- Keyboard navigation: logical focus order, visible focus states.  
- Duplicate color indicators with text/icons for colorblind users.  
- Provide subtitles/captions for video content; accessible error messages linked to fields.  
- Ensure motion-reduced mode—disable confetti & large animations when OS reduce motion is on.

## 10. Localization & Culturalization
- Languages: Russian (default), Kazakh, English.  
- Support localized currency `₸` with grouping (e.g., `5 000 ₸`).  
- Adjust date/time format to `DD MMM YYYY`.  
- Include localized holidays in splash themes and event recommendations.  
- No RTL required; keep copy length flexible (allow 30% expansion).  
- Illustrations should reflect diverse Kazakh student life.

## 11. Responsiveness & Platforms
- **Breakpoints:** Mobile 320–428px, Tablet 768–1024px, Desktop ≥1280px.  
- **Adaptive patterns:**  
  - Mobile: stacked content, bottom sheets, full-screen modals.  
  - Tablet: two-column layouts for lists + detail; persistent filters in sidebar.  
  - Desktop (web app/admin): multi-column grids, enlarged hero modules.  
- Respect safe areas on iOS/Android, handle notch/punch-hole spaces.  
- Provide offline messaging for poor network states (cached content, retry prompts).

## 12. Design Ops & Figma Structure
- **File organization:**
  ```
  📁 StudenKZ Design System
    ├── 🎨 Brand (colors, typography, logo assets)
    ├── 🧩 Components (atoms → organisms)
    ├── 📱 Screens (Onboarding, Home, Marketplace, Food Delivery, Community, Tutors & Roommates, FinTech, Profile, Messaging)
    ├── 🌙 Dark Mode variants
    ├── 📐 Templates (flows, responsive frames)
    └── 📚 Documentation (usage notes, redlines)
  ```
- **Component naming:** `Category / Component / Variant / State` (e.g., `Button/Primary/Medium/Loading`).  
- **Auto-layout:** enforce spacing tokens, padding, responsiveness.  
- **Variant properties:** state, size, theme, language as needed.  
- **Annotations:** use callouts for interaction notes, transition timings, accessibility considerations.  
- **Prototyping:** leverage Smart Animate for tab transitions, overlays for bottom sheets, maintain 300ms transitions. Include scroll behaviors and fixed headers. Show keyboard on focused inputs.  
- **Asset export:** prepare @1x/@2x/@3x PNG/SVG. Optimize icons for 24px baseline.

## 13. QA & Pre-Launch Checklist
- [ ] All screens responsive (iPhone SE → iPhone 14 Pro Max).  
- [ ] Dark mode parity for screens and components.  
- [ ] Empty, error, and loading states covered.  
- [ ] Accessibility labels + focus order validated.  
- [ ] Animations under 300ms; reduced motion compliance.  
- [ ] Touch targets ≥44px.  
- [ ] Copy proofread in Russian & Kazakh.  
- [ ] Localization applied to dates, currency, measurement.  
- [ ] Performance check on glassmorphism usage.  
- [ ] Interactive prototype with primary flows (onboarding, purchase, order, booking, transfer).

## 14. Contacts & Timeline
- **Design owner:** Alizhan Bizhan — `alizhan695@gmail.com`, Telegram `@alizhan006`.  
- **MVP deadline:** December 2025.  
- **Target release:** Q1 2026.

---
This document consolidates the StudenKZ experience blueprint. Use it as the single source of truth for product, design, and engineering teams while iterating toward Kazakhstan’s leading student super-platform.
