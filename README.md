# StudenKZ Design System & UI/UX Specifications

## Product Snapshot
- **Product:** StudenKZ — Kazakhstan’s first student-focused digital super-platform
- **Tagline:** One App. All Student Needs.
- **Audience:** Tech-savvy Gen Z university students (17–25), budget-aware, socially active, 500K+ users nationwide
- **MVP Deadline:** December 2025
- **First Release:** Q1 2026

## Brand Identity & Voice
- **Attributes:** Modern, youthful, dynamic, trustworthy, community-first
- **Primary Tone:** Supportive, energetic, pragmatic
- **Secondary Tone:** Empowering, inclusive, witty microcopy for delight moments

### Color Tokens
| Token | Hex | Usage |
| --- | --- | --- |
| `color-primary` | `#1FB8CD` | Accents, active states, CTAs |
| `color-secondary` | `#13343B` | Core text, headers, strong contrasts |
| `color-accent` | `#5D878F` | Secondary UI elements, dividers |
| `color-success` | `#34D399` | Success feedback, confirmations |
| `color-background` | `#FCFCF9` | App background, large surfaces |
| `color-surface` | `#FFFFFF` | Cards, modals, floating panels |

### Dark Mode Tokens
| Token | Hex | Usage |
| --- | --- | --- |
| `dark-background` | `#0F1419` | Base background |
| `dark-surface` | `#1A1F25` | Cards, sheets |
| `dark-text-primary` | `#E7EBF0` | Primary text |
| `dark-text-secondary` | `#8B97A4` | Secondary text |
| `dark-border` | `#2F3740` | Dividers, outlines |

### Typography
- **Primary Typeface:** FK Grotesk Neue (fallbacks: Inter, SF Pro Display, Montserrat)
- **Heading Styles:** Weight 700, letter-spacing −0.02em, include responsive scaling
- **Body Text:** Weight 400–500, line-height 1.5–1.6
- **Accent Text:** Weight 600 for highlights, buttons, and emphasized labels
- **Guidelines:** Maintain hierarchy clarity, pair typography with iconography for accessibility

### Iconography & Illustration
- **Icon Set:** Lucide Icons / Heroicons (outline + optional fill for active state)
- **Icon Sizes:** 16, 24, 32, 48 px; stroke width 2 px
- **Illustrations:** Flat, youthful characters, light gradients, localized cultural cues, occasional isometric accents

## Design Tokens & Foundations
- **Spacing Scale:** 2, 4, 8, 12, 16, 24, 32, 48, 64 px
- **Border Radius:** 8–16 px for cards and surfaces; 12 px for inputs; 50% for avatars; 100 px for badges
- **Elevation Levels:** Glassmorphism feel via subtle blur + 0 2px 8px rgba(0,0,0,0.06); increase shadow on hover
- **Gradients:** Cyan → purple blends for hero areas, buttons, highlight cards
- **Glassmorphism:** Apply controlled blur and transparency for premium overlays (eg. bottom sheets)
- **Breakpoints:** Mobile 320–428 px, Tablet 768–1024 px, Desktop 1280+ px; maintain responsive grid

## Component Library
- **Buttons:** Primary gradient (cyan → purple), secondary outline, ghost, danger; sizes 32/44/56 px; states include hover, active, disabled, loading; add 0.98 scale on press and ripple effect
- **Inputs:** 12 px radius, 1 px border `#E5E7EB`, icon support, success checkmark, error red border, focus glow in primary color
- **Cards:** White surface, 16 px radius, 16–24 px padding, drop shadow; hover scale 1.02 with stronger shadow
- **Avatars:** 32/48/64/120 px, circular; gradient placeholders with initials; add 2 px white border for group display
- **Badges:** Pill shape, 20/24 px height, variants (Success, Warning, Error, Info, Neutral), use for NEW/HOT/-20%/VERIFIED
- **Bottom Sheets:** Blur backdrop, top handle, smooth slide-up; ideal for filters and quick actions
- **Toasts:** Slide from top, bounce entry, auto-dismiss 3–5 s; support success, error, info, warning
- **Loading States:** Skeletons, shimmer placeholders, button spinners, upload progress bars

## Core Experience Map

### Onboarding & Authentication
- **Splash:** Animated logo over cyan → purple gradient; tagline “Your Student Life, Simplified”
- **Onboarding Carousel (3 slides):** Save Money, All-in-One, Community — each with custom illustration, headline, description
- **Registration:** Email/phone + password, social login (Google, Apple), optional university verification and selection

### Home
- **Top Bar:** Compact logo left; notification icon with badge; profile avatar right
- **Hero:** Personalized greeting (“Hey, Alizhan! 👋”), weather + university location, quick stats (balance, active orders, new messages)
- **Service Grid:** 2×3 layout with gradient cards for Marketplace, Food, Clubs & Events, Tutors & Roommates, FinTech Services, Deals & Discounts; include icon, title, one-line copy, subtle depth
- **Featured Banners:** Horizontal scroll, auto-rotate every 5 s for promos/events/news
- **Bottom Navigation:** Five tabs (Home, Marketplace, Food, Community, Profile); active tab uses primary color + filled icon

### Marketplace (Textbooks & Materials)
- **Top Bar:** Search with filters, quick category tabs (Textbooks, Notes, Coursework, Equipment), sort options (Price, Date, Popularity)
- **Filters Sheet:** University, major, year, subject, condition, price range, transaction type (Sale/Rent/Exchange)
- **Product Card:** 16:9 image, title, author/year, context chips (eg. 🎓 KBTU • Year 2, 📊 Excellent), price and likes
- **Detail Page:** Gallery, meta (title, author, ISBN), description, condition evidence, buy/rent toggle, seller info, CTA buttons, similar items carousel
- **Selling Flow:** Floating “+” entry; steps for photos (≤5), details, condition, price/terms, preview & publish

### Food Delivery
- **Restaurant List:** Filters for cuisine, price, rating, delivery time; highlight “Student Portions”, “Under 1000₸”
- **Restaurant Card:** Banner image, promo badge (eg. 🏷️ −20% first order), rating, time, price range, cuisine tags
- **Menu Page:** Sticky categories, popular dishes first, dish cards with 1:1 photo, details, price, add button
- **Cart & Checkout:** Floating CTA showing items + total; include address selector with map, promo codes, payment method, delivery time, order comments
- **Order Tracking:** Stage tracker (Accepted → Preparing → On the way → Delivered), live map, courier profile, ETA countdown

### Community (Clubs & Events)
- **Categories:** Arts, Sports, Gaming, Academic, Music, Debate, Travel, Entrepreneurship
- **Club Cards:** Cover + avatar, member count, meeting schedule, “Join” and “Info” buttons
- **Club Detail:** Description, member avatars, upcoming events, gallery, chat, admin “Create Event”
- **Events Feed:** Calendar + list views, filters (Today/Week/Month/All), event cards with time, location, organizer, attendee count, “I’m Going” CTA

### Tutors & Roommates
- **Tabs:** Tutors, Roommates
- **Tutor Cards:** Avatar, university/year, subjects list, rating/reviews, rate, “Message” and “Book” CTAs
- **Tutor Filters:** Subject, university, year, price range, rating, format (Online/Offline)
- **Roommate Filters:** Gender, age, university, district, budget, lifestyle, interests

### FinTech Services
- **Dashboard:** Virtual student card, current balance, transaction feed, spending analytics (pie chart)
- **Actions:** Top up, transfer, university payments, cashback tracker (3–5%), split bill, financial planning
- **Transaction Card:** Merchant icon, timestamp, amount change, cashback highlight

### Profile
- **Header:** Editable cover, centered 120 px avatar, name, university, year, “Edit Profile”
- **Stats Row:** Orders, rating, friends
- **Sections:** My Listings, Order History, Favorites, Reviews, Settings, My Studies, My Clubs, Statistics
- **Settings:** Personal info, security, notifications, privacy, language (RU/KZ/EN), theme (Light/Dark/Auto), university link, about, support

## Differentiating Features
- **Student Verification Badge:** Gold gradient badge with tooltip “Verified KBTU Student”
- **Campus Mode:** Auto-detect campus; unlock campus-only offers, quick campus services
- **Study Timer:** Pomodoro with productivity analytics and schedule sync
- **Group Orders:** Shared food cart with bill split and coordination chat
- **Emergency Contacts:** Quick-access list (Dean’s office, dorm, medical, tech support)

## Motion & Micro-Interactions
- Button press (scale 0.98 + ripple), card tap bounce, sliding tab transitions, elastic pull-to-refresh, heart pop particles, add-to-cart fly animation, success confetti, error shake, skeleton pulse, notification badge pulse
- Keep animations ≤300 ms; apply Smart Animate and haptic feedback cues in prototypes

## Accessibility & Inclusivity
- Minimum contrast 4.5:1 across light/dark modes
- Touch targets ≥44×44 px
- Provide screen reader labels, keyboard focus states, icon + text redundancy for critical statuses
- Localized copy proofread in Russian and Kazakh; maintain consistent tone

## Localization & Regionalization
- Languages: Russian (default), Kazakh, English
- No RTL requirement
- Localized dates, currency (₸), academic calendars, university-specific imagery
- Themed splash backgrounds for day/evening/holidays (Nauryz, New Year)

## Data Visualization
- Charts: Pie (spending), line (usage), bar (comparisons), donut (goals)
- Use brand palette, smooth entrance animation, interactive tooltips, minimalist legends

## Notifications & Messaging
- **Push Template:** Compact card with logo, title, message, timestamp
- **In-App Center:** Slide-in panel with categories (Orders, Messages, System, Promo), mark-all-read, per-category settings
- **Chat Experience:** Bubble layout (user right/primary color, others left/neutral), timestamps grouped, read receipts, typing indicator, support for media, voice, stickers, quick replies, saved messages; chat list with avatars, preview, time, unread badge, online indicator, swipe actions

## Gamification & Trust
- **Achievements:** First Purchase, Seller of the Month, Active Member, Eco Student; display badges on profile
- **Loyalty Levels:** Newbie → Student → Veteran → Legend with progress bar and perks
- **Referral Program:** “Invite a friend – get 1000₸” with shareable code and tracking
- **Safety:** Verification badges (student blue, seller green, partner gold), ratings/reviews with photos, verified purchase marker, helpful votes, report/block actions, escrow transactions, guidelines & FAQ

## Media & Content Management
- **Photo Specs:** ≥800×800 px, JPG/PNG, ≤5 MB; 1:1 products, 16:9 banners, 3:4 profile
- **Tools:** Auto optimization, crop/rotate, optional filters, watermarking
- **Video Support:** ≤30 s clips for demos and event stories
- **Share Cards:** Include preview image, pricing, branding, “Download the app” CTA; integrate QR codes for payments, invites, club joins

## University Integrations
- **University Hub:** Class schedule, grades, news, campus map, dean contacts
- **Campus Services:** Document requests, consultation booking, room reservations, library search

## Prototyping & Handoff
- **File Structure:**  
  📁 StudenKZ Design System  
  ├── 🎨 Brand (colors, typography, logos)  
  ├── 🧩 Components (buttons, inputs, cards, navigation, icons)  
  ├── 📱 Screens (Onboarding, Home, Marketplace, Food Delivery, Community, FinTech, Profile)  
  ├── 🌙 Dark Mode  
  ├── 📐 Templates  
  └── 📚 Documentation
- **Prototype Guidance:** Use Smart Animate, overflow scrolling, keyboard overlays, haptic annotations
- **Handoff:** Clear naming, component states, px measurements, asset exports @1x/@2x/@3x, annotate complex interactions

## Pre-Launch Checklist
- [ ] Responsive (iPhone SE → iPhone 14 Pro Max)
- [ ] Full dark mode coverage
- [ ] Empty states for all flows
- [ ] Error states with clear recovery
- [ ] Loading states across key steps
- [ ] Accessibility labels verified
- [ ] Animations under 300 ms
- [ ] Touch targets ≥44×44 px
- [ ] Contrast validated
- [ ] Russian and Kazakh copy proofed

## Contact
- **Product Lead:** Alizhan Bizhan  
- **Email:** alizhan695@gmail.com  
- **Telegram:** @alizhan006

Let’s build the definitive student experience for Kazakhstan!