# RoomSwipe Development Checklist

**Last Updated:** March 3, 2026  
**Current Phase:** Phase 0 - Validation & Prototype

---

## 🚀 Quick Start (Week 1 - Critical Path)

### Deployment & Setup
- [x] Create GitHub repository
- [x] Deploy landing page (index.html) to GitHub
- [ ] Enable GitHub Pages
  - Go to: https://github.com/rblagahit/roomswipe/settings/pages
  - Select "main" branch → Save
  - Verify live at: https://rblagahit.github.io/roomswipe/
- [ ] Get custom domain (optional - ₱500/year)
  - Register: roomswipe.ph or roomswipe.com.ph
  - Configure DNS in GitHub Pages settings

### Legal & Compliance (Required Before Collecting Data)
- [ ] Create Privacy Policy
  - Use generator: https://www.termsfeed.com/privacy-policy-generator/
  - Include: Data collection, storage, user rights, PH Data Privacy Act compliance
  - Add to website footer
- [ ] Create Terms of Service
  - Use generator: https://www.termsfeed.com/terms-service-generator/
  - Include: User responsibilities, liability limits, content policy
  - Add to website footer
- [ ] Add cookie consent banner (if using analytics)

### Waitlist & Validation Tools
- [ ] Create Google Form for waitlist
  - Fields: Name, Email, Role (Seeker/Host/Manager), City, Interest in vacation splits (Yes/No)
  - Add: "How did you hear about us?" (track marketing sources)
- [ ] Add "Join Waitlist" button to index.html
  - Replace demo text or add prominent CTA
  - Link to Google Form
- [ ] Set up Google Sheets for responses
  - Auto-collect form responses
  - Add columns: Sign-up Date, Status (Pending/Contacted/Matched)
  - Create filter views for each role type

### Social Media Setup
- [ ] Create accounts
  - [ ] Twitter/X: @RoomSwipePH
  - [ ] Instagram: @roomswipe.ph
  - [ ] Facebook Page: RoomSwipe Philippines
  - [ ] TikTok: @roomswipe (optional but recommended)
- [ ] Design simple logo
  - Use Canva (free): https://www.canva.com/
  - Colors: #00a3c4 (teal - from current site) + complementary
  - Export: PNG (transparent background) + SVG
- [ ] Create cover photos/profile images
  - Consistent branding across platforms

---

## 📊 Phase 0: Validation (Weeks 1-8)

### Week 1-2: Launch & Initial Outreach

#### Marketing - Day 1
- [ ] Share on personal social media
  - [ ] Facebook personal profile
  - [ ] Twitter/X with hashtags: #RoomSwipePH #CebuRentals #RoommateSearch
  - [ ] LinkedIn (professional network)
- [ ] Join relevant Facebook groups (5-10)
  - [ ] Cebu Rentals & Room for Rent
  - [ ] Manila Room for Rent / Bedspace
  - [ ] UP Diliman Housing & Rentals
  - [ ] Ateneo de Manila Roommate Finder
  - [ ] UST Housing & Dormitories
- [ ] Post on Reddit
  - [ ] r/Philippines
  - [ ] r/Cebu
  - [ ] r/CasualPH (low-key intro)

#### Analytics Setup
- [ ] Set up Google Analytics 4 (free)
  - Add tracking code to index.html
  - Track: Page views, button clicks, form submissions
- [ ] Create short link for tracking
  - Use Bitly: bit.ly/roomswipe-demo
  - Track clicks from different sources

#### Content Creation
- [ ] Create demo video (1-2 min)
  - Screen recording of swipe interface
  - Explain value prop: "Tinder for roommates"
  - Upload to: YouTube, TikTok, IG Reels, FB
- [ ] Write launch post copy
  - Problem: Hard to find compatible roommates
  - Solution: Swipe-based matching
  - CTA: Join waitlist for early access

### Week 3-4: Manual Matching Experiment

#### Data Collection
- [ ] Create matching spreadsheet
  - Columns: Name, Role, Location, Budget, Lifestyle Prefs, Match Score
  - Use formulas for basic compatibility scoring
- [ ] Contact first 20 sign-ups
  - Send welcome email via Gmail (manual for now)
  - Ask: "Tell me more about your ideal roommate/space"
  - Collect detailed preferences

#### Matching Process
- [ ] Review profiles manually
  - Look for: Similar budget, location, lifestyle (quiet/social, cleanliness, pets)
- [ ] Introduce matches via WhatsApp/Email
  - Template: "Hi [Name], I found a potential match! Meet [Match]..."
  - Provide both parties' contact info (with permission)
- [ ] Follow up after 3 days
  - Ask: Did you connect? Are you happy with the match?
- [ ] Track outcomes in spreadsheet
  - Status: Contacted / Met / Moved In / Declined / No Response

### Week 5-6: User Interviews

#### Research Goals
- [ ] Understand pain points deeper
- [ ] Validate feature priorities
- [ ] Test pricing willingness (₱99/month premium)
- [ ] Gauge interest in vacation splits

#### Interview Script (10 people minimum)
- [ ] Recruit interviewees (offer ₱100 GCash for 30 min)
  - [ ] 5 seekers (students/young professionals)
  - [ ] 3 hosts (individual landlords)
  - [ ] 2 managers (property management companies)
- [ ] Questions:
  - "Walk me through your last roommate search"
  - "What went wrong? What was frustrating?"
  - "If you could change one thing, what would it be?"
  - "Would you pay ₱99/month for [list premium features]?"
  - "Would you use this to find travel buddies to split vacation costs?"
- [ ] Record findings (notes + voice recording with permission)
- [ ] Create insights summary document

### Week 7-8: Analysis & Decision

#### Metrics Review
- [ ] Count total sign-ups (Goal: 150+)
- [ ] Calculate match success rate (Goal: 80% satisfaction)
- [ ] Review survey responses (positive sentiment >70%?)
- [ ] Assess manager interest (Goal: 3+ willing to pay)

#### Competitive Analysis
- [ ] Research existing solutions
  - [ ] Lamudi.com.ph - room rentals
  - [ ] OLX.ph - classifieds
  - [ ] Facebook Marketplace
  - [ ] University bulletin boards
  - Document: What do they do well? What's missing?
- [ ] Identify differentiation
  - Our edge: Swipe UX, personality matching, trust features

#### Go/No-Go Decision
- [ ] Review all Phase 0 data
- [ ] Calculate estimated Phase 1 costs (Firebase, time)
- [ ] Decide: Proceed to MVP or pivot?
- [ ] If GO: Write Phase 1 detailed spec document

---

## 🏗️ Phase 1: Core MVP (Months 2-5)

### Pre-Development Setup

#### Technical Infrastructure
- [ ] Set up Firebase project
  - [ ] Create project in Firebase Console
  - [ ] Enable Authentication (Email/Password + Google)
  - [ ] Create Firestore database
  - [ ] Set up Storage for images
  - [ ] Install Firebase SDK in project
- [ ] Choose frontend framework
  - [ ] Decision: React vs Vue vs Vanilla JS?
  - [ ] Initialize project with Vite
  - [ ] Set up TailwindCSS
- [ ] Set up development environment
  - [ ] Install Node.js & npm
  - [ ] Set up ESLint + Prettier
  - [ ] Create .env for API keys (don't commit!)
  - [ ] Set up local dev server

#### Design System
- [ ] Create UI mockups (Figma - free)
  - [ ] Sign-up flow (4 screens)
  - [ ] Profile setup (3 screens)
  - [ ] Swipe interface (main screen)
  - [ ] Match screen
  - [ ] Chat interface
- [ ] Design components library
  - [ ] Buttons (primary, secondary, danger)
  - [ ] Input fields, dropdowns
  - [ ] Cards (profile cards)
  - [ ] Navigation (bottom tabs for mobile)

### Core Features Development

#### Authentication (Week 1-2)
- [ ] Sign-up page
  - [ ] Email/password form
  - [ ] Google Sign-In button
  - [ ] Role selection (Seeker/Host/Manager)
  - [ ] Email verification required
- [ ] Login page
  - [ ] Remember me option
  - [ ] Forgot password flow
- [ ] Firestore security rules
  - [ ] Users can only read/write their own data
  - [ ] Admin role for moderation
- [ ] Test all auth flows

#### Profile Setup (Week 3-4)
- [ ] Basic info form
  - [ ] Name, age, gender (optional)
  - [ ] Location (city + area)
  - [ ] Bio (50 char minimum, 300 max)
- [ ] Photo uploads
  - [ ] Minimum 2 photos required
  - [ ] Client-side validation (size <2MB, format JPG/PNG)
  - [ ] Upload to Firebase Storage
  - [ ] Compress images before upload
- [ ] Preferences (for seekers)
  - [ ] Budget range (slider: ₱2k - ₱20k)
  - [ ] Move-in date (calendar picker)
  - [ ] Lifestyle: Cleanliness, Noise level, Pets, Smoking, Guests
  - [ ] Must-haves vs Nice-to-haves
- [ ] Property details (for hosts)
  - [ ] Address (hide exact location until match)
  - [ ] Room type (Single/Shared/Studio)
  - [ ] Rent price
  - [ ] Amenities (WiFi, AC, Parking, etc.)
  - [ ] House rules

#### Swipe Interface (Week 5-6)
- [ ] Port existing swipe code to framework
  - [ ] Card stack component
  - [ ] Drag gesture handling (touch + mouse)
  - [ ] Like/Nope/Super Like animations
- [ ] Fetch profiles from Firestore
  - [ ] Query: opposite role, same city, budget compatible
  - [ ] Limit: 50 profiles per load
  - [ ] Pagination (lazy load more)
- [ ] Match algorithm (client-side)
  - [ ] Calculate compatibility score (0-100%)
  - [ ] Weight factors: Budget match (30%), Location (25%), Lifestyle (45%)
  - [ ] Show match % on card
- [ ] Daily swipe limit (free tier: 10/day)
  - [ ] Store count in Firestore user doc
  - [ ] Reset at midnight (Cloud Function or client-side)
- [ ] Action buttons
  - [ ] Nope (pass)
  - [ ] Like (match if mutual)
  - [ ] Super Like (priority notification)
  - [ ] Undo (last action only)

#### Matching & Chat (Week 7-8)
- [ ] Match detection
  - [ ] When both users like each other → create match document
  - [ ] Send push notification (if implemented) or email
- [ ] Matches screen
  - [ ] List all matched users
  - [ ] Show match date, compatibility %
  - [ ] Quick "start chat" button
- [ ] Basic chat
  - [ ] Real-time messages (Firestore listeners)
  - [ ] Text only (no images/files in MVP)
  - [ ] Typing indicator (optional)
  - [ ] Timestamp on messages
- [ ] Safety features
  - [ ] Report button (Scam/Harassment/Fake/Inappropriate)
  - [ ] Block user (hide from swipes + matches)
  - [ ] Safety tips modal on first chat

#### Analytics (Week 8)
- [ ] Firebase Analytics events
  - [ ] User sign-up (with role)
  - [ ] Profile completed
  - [ ] Swipe action (like/nope/super)
  - [ ] Match created
  - [ ] Message sent
- [ ] Client-side counter (for user dashboard)
  - [ ] Profile views: X people saw you
  - [ ] Likes received: X people liked you
  - [ ] Match rate: X% of your likes matched

### Monetization Integration

#### AdMob Setup (if mobile app)
- [ ] Create AdMob account
- [ ] Add AdMob SDK
- [ ] Implement interstitial ad
  - [ ] Show 1x after sign-up
  - [ ] Show 1x every 10 swipes (free tier)
- [ ] Test ads in dev mode
- [ ] Get ads approved (submit for review)

#### In-App Purchase (if mobile app)
- [ ] Set up payment provider
  - [ ] Google Play Billing (Android)
  - [ ] Apple In-App Purchase (iOS)
  - [ ] Or web: Stripe/PayMongo
- [ ] Create products
  - [ ] ₱149 Remove Ads (one-time)
  - [ ] ₱99 Premium Monthly (subscription)
  - [ ] ₱999 Premium Annual (subscription)
- [ ] Implement purchase flow
  - [ ] Product listing page
  - [ ] Payment button
  - [ ] Success/failure handling
  - [ ] Update Firestore (premium: true)
- [ ] Test with test payment methods

### Testing & QA (Week 9-10)

#### User Acceptance Testing
- [ ] Recruit 20 beta testers (from Phase 0 waitlist)
- [ ] Provide test credentials
- [ ] Create feedback form (bugs, confusing UX, feature requests)
- [ ] Monitor Firebase Console for errors
- [ ] Fix critical bugs

#### Performance Testing
- [ ] Test with 100+ profile database
- [ ] Check load times (<3 seconds)
- [ ] Optimize images (lazy load, compression)
- [ ] Test on slow 3G network

#### Security Audit
- [ ] Review Firestore security rules
  - [ ] Try accessing other users' data (should fail)
  - [ ] Test admin-only operations
- [ ] Check for exposed API keys (use .env)
- [ ] XSS prevention (sanitize user inputs)
- [ ] Rate limiting on swipes (prevent abuse)

### Launch Preparation (Week 10)

#### Content & Legal
- [ ] Update Privacy Policy (add specific features)
- [ ] Create onboarding tutorial (3 screens)
  - Screen 1: "Swipe right to like"
  - Screen 2: "Match when both like each other"
  - Screen 3: "Chat safely and meet in public"
- [ ] Write safety guidelines page
- [ ] FAQs page (10 common questions)

#### Marketing Assets
- [ ] App Store screenshots (if mobile)
- [ ] Launch video (30-60 seconds)
- [ ] Press release draft
- [ ] Social media launch posts (schedule)
- [ ] Email to waitlist: "We're live!"

#### Launch Checklist
- [ ] Domain configured (if custom)
- [ ] SSL certificate active (HTTPS)
- [ ] Analytics tracking confirmed
- [ ] Ads tested and approved
- [ ] Payment processing tested
- [ ] All critical bugs fixed
- [ ] Backup plan if server crashes

---

## 📈 Phase 2: Growth (Months 5-9)

### Manager Dashboard
- [ ] Design manager portal UI
- [ ] List properties (up to 5 free, 20 for ₱299/mo)
- [ ] Edit/delete listings
- [ ] View analytics per property (views, likes, messages)
- [ ] Vacancy calendar
- [ ] Inquiry management

### Enhanced Analytics
- [ ] User dashboard (pretty stats)
- [ ] Charts: Match rate over time
- [ ] Insights: "You get 30% more likes with better photos!"
- [ ] Heatmap: Where are your matches? (geographic)

### Chat Improvements
- [ ] Icebreaker suggestions ("Ask about their hobbies")
- [ ] Read receipts
- [ ] Push notifications (via Firebase Cloud Messaging)
- [ ] Message search
- [ ] Report detailed reasons

### Social Features
- [ ] Post-match "Share" button
  - [ ] Generate image card: "I found my roommate on RoomSwipe!"
  - [ ] Auto-share to X/FB/IG Stories
- [ ] Referral system
  - [ ] Unique referral code per user
  - [ ] Track sign-ups from code
  - [ ] Reward: 1 week unlimited swipes for both users

### Vacation Split Soft Launch
- [ ] Add "Vertical" field to profiles (Roommate/Vacation)
- [ ] Separate onboarding for vacation users
  - [ ] Travel dates, destination, group size, budget
- [ ] Swipe on vacation matches
- [ ] Test with 50 users
- [ ] Measure: Engagement vs roommate vertical

---

## 🌍 Phase 3: Expansion (Months 9-15)

### Resort Bookings Split
- [ ] Partner with 3-5 Cebu resorts
- [ ] Create resort listing format
- [ ] Group matching algorithm (2-6 people)
- [ ] Calendar integration for booking dates
- [ ] Payment split calculator (no in-app payment)

### Vacation Rentals
- [ ] Airbnb-style listing format
- [ ] Short-term stay swipe (weekends, holidays)
- [ ] Host verification (property photos, ID)

### Co-Working Space Sharing (New Vertical)
- [ ] Partner with co-working spaces in Manila/Cebu
- [ ] Split daily/monthly passes
- [ ] Match remote workers with similar schedules

### Advanced Features
- [ ] True ML matching (if budget allows)
- [ ] Fraud detection patterns
- [ ] Dynamic boost pricing (demand-based)

---

## 🚀 Phase 4: Scale (Month 15+)

### Infrastructure Scaling
- [ ] Monitor Firebase costs (set alerts)
- [ ] Optimize Firestore queries (indexes)
- [ ] Compress/archive old data (90+ days inactive)
- [ ] CDN for image delivery (Firebase Hosting + Cloudflare)

### Payment Integration
- [ ] GCash API for premium subscriptions
- [ ] PayMaya alternative
- [ ] Stripe for international users

### Advanced Security
- [ ] Cloud Vision API for photo moderation
- [ ] Rate limiting (Cloud Functions)
- [ ] Two-factor authentication (optional for users)

### Business Development
- [ ] App Store submissions (iOS/Android if not done)
- [ ] PR campaign (TechCrunch, TechInAsia)
- [ ] Partnership agreements (resorts, universities, corporations)
- [ ] Consider Series A funding (if applicable)

---

## 🔍 Ongoing Tasks (Every Week)

### Monitoring
- [ ] Check Firebase Console (errors, usage)
- [ ] Review user feedback (in-app + social media)
- [ ] Track KPIs: DAU, matches, revenue
- [ ] Monitor competitors (new features?)

### Marketing
- [ ] Post 3x/week on social media
- [ ] Respond to comments/DMs within 24h
- [ ] Engage with community (FB groups, Reddit)
- [ ] Share user success stories (with permission)

### Support
- [ ] Answer user questions (email/social)
- [ ] Review reports (scams, inappropriate content)
- [ ] Update FAQs based on common questions

---

## 📊 Success Metrics Tracker

### Phase 0 Goals
- [ ] 150+ waitlist sign-ups (Current: ___)
- [ ] 15+ manual matches (Current: ___)
- [ ] 80%+ satisfaction (Current: ___%)
- [ ] 3+ managers interested (Current: ___)

### Phase 1 Goals
- [ ] 500-1k registered users (Current: ___)
- [ ] 100+ matches (Current: ___)
- [ ] ₱1k+ monthly revenue (Current: ₱___)
- [ ] <5% churn rate (Current: ___%)

### Phase 2 Goals
- [ ] 2-5k DAU (Current: ___)
- [ ] 10+ properties listed (Current: ___)
- [ ] ₱5-10k monthly revenue (Current: ₱___)
- [ ] Viral coefficient >1.0 (Current: ___)

---

## 🎯 Priority Matrix

### Must Have (Critical for launch)
- Landing page live with waitlist
- Privacy Policy + Terms
- Firebase authentication
- Basic swipe interface
- Match + chat functionality

### Should Have (Important but not blocking)
- Photo uploads (can start text-only)
- Premium subscriptions (can add later)
- Manager dashboard (can wait for demand)
- Vacation vertical (Phase 2)

### Nice to Have (Future enhancements)
- Push notifications
- Advanced analytics
- ML matching
- Payment integration

---

## 📝 Notes

**Update this checklist weekly!**  
- Check off completed items
- Add new tasks as needed
- Update metrics section
- Move priorities as project evolves

**Next Review Date:** ___________

**Questions/Blockers:** (Add below)
- 
- 
- 

---

🇵🇭 **Let's build RoomSwipe!** 🚀
