# AARRR Model - Tendd

**Status:** v1 - initial model. Metrics targets are hypotheses. All targets marked [? hypothesis].

---

## Acquisition

**Channels and mechanics:**
- Organic search (SEO): content around "subscription tracker," "how to cancel subscriptions," "am I overpaying for subscriptions," "best way to track recurring payments"
- Social content (TikTok, Instagram Reels, Reddit): UGC-style content showing the discovery moment - the reveal of hidden subscriptions and the calm they create
- Reddit communities: r/personalfinance, r/frugal, r/UKPersonalFinance, r/malelivingspace (cross-post adjacency)
- Word of mouth: friend showing a friend the subscription list reveal
- App store / ProductHunt listing (for awareness, not primary driver)
- Paid social (later stage): retargeting after organic content validates messaging

**Key hypotheses:**
1. The "subscription reveal" moment is shareable content - a clean before/after or a count ("I found 14 subscriptions I forgot about") will drive organic sharing [? hypothesis]
2. SEO around "subscription tracker" and "how to cancel X subscription" will capture high-intent users cheaply [? hypothesis]
3. The product does not need paid acquisition in early stages if the free tier delivers clear enough value to generate referrals [? hypothesis]

**What's unknown:**
- Whether Reddit and TikTok audiences convert at meaningfully different rates
- Whether "subscription tracker" or "spending tracker" is the better SEO anchor term
- CPAs for paid social in this category

**Primary metric:** New signups per week
**Target:** 100 signups/week within 3 months of launch [? hypothesis]

**MVP product decision:** Build a shareable "subscription snapshot" - a single-screen summary a user can screenshot or share (e.g. "I pay for X subscriptions totaling $Y/month") that acts as organic acquisition content.

---

## Activation

**Channels and mechanics:**
- Onboarding: single-purpose flow - one job, one screen, one action
- Bank connection (Plaid/TrueLayer): the fastest path to the "aha moment"
- Manual entry fallback: for users who don't want to connect a bank account yet
- Progressive disclosure: show value immediately with basic info, ask for more later
- "Aha moment" trigger: the first time a user sees their full subscription list with a total

**Key hypotheses:**
1. The "aha moment" - the subscription list with total - is the activation event. Users who see this are significantly more likely to return and eventually pay [? hypothesis]
2. Bank connection dramatically increases activation quality but increases friction. The correct design is to make bank connection feel safe and optional-but-recommended, not required [? hypothesis]
3. Users who add at least 3 subscriptions (manually or via bank) in their first session are 3x more likely to return within 7 days [? hypothesis]

**What's unknown:**
- What percentage of users will connect a bank account vs. add manually
- How much trust language/UI around bank connection changes connection rates
- Optimal number of "subscriptions seen" to trigger the aha moment

**Primary metric:** % of new users who experience the "aha moment" (see their subscription list with a total) within their first session
**Target:** 40% within 24 hours of signup [? hypothesis]

**MVP product decision:** Design the entire onboarding around one moment: "See your subscriptions." Every step before that is eliminated or deferred. The first screen after sign-up shows: "Here's what we found" or prompts to add the first subscription. No configuration, no profile setup, no feature tour.

---

## Retention

**Channels and mechanics:**
- Email: weekly "subscription digest" - a calm summary of what's happening (upcoming renewals, any changes)
- Push notifications (web push): price change alert, failed payment alert, trial ending alert
- In-app return hooks: "Your Netflix price went up" visible on next login
- Monthly insight: "Here's what you spent on subscriptions this month vs last month"
- Cancel assist prompt: "You haven't used X in 30 days - want to cancel it?"

**Key hypotheses:**
1. A weekly email digest is the highest-ROI retention mechanic. Users who receive it return at 2x the rate of those who don't [? hypothesis]
2. Price change alerts are the single best push notification because they are genuinely helpful (not marketing). They create a "Tendd caught that before I did" trust moment [? hypothesis]
3. Users who cancel at least one subscription via Tendd in the first 30 days have dramatically higher 90-day retention because they feel the product delivered on its promise [? hypothesis]

**What's unknown:**
- Optimal frequency for the email digest (weekly vs bi-weekly)
- Whether free users or paid users respond better to price-change push notifications
- What "subscription reviewed" behavior (vs "subscription cancelled") looks like in terms of retention impact

**Primary metric:** 30-day retention rate (% of users still active 30 days after signup)
**Target:** 30% for free users, 60% for paid users [? hypothesis]

**MVP product decision:** Ship the weekly email digest on day 1. It is the lowest-cost, highest-value retention mechanic and can be built before the full notification system. The digest content: upcoming renewals in the next 7 days, total monthly spend, one callout (e.g. "Your Spotify Premium renewed yesterday - $9.99").

---

## Revenue

**Channels and mechanics:**
- Freemium conversion: free users hit the 10-subscription limit or want a premium feature
- Upgrade triggers: encountering the paywall at moments of high motivation (after discovering a forgotten subscription, after seeing a price increase)
- Pricing: approximately $4 to $6/month or $40 to $50/year (hypothesis)
- Annual discount: 2 months free (standard SaaS incentive)

**Key hypotheses:**
1. The highest-converting upgrade trigger is the moment after discovering a forgotten subscription. "You found a subscription you forgot about - upgrade to see all your history and cancel it easily" [? hypothesis]
2. Annual billing will account for 40 to 60% of paid users because the annual price feels like "less than one cancelled subscription pays for itself" [? hypothesis]
3. $4.99/month is the optimal price point - below the $5 psychological threshold while still generating meaningful LTV [? hypothesis]

**What's unknown:**
- Actual willingness to pay (requires user research)
- Whether the 10-subscription free limit is the right trigger or whether another feature is more motivating
- Competitor pricing dynamics (to be validated in Phase 3)

**Primary metric:** Free-to-paid conversion rate
**Target:** 5 to 8% of active free users within 90 days [? hypothesis]

**MVP product decision:** The free tier must feel genuinely useful (not crippled) to build trust and word of mouth. The limit should be quantity (subscriptions) not quality (features). Users should not feel punished - they should feel that they have outgrown the free tier naturally.

---

## Referral

**Channels and mechanics:**
- Shareable subscription snapshot: a card or screenshot users can share ("I pay for 14 subscriptions - here's my monthly total")
- Partner invite: "Track subscriptions together" shared household feature
- Word of mouth trigger: the surprise moment when a user realizes how much they're spending
- App store reviews: prompted after a user successfully cancels a subscription
- NPS survey at day 30

**Key hypotheses:**
1. The "subscription count reveal" is inherently shareable because it is surprising and relatable. People will share it the same way they share their Spotify Wrapped result [? hypothesis]
2. Users who have cancelled at least one subscription are the most likely to recommend because they have a concrete story to tell [? hypothesis]
3. A formal referral program (give $X, get $X) is less effective than making the product itself shareable for this audience [? hypothesis]

**What's unknown:**
- Whether users are comfortable sharing subscription data publicly (even anonymized)
- Whether partner invite drives meaningful volume in the MVP timeframe
- NPS benchmark for this category

**Primary metric:** Referral rate (% of new signups attributed to a referral from an existing user)
**Target:** 15 to 20% of new signups from referrals within 6 months [? hypothesis]

**MVP product decision:** Build the shareable snapshot card (just a well-designed image or link) before building a formal referral program. The shareable card is lower cost and more authentic for this audience.

---

## Summary Metrics Table

| Stage | Primary Metric | MVP Target | Source |
|-------|---------------|-----------|--------|
| Acquisition | New signups/week | 100/week at 3 months [? hypothesis] | Internal |
| Activation | % users who see full subscription list in session 1 | 40% within 24h [? hypothesis] | Internal |
| Retention | 30-day active rate | 30% free / 60% paid [? hypothesis] | Internal |
| Revenue | Free-to-paid conversion | 5 to 8% within 90 days [? hypothesis] | Internal |
| Referral | % signups from referrals | 15 to 20% at 6 months [? hypothesis] | Internal |

---

## Key Product Takeaways

1. **Activation is everything.** The entire product experience should be designed around one goal: getting a user to the "subscription list reveal" moment as quickly and calmly as possible. Every step that delays that moment is a conversion killer.

2. **Trust unlocks activation.** Bank connection is the fastest path to value, but only if the user trusts us enough to do it. This means trust-building language, privacy explainers, and transparency must come before the connection prompt - not after.

3. **Retention is built on notifications done right.** The weekly digest and price-change alerts are not features - they are the core retention engine. They must be useful and calm, not pushy or frequent. One genuinely helpful alert beats ten promotional ones.

4. **The cancel moment is the revenue moment.** The upgrade trigger is most powerful immediately after a user finds a forgotten subscription or sees a price increase. The product must detect and surface these moments and connect them directly to the upgrade flow.
