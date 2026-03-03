# RoomSwipe Project Roadmap - Review & Updates

**Review Date:** March 3, 2026  
**Reviewer:** Development Analysis  
**Status:** Ready for Phase 0 Implementation

---

## Executive Summary

The roadmap is **well-structured** with clear phases, realistic constraints, and a viable path from validation to scale. Key strengths: focus on free tiers, viral mechanics, and phased feature rollout. Below are strategic updates and tactical refinements.

---

## ✅ Strengths

1. **Lean Validation Approach** - Phase 0 manual matching is smart; validates demand before coding
2. **Cost-Conscious** - Free tier strategy (Firebase Spark, Vercel) minimizes burn
3. **Viral Mechanics Built-In** - Referrals, social sharing, group matching create growth loops
4. **Clear Expansion Path** - Travel verticals leverage existing swipe mechanics (smart code reuse)
5. **Philippine Market Focus** - Targets specific pain points (urban rentals, beach trips)

---

## 🔄 Recommended Updates

### Phase 0 Enhancements

#### Add These Activities:
- **Landing Page CTA**: Add "Join Waitlist" button linking to Google Form directly on current index.html
- **Social Proof**: Track & display "X people waiting" counter on landing page (Google Sheets + simple API)
- **Competition Analysis**: Research existing PH roommate/travel split apps (Lamudi, OLX, FB groups) - document gaps
- **Legal Check**: Verify data privacy compliance (PH Data Privacy Act 2012) before collecting emails

#### Updated Timeline:
- Week 1-2: Deploy landing + forms, share on 3-5 FB groups + Reddit
- Week 3-4: Manual matching experiment (target 20-30 users minimum)
- Week 5-6: Interview 10 users (5 seekers, 5 hosts/managers) for feature prioritization
- Week 7-8: Compile findings, decide Phase 1 go/no-go

**Success Criteria Adjustment:**
- 100+ sign-ups → **150+ sign-ups** (higher bar for validation)
- 10+ manual matches → **15+ matches with 80% satisfaction**
- Add: **3+ property managers expressing interest in paid tools**

---

### Phase 1 Critical Additions

#### Security & Trust (Must-Haves for Launch):
1. **ID Verification (Light)**: 
   - Option to upload government ID (stored securely, not publicly visible)
   - Badge for verified users (increases matches by ~40% per similar apps)
   - Use Firebase Storage with security rules (only user + admin access)

2. **Safety Features**:
   - In-app "Safety Tips" section (meeting in public, telling friends, etc.)
   - Emergency contact field in profile (optional, private)
   - Report reasons: Scam, Harassment, Fake Profile, Inappropriate Photos

3. **Profile Quality**:
   - Minimum 2 photos required (increases match rate)
   - Bio character minimum (50 chars) to reduce low-effort profiles
   - Preference matching algorithm (client-side scoring is good, but document logic clearly)

#### Technology Stack Refinements:

**Frontend:**
- Consider **React** or **Vue** instead of vanilla JS (easier to maintain as features grow)
- Use **TailwindCSS** (already similar to your current styling approach)
- **Vite** for build tooling (faster than Webpack)

**Backend:**
- Firebase is correct choice, but add:
  - **Firestore Security Rules** from day 1 (critical)
  - **Cloud Functions** for sensitive operations (e.g., match notifications)
  - **Firebase Analytics** (free, better than client-side counting)

**Mobile Consideration:**
- Phase 1 should be **PWA** (Progressive Web App) - add manifest.json + service worker
- This gives "install to home screen" capability without app store submission
- Can convert to React Native in Phase 3 if needed

#### Monetization Adjustment:

**Issue with Current Plan:** One-time ₱149 IAP may not sustain long-term

**Better Hybrid Model:**
```
Free Tier:
- 10 swipes/day
- Basic chat
- 1 photo upload
- Ads (1 per session)

Premium Subscription (₱99/month or ₱999/year):
- Unlimited swipes
- No ads
- 5 photo uploads
- See who liked you
- Priority in search results

Manager Tools (₱299/month):
- List up to 20 properties
- Analytics dashboard
- Featured listings (1/week)
- Direct inquiry management
```

**Why This Works:**
- Recurring revenue > one-time payment
- Free tier validates users before they pay
- Manager tier taps landlord market (higher willingness to pay)
- Still accessible to students/young adults

---

### Phase 2 Updates

#### Analytics Scope:
Add these specific metrics to track:
- **Funnel Conversion**: Sign-up → Profile → Swipe → Match → Chat → Meetup
- **Match Quality Score**: Track "unmatch rate" + "report rate" to refine algorithm
- **Geographic Heatmap**: Where are users? (target marketing per city)
- **Time-Based Patterns**: Peak usage hours (optimize server costs + ad timing)

#### Manager Dashboard Must-Haves:
- **Vacancy Calendar**: Mark when rooms are available
- **Inquiry Management**: In-app notification when someone matches/messages about property
- **Performance Stats**: Views, likes, messages per listing
- **Competitive Pricing**: Show average rent in their area (crowd-sourced from other listings)

#### Seasonal Vacation Soft Launch:
**Better Approach:** Don't just add category, create **separate mini-brand**

- **"VacaySplit by RoomSwipe"** (clearer positioning)
- Separate onboarding flow (different questions: travel dates, group size, budget)
- Cross-promote: "RoomSwipe users, try VacaySplit for summer!"
- A/B test: Does same app dilute focus vs. cross-promotion benefits?

---

### Phase 3 Strategic Refinements

#### Expansion Prioritization:

**Recommended Order (Based on PH Market):**
1. **Resort Bookings Split** (highest viral potential - people share vacation plans naturally)
2. **Vacation Rentals** (Airbnb alternative - strong demand)
3. **Vacation Packages** (hardest - requires tour operator partnerships)

**Add: Co-Working Space Sharing**
- Splitting daily/monthly co-working passes (trending in PH remote work scene)
- Same swipe mechanics
- Targets digital nomads, freelancers
- Lower risk than travel (less commitment)

#### Partnership Strategy:

**Resorts/Hotels:**
- Approach with data: "We have 10k users looking for group stays"
- Revenue share vs. flat fee? (e.g., 5% booking commission vs. ₱5k/month listing fee)
- Start with Cebu properties (your local market), then expand

**Travel Agencies:**
- Joint ventures for vacation packages
- They provide inventory, you provide matching
- White-label option: They can embed your swipe UI on their site

#### Group Matching Complexity:

**Challenge:** Matching 4-6 people is NP-hard (combinatorics explode)

**Practical Solution:**
- Phase 3A: "Find 1-2 more people for existing group" (simpler)
- Phase 3B: "Match multiple solo travelers into groups" (harder, use basic clustering)
- Let groups self-form: Post "Looking for 2 more for Boracay trip" → targeted swipes

---

### Phase 4 Considerations

#### When to Scale Infrastructure:

**Triggers to Move from Free Tier:**
- Firestore: >1GB storage or >50k reads/day
- Cloud Functions: >125k invocations/month
- Storage: >5GB hosted files
- Hosting: >100GB bandwidth/month

**Cost Management:**
- Set budget alerts in Firebase Console (₱1k, ₱3k, ₱5k thresholds)
- Archive old inactive users (>90 days no login)
- Compress images (use Cloud Functions + Sharp library)
- Cache common queries (reduce Firestore reads)

#### Advanced Features:

**AI/ML (when profitable):**
- True ML matching (TensorFlow.js or Cloud ML API)
- Fraud detection (flag suspicious patterns)
- Dynamic pricing for boosts (demand-based)

**Payment Integration:**
- GCash API (primary for PH market)
- PayMaya (alternative)
- Stripe (international users)
- **Important:** Don't hold money - link to external payment splits (Splitwise API, etc.)

---

## 🚨 Risk Mitigation

### Legal/Compliance Risks:

1. **Data Privacy**
   - Action: Add Privacy Policy + Terms of Service (use template from Termly.io)
   - Store sensitive data (IDs) with encryption at rest
   - Right to deletion (GDPR-style even if not required in PH)

2. **Liability for Scams/Safety**
   - Disclaimer: "RoomSwipe is a platform; we don't verify users"
   - Verification badge mitigates but doesn't eliminate risk
   - Consider insurance or legal consult when DAU >5k

3. **Property Listing Regulations**
   - Some LGUs (Local Government Units) require permits for rental listings
   - Not your liability as platform, but warn managers
   - Partner with licensed brokers for legitimacy

### Technical Risks:

1. **Firebase Limits**
   - Firestore has 1 write/second per document limit
   - Solution: Shard popular documents (e.g., user counters)
   - Test at scale with load testing tools (Apache JMeter)

2. **Spam/Bots**
   - reCAPTCHA on sign-up (free, 1M requests/month)
   - Rate limiting: Max 100 swipes/hour per user (client + server-side)

3. **Photo Moderation**
   - Manual review queue for first 1000 users
   - Then add Cloud Vision API (free tier: 1k images/month)
   - Community reporting (if 3+ users report, auto-hide pending review)

### Market Risks:

1. **Competition**
   - Large players (e.g., Lamudi, OLX) could clone your swipe UX
   - Differentiation: **Community** + **Trust** + **Niche** (travel splits)
   - Build moat: Network effects (more users = better matches)

2. **User Acquisition Cost**
   - Organic growth may plateau at 5-10k users
   - Paid ads in PH: ₱10-50 per install (Facebook/IG)
   - Break-even: If Premium is ₱99/mo, need <1 month CAC payback
   - Focus on virality (referral rewards) to keep CAC near zero

---

## 📊 Updated Success Metrics

### Phase 0 (Validation):
- [ ] 150+ waitlist sign-ups
- [ ] 15+ manual matches (80% satisfaction)
- [ ] 3+ property managers interested
- [ ] 50+ demo shares on social media

### Phase 1 (MVP):
- [ ] 500-1k registered users
- [ ] 250+ matches completed
- [ ] 50+ active chats/day
- [ ] ₱1k+ monthly from ads/IAP (validates monetization)
- [ ] <5% churn rate

### Phase 2 (Growth):
- [ ] 2-5k DAU
- [ ] 10+ properties listed by managers
- [ ] ₱5-10k monthly revenue
- [ ] Viral coefficient >1.0 (organic growth)
- [ ] 50+ vacation split sign-ups (validates expansion)

### Phase 3 (Scale):
- [ ] 10-20k DAU
- [ ] 1k+ vacation matches
- [ ] ₱20-50k monthly revenue
- [ ] Partnership with 5+ resorts/agencies
- [ ] Featured in 1+ major PH tech blog

### Phase 4 (Sustainability):
- [ ] 50k+ DAU
- [ ] Profitable (revenue > costs + time value)
- [ ] 90-day retention >30%
- [ ] Ready for Series A funding (if desired)

---

## 🎯 Immediate Action Items (Next 7 Days)

### Priority 1 (Must Do):
1. ✅ Deploy current index.html to Vercel (DONE)
2. ✅ Push to GitHub (DONE)
3. ⏳ Enable GitHub Pages (IN PROGRESS)
4. ⏳ Create Google Form for waitlist (link in index.html)
5. ⏳ Draft Privacy Policy + Terms (use generator, refine later)

### Priority 2 (Should Do):
6. Set up Firebase project (Spark tier)
7. Create social media accounts (X: @RoomSwipePH, IG: @roomswipe.ph)
8. Design simple logo (Canva free tier)
9. Join 5 PH roommate/rental FB groups, introduce softly

### Priority 3 (Nice to Have):
10. Competitive analysis doc (30min research)
11. Create pitch deck (for future partnerships)
12. Set up analytics tracking (Firebase or Google Analytics)

---

## 💡 Strategic Recommendations

### Go-to-Market Twist:

**Consider: Launch on TikTok/Reels FIRST**
- Create "Day in the Life: Finding Roommates via Swipe" videos
- Show demo, real reactions
- PH social media users are heavy on short-form video
- Could get 10k+ waitlist faster than traditional marketing

### Pricing Psychology:

- ₱99/month positions as "daily coffee" (affordable)
- Annual ₱999 = 2 months free (incentivizes commitment)
- Manager tier ₱299 = "less than 1 day rental income"

### Partnership Leverage:

- Approach Cebu co-working spaces (The Company, IGBP) for cross-promo
- University partnerships (dorm alternatives for students)
- Corporate HR (relocation assistance for new hires)

---

## 📝 Documentation Needs

Before Phase 1 launch, document:

1. **Technical Architecture Diagram** (Firebase services, data flow)
2. **API Documentation** (Firestore structure, security rules)
3. **Brand Guidelines** (logo usage, colors, tone)
4. **Content Moderation Policy** (what gets flagged/banned)
5. **User Research Findings** (from Phase 0, inform Phase 1)

---

## Final Verdict

**Overall Assessment:** ⭐⭐⭐⭐ (4/5)

The roadmap is **production-ready** with minor adjustments. Strong focus on validation, lean operations, and viral mechanics. Main gap: under-emphasis on trust/safety features which are critical for marketplace apps.

**Recommended Changes Summary:**
- ✅ Keep: Phased approach, free tier strategy, expansion vision
- 🔄 Adjust: Monetization to subscription, add verification early
- ➕ Add: PWA capability, co-working vertical, partnership strategy
- ⚠️ Watch: Legal compliance, fraud prevention, CAC vs. LTV

**Go/No-Go:** ✅ **GO** - Proceed with Phase 0 immediately

---

**Next Review:** After Phase 0 completion (~2 months) to assess Phase 1 readiness

**Questions/Concerns?** Document in GitHub Issues for tracking.

🚀 Ready to build! 🇵🇭
