# StudenKZ Screen Specifications
## Detailed Screen-by-Screen Documentation

---

## 📋 Table of Contents
1. [Onboarding & Authentication](#onboarding--authentication)
2. [Home Screen](#home-screen)
3. [Marketplace](#marketplace)
4. [Food Delivery](#food-delivery)
5. [Community](#community)
6. [Tutors & Roommates](#tutors--roommates)
7. [FinTech Services](#fintech-services)
8. [Profile](#profile)
9. [Additional Screens](#additional-screens)

---

## Onboarding & Authentication

### 1.1 Splash Screen

**Purpose:** Brand introduction, app loading

**Layout:**
```
┌────────────────────────┐
│                        │
│                        │
│                        │
│      [StudenKZ         │
│         Logo]          │
│                        │
│                        │
│  "Your Student Life,   │
│     Simplified"        │
└────────────────────────┘
```

**Elements:**
- Background: Gradient (Cyan #1FB8CD → Purple #8B5CF6)
- Logo: Centered, 120×120px
- Tagline: 14px, white, opacity 0.9
- Animation: Logo scale up + fade in (800ms)
- Duration: 2-3 seconds

**Variants:**
- **Day Mode:** Light gradient
- **Evening Mode:** Dark gradient
- **Holiday Themes:** Nauryz, New Year, etc.

---

### 1.2 Onboarding Flow

**Navigation:** 3 screens with skip option

#### Screen 1: "Save Money"
```
┌────────────────────────┐
│        [Skip]          │
│                        │
│   [Illustration:       │
│    Student with        │
│    books & coins]      │
│                        │
│  Save up to 50%        │
│  on textbooks          │
│                        │
│  Buy, sell and         │
│  exchange materials    │
│                        │
│   ● ○ ○    [Next →]   │
└────────────────────────┘
```

**Elements:**
- Skip button: Top-right, ghost style
- Illustration: 240×240px, centered
- Title: 24px, 700 weight
- Description: 14px, secondary text
- Progress dots: Bottom-center
- Next button: Bottom-right, primary

#### Screen 2: "All-in-One"
**Focus:** Multiple services in one app
**Illustration:** Smartphone with floating service icons

#### Screen 3: "Community"
**Focus:** Social features and networking
**Illustration:** Group of diverse students
**Button:** "Get Started" instead of "Next"

---

### 1.3 Registration Screen

```
┌────────────────────────────┐
│ [← Back]      Registration │
│                            │
│  Create your account       │
│                            │
│  Email or Phone            │
│  ┌──────────────────────┐ │
│  │ your@email.com       │ │
│  └──────────────────────┘ │
│                            │
│  Password                  │
│  ┌──────────────────────┐ │
│  │ ••••••••        👁️   │ │
│  └──────────────────────┘ │
│                            │
│  University (optional)     │
│  ┌──────────────────────┐ │
│  │ Select university ▾  │ │
│  └──────────────────────┘ │
│                            │
│  ☐ I agree to Terms       │
│                            │
│  [Register]                │
│                            │
│  ─── or continue with ───  │
│                            │
│  [🔵 Google] [🍎 Apple]   │
│                            │
│  Already registered? Login │
└────────────────────────────┘
```

**Fields:**
- Email/Phone (with validation)
- Password (with strength indicator)
- University selection (dropdown)
- Terms agreement (checkbox)

**Social Login:**
- Google OAuth
- Apple Sign In
- Auto-fills profile data

---

### 1.4 Login Screen

```
┌────────────────────────────┐
│ [← Back]          Login    │
│                            │
│  Welcome back! 👋          │
│                            │
│  Email or Phone            │
│  ┌──────────────────────┐ │
│  │                      │ │
│  └──────────────────────┘ │
│                            │
│  Password                  │
│  ┌──────────────────────┐ │
│  │ ••••••••        👁️   │ │
│  └──────────────────────┘ │
│                            │
│         Forgot password?   │
│                            │
│  [Login]                   │
│                            │
│  ─── or continue with ───  │
│                            │
│  [🔵 Google] [🍎 Apple]   │
│                            │
│  New here? Register        │
└────────────────────────────┘
```

**Features:**
- Remember me option
- Biometric login (after first login)
- "Forgot password" flow
- Social login shortcuts

---

### 1.5 University Verification

```
┌────────────────────────────┐
│ [← Back]   University ID   │
│                            │
│  Verify your student       │
│  status                    │
│                            │
│  [Upload student ID photo] │
│                            │
│  ┌──────────────────────┐ │
│  │   [📷 Take photo]    │ │
│  │   [📁 From gallery]  │ │
│  └──────────────────────┘ │
│                            │
│  Student ID Number         │
│  ┌──────────────────────┐ │
│  │                      │ │
│  └──────────────────────┘ │
│                            │
│  University                │
│  ┌──────────────────────┐ │
│  │ KBTU              ▾  │ │
│  └──────────────────────┘ │
│                            │
│  [Submit for verification] │
│                            │
│  ⏱️ Verification takes     │
│     24-48 hours           │
└────────────────────────────┘
```

---

## Home Screen

### 2.1 Main Home Screen

```
┌────────────────────────────┐
│ [Logo]            🔔 👤   │
├────────────────────────────┤
│                            │
│  Hey, Alizhan! 👋          │
│  ☀️ 22°C • KBTU Campus     │
│                            │
│  ┌──────────────────────┐ │
│  │ Balance: 45,000₸     │ │
│  │ Active orders: 2     │ │
│  │ New messages: 5      │ │
│  └──────────────────────┘ │
│                            │
│  Quick Access:             │
│  ┌─────────┬──────────┐   │
│  │ 📖      │ 🍔       │   │
│  │ Market  │ Food     │   │
│  │ place   │ Delivery │   │
│  ├─────────┼──────────┤   │
│  │ 👥      │ 🎓       │   │
│  │ Clubs & │ Tutors & │   │
│  │ Events  │ Rooms    │   │
│  ├─────────┼──────────┤   │
│  │ 💳      │ 🎁       │   │
│  │ FinTech │ Deals &  │   │
│  │ Services│ Discounts│   │
│  └─────────┴──────────┘   │
│                            │
│  Featured Deals ─────────→ │
│  ┌──────────────────────┐ │
│  │ [Banner carousel]    │ │
│  └──────────────────────┘ │
│                            │
│  Recent Activity           │
│  • Your order delivered    │
│  • New club event          │
│                            │
├────────────────────────────┤
│ 🏠  🛍️  🍔  👥  👤        │
│ Home Shop Food Social Me   │
└────────────────────────────┘
```

**Sections:**

1. **Top Bar (64px)**
   - Logo (32px)
   - Notification bell (badge if new)
   - Profile avatar (32px)

2. **Hero Section**
   - Personalized greeting
   - Weather widget + location
   - Quick stats card (glassmorphism effect)

3. **Service Grid (2×3)**
   - Each card: 160×140px
   - Gradient backgrounds (unique per service)
   - Icon: 48×48px
   - Title: 16px, 700 weight
   - Description: 12px
   - Tap to navigate

4. **Featured Banner**
   - Horizontal scroll
   - Auto-rotate every 5 seconds
   - Pagination dots
   - 16:9 aspect ratio

5. **Recent Activity Feed**
   - Last 5 activities
   - Icons + text
   - Timestamp
   - Tap to view details

6. **Bottom Navigation (72px)**
   - 5 tabs evenly spaced
   - Icons: 24×24px
   - Labels: 10px
   - Active state: Primary color

---

### 2.2 Service Cards Details

#### Marketplace Card
```
┌─────────────────┐
│ 📖             │
│                 │
│ Marketplace     │
│ Buy & sell      │
│ textbooks       │
│                 │
│ NEW 12 items    │
└─────────────────┘
```
- Gradient: Blue-Cyan
- Badge: New item count

#### Food Delivery Card
```
┌─────────────────┐
│ 🍔             │
│                 │
│ Food Delivery   │
│ Order from      │
│ restaurants     │
│                 │
│ -20% PROMO      │
└─────────────────┘
```
- Gradient: Orange-Red
- Badge: Current promo

#### Clubs & Events Card
- Gradient: Purple-Pink
- Badge: Upcoming events count

#### Tutors & Roommates Card
- Gradient: Green-Teal
- Badge: New tutors available

#### FinTech Services Card
- Gradient: Indigo-Purple
- Badge: Cashback earned

#### Deals & Discounts Card
- Gradient: Yellow-Orange
- Badge: Active deals count

---

### 2.3 Notification Center

```
┌────────────────────────────┐
│ [← Back]   Notifications   │
│ [Mark all read] [Settings] │
├────────────────────────────┤
│  Today                     │
│                            │
│  🔵 Order Delivered        │
│  Your textbook "Math" has  │
│  been delivered            │
│  5 minutes ago             │
│                            │
│  💬 New Message            │
│  Aida sent you a message   │
│  about the textbook        │
│  1 hour ago                │
│                            │
│  Yesterday                 │
│                            │
│  🎉 New Club Event         │
│  Robotics Club meeting     │
│  scheduled for Friday      │
│  Yesterday, 8:30 PM        │
│                            │
│  📦 Order Update           │
│  Your order is on the way  │
│  Yesterday, 3:15 PM        │
└────────────────────────────┘
```

**Features:**
- Grouped by date
- Icon-coded by type
- Swipe to delete
- Tap to view details
- Filter by category
- Mark as read/unread

---

## Marketplace

### 3.1 Marketplace Home

```
┌────────────────────────────┐
│ [← Back]    Marketplace    │
│ ┌────────────────────────┐ │
│ │ 🔍 Search books...     │ │
│ └────────────────────────┘ │
│                            │
│ All • Books • Notes •      │
│ Equipment • Coursework     │
│                            │
│ [Filter] [Sort]            │
│                            │
│ ┌──────────┬──────────┐   │
│ │ [Image]  │ [Image]  │   │
│ │ Math     │ Physics  │   │
│ │ Year 2   │ Year 1   │   │
│ │ 5,000₸  │ 3,500₸  │   │
│ ├──────────┼──────────┤   │
│ │ [Image]  │ [Image]  │   │
│ │ English  │ History  │   │
│ │ Year 3   │ Year 2   │   │
│ │ 4,200₸  │ 2,800₸  │   │
│ └──────────┴──────────┘   │
│                            │
│ [+ Add Listing]            │
└────────────────────────────┘
```

**Features:**
- Search bar with autocomplete
- Category tabs (horizontal scroll)
- Filter button (opens side panel)
- Sort options (price, date, popularity)
- Grid view (2 columns on mobile)
- Floating action button for new listing

---

### 3.2 Product Card (Grid View)

```
┌──────────────────┐
│  [Image 1:1]     │
│  NEW             │ ← Badge
│  ❤️              │ ← Favorite
├──────────────────┤
│ Higher Math      │
│ Year 2           │
│                  │
│ 🎓 KBTU • Y2     │
│ 📊 Excellent     │
│                  │
│ 5,000 ₸   ❤️ 24 │
└──────────────────┘
```

**Elements:**
- Image: 1:1 aspect ratio
- Badge: NEW, SALE, HOT (top-left)
- Favorite button: Top-right heart
- Title: 14px, 600 weight, 2 lines max
- Context: University, year
- Condition indicator with icon
- Price: 16px, 700 weight
- Like count

---

### 3.3 Filters Panel

```
┌────────────────────────────┐
│ Filters          [✓ Apply] │
├────────────────────────────┤
│                            │
│ University                 │
│ ☑ KBTU                     │
│ ☐ Nazarbayev University    │
│ ☐ AITU                     │
│ ☐ Satbayev University      │
│                            │
│ Category                   │
│ • All                      │
│ ○ Textbooks                │
│ ○ Notes                    │
│ ○ Coursework               │
│                            │
│ Year                       │
│ ☐ 1  ☐ 2  ☐ 3  ☐ 4        │
│                            │
│ Condition                  │
│ ☑ Excellent  ☑ Good        │
│ ☐ Fair       ☐ New         │
│                            │
│ Price Range                │
│ ├─────●─────●─────┤        │
│ 0₸         50,000₸        │
│                            │
│ Transaction Type           │
│ ☑ Sale  ☑ Rent  ☐ Exchange│
│                            │
│ [Clear All]  [Apply]       │
└────────────────────────────┘
```

**Interaction:**
- Slides in from right
- Backdrop with blur
- Real-time result count update
- Save filter presets option

---

### 3.4 Product Detail Page

```
┌────────────────────────────┐
│ [← Back]  📤 Share  ❤️     │
├────────────────────────────┤
│ ┌────────────────────────┐ │
│ │  [Image Gallery]       │ │
│ │  ← • • • • →           │ │
│ └────────────────────────┘ │
│                            │
│ Higher Mathematics         │
│ Year 2 Textbook            │
│                            │
│ ⭐ 4.8 • 24 reviews        │
│                            │
│ 7,500 ₸                    │
│ 🏷️ -25% (was 10,000₸)     │
│                            │
│ Description                │
│ Comprehensive textbook for │
│ second-year mathematics... │
│                            │
│ Details                    │
│ • Author: Smith & Jones    │
│ • Edition: 5th Edition     │
│ • Year: 2023               │
│ • ISBN: 978-1234567890     │
│ • Condition: Excellent     │
│   (Minor highlights)       │
│                            │
│ Condition Photos           │
│ [📷] [📷] [📷]             │
│                            │
│ 🎓 KBTU • Year 2           │
│ 📊 Excellent condition     │
│                            │
│ ┌────────────────────────┐ │
│ │ [Avatar] Aida K.       │ │
│ │ ⭐ 4.9 (23 ratings)     │ │
│ │ Member since 2024      │ │
│ │ [View Profile →]       │ │
│ └────────────────────────┘ │
│                            │
│ Similar Items              │
│ ┌───┬───┬───┐             │
│ │ • │ • │ • │             │
│ └───┴───┴───┘             │
│                            │
├────────────────────────────┤
│ [💬 Message] [🛒 Buy Now] │
└────────────────────────────┘
```

**Sections:**
1. Image gallery (swipeable, pinch to zoom)
2. Title and subtitle
3. Rating and review count
4. Price with discount badge
5. Description (expandable)
6. Item details
7. Condition photos
8. Context badges
9. Seller card
10. Similar items carousel
11. Action buttons (sticky bottom)

---

### 3.5 Create Listing Flow

#### Step 1: Photos
```
┌────────────────────────────┐
│ [✓ Done]    Add Photos     │
├────────────────────────────┤
│  Add up to 5 photos        │
│                            │
│  ┌────┬────┬────┬────┬──┐ │
│  │ +  │    │    │    │  │ │
│  │📷  │    │    │    │  │ │
│  └────┴────┴────┴────┴──┘ │
│                            │
│  Tips:                     │
│  • Good lighting           │
│  • Show condition clearly  │
│  • Include all angles      │
│                            │
│  [Continue]                │
└────────────────────────────┘
```

#### Step 2: Details
```
┌────────────────────────────┐
│ [← Back]    Item Details   │
├────────────────────────────┤
│  Category                  │
│  ┌──────────────────────┐ │
│  │ Textbooks         ▾  │ │
│  └──────────────────────┘ │
│                            │
│  Title *                   │
│  ┌──────────────────────┐ │
│  │                      │ │
│  └──────────────────────┘ │
│                            │
│  Author                    │
│  ┌──────────────────────┐ │
│  │                      │ │
│  └──────────────────────┘ │
│                            │
│  ISBN (optional)           │
│  ┌──────────────────────┐ │
│  │                      │ │
│  └──────────────────────┘ │
│                            │
│  Description              │
│  ┌──────────────────────┐ │
│  │                      │ │
│  │                      │ │
│  │                      │ │
│  └──────────────────────┘ │
│                            │
│  [Continue]                │
└────────────────────────────┘
```

#### Step 3: Condition
```
┌────────────────────────────┐
│ [← Back]    Condition      │
├────────────────────────────┤
│  Select condition:         │
│                            │
│  ● Excellent               │
│    Like new, minimal wear  │
│                            │
│  ○ Good                    │
│    Minor wear, readable    │
│                            │
│  ○ Fair                    │
│    Noticeable wear         │
│                            │
│  ○ New                     │
│    Sealed, never used      │
│                            │
│  Add condition notes:      │
│  ┌──────────────────────┐ │
│  │ Minor highlighting   │ │
│  │ on pages 45-60       │ │
│  └──────────────────────┘ │
│                            │
│  [Continue]                │
└────────────────────────────┘
```

#### Step 4: Pricing
```
┌────────────────────────────┐
│ [← Back]    Price & Terms  │
├────────────────────────────┤
│  Transaction Type          │
│  ☑ Sale  ☐ Rent  ☐ Exchange│
│                            │
│  Price                     │
│  ┌──────────────────────┐ │
│  │ 5,000            ₸   │ │
│  └──────────────────────┘ │
│                            │
│  💡 Suggested: 4,500-6,000₸│
│                            │
│  Negotiable?               │
│  ☑ Yes, open to offers     │
│                            │
│  Location                  │
│  ┌──────────────────────┐ │
│  │ KBTU Campus       ▾  │ │
│  └──────────────────────┘ │
│                            │
│  Meetup options           │
│  ☑ Campus meetup          │
│  ☐ Home delivery          │
│                            │
│  [Continue]                │
└────────────────────────────┘
```

#### Step 5: Preview & Publish
```
┌────────────────────────────┐
│ [← Back]    Preview        │
├────────────────────────────┤
│  [Product card preview]    │
│                            │
│  ✓ Photos uploaded         │
│  ✓ Details complete        │
│  ✓ Condition specified     │
│  ✓ Price set               │
│                            │
│  Listing visibility        │
│  ● Public                  │
│  ○ University only         │
│  ○ Year only               │
│                            │
│  [📝 Edit]  [✓ Publish]   │
└────────────────────────────┘
```

---

## Food Delivery

### 4.1 Food Home Screen

```
┌────────────────────────────┐
│ [← Back]    Food Delivery  │
│ ┌────────────────────────┐ │
│ │ 📍 KBTU Campus     ▾   │ │
│ └────────────────────────┘ │
│                            │
│ ┌────────────────────────┐ │
│ │ 🔍 Search restaurants  │ │
│ └────────────────────────┘ │
│                            │
│ All • Fast Food • Asian •  │
│ European • Desserts •      │
│                            │
│ 🎯 Student Favorites       │
│ ┌──────────────────────┐  │
│ │ [Restaurant Card]    │  │
│ │ -20% First Order     │  │
│ └──────────────────────┘  │
│                            │
│ ⚡ Fast Delivery (<30min)  │
│ ┌──────────────────────┐  │
│ │ [Restaurant Card]    │  │
│ └──────────────────────┘  │
│                            │
│ 💰 Under 1,000₸            │
│ ┌──────────────────────┐  │
│ │ [Restaurant Card]    │  │
│ └──────────────────────┘  │
│                            │
│ All Restaurants            │
│ ┌──────────────────────┐  │
│ │ [Restaurant Cards]   │  │
│ └──────────────────────┘  │
└────────────────────────────┘
```

**Features:**
- Location selector
- Search with filters
- Category tabs
- Curated sections:
  - Student Favorites
  - Fast Delivery
  - Budget Options
- All restaurants list

---

### 4.2 Restaurant Card

```
┌──────────────────────────┐
│ [Cover Image 16:9]       │
│ 🏷️ -20% first order     │
│ ✓ PARTNER                │
├──────────────────────────┤
│ Burger House             │
│ ⭐ 4.8 (234) • 🕐 25-35m │
│ 💰 500-1,500₸ • 🍔 Fast │
│                          │
│ Free delivery over 2000₸ │
└──────────────────────────┘
```

**Elements:**
- Cover photo with overlay
- Promo badges (top-left)
- Partner badge (top-right)
- Restaurant name (18px, bold)
- Rating + review count
- Delivery time estimate
- Price range
- Cuisine type
- Special offers text

---

### 4.3 Restaurant Menu

```
┌────────────────────────────┐
│ [← Back]    Burger House   │
│ ⭐ 4.8 • 🕐 25-35 min      │
├────────────────────────────┤
│ [Cover image with info]    │
│                            │
│ Popular • Burgers •        │
│ Sides • Drinks • Desserts  │
│                            │
│ ━━━━━━━━━━━━━━━━━━━       │ ← Sticky tabs
│                            │
│ 🔥 Popular                 │
│                            │
│ ┌────────────────────────┐ │
│ │ [Img] Classic Burger   │ │
│ │       Beef patty...    │ │
│ │       450 kcal         │ │
│ │       1,200₸      [+]  │ │
│ └────────────────────────┘ │
│                            │
│ ┌────────────────────────┐ │
│ │ [Img] Chicken Burger   │ │
│ │       Grilled...       │ │
│ │       380 kcal         │ │
│ │       1,100₸      [+]  │ │
│ └────────────────────────┘ │
│                            │
│ 🍔 Burgers                 │
│ [More dishes...]           │
│                            │
├────────────────────────────┤
│ 🛒 Cart (3) • 3,500₸      │
└────────────────────────────┘
```

**Features:**
- Restaurant header (collapsible)
- Sticky category tabs
- Dish cards with:
  - Photo (1:1, 80×80px)
  - Name and description
  - Calories (optional)
  - Price
  - Add button (+)
- Floating cart button

---

### 4.4 Dish Detail (Modal)

```
┌────────────────────────────┐
│              [✕]           │
│                            │
│ [Large dish image]         │
│                            │
│ Classic Burger             │
│ 100% beef patty, lettuce,  │
│ tomato, pickles, cheese    │
│                            │
│ 450 kcal • 🔥 Spicy       │
│                            │
│ Customize:                 │
│                            │
│ Add-ons:                   │
│ ☐ Extra Cheese (+200₸)    │
│ ☐ Bacon (+300₸)           │
│ ☐ Avocado (+250₸)         │
│                            │
│ Remove:                    │
│ ☐ Pickles                  │
│ ☐ Onions                   │
│                            │
│ Special instructions       │
│ ┌──────────────────────┐  │
│ │ Add note...          │  │
│ └──────────────────────┘  │
│                            │
│ ┌────────────────────────┐ │
│ │ [-] 1 [+]    1,200₸   │ │
│ │ [Add to Cart]         │ │
│ └────────────────────────┘ │
└────────────────────────────┘
```

**Features:**
- Large product image
- Description and details
- Customization options
- Special instructions field
- Quantity selector
- Add to cart with price update

---

### 4.5 Cart & Checkout

```
┌────────────────────────────┐
│ [← Back]    Your Cart      │
├────────────────────────────┤
│ Burger House               │
│                            │
│ ┌────────────────────────┐ │
│ │ [Img] Classic Burger   │ │
│ │ • Extra cheese         │ │
│ │ • No pickles           │ │
│ │                        │ │
│ │ [-] 2 [+]      2,800₸ │ │
│ └────────────────────────┘ │
│                            │
│ ┌────────────────────────┐ │
│ │ [Img] Fries            │ │
│ │ Regular size           │ │
│ │                        │ │
│ │ [-] 1 [+]        500₸ │ │
│ └────────────────────────┘ │
│                            │
│ [+ Add more items]         │
│                            │
│ ─────────────────────      │
│                            │
│ Order Summary              │
│ Subtotal          3,300₸  │
│ Delivery fee        200₸  │
│ Service fee         100₸  │
│ ─────────────────────      │
│ Total             3,600₸  │
│                            │
│ 💰 You'll earn 108₸ back  │
│                            │
│ [Proceed to Checkout]      │
└────────────────────────────┘
```

---

### 4.6 Checkout Screen

```
┌────────────────────────────┐
│ [← Back]    Checkout       │
├────────────────────────────┤
│ Delivery Address           │
│ ┌────────────────────────┐ │
│ │ 📍 KBTU Campus         │ │
│ │    Dorm Building 3     │ │
│ │    [Change →]          │ │
│ └────────────────────────┘ │
│                            │
│ Delivery Time              │
│ ● ASAP (25-35 min)         │
│ ○ Schedule for later       │
│                            │
│ Contact                    │
│ ┌────────────────────────┐ │
│ │ 📱 +7 777 123 4567     │ │
│ └────────────────────────┘ │
│                            │
│ Payment Method             │
│ ┌────────────────────────┐ │
│ │ 💳 StudenKZ Balance    │ │
│ │    45,000₸ available   │ │
│ │    ✓ Selected          │ │
│ └────────────────────────┘ │
│ [+ Add payment method]     │
│                            │
│ Promo Code                 │
│ ┌──────────────────────┐  │
│ │ Enter code...   [✓]  │  │
│ └──────────────────────┘  │
│                            │
│ Order notes                │
│ ┌────────────────────────┐ │
│ │ Ring doorbell...       │ │
│ └────────────────────────┘ │
│                            │
│ ─────────────────────      │
│ Total: 3,600₸             │
│                            │
│ [Place Order]              │
└────────────────────────────┘
```

---

### 4.7 Order Tracking

```
┌────────────────────────────┐
│ [✕ Close]   Order #12345   │
├────────────────────────────┤
│                            │
│ ●━━━●━━━●━━━○             │
│ Placed Prep Way  Delivered │
│                            │
│ Estimated: 18:45           │
│ 15 minutes remaining       │
│                            │
│ ┌────────────────────────┐ │
│ │   [Live Map]           │ │
│ │   📍 You   🛵 Courier  │ │
│ └────────────────────────┘ │
│                            │
│ Your Courier               │
│ ┌────────────────────────┐ │
│ │ [Avatar] Askar K.      │ │
│ │ ⭐ 4.9 (1,234)         │ │
│ │ 🏍️ #A123BC            │ │
│ │                        │ │
│ │ [📱 Call] [💬 Message] │ │
│ └────────────────────────┘ │
│                            │
│ Order Details              │
│ Burger House               │
│ 2x Classic Burger          │
│ 1x Fries                   │
│                            │
│ Total: 3,600₸             │
│                            │
│ [❌ Cancel Order]          │
│ [🆘 Need Help?]            │
└────────────────────────────┘
```

**Features:**
- Progress indicator
- ETA countdown
- Live map tracking
- Courier information
- Call/message courier
- Order details
- Cancel option (early stage only)
- Help button

---

## Community

### 5.1 Community Home

```
┌────────────────────────────┐
│ [← Back]    Community      │
│                            │
│ ┌────────────────────────┐ │
│ │ 🔍 Search clubs...     │ │
│ └────────────────────────┘ │
│                            │
│ My Clubs • Events •        │
│ Discover • Popular         │
│                            │
│ 🌟 My Clubs (3)            │
│ ┌──────────────────────┐  │
│ │ [Club Card]          │  │
│ │ Robotics Club        │  │
│ │ 🔴 Live now          │  │
│ └──────────────────────┘  │
│                            │
│ 📅 Upcoming Events         │
│ ┌──────────────────────┐  │
│ │ NOV 10 • 6:00 PM     │  │
│ │ Hackathon 2025       │  │
│ │ 📍 KBTU Lab          │  │
│ │ 45 going            │  │
│ └──────────────────────┘  │
│                            │
│ 🎯 Recommended             │
│ ┌──────────────────────┐  │
│ │ [Club Cards]         │  │
│ └──────────────────────┘  │
│                            │
│ [+ Create Club]            │
└────────────────────────────┘
```

---

### 5.2 Club Categories

```
┌────────────────────────────┐
│ [← Back]    Discover       │
├────────────────────────────┤
│                            │
│ ┌──────────┬──────────┐   │
│ │ 🎨       │ 💪       │   │
│ │ Arts &   │ Sports & │   │
│ │ Creativi │ Fitness  │   │
│ │ 24 clubs │ 31 clubs │   │
│ ├──────────┼──────────┤   │
│ │ 🎮       │ 📚       │   │
│ │ Gaming   │ Academic │   │
│ │ 18 clubs │ 45 clubs │   │
│ ├──────────┼──────────┤   │
│ │ 🎵       │ 🗣️       │   │
│ │ Music    │ Debate   │   │
│ │ 12 clubs │ 8 clubs  │   │
│ ├──────────┼──────────┤   │
│ │ 🌍       │ 💼       │   │
│ │ Travel   │ Business │   │
│ │ 15 clubs │ 22 clubs │   │
│ └──────────┴──────────┘   │
└────────────────────────────┘
```

---

### 5.3 Club Detail Page

```
┌────────────────────────────┐
│ [← Back]  ••• More        │
├────────────────────────────┤
│ [Cover Image]              │
│ [Avatar]                   │
│                            │
│ Robotics Club              │
│ 👥 245 members             │
│ ⭐ 4.9 rating              │
│                            │
│ [Join Club]                │
│                            │
│ ────── About ──────        │
│                            │
│ We build robots and        │
│ compete in competitions... │
│                            │
│ 📍 KBTU Engineering Lab    │
│ 📅 Every Friday, 6:00 PM   │
│ 🎯 All levels welcome      │
│                            │
│ ────── Members ─────── →   │
│ [Avatars...]               │
│                            │
│ ────── Events ──────── →   │
│ ┌──────────────────────┐  │
│ │ NOV 10 • Hackathon   │  │
│ │ 45 going • 3 interested│  │
│ └──────────────────────┘  │
│                            │
│ ────── Photos ─────── →   │
│ ┌───┬───┬───┬───┐        │
│ │ • │ • │ • │ • │        │
│ └───┴───┴───┴───┘        │
│                            │
│ ────── Discussion ────  →  │
│ Latest posts...            │
│                            │
│ [Chat] [Events] [Members]  │
└────────────────────────────┘
```

**Tabs at bottom:**
- Chat: Club discussion
- Events: Event calendar
- Members: Member list

---

### 5.4 Event Detail

```
┌────────────────────────────┐
│ [← Back]  📤 Share  ⭐     │
├────────────────────────────┤
│ [Event Cover Image]        │
│                            │
│ NOV 10                     │
│ 2025                       │
│                            │
│ Robotics Hackathon 2025    │
│                            │
│ Organized by Robotics Club │
│                            │
│ 📅 Friday, Nov 10, 2025    │
│    6:00 PM - 11:59 PM      │
│                            │
│ 📍 KBTU Engineering Lab    │
│    Building 3, Floor 2     │
│    [View on Map]           │
│                            │
│ 👥 45 going • 12 interested│
│    [See who's going →]     │
│                            │
│ ────── Description ──────  │
│ Join us for an exciting    │
│ 6-hour hackathon...        │
│                            │
│ ────── Schedule ──────     │
│ 6:00 PM - Registration     │
│ 6:30 PM - Team formation   │
│ 7:00 PM - Hacking starts   │
│ ...                        │
│                            │
│ ────── Attendees ────── →  │
│ [Avatar grid]              │
│                            │
│ ────── Comments ────── →   │
│ [Comment list]             │
│                            │
├────────────────────────────┤
│ [💬 Comment]  [✓ I'm Going]│
└────────────────────────────┘
```

---

## Tutors & Roommates

### 6.1 Tutors Tab

```
┌────────────────────────────┐
│ [← Back]    Find Help      │
│                            │
│ Tutors • Roommates         │
│ ━━━━━━                     │
│                            │
│ ┌────────────────────────┐ │
│ │ 🔍 Search tutors...    │ │
│ └────────────────────────┘ │
│                            │
│ Subject: All               │
│ [Filter] [Sort by Rating]  │
│                            │
│ ┌────────────────────────┐ │
│ │ [Avatar] Aida K.       │ │
│ │ 🎓 KBTU • Year 3       │ │
│ │                        │ │
│ │ Subjects:              │ │
│ │ • Higher Mathematics   │ │
│ │ • Linear Algebra       │ │
│ │                        │ │
│ │ ⭐ 4.9 (23 reviews)     │ │
│ │ 💰 3,000₸/hour         │ │
│ │ 🎯 Online & Offline    │ │
│ │                        │ │
│ │ [Message] [Book]       │ │
│ └────────────────────────┘ │
│                            │
│ [More tutors...]           │
│                            │
│ [Become a Tutor]           │
└────────────────────────────┘
```

**Filters:**
- Subject
- University
- Year/Level
- Price range
- Rating
- Format (Online/Offline/Both)
- Availability

---

### 6.2 Tutor Profile

```
┌────────────────────────────┐
│ [← Back]  📤 Share  ⭐     │
├────────────────────────────┤
│ [Cover]                    │
│                            │
│    [Avatar 120px]          │
│                            │
│    Aida Karimova           │
│    🎓 KBTU • Year 3        │
│    ⭐ 4.9 (23 reviews)     │
│    💰 3,000₸/hour          │
│                            │
│    [Message] [Book Session]│
│                            │
│ ────── About ──────        │
│ 3rd year Computer Science  │
│ student passionate about   │
│ teaching mathematics...    │
│                            │
│ ────── Subjects ──────     │
│ • Higher Mathematics       │
│   ⭐ 5.0 (12 reviews)      │
│ • Linear Algebra           │
│   ⭐ 4.8 (8 reviews)       │
│ • Programming (Python)     │
│   ⭐ 4.9 (3 reviews)       │
│                            │
│ ────── Availability ─────  │
│ Mon-Fri: 6:00 PM - 9:00 PM │
│ Sat-Sun: 2:00 PM - 8:00 PM │
│                            │
│ ────── Format ──────       │
│ 🏠 In-person (KBTU Campus) │
│ 💻 Online (Zoom, Google)   │
│                            │
│ ────── Reviews ───────── → │
│ ┌──────────────────────┐  │
│ │ ⭐⭐⭐⭐⭐             │  │
│ │ "Excellent teacher..." │  │
│ │ - Arman, 2 weeks ago   │  │
│ └──────────────────────┘  │
│                            │
│ [Book a Session]           │
└────────────────────────────┘
```

---

### 6.3 Booking Flow

```
┌────────────────────────────┐
│ [← Back]    Book Session   │
├────────────────────────────┤
│ Tutor: Aida K.             │
│ Subject: Higher Math       │
│ 3,000₸/hour               │
│                            │
│ Select Date                │
│ ┌────────────────────────┐ │
│ │   [Calendar]           │ │
│ │   Nov 10 selected      │ │
│ └────────────────────────┘ │
│                            │
│ Select Time                │
│ 6:00 PM • 7:00 PM •        │
│ 8:00 PM                    │
│                            │
│ Duration                   │
│ ● 1 hour (3,000₸)         │
│ ○ 1.5 hours (4,500₸)      │
│ ○ 2 hours (6,000₸)        │
│                            │
│ Format                     │
│ ● Online                   │
│ ○ In-person (KBTU)         │
│                            │
│ Topic (optional)           │
│ ┌────────────────────────┐ │
│ │ Derivatives & integrals│ │
│ └────────────────────────┘ │
│                            │
│ ─────────────────────      │
│ Total: 3,000₸             │
│                            │
│ [Confirm Booking]          │
└────────────────────────────┘
```

---

### 6.4 Roommates Tab

```
┌────────────────────────────┐
│ [← Back]    Find Roommate  │
│                            │
│ Tutors • Roommates         │
│          ━━━━━━━━━━        │
│                            │
│ ┌────────────────────────┐ │
│ │ 🔍 Search...           │ │
│ └────────────────────────┘ │
│                            │
│ [Filter] [Sort]            │
│                            │
│ ┌────────────────────────┐ │
│ │ [Avatar] Yerlan M.     │ │
│ │ 21 • Male • KBTU Y2    │ │
│ │                        │ │
│ │ 📍 Looking in Almaty   │ │
│ │    Medeu District      │ │
│ │ 💰 Budget: ~60,000₸    │ │
│ │                        │ │
│ │ Preferences:           │ │
│ │ 🚭 Non-smoker          │ │
│ │ 🐕 Pet-friendly        │ │
│ │ 🎵 Music lover         │ │
│ │                        │ │
│ │ [View Profile]         │ │
│ └────────────────────────┘ │
│                            │
│ [More profiles...]         │
│                            │
│ [Post Your Ad]             │
└────────────────────────────┘
```

**Filters:**
- Gender
- Age range
- University
- District
- Budget range
- Move-in date
- Room type (shared/private)
- Lifestyle preferences

---

## FinTech Services

### 7.1 FinTech Dashboard

```
┌────────────────────────────┐
│ [← Back]    StudenKZ Pay   │
├────────────────────────────┤
│                            │
│ ┌────────────────────────┐ │
│ │ [Virtual Card Design]  │ │
│ │                        │ │
│ │ StudenKZ               │ │
│ │                        │ │
│ │ •••• •••• •••• 4567    │ │
│ │                        │ │
│ │ ALIZHAN BIZHAN         │ │
│ │ 12/25                  │ │
│ └────────────────────────┘ │
│                            │
│ Current Balance            │
│ 45,000 ₸                  │
│ 💚 +1,250₸ cashback earned│
│                            │
│ Quick Actions              │
│ ┌────┬────┬────┬────┐     │
│ │ 📥 │ 📤 │ 💳 │ 💰 │     │
│ │Top │Send│Pay │Split│     │
│ │ Up │ $  │Bills│Bill│     │
│ └────┴────┴────┴────┘     │
│                            │
│ ────── Transactions ────── │
│                            │
│ Today                      │
│ ┌──────────────────────┐  │
│ │ 🍔 Burger House      │  │
│ │ 2:23 PM              │  │
│ │ -1,850₸      +55₸ 💚 │  │
│ └──────────────────────┘  │
│                            │
│ ┌──────────────────────┐  │
│ │ 📖 Math Textbook     │  │
│ │ 11:45 AM             │  │
│ │ -5,000₸     +150₸ 💚 │  │
│ └──────────────────────┘  │
│                            │
│ Yesterday                  │
│ [More transactions...]     │
│                            │
│ [View All Transactions]    │
└────────────────────────────┘
```

---

### 7.2 Top Up

```
┌────────────────────────────┐
│ [← Back]    Top Up         │
├────────────────────────────┤
│                            │
│ Current Balance: 45,000₸  │
│                            │
│ Amount                     │
│ ┌────────────────────────┐ │
│ │ 10,000            ₸    │ │
│ └────────────────────────┘ │
│                            │
│ Quick amounts:             │
│ ┌─────┬─────┬─────┬─────┐ │
│ │5,000│10,000│20,000│50,000││
│ └─────┴─────┴─────┴─────┘ │
│                            │
│ Payment Method             │
│ ● 💳 Card ending •••• 4567│
│ ○ 🏦 Bank transfer         │
│ ○ 🏪 Cash (Kaspi terminal) │
│                            │
│ [+ Add payment method]     │
│                            │
│ ─────────────────────      │
│ You'll receive: 10,000₸   │
│ Fee: 0₸ (free)            │
│                            │
│ [Top Up]                   │
└────────────────────────────┘
```

---

### 7.3 Send Money

```
┌────────────────────────────┐
│ [← Back]    Send Money     │
├────────────────────────────┤
│                            │
│ Send to                    │
│ ┌────────────────────────┐ │
│ │ 🔍 Search by name,     │ │
│ │    phone, or email     │ │
│ └────────────────────────┘ │
│                            │
│ Recent                     │
│ ┌────────────────────────┐ │
│ │ [A] Aida K.         → │ │
│ │ [Y] Yerlan M.       → │ │
│ │ [A] Arman T.        → │ │
│ └────────────────────────┘ │
│                            │
│ Or send via               │
│ • Phone number             │
│ • Email address            │
│ • StudenKZ username        │
│ • QR code                  │
└────────────────────────────┘
```

**Next Step: Amount & Note**
```
┌────────────────────────────┐
│ [← Back]    Send to Aida   │
├────────────────────────────┤
│                            │
│ [Avatar] Aida K.           │
│ @aida_karimova             │
│                            │
│ Amount                     │
│ ┌────────────────────────┐ │
│ │                        │ │
│ │      5,000 ₸           │ │
│ │                        │ │
│ └────────────────────────┘ │
│                            │
│ [Keypad]                   │
│ ┌──────────────┐          │
│ │ 1   2   3    │          │
│ │ 4   5   6    │          │
│ │ 7   8   9    │          │
│ │ 00  0   ←    │          │
│ └──────────────┘          │
│                            │
│ Note (optional)            │
│ ┌────────────────────────┐ │
│ │ For textbook...        │ │
│ └────────────────────────┘ │
│                            │
│ [Send 5,000₸]             │
└────────────────────────────┘
```

---

### 7.4 Spending Analytics

```
┌────────────────────────────┐
│ [← Back]    Analytics      │
├────────────────────────────┤
│                            │
│ Nov 2025                   │
│ [← Oct •  Nov  • Dec →]   │
│                            │
│ Total Spent                │
│ 127,500 ₸                 │
│ ▲ 12% vs last month        │
│                            │
│ Cashback Earned            │
│ 💚 3,825 ₸                │
│                            │
│ ┌────────────────────────┐ │
│ │   [Pie Chart]          │ │
│ │   Spending by Category │ │
│ └────────────────────────┘ │
│                            │
│ Category Breakdown         │
│ 🍔 Food: 45,000₸ (35%)    │
│ ████████░░░░░░░░░          │
│                            │
│ 📖 Education: 38,000₸(30%) │
│ ███████░░░░░░░░░░░         │
│                            │
│ 🚕 Transport: 25,000₸(20%) │
│ █████░░░░░░░░░░░░░         │
│                            │
│ 🎉 Other: 19,500₸ (15%)   │
│ ████░░░░░░░░░░░░░░         │
│                            │
│ ────── Trends ──────── →   │
│ [Line chart]               │
│                            │
│ [Export Report]            │
└────────────────────────────┘
```

---

## Profile

### 8.1 Profile Screen

```
┌────────────────────────────┐
│              ⚙️  📤        │
├────────────────────────────┤
│ [Cover Image]              │
│                            │
│    [Avatar 120px]          │
│    ✓ Verified Student      │
│                            │
│    Alizhan Bizhan          │
│    🎓 KBTU • Year 2        │
│    📍 Almaty, Kazakhstan   │
│                            │
│ ┌────┬────────┬──────────┐ │
│ │ 24 │  4.8   │   156    │ │
│ │Orders│Rating │ Friends  │ │
│ └────┴────────┴──────────┘ │
│                            │
│ ────── My Activity ──────  │
│ 🛍️ My Listings (5)        │
│ 🧾 Order History (24)      │
│ ❤️ Favorites (12)          │
│ 💬 Reviews (15)            │
│                            │
│ ────── Academic ──────     │
│ 🎓 My Studies              │
│ 📊 Statistics              │
│                            │
│ ────── Social ──────       │
│ 🎟️ My Clubs (3)           │
│ 👥 Find Friends            │
│                            │
│ ────── Other ──────        │
│ ⚙️ Settings                │
│ 🆘 Support                 │
│ ℹ️ About App               │
│                            │
│ [Sign Out]                 │
└────────────────────────────┘
```

---

### 8.2 Edit Profile

```
┌────────────────────────────┐
│ [Cancel]  Edit Profile [✓] │
├────────────────────────────┤
│                            │
│ [Cover Image]              │
│ [Change Cover]             │
│                            │
│    [Avatar]                │
│    [Change Photo]          │
│                            │
│ First Name                 │
│ ┌────────────────────────┐ │
│ │ Alizhan                │ │
│ └────────────────────────┘ │
│                            │
│ Last Name                  │
│ ┌────────────────────────┐ │
│ │ Bizhan                 │ │
│ └────────────────────────┘ │
│                            │
│ Bio                        │
│ ┌────────────────────────┐ │
│ │ CS student at KBTU...  │ │
│ │                        │ │
│ └────────────────────────┘ │
│                            │
│ University                 │
│ ┌────────────────────────┐ │
│ │ KBTU                ▾  │ │
│ └────────────────────────┘ │
│                            │
│ Year                       │
│ ┌────────────────────────┐ │
│ │ 2                   ▾  │ │
│ └────────────────────────┘ │
│                            │
│ Major                      │
│ ┌────────────────────────┐ │
│ │ Computer Science    ▾  │ │
│ └────────────────────────┘ │
│                            │
│ Location                   │
│ ┌────────────────────────┐ │
│ │ Almaty              ▾  │ │
│ └────────────────────────┘ │
│                            │
│ Social Links               │
│ [+ Add Link]               │
│                            │
│ [Save Changes]             │
└────────────────────────────┘
```

---

### 8.3 Settings

```
┌────────────────────────────┐
│ [← Back]    Settings       │
├────────────────────────────┤
│                            │
│ 👤 Account                 │
│ • Personal Information  →  │
│ • Email & Phone         →  │
│ • Change Password       →  │
│ • University Link       →  │
│                            │
│ 🔒 Security & Privacy      │
│ • Two-Factor Auth       →  │
│ • Biometric Login       ✓  │
│ • Privacy Settings      →  │
│ • Blocked Users         →  │
│                            │
│ 🔔 Notifications           │
│ • Push Notifications    →  │
│ • Email Notifications   →  │
│ • SMS Notifications     →  │
│                            │
│ 🎨 Appearance              │
│ • Theme                 →  │
│   Auto • Light • Dark      │
│ • Language              →  │
│   English • Русский • Қаз  │
│                            │
│ 💳 Payment & Billing       │
│ • Payment Methods       →  │
│ • Transaction History   →  │
│ • Cashback Program      →  │
│                            │
│ ℹ️ About                   │
│ • Version 1.0.0            │
│ • Terms of Service      →  │
│ • Privacy Policy        →  │
│ • Licenses              →  │
│                            │
│ 🆘 Support                 │
│ • Help Center           →  │
│ • Contact Us            →  │
│ • Report a Bug          →  │
│                            │
│ [Sign Out]                 │
│ [Delete Account]           │
└────────────────────────────┘
```

---

## Additional Screens

### 9.1 Empty States

#### No Results
```
┌────────────────────────────┐
│                            │
│    [Illustration]          │
│    🔍                      │
│                            │
│    No results found        │
│                            │
│    Try adjusting your      │
│    search or filters       │
│                            │
│    [Clear Filters]         │
└────────────────────────────┘
```

#### Empty Favorites
```
┌────────────────────────────┐
│                            │
│    [Illustration]          │
│    ❤️                      │
│                            │
│    No favorites yet        │
│                            │
│    Save items you like     │
│    to find them here       │
│                            │
│    [Explore Marketplace]   │
└────────────────────────────┘
```

---

### 9.2 Error States

#### No Internet
```
┌────────────────────────────┐
│                            │
│    [Illustration]          │
│    📡                      │
│                            │
│    No Internet Connection  │
│                            │
│    Please check your       │
│    connection and try again│
│                            │
│    [Try Again]             │
└────────────────────────────┘
```

#### Server Error
```
┌────────────────────────────┐
│                            │
│    [Illustration]          │
│    ⚠️                      │
│                            │
│    Something went wrong    │
│                            │
│    We're working on it.    │
│    Please try again later. │
│                            │
│    [Go Home]  [Try Again]  │
└────────────────────────────┘
```

---

### 9.3 Success States

#### Order Placed
```
┌────────────────────────────┐
│                            │
│          ✓                 │
│       (Animated)           │
│                            │
│    Order Placed!           │
│                            │
│    Your order #12345 has   │
│    been confirmed          │
│                            │
│    [Track Order]           │
│    [Continue Shopping]     │
└────────────────────────────┘
```

---

**Version:** 1.0  
**Last Updated:** November 8, 2025  
**Contact:** Alizhan Bizhan | alizhan695@gmail.com
