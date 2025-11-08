# StudenKZ Developer Handoff
## Technical Specifications & Implementation Guide

---

## 📋 Table of Contents
1. [Project Overview](#project-overview)
2. [Tech Stack Recommendations](#tech-stack-recommendations)
3. [Figma Setup](#figma-setup)
4. [Asset Export](#asset-export)
5. [API Requirements](#api-requirements)
6. [Implementation Checklist](#implementation-checklist)
7. [Third-Party Integrations](#third-party-integrations)
8. [Deployment Guidelines](#deployment-guidelines)

---

## Project Overview

**Product:** StudenKZ - Student Super-Platform  
**Timeline:** MVP by December 2025, Launch Q1 2026  
**Platforms:** iOS, Android (React Native recommended)  
**Target:** Kazakhstan university students (500K+ users)

**Core Modules:**
1. Marketplace (Textbooks & Materials)
2. Food Delivery
3. Community (Clubs & Events)
4. Tutors & Roommates
5. FinTech Services
6. Profile & Settings

---

## Tech Stack Recommendations

### Mobile App

#### Framework
**Recommended: React Native (Expo)**

**Pros:**
- Single codebase for iOS and Android
- Large community and ecosystem
- Fast development cycle
- Good performance for this use case
- Easy to find developers in Kazakhstan

**Alternative: Flutter**
- Better performance
- Beautiful animations out of the box
- Growing ecosystem

---

#### Core Libraries

```json
{
  "dependencies": {
    "react-native": "latest",
    "expo": "latest",
    "@react-navigation/native": "^6.x",
    "@react-navigation/stack": "^6.x",
    "@react-navigation/bottom-tabs": "^6.x",
    "react-native-reanimated": "^3.x",
    "react-native-gesture-handler": "^2.x",
    "axios": "^1.x",
    "react-query": "^3.x",
    "zustand": "^4.x",
    "react-hook-form": "^7.x",
    "react-native-maps": "^1.x",
    "react-native-firebase": "^18.x",
    "react-native-push-notification": "^8.x"
  }
}
```

---

#### State Management
**Recommended: Zustand + React Query**

```javascript
// Example store structure
import create from 'zustand';

export const useAuthStore = create((set) => ({
  user: null,
  token: null,
  setUser: (user) => set({ user }),
  setToken: (token) => set({ token }),
  logout: () => set({ user: null, token: null })
}));
```

---

#### Navigation Structure

```javascript
// App.js
<NavigationContainer>
  <Stack.Navigator>
    {!isAuthenticated ? (
      <>
        <Stack.Screen name="Splash" component={SplashScreen} />
        <Stack.Screen name="Onboarding" component={OnboardingScreen} />
        <Stack.Screen name="Auth" component={AuthScreen} />
      </>
    ) : (
      <>
        <Stack.Screen name="Main" component={MainTabNavigator} />
        <Stack.Screen name="ProductDetail" component={ProductDetailScreen} />
        <Stack.Screen name="RestaurantMenu" component={RestaurantMenuScreen} />
        {/* ... more screens */}
      </>
    )}
  </Stack.Navigator>
</NavigationContainer>

// MainTabNavigator.js
<Tab.Navigator>
  <Tab.Screen name="Home" component={HomeScreen} />
  <Tab.Screen name="Marketplace" component={MarketplaceScreen} />
  <Tab.Screen name="Food" component={FoodScreen} />
  <Tab.Screen name="Community" component={CommunityScreen} />
  <Tab.Screen name="Profile" component={ProfileScreen} />
</Tab.Navigator>
```

---

### Backend

#### Framework
**Recommended: Node.js + Express** or **NestJS**

**Alternative:** Django REST Framework (Python)

---

#### Database
**PostgreSQL** for relational data  
**Redis** for caching and real-time features  
**MongoDB** for flexible schemas (optional)

**Schema Examples:**

```sql
-- Users Table
CREATE TABLE users (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  email VARCHAR(255) UNIQUE NOT NULL,
  phone VARCHAR(20) UNIQUE,
  password_hash VARCHAR(255) NOT NULL,
  first_name VARCHAR(100),
  last_name VARCHAR(100),
  university_id INTEGER REFERENCES universities(id),
  year INTEGER CHECK (year BETWEEN 1 AND 4),
  major VARCHAR(100),
  verified BOOLEAN DEFAULT false,
  created_at TIMESTAMP DEFAULT NOW(),
  updated_at TIMESTAMP DEFAULT NOW()
);

-- Products Table (Marketplace)
CREATE TABLE products (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  seller_id UUID REFERENCES users(id),
  title VARCHAR(255) NOT NULL,
  description TEXT,
  price DECIMAL(10, 2),
  condition VARCHAR(50),
  category VARCHAR(50),
  isbn VARCHAR(20),
  university_id INTEGER,
  year INTEGER,
  images JSONB,
  status VARCHAR(20) DEFAULT 'active',
  created_at TIMESTAMP DEFAULT NOW(),
  updated_at TIMESTAMP DEFAULT NOW()
);

-- Orders Table
CREATE TABLE orders (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  user_id UUID REFERENCES users(id),
  restaurant_id UUID REFERENCES restaurants(id),
  items JSONB NOT NULL,
  total_amount DECIMAL(10, 2),
  delivery_fee DECIMAL(10, 2),
  status VARCHAR(50),
  delivery_address JSONB,
  courier_id UUID REFERENCES couriers(id),
  created_at TIMESTAMP DEFAULT NOW(),
  updated_at TIMESTAMP DEFAULT NOW()
);

-- More tables: clubs, events, tutors, transactions, etc.
```

---

#### API Architecture
**REST API** with potential **GraphQL** for complex queries

**Base URL:** `https://api.studenkz.com/v1/`

---

### Cloud Infrastructure

#### Hosting
- **App:** AWS EC2 or DigitalOcean
- **Database:** AWS RDS (PostgreSQL)
- **Storage:** AWS S3 or Cloudflare R2
- **CDN:** Cloudflare
- **Container:** Docker + Kubernetes (for scaling)

#### Services
- **Authentication:** Firebase Auth or Auth0
- **Push Notifications:** Firebase Cloud Messaging
- **Analytics:** Mixpanel or Amplitude
- **Error Tracking:** Sentry
- **Payment Gateway:** Kaspi, Wooppay, or Stripe

---

## Figma Setup

### File Structure

```
📁 StudenKZ Design System
  ├── 🎨 Brand
  │   ├── Colors (Styles)
  │   ├── Typography (Styles)
  │   └── Logo Assets
  ├── 🧩 Components
  │   ├── Buttons
  │   ├── Input Fields
  │   ├── Cards
  │   ├── Navigation
  │   └── Icons
  ├── 📱 Screens
  │   ├── 01 - Onboarding
  │   ├── 02 - Home
  │   ├── 03 - Marketplace
  │   ├── 04 - Food Delivery
  │   ├── 05 - Community
  │   ├── 06 - Tutors & Roommates
  │   ├── 07 - FinTech
  │   └── 08 - Profile
  ├── 🌙 Dark Mode
  ├── 📐 Templates
  └── 📚 Documentation
```

---

### Design Tokens

**Export as JSON for code:**

```json
{
  "colors": {
    "primary": "#1FB8CD",
    "primaryDark": "#13343B",
    "accent": "#5D878F",
    "success": "#34D399",
    "background": "#FCFCF9",
    "surface": "#FFFFFF"
  },
  "spacing": {
    "xxs": "2px",
    "xs": "4px",
    "sm": "8px",
    "md": "12px",
    "lg": "16px",
    "xl": "24px",
    "2xl": "32px",
    "3xl": "48px",
    "4xl": "64px"
  },
  "borderRadius": {
    "sm": "8px",
    "md": "12px",
    "lg": "16px",
    "xl": "24px",
    "full": "9999px"
  },
  "typography": {
    "h1": {
      "fontSize": "32px",
      "fontWeight": "700",
      "lineHeight": "40px",
      "letterSpacing": "-0.02em"
    }
  }
}
```

**Generate with:** Figma Tokens plugin or manual export

---

### Component Library

**Create in Figma:**
- All components as Figma Components
- Variants for different states (default, hover, active, disabled)
- Auto-layout for responsive sizing
- Design system organized in separate page

**Naming Convention:**
```
Component/Variant/State

Examples:
- Button/Primary/Default
- Button/Primary/Hover
- Button/Primary/Disabled
- Card/Product/Empty
```

---

### Prototyping

**Create interactive prototype:**
- All main user flows
- Smart Animate for transitions
- Overflow scrolling for lists
- Keyboard interaction for inputs

**Export:**
- Share link for developers
- Record video walkthrough
- Document interaction notes

---

## Asset Export

### Icons

**Format:** SVG (preferred) or PNG (@1x, @2x, @3x)  
**Size:** Multiple sizes (16px, 24px, 32px, 48px)  
**Color:** Single color (use CSS/code to tint)

**Naming:**
```
icon_name_size.svg

Examples:
- home_24.svg
- cart_32.svg
- profile_24.svg
```

---

### Images

**Formats:**
- **Photos:** JPG (optimized)
- **Graphics:** PNG (with transparency)
- **Illustrations:** SVG (preferred) or PNG

**Sizes:**
- @1x (base)
- @2x (retina)
- @3x (high-res mobile)

**Optimization:**
- Compress all images (TinyPNG, ImageOptim)
- Target: <200KB per image
- Use WebP where supported

---

### Illustrations

**Format:** SVG (vector) or PNG (raster)  
**Size:** Flexible SVG or @3x PNG  
**Organization:** By category (onboarding, empty-states, errors)

---

### Logo

**Export:**
- Full logo (horizontal)
- Icon only (square)
- Wordmark only

**Formats:**
- SVG (all uses)
- PNG (@1x, @2x, @3x)
- App icons (all iOS/Android sizes)

**iOS App Icon Sizes:**
- 180×180 (iPhone)
- 167×167 (iPad Pro)
- 152×152 (iPad)
- 120×120 (iPhone)
- 87×87 (iPhone)
- 80×80 (iPad)
- 76×76 (iPad)
- 60×60 (iPhone)
- 58×58 (iPhone)
- 40×40 (all)
- 29×29 (all)
- 20×20 (all)

**Android App Icon Sizes:**
- 512×512 (Play Store)
- 192×192 (xxxhdpi)
- 144×144 (xxhdpi)
- 96×96 (xhdpi)
- 72×72 (hdpi)
- 48×48 (mdpi)

---

## API Requirements

### Authentication

#### Register
```http
POST /api/v1/auth/register
Content-Type: application/json

{
  "email": "student@kbtu.kz",
  "password": "securepassword",
  "firstName": "Alizhan",
  "lastName": "Bizhan",
  "universityId": 1,
  "year": 2
}

Response:
{
  "user": { ... },
  "token": "jwt_token_here"
}
```

#### Login
```http
POST /api/v1/auth/login
Content-Type: application/json

{
  "email": "student@kbtu.kz",
  "password": "securepassword"
}

Response:
{
  "user": { ... },
  "token": "jwt_token_here"
}
```

---

### Marketplace

#### Get Products
```http
GET /api/v1/products?category=textbooks&university=1&year=2&page=1&limit=20
Authorization: Bearer {token}

Response:
{
  "products": [
    {
      "id": "uuid",
      "title": "Higher Mathematics",
      "price": 5000,
      "condition": "excellent",
      "images": ["url1", "url2"],
      "seller": {
        "id": "uuid",
        "name": "Aida K.",
        "rating": 4.9
      }
    }
  ],
  "pagination": {
    "page": 1,
    "limit": 20,
    "total": 145
  }
}
```

#### Create Product
```http
POST /api/v1/products
Authorization: Bearer {token}
Content-Type: multipart/form-data

{
  "title": "Higher Mathematics",
  "description": "Year 2 textbook...",
  "price": 5000,
  "condition": "excellent",
  "category": "textbooks",
  "images": [file1, file2]
}

Response:
{
  "product": { ... }
}
```

---

### Food Delivery

#### Get Restaurants
```http
GET /api/v1/restaurants?lat=43.238949&lng=76.889709&cuisine=fastfood
Authorization: Bearer {token}

Response:
{
  "restaurants": [
    {
      "id": "uuid",
      "name": "Burger House",
      "rating": 4.8,
      "deliveryTime": "25-35",
      "priceRange": [500, 1500],
      "cuisine": "fast food",
      "image": "url"
    }
  ]
}
```

#### Create Order
```http
POST /api/v1/orders
Authorization: Bearer {token}
Content-Type: application/json

{
  "restaurantId": "uuid",
  "items": [
    {
      "dishId": "uuid",
      "quantity": 2,
      "customizations": ["extra cheese", "no pickles"]
    }
  ],
  "deliveryAddress": {
    "lat": 43.238949,
    "lng": 76.889709,
    "address": "KBTU Dorm 3, Room 204",
    "phone": "+77771234567"
  },
  "paymentMethod": "studenkz_balance",
  "notes": "Ring doorbell"
}

Response:
{
  "order": {
    "id": "uuid",
    "status": "placed",
    "estimatedTime": "30 min",
    "total": 3600
  }
}
```

---

### Real-time Features

**Use WebSocket for:**
- Order tracking (courier location)
- Chat messages
- Notifications

```javascript
// WebSocket connection
const ws = new WebSocket('wss://api.studenkz.com/ws');

ws.on('message', (data) => {
  const event = JSON.parse(data);
  
  switch(event.type) {
    case 'order_update':
      // Update order status
      break;
    case 'courier_location':
      // Update map with courier location
      break;
    case 'new_message':
      // Show new message notification
      break;
  }
});
```

---

### FinTech

#### Get Balance
```http
GET /api/v1/wallet/balance
Authorization: Bearer {token}

Response:
{
  "balance": 45000,
  "cashbackEarned": 1250,
  "currency": "KZT"
}
```

#### Send Money
```http
POST /api/v1/wallet/transfer
Authorization: Bearer {token}
Content-Type: application/json

{
  "recipientId": "uuid",
  "amount": 5000,
  "note": "For textbook"
}

Response:
{
  "transaction": {
    "id": "uuid",
    "status": "completed",
    "amount": 5000,
    "timestamp": "2025-11-08T14:30:00Z"
  }
}
```

---

## Implementation Checklist

### Phase 1: Foundation (Weeks 1-2)
- [ ] Set up development environment
- [ ] Initialize React Native project with Expo
- [ ] Configure navigation structure
- [ ] Implement design system (colors, typography, spacing)
- [ ] Create reusable components (Button, Input, Card)
- [ ] Set up state management (Zustand)
- [ ] Configure API client (Axios + React Query)

### Phase 2: Authentication (Weeks 3-4)
- [ ] Splash screen
- [ ] Onboarding flow (3 screens)
- [ ] Registration screen
- [ ] Login screen
- [ ] Password reset flow
- [ ] Social login (Google, Apple)
- [ ] University verification
- [ ] Token storage (SecureStore)

### Phase 3: Core Features (Weeks 5-8)
- [ ] Home screen with service cards
- [ ] Bottom tab navigation
- [ ] Marketplace listing and detail
- [ ] Product creation flow
- [ ] Search and filters
- [ ] Food restaurant list and menu
- [ ] Cart and checkout
- [ ] Basic profile screen

### Phase 4: Advanced Features (Weeks 9-12)
- [ ] Order tracking with live map
- [ ] Community (clubs and events)
- [ ] Chat/messaging
- [ ] Tutors and roommates
- [ ] FinTech dashboard
- [ ] Transaction history
- [ ] Notifications

### Phase 5: Polish (Weeks 13-14)
- [ ] Animations and transitions
- [ ] Error handling
- [ ] Loading states
- [ ] Empty states
- [ ] Dark mode
- [ ] Localization (RU, KZ, EN)
- [ ] Performance optimization

### Phase 6: Testing (Weeks 15-16)
- [ ] Unit tests (Jest)
- [ ] Integration tests
- [ ] E2E tests (Detox)
- [ ] Accessibility testing
- [ ] Device testing (multiple screen sizes)
- [ ] Beta testing with users

---

## Third-Party Integrations

### Payment Providers

#### Kaspi (Kazakhstan)
```javascript
import { KaspiPay } from 'kaspi-payment-sdk';

const payment = await KaspiPay.charge({
  amount: 10000,
  currency: 'KZT',
  description: 'Top up StudenKZ balance',
  returnUrl: 'studenkz://payment/success'
});
```

#### Wooppay (Kazakhstan)
```javascript
import Wooppay from 'wooppay-sdk';

const payment = await Wooppay.createInvoice({
  amount: 10000,
  description: 'StudenKZ top-up'
});
```

---

### Maps & Location

#### Google Maps (for delivery)
```javascript
import MapView, { Marker } from 'react-native-maps';

<MapView
  initialRegion={{
    latitude: 43.238949,
    longitude: 76.889709,
    latitudeDelta: 0.01,
    longitudeDelta: 0.01
  }}
>
  <Marker coordinate={userLocation} title="You" />
  <Marker coordinate={courierLocation} title="Courier" />
</MapView>
```

---

### Analytics

#### Mixpanel
```javascript
import Mixpanel from 'mixpanel-react-native';

Mixpanel.track('Product Viewed', {
  productId: 'uuid',
  category: 'textbooks',
  price: 5000
});
```

---

### Push Notifications

#### Firebase Cloud Messaging
```javascript
import messaging from '@react-native-firebase/messaging';

// Request permission
const authStatus = await messaging().requestPermission();

// Get token
const token = await messaging().getToken();

// Listen for messages
messaging().onMessage(async remoteMessage => {
  // Show notification
});
```

---

## Deployment Guidelines

### iOS (App Store)

#### Requirements
- Apple Developer account ($99/year)
- App Store Connect account
- TestFlight for beta testing

#### Build
```bash
# Build with Expo
expo build:ios

# Or with EAS (recommended)
eas build --platform ios
```

#### Checklist
- [ ] App icons (all sizes)
- [ ] Screenshots (6.5", 5.5")
- [ ] App description (RU, KZ, EN)
- [ ] Privacy policy URL
- [ ] Age rating: 4+
- [ ] Category: Education
- [ ] TestFlight beta testing

---

### Android (Google Play)

#### Requirements
- Google Play Developer account ($25 one-time)

#### Build
```bash
# Build with Expo
expo build:android

# Or with EAS (recommended)
eas build --platform android
```

#### Checklist
- [ ] App icon (512×512)
- [ ] Feature graphic (1024×500)
- [ ] Screenshots (multiple devices)
- [ ] App description (RU, KZ, EN)
- [ ] Privacy policy URL
- [ ] Content rating questionnaire
- [ ] Category: Education
- [ ] Closed/Open beta testing

---

### Backend Deployment

#### Docker Setup
```dockerfile
# Dockerfile
FROM node:18-alpine

WORKDIR /app

COPY package*.json ./
RUN npm install --production

COPY . .

EXPOSE 3000

CMD ["node", "server.js"]
```

#### Environment Variables
```env
# .env
NODE_ENV=production
PORT=3000
DATABASE_URL=postgresql://user:pass@host:5432/studenkz
JWT_SECRET=your_secret_key
REDIS_URL=redis://localhost:6379
AWS_S3_BUCKET=studenkz-assets
AWS_ACCESS_KEY_ID=your_key
AWS_SECRET_ACCESS_KEY=your_secret
FIREBASE_SERVER_KEY=your_firebase_key
```

---

### CI/CD Pipeline

#### GitHub Actions
```yaml
# .github/workflows/deploy.yml
name: Deploy

on:
  push:
    branches: [main]

jobs:
  build:
    runs-on: ubuntu-latest
    
    steps:
    - uses: actions/checkout@v2
    
    - name: Setup Node
      uses: actions/setup-node@v2
      with:
        node-version: '18'
    
    - name: Install dependencies
      run: npm install
    
    - name: Run tests
      run: npm test
    
    - name: Build
      run: npm run build
    
    - name: Deploy to server
      run: |
        # Deployment script
```

---

### Monitoring

#### Sentry (Error Tracking)
```javascript
import * as Sentry from "@sentry/react-native";

Sentry.init({
  dsn: "your_sentry_dsn",
  environment: "production"
});
```

#### Uptime Monitoring
- Use UptimeRobot or Pingdom
- Monitor API endpoints
- Alert on downtime

---

## Security Considerations

### Data Protection
- [ ] All API requests over HTTPS
- [ ] JWT tokens with expiration
- [ ] Sensitive data encrypted at rest
- [ ] User passwords hashed (bcrypt)
- [ ] Input validation and sanitization
- [ ] Rate limiting on API endpoints

### Privacy
- [ ] GDPR/Privacy policy compliance
- [ ] User data export option
- [ ] Account deletion option
- [ ] Anonymous analytics
- [ ] Consent for data collection

---

## Performance Targets

### Mobile App
- [ ] App launch: <2s
- [ ] Screen navigation: <300ms
- [ ] Image loading: Progressive, <1s
- [ ] API calls: <500ms (local), <2s (international)
- [ ] App size: <50MB

### Backend
- [ ] API response time: <200ms (p95)
- [ ] Database queries: <50ms
- [ ] Uptime: 99.9%
- [ ] Concurrent users: 10,000+

---

## Launch Checklist

### Pre-Launch
- [ ] All features tested
- [ ] Bug-free on major devices
- [ ] Privacy policy published
- [ ] Terms of service published
- [ ] Customer support ready
- [ ] Marketing materials prepared
- [ ] Press kit ready
- [ ] Beta tester feedback incorporated

### App Store Submission
- [ ] iOS TestFlight beta complete
- [ ] Android closed beta complete
- [ ] All metadata submitted
- [ ] Screenshots uploaded
- [ ] App description optimized
- [ ] Submitted for review

### Launch Day
- [ ] Monitor crash reports
- [ ] Watch server load
- [ ] Respond to reviews
- [ ] Social media announcement
- [ ] University partnerships activated

---

## Post-Launch

### Week 1
- [ ] Daily crash monitoring
- [ ] User feedback collection
- [ ] Critical bug fixes
- [ ] Server scaling if needed

### Month 1
- [ ] Analytics review
- [ ] Feature usage analysis
- [ ] User retention metrics
- [ ] Plan next features

---

## Contact & Support

**Project Lead:** Alizhan Bizhan  
**Email:** alizhan695@gmail.com  
**Telegram:** @alizhan006

**Documentation Repository:** [GitHub Link]  
**Figma Design:** [Figma Link]  
**API Documentation:** [Swagger/Postman Link]

---

**Version:** 1.0  
**Last Updated:** November 8, 2025  
**Next Review:** December 2025
