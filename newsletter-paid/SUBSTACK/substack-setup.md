# Substack Setup Guide

> Complete walkthrough for setting up Substack for maximum growth and monetization. Based on Dickie Bush & Nicolas Cole's Substack Starter Kit.

---

## Account Creation Checklist

### Step 1: Basic Setup
- [ ] Create Substack account with professional email
- [ ] Choose publication name (see `POSITIONING/naming.md`)
- [ ] Write compelling one-line description
- [ ] Upload profile photo (headshot, not logo)
- [ ] Design publication logo/banner
- [ ] Connect custom domain (optional but recommended)

### Step 2: Publication Settings
- [ ] Set publication URL (subdomain.substack.com)
- [ ] Configure publication details
- [ ] Set up About page (use template in `AUTOMATION/platform-templates.md`)
- [ ] Write Welcome email (use `AUTOMATION/welcome-sequence.md`)
- [ ] Configure paid subscription settings
- [ ] Set up founding member tier

### Step 3: Content Settings
- [ ] Enable/disable comments (recommend: enabled)
- [ ] Configure thread notifications
- [ ] Set up section organization
- [ ] Enable podcast/audio if relevant
- [ ] Configure chat settings

### Step 4: Design & Branding
- [ ] Choose theme (keep simple, focus on readability)
- [ ] Set accent color (brand color)
- [ ] Upload favicon
- [ ] Configure Open Graph image

---

## The Substack Grand Tour

### Home Tab
Your publication's front page - what visitors see first
- Featured post controls first impression
- Organize sections logically
- Use Pinned Post strategically

### Posts Tab
Where you write and manage content
- Drafts, scheduled, and published posts
- Newsletter vs. post distinction
- Paywall settings per post

### Subscribers Tab
Your audience management center
- Subscriber growth tracking
- Free vs. paid breakdown
- Import/export functionality

### Stats Tab
Analytics dashboard
- Open rates, click rates
- Traffic sources
- Revenue tracking

### Settings Tab
All configuration options
- Publication details
- Monetization settings
- Integrations

---

## Substack-Specific Growth Features

### Substack Notes
- Short-form content platform
- Drives significant traffic to newsletter
- Algorithm favors engagement
- See `GROWTH/notes-traffic.md` for full strategy

### Recommendations
- Cross-promotion with other newsletters
- Give and receive recommendations
- Major growth lever at 1k+ subscribers

### Leaderboard
- Top publications by category
- Goal: reach category leaderboard

### Chat
- Community feature
- Use for premium subscribers
- Engagement and retention tool

---

## The Tech Stack Trap

**Warning (Dickie Bush):** Writers spend 80% of setup time on tech and 20% on what actually drives growth — writing, positioning, and offer clarity. The tech stack is a displacement activity.

**Rule:** Get writing before you get tools. Substack alone is enough to launch, grow to 1,000 subscribers, and monetize. Every tool added is a decision tax.

## Substack Tech Stack Integration

### Recommended Tools (add only when needed)

| Tool | Purpose | When to Add |
|------|---------|------------|
| **Notion** | Content calendar, idea bank, SOPs | After 4 weeks of consistent publishing |
| **Canva** | Cover images, social graphics, lead magnet PDFs | When visual assets become a bottleneck |
| **Claude / ChatGPT** | Drafting, editing, ideation — never publish AI first drafts | Day 1 |
| **WriteStack** | Substack-specific analytics (open rates, top posts, growth tracking) | After 500 subscribers — data is noise before this |
| **Kit (ConvertKit)** | Email automation, lead magnet delivery, external list building | When you need a lead magnet bridge or drip campaigns Substack can't handle |
| **Typeform** | Subscriber surveys (Welcome Post Upgrade) | After publishing your Welcome Post |
| **Typefully** | Cross-post Notes to Twitter/X for double distribution | When you want to amplify Notes with no extra work |
| **SparkLoop** | Paid referral growth | After 1,000 subscribers |
| **Grammarly** | Editing | Optional at any stage |
| **OBS** | Screen recording for video posts | If adding video |

### Integrations
- Stripe for payments (built-in to Substack — connect in Settings > Monetization)
- Google Analytics (limited; available via custom domain only)
- Custom domains via Cloudflare
- No public Substack API — Kit/Zapier connection requires a separate opt-in form that writes to both Substack and Kit simultaneously (lead magnet bridge strategy)

---

## The 7-Day Homepage Test

Before launching, test your Substack homepage:

**Day 1:** Look at homepage with fresh eyes
- Is the value prop clear in 3 seconds?
- Would you subscribe?

**Day 2:** Test on mobile
- 70% of traffic is mobile
- Ensure readability

**Day 3:** Share with 3 friends
- Get honest feedback
- Ask: "What do you think this is about?"

**Day 4:** Check load speed
- Substack is fast, but images slow it down
- Compress all images

**Day 5:** Review pinned post
- Does it represent your best work?
- Does it convert readers to subscribers?

**Day 6:** Test social sharing
- Share on Twitter/LinkedIn
- Check how preview cards look

**Day 7:** Final review
- All settings correct?
- Ready to promote?

---

## Substack Analytics Deep Dive

### Key Metrics to Track

**Growth Metrics**
- Total subscribers
- Free subscribers
- Paid subscribers
- Paid conversion rate
- Net new subscribers/week

**Engagement Metrics**
- Open rate (benchmark: 40-50%)
- Click rate (benchmark: 5-10%)
- Shares per post
- Comments per post

**Revenue Metrics**
- Monthly recurring revenue (MRR)
- Annual recurring revenue (ARR)
- Average revenue per user (ARPU)
- Churn rate (target: <5%/month)

**Traffic Sources**
- Substack network
- Direct traffic
- Social media
- Search
- Referrals

---

## Migration to Substack

### From Other Platforms

**ConvertKit → Substack**
- Export subscribers as CSV
- Import via Substack subscriber import
- Recreate sequences as posts
- Note: Automation not available in Substack

**Beehiiv → Substack**
- Export subscriber list
- Import to Substack
- Migrate posts manually or via API
- Reconfigure landing pages

**Ghost → Substack**
- Export members JSON
- Import to Substack
- Manual post migration
- Rebuild theme elements

### Import Checklist
- [ ] Export current subscriber list
- [ ] Clean list (remove bounces, unsubscribes)
- [ ] Import to Substack
- [ ] Send migration announcement
- [ ] Explain new features/benefits
- [ ] Set up redirect from old platform
- [ ] Update social media links

---

## Substack Best Practices

### Publishing Frequency
- **Free tier:** 1-2x per week
- **Paid tier:** 2-4x per week
- **Notes:** Daily or multiple times per day

### Post Timing
- Tuesday-Thursday: best open rates
- 8-10am in audience timezone
- Consistency > perfect timing

### Paywall Strategy
- First post: always free
- Regular cadence: 1 free, 1 paid
- Special content: paid exclusive
- Archive access: paid benefit

### Engagement Tactics
- Reply to all comments in first 24 hours
- Ask questions in posts
- Create polls
- Use "Ask me anything" format monthly

---

## Troubleshooting Common Issues

### Low Open Rates
- Check spam folder placement
- Improve subject lines
- Segment and re-engagement campaign
- Review sending frequency

### Low Paid Conversion
- Review offer clarity
- Improve free content value
- Add more lead magnets
- Test different paywall positions

### Subscriber Churn
- Survey departing subscribers
- Review content relevance
- Check deliverability
- Improve onboarding

### Technical Issues
- Contact Substack support
- Check status page
- Community forums
- Twitter/X DMs to Substack team
