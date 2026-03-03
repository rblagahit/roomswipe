# RoomSwipe Project Plan – Phased Development Roadmap

## Overview

This concrete project plan organizes all prior suggestions into prioritized phases, focusing on urgency (quick validation/growth) and impact (viral loops via free core, sharing, expansions). The app starts as a lightweight Tinder-style roommate finder (free tier Firebase/Vercel hosting, scalable via their pay-as-you-go). Core remains free with one-time pop-up ads (AdMob) + ₱149 lifetime remove-ads IAP.

Expansions tap new verticals: shared accommodations (e.g., resort bookings split among friends/groups), vacation rentals (Airbnb-style sharing costs), vacation packages (tour groups splitting flights/hotels). These build on swipe-matching for "cost-sharing matches" to go viral in PH travel/young adult scenes (e.g., Cebu beaches, Manila weekends).

### Key Constraints

- **Zero/minimal cost**: Free tiers only in early phases
- **Lightweight**: Client-side logic first
- **Scalable**: Firebase auto-scales; monitor limits ~10k users before Blaze tier ~₱200–1,000/mo

### Quick Wins/Big Impact Suggestions (Integrated into Phases)

**Features:**
- Referral program (invite friends → free boosts)
- Social sharing ("Matched! Share your roommate/vacay split")
- AI match suggestions (basic client-side scoring for virality)

**Security Protocols:**
- Firebase Auth rules (role-based access)
- Email verification
- Report/block in chats
- Photo moderation via free Cloud Vision API (if needed later)
- Keep lightweight: no heavy encryption early; focus on client-side validation + Firestore security rules

> **Note:** Phases are sequenced for viral effect: Start with core roommate matching (high urgency in urban PH like Cebu rentals), validate fast, monetize minimally, then expand verticals for broader appeal (travel sharing taps seasonal virality, e.g., summer resorts).

---

## Phase 0: Validation & Prototype

**Duration:** 1–2 Months  
**Urgency:** High  
**Impact:** Low Cost Proof-of-Concept

### Goal
Confirm demand before heavy dev; achieve early viral signals via manual loops.

### Core Activities

1. Deploy existing HTML/CSS/JS swipe prototype to Vercel (free) as landing/demo
2. Add Google Forms for waitlist/sign-up (role: seeker/host/manager) + interest in expansions (e.g., "Would you split resort bookings?")
3. Manual matching: Use Sheets + WhatsApp for first 20–50 users (test roommate + basic vacay split ideas)
4. Feedback: Post-demo surveys via Forms

### Quick Wins

- Social share button on demo ("Try the swipe! Share with friends") → viral loop starter
- Security: Basic form validation (no real data yet)

### Expansions Tapped
Survey for vertical interest (resorts/vacations) to prioritize

### Success Metrics
- 100+ sign-ups
- 10+ manual matches
- Positive feedback on expansions

### Cost
₱0

---

## Phase 1: Core MVP Launch – Roommate Focus

**Duration:** 2–4 Months  
**Urgency:** High  
**Impact:** Initial Virality

### Goal
Live app with free core; get to 500–1k users via local marketing (FB groups, Reddit r/Philippines, Cebu schools).

### Key Features

- **Auth:** Firebase (email/Google, roles)
- **Profiles:** Setup with prefs (lifestyle, budget)
- **Swipe/Match/Chat:** Existing code + Firestore for storage
- **Basic analytics:** Client-side counts (views/likes)

### Quick Wins/Big Impact

- **Referral:** "Invite friend → both get unlimited swipes for 1 week" (Firestore counter, viral in condos/groups)
- **AI-like scoring:** Simple client-side match % (e.g., 80% if prefs align) → better matches = more shares
- **Security:** Firestore rules (users see own data only), email verify on sign-up

### Monetization
- Add AdMob interstitial (1x per login/registration)
- ₱149 remove-ads IAP (in_app_purchase package)

### Expansions
None yet; focus on roommate vertical for quick wins (high demand in urban rentals)

### Deployment
Vercel frontend + Firebase backend (Spark free tier)

### Marketing
Share in local X/FB (e.g., "@lagahit testing RoomSwipe – Cebu roommates!")

### Success Metrics
- 500 DAU
- 100 matches
- Ad impressions >0

### Cost
₱0 (until limits)

---

## Phase 2: Polish & Monetization Ramp

**Duration:** 4–6 Months  
**Urgency:** Medium  
**Impact:** Revenue + Retention

### Goal
Stabilize core, add manager tools, start earning from ads/IAP; prep viral via expansions.

### Key Features

- **Manager Dashboard:** Simple list/add/edit properties (up to 5 free)
- **User Analytics:** Concise screen (top stats + 1 chart + insights)
- **Chat enhancements:** Icebreakers + report/block

### Quick Wins/Big Impact

- **Social sharing:** Post-match "Share your split!" button (to X/FB) → viral stories (e.g., "Found my Cebu roommate!")
- **Boost mechanic:** Free daily (or ad-view) for 1 listing → encourages daily logins/virality
- **Security:** Add photo upload limits + basic moderation (client-side size check; flag suspicious via reports)

### Monetization
- Optimize AdMob (A/B test frequency)
- Track IAP conversions (aim 5% of users)

### Expansions
Soft-launch "Vacation Split" category (swipe on shared resort bookings – e.g., match for Siargao group trips). Use same swipe logic; add "vertical" field in profiles (roommate vs. vacay).

### Deployment
Add Firebase Storage for photos (free tier 1GB)

### Marketing
Partnerships with Cebu resorts (free shoutouts for beta access)

### Success Metrics
- ₱5k+ monthly from ads/IAP
- 2k DAU
- 20% referral growth

### Cost
₱0–500 (if custom domain or exceed free tier slightly)

---

## Phase 3: Vertical Expansions & Virality Boost

**Duration:** 6–9 Months  
**Urgency:** Medium  
**Impact:** Broader Market

### Goal
Tap travel verticals for seasonal virality (e.g., summer resorts, holidays); scale users 10x.

### Key Expansions (Build on Core Swipe)

1. **Resort Bookings Split:** Swipe on group stays (e.g., "Split Boracay room – 4 people, ₱2k/night each"). Integrate basic calendar (free Datepicker lib)

2. **Vacation Rentals:** Match for Airbnb-style shares (e.g., "Split Manila condo for weekend")

3. **Vacation Packages:** Group matching for tours (e.g., "Split Cebu whale shark trip – flights/hotels included"). Partner with free APIs (e.g., browse travel sites for listings)

### Quick Wins/Big Impact

- **Group matching:** Allow 2–6 person swipes → viral among friends (share invites)
- **Seasonal campaigns:** Free boosts for summer vacays → timed virality
- **Security:** Add group verification (e.g., shared code for matches), transaction warnings (no payments in-app yet)

### Monetization
- Ads in expansions (e.g., resort pop-ups)
- Optional ₱99 boosts for vacay listings

### Deployment
Firebase Functions for any server logic (free tier 125k invokes/mo); scale to Blaze if traffic hits ~10k DAU

### Marketing
X/IG influencers in Cebu travel (free beta access for promo)

### Success Metrics
- 10k DAU
- 1k vacay matches
- Viral coefficient >1.2 (referrals drive growth)

### Cost
₱500–2,000/mo (Blaze + potential AdMob optimizations)

---

## Phase 4: Scaling & Advanced Security

**Duration:** 9+ Months  
**Urgency:** Low  
**Impact:** Sustainability

### Goal
Handle growth; add robust features once viral.

### Key Features

- Full analytics (heatmaps, demographics – premium tease)
- Integrations: Browse travel APIs for resort listings (free tiers)

### Quick Wins/Big Impact

- **Viral loops:** "Matched group? Rate & share photo" → user-generated content
- **Security:** Cloud Vision for photo moderation (free tier 1k/month), rate limiting on swipes

### Expansions
Deepen verticals (e.g., integrate vacay payment splits via GCash links – no in-app fees)

### Deployment
Monitor Firebase/Vercel; auto-scale (pay only for usage)

### Marketing
App Store optimization + paid ads if revenue allows

### Success Metrics
- 50k+ DAU
- Profitable ads/IAP

### Cost
Usage-based (~₱5k+/mo at scale)

---

## Summary

This plan prioritizes roommate core for urgent urban needs (virality via daily use), then expands to travel for big-impact seasonal spikes.

**Current Status:** Phase 0 - Landing page deployed, ready for validation phase.

**Next Immediate Steps:**
1. Deploy to Vercel
2. Create Google Forms for waitlist
3. Share demo on social media
4. Collect initial feedback

---

🇵🇭 Made with ❤️ in the Philippines
