# MEEM YASER STUDIO — COMPLETE PROJECT CONTEXT
## Every Detail From Every Session, Email, Demo, and Questionnaire

**Compiled:** 2026-04-24  
**Client:** Meem Yaser Studio  
**Email:** hello@meemyaserstudio.ae  
**Location:** Dubai, UAE  
**Instagram:** @meemyaserstudio  
**Website:** meemyaserstudio.ae  
**Contact:** Meem Yaser (she/her)

---

## 1. BRAND & NAMING (CRITICAL — DO NOT GET THIS WRONG)

### Trademark Hierarchy
| Level | Name | Usage |
|---|---|---|
| **Registered Trademark** | **Restless Worlds™** | The brand. The universe. The studio identity. |
| **Content Category** | **Rūsuma** (EN) / **روسوما** (AR) | Meem coined this to fill the Arabic gap for "comics/manga." No proper Arabic equivalent exists. |
| **Platform Name** | **Reading Club** | Was "Private Reading Club" — changed to "Reading Club" to be more open and welcoming. |
| **Proposed Domain** | **restlessworlds.com/reading-club** | |

### Brand Colors
- **Palette:** White, black, grey, **gold** (#D4AF37 / #C9A227 / #E8C84A)
- **Red/crimson was explored** — acknowledged as sophisticated but gold is preferred and on-brand.
- **Landing pages:** Light warm off-white (#FAFAF8)
- **Reader/Admin:** Always dark (#0A0A0A)

### Typography
- **Display:** Cormorant (serif, premium editorial)
- **Body:** Space Grotesk (geometric sans, clean)
- **Arabic:** Full RTL support required. Arabic font rendering issue was flagged and needs fixing before production.

### What NOT to Say
- **NEVER** call it "manga" or "comics" in the UI. SEO/meta tags can use those terms for discoverability, but the platform itself uses "Rūsuma" or "Stories."
- "Private Reading Club" → **"Reading Club"** (more welcoming)

---

## 2. CLIENT BACKGROUND & WORKFLOW

### Who Is Meem
- Creator — she writes AND draws the stories.
- Will **NOT** personally moderate the forum or comments.
- Will appoint dedicated moderator(s) later.
- Has **300+ characters** across her stories.
- Stories may include **seasons** (StoryName/Season01/Ch01/).
- Sometimes splits chapters into parts (uploads 20 pages as "Part 1," continues later).
- Has existing websites and social media accounts to integrate.
- Will set up Stripe when ready to launch subscriptions (not before).

### Content Creation Workflow
- Organizes files as: `StoryName/Season01/Ch01/`
- Names pages: `001.jpg`, `002.jpg` (zero-padded)
- Uses a mix of **PNG and JPEG**
- Wants **automatic WebP conversion** on upload
- Wants **drag-and-drop folder upload** (like Dropbox) — NO zipping required
- Does NOT always upload full chapters at once — needs progressive chapter updates

### Assets She Can Provide
- **Logo only** — VeloxStudio designs everything else
- Chapter images + cover art + title/synopsis/tags metadata per story
- Character art and world-building docs exist but need their own upload section
- Full brand kit does NOT exist yet

---

## 3. PLATFORM VISION & DESIGN PHILOSOPHY

### Emotional Mandate (Direct Quote)
> "I care a lot about how the reader feels while using the platform — it should be comfortable, immersive, and easy to navigate. I prefer a calm, uncluttered experience where the focus is always on the story."

### Aesthetic Direction
- **Premium / luxury / editorial / high-end**
- **Clean, minimal, elegant**
- **Zero visual noise**
- **No clutter, no distraction**
- **Apple + Notion + Webtoon + Discord** feel
- Every screen must feel intentional
- The reader experience is sacred — no feature competes with the page

### Homepage
- **Cover grid** of main stories (not "trending this week")
- Less crowded, reading-focused
- Random character strip for dynamic feel
- FAQs in side menu (not on homepage)
- Membership prompt placed later in flow (not upfront/intimidating)

---

## 4. ACCESS MODEL & MEMBERSHIP

### User Roles
1. **Guest** — can browse library, sees locked chapters
2. **Member** — premium access to locked chapters
3. **Admin** — full access, content management

### Membership Flow
- Visitors browse freely
- Meem defines which chapters are free vs locked
- Locked chapters require sign-up
- **Auto-approval after T&C acceptance** — no manual approval queue
- Forum requires sign-up
- Paid subscriptions / paid access **deferred** — focus on building reader base first
- When subscriptions launch: Stripe (she'll set up when ready)

### Content Protection
- **NO right-click / download / save image** — reading stays fully within the site
- NO offline reading or caching chapters on device
- PWA experience (add to home screen, fullscreen) BUT no offline storage

---

## 5. DEMO HISTORY & FEEDBACK CYCLES

### Demos Built
All deployed at `https://kovadev17.github.io/meem-yaser-deploy/`

**Directions explored:**
1. Meem Yaser Platform (main system shell)
2. Restless Worlds Reader (core reading experience — **Meem's favorite**)
3. Restless Worlds (dark/atmospheric)
4. Dropbox Pure (upload-focused)
5. Webtoon Vertical (vertical scroll reader)
6. Character Universe (character-focused)
7. Club Forum (community-focused)

### Final Direction: COMBINED APPROACH
- **Restless Worlds Reader** as the core reading experience
- Integrated into **Meem Yaser Platform** as the main system shell

### Meem's Reader Feedback (Demo 5 / Restless Worlds Reader)
- ✅ Best reader so far — fills phone screen well, smooth page swiping
- ⚠️ Zoom issues (pinch-zoom problematic on mobile)
- ✅ Preferred over all other directions

### Fixes Applied After Feedback
- Removed star ratings (Meem doesn't want comparisons between stories)
- Replaced numbered thumbnail placeholders with manga-style character faces
- Removed annotation pins from reader by default (accessible via comment icon toggle)
- Gold color scheme replacing crimson
- Improved typography and readability
- Fixed mobile chapter-opening bugs
- Zoom fixes: boundary clamping for pan, improved pinch-to-zoom, 1-second lockout after pinch release, double-tap toggles 1x/2x
- Cache-busting with `?v=2` parameter

### Critical Note from Kova
> "These demos are standalone capability proofs/prototypes, NOT drafts of the final site. Production build will be from scratch with proper architecture, 60fps+ animations, and custom backend."

---

## 6. COMPLETE QUESTIONNAIRE ANSWERS — ROUND 1 (Original 30-question)

**NOTE:** Meem answered an older cached 30-question version. Q8 decoded as "es" (corrupted). Q18 skipped.

| Q# | Question | Answer |
|---|---|---|
| 1 | How should series be presented on homepage? | Cover grid |
| 2 | How should chapters be organized? | Simple numbered list, group into volumes/arcs later |
| 3 | How should chapters be listed? | Chapter title only |
| 4 | How should reading progress be tracked? | Notification-based |
| 5 | What at end of chapter? | Next button (explicit, not auto-advance) |
| 6 | Preload chapter images? | Yes, auto-preload |
| 7 | Double-page spreads? | Horizontal pan/zoom, keep full image intact |
| 8 | Subtitles for translated content? | **CORRUPTED** — decoded as "es" |
| 9 | Page turn animation? | Natural |
| 10 | Loading style? | Draft (low-res first, then sharpen) |
| 11 | Custom keyboard shortcuts? | Yes, custom |
| 12 | Right arrow key? | Next page |
| 13 | Swipe left? | Next page |
| 14 | Fullscreen mode? | Yes, simple |
| 15 | Reader background? | Blur (blurred current page) |
| 16 | Chapter list access? | Sidebar |
| 17 | Chapter list navigation? | Both (sidebar + floating) |
| 18 | Reader zoom? | **SKIPPED** |
| 19 | Notification types? | Both (in-app + email) |
| 20 | Notification system? | Rich |
| 21 | Notification design? | All types with user-level controls |
| 22 | Email vs WhatsApp? | Email ONLY. Required: new chapters. Optional: announcements. NO replies. |
| 23 | Notification tone? | Premium |
| 24 | High contrast mode? | Yes, manual toggle |
| 25 | Dyslexia font? | No |
| 26 | RTL layout? | Yes |
| 27 | Update frequency? | Irregular |
| 28 | Offline reading importance? | Low |
| 29 | Upload priority? | Three payments (payment schedule leaked into wrong section) |
| 30 | What matters most? | "Comfortable, immersive, easy to navigate. Calm, uncluttered. Focus on the story." |

---

## 7. COMPLETE QUESTIONNAIRE ANSWERS — ROUND 2 (Follow-up, 27 questions)

### Clarifications
| Q# | Question | Answer |
|---|---|---|
| 1 | Subtitles? | Other: "I prefer no overlay subtitles. Each language gets its own dedicated page version." |
| 2 | Zoom? | Other: "Pinch-to-zoom on mobile/iPad (no buttons). Desktop: zoom buttons minimal/auto-hide. Must not interfere with swiping." |

### Moderation & Team
| Q# | Question | Answer |
|---|---|---|
| 3 | How many moderators? | Not yet — will appoint later |
| 4 | Moderator autonomy? | Most actions, but bans/permanent removals need owner sign-off |
| 5 | Approval queue handler? | Other (no text) — BUT Q6 clarifies NO APPROVAL QUEUE |
| 6 | Same rules forum + comments? | Other: "Comments visible immediately (no pre-approval). Moderation via reporting, delete, ban." |
| 7 | Audit log? | Yes — detailed: who, what, when, reason |

### Content Upload
| Q# | Question | Answer |
|---|---|---|
| 8 | Folder structure? | Other: StoryName/Season01/Ch01/ |
| 9 | Page naming? | Zero-padded: 001.jpg, 002.jpg |
| 10 | File formats? | Other: PNG + JPEG mix. Auto-convert to WebP on upload. |
| 11 | Upload method? | Drag-and-drop folder |
| 12 | Character/world-building upload? | Separate section |
| 13 | Sample chapter for testing? | Yes — after scope signed (IP protection) |

### Assets & Brand
| Q# | Question | Answer |
|---|---|---|
| 14 | Visual assets per story? | Images + covers + title/synopsis/tags metadata |
| 15 | Existing brand assets? | Logo only |
| 16 | Landing page feel? | Premium / luxury / editorial |
| 17 | Theater mode? | Other: "No visible toggle. UI hides/shows on tap (like Dropbox). Clean, minimal, immersive." |
| 18 | Light/dark mode? | Other: "Reader = dark mode ONLY. Main website = light. No toggle needed." |

### Infrastructure
| Q# | Question | Answer |
|---|---|---|
| 19 | Domain ownership? | Yes — but needs DNS guidance |
| 20 | Repo handling? | She creates GitHub repo, invites us |
| 21 | Payment processor? | Other: "I'll set up Stripe when ready to launch subscriptions" |
| 22 | Existing infrastructure? | Other: "I have existing websites and social media to integrate" |

### Payment & Terms
| Q# | Question | Answer |
|---|---|---|
| 23 | Payment schedule? | Three payments |
| 24 | Payment method? | PayPal invoice |
| 25 | Platform priority? | Mobile-first |
| 26 | Merchandise later? | Maybe — but don't design around it |
| 27 | Anything else? | "I don't always upload full chapters at once. Need progressive chapter updates without breaking reading order." |

---

## 8. EMAIL THREAD HISTORY

### Thread 1: "Re: Reader feedback + your 5 questions" (Active)
- Meem sent questionnaire code (Round 1)
- Meem clarified: "I won't be personally moderating the forum or comments"
- Meem confirmed: "I'm ready to move forward with Phase 1"
- Meem requested: formal scope document and pricing before kickoff
- Meem wants: Dropbox-like folder upload (JPEG/PNG, no zipping)
- Meem flagged: Arabic font issue needs fixing
- Phase 2 scope: notifications, moderation system, roles, subscriptions

### Thread 2: "Rūsuma — Feedback Applied, Production Ready"
- Meem wants PWA behavior (add to home screen, fullscreen)
- Meem does NOT want offline reading or caching
- Meem does NOT want right-click/download/save image
- Reading must stay fully within the site

### Thread 3: "Manga Platform Prototype — Live Demo & Portfolio"
- Changed from "Private Reading Club" to "Reading Club"
- Proposed domain: restlessworlds.com/reading-club

### Kova's Business Terms Email (Original Offer)
Three options offered:
- A) More demo tweaks
- B) Start production
- C) Discuss terms first

**Meem chose C** — wants clarity on scope, payment schedule, timeline.

---

## 9. PRICING & PAYMENT (NEGOTIATED)

### Original Reddit Agreement
- Standard build: $2,000 Phase 1
- Phase 2: $1,600
- Total: $3,600 (discounted from $5,000–6,000 normal rate)
- Hosting: ~$10–15/month
- Maintenance: $80–150/year (NOTE: this was initially yearly — later corrected to monthly)

### Final Payment Schedule (Client Chose)
| Payment | Amount | When |
|---|---|---|
| Payment 1 | $1,500 | Before work begins |
| Payment 2 | $1,050 | Upon Phase 1 delivery |
| Payment 3 | $1,050 | Upon Phase 2 delivery |
| **Total** | **$3,600** | |

- **Method:** PayPal invoice ONLY
- No other payment methods available
- Minimum first payment: $1,500

### Maintenance (Post-Project, Optional)
| Tier | Price | Includes |
|---|---|---|
| Basic | $80/month | Hosting, security patches, critical fixes |
| Proactive | $150/month | + Performance monitoring, content updates, feature tweaks |

### Bug-Fix Warranty
- 30 days free after each phase delivery
- Covers defects only, not new features or scope changes

---

## 10. PHASE BREAKDOWN

### PHASE 1 — Core Reading Experience ($2,000)
**Timeline:** ~2 weeks from Payment 1

**Must Include:**
1. Landing & Library
   - Light mode (#FAFAF8), cover grid homepage
   - Story detail: cover, title, synopsis, tags, chapter list
   - Chapter list: simple numbered, title only
   - Bilingual EN/AR with full RTL
   - Mobile-first responsive

2. Horizontal Image Reader
   - Dark mode ONLY (#0A0A0A), no toggle
   - Blurred page background
   - Natural transitions, draft loading
   - Auto-preload next chapter
   - Double-page spread pan/zoom intact
   - Fullscreen simple toggle
   - Theater mode: tap to hide/show chrome (no visible button)
   - Chapter list: sidebar + floating
   - End-of-chapter: explicit Next button
   - High contrast manual toggle

3. Navigation & Controls
   - Right arrow = next page
   - Swipe adapts to LTR/RTL
   - Custom keyboard shortcuts
   - Mobile: pinch-to-zoom, no buttons
   - Desktop: minimal zoom buttons, auto-hide
   - Zoom never blocks swipe
   - 44px minimum touch targets

4. Content Upload System
   - Drag-and-drop folder upload
   - Folder name = chapter name
   - Natural sort by filename
   - Zero-padded filenames supported
   - Season support: StoryName/Season01/Ch01/
   - PNG/JPEG input, auto WebP conversion
   - Progressive chapter part updates

5. Auth & Roles
   - Guest / Member / Admin
   - Login gate with role routing
   - Admin panel foundation

6. Comment System Foundation
   - Spatial pinned comments (click page → pin → threaded sidebar)
   - Responsive pin scaling
   - Comments visible immediately (no pre-approval)
   - Reporting mechanism

### PHASE 2 — Community & Polish ($1,600)
**Timeline:** ~2 weeks from Phase 1 + Payment 2

**Must Include:**
1. Forum
   - Thread list with pin/hot badges
   - Thread detail with replies
   - Same moderation tooling

2. Character Profiles & World-Building
   - Separate upload section
   - Character grid with slide-in detail panels
   - World-building document hosting

3. Notification System
   - Rich in-app notifications
   - Email: new chapters (required), announcements (optional, user-controlled)
   - NO email for replies or interactions
   - NO WhatsApp
   - Premium tone
   - Per-user notification preferences

4. Moderation Tools
   - Comment deletion by moderators
   - User banning (permanent bans require owner sign-off)
   - Content reporting
   - Detailed audit log (who, what, when, reason)
   - Permission tier: routine moderation autonomous, escalations to owner

5. Membership & Access Control
   - Subscription gating architecture (Stripe-ready)
   - Free vs premium chapter badges
   - User role system

6. Integrations
   - Social media links
   - Existing website continuity
   - DNS configuration guidance

---

## 11. TECHNICAL REQUIREMENTS

### Architecture
- Web-based responsive SPA
- NO native apps
- Modern browser APIs for folder drag-and-drop
- Image processing pipeline for WebP conversion
- Responsive coordinate mapping for spatial comments
- RTL-aware components (flipped nav, mirrored layouts, Arabic typography)

### Performance
- Image lazy loading + preloading
- WebP delivery with fallback
- Optimized for irregular publishing
- Offline: low priority, basic caching only
- NO chapter download/offline storage

### Security
- Role-based access control
- Moderator permission tiers
- Audit logging
- Content protection: disable right-click, prevent image download/save

### PWA
- Add to home screen
- Fullscreen app-like experience
- NO offline reading
- NO caching chapters

---

## 12. CONTENT MODEL

```
Story
├── Season (optional)
│   ├── Chapter
│   │   ├── Part 1 (e.g., first 20 pages)
│   │   ├── Part 2 (appended later)
│   │   └── ... (progressive updates)
│   └── ...
├── Cover art
├── Title / Synopsis / Tags
├── Character profiles (separate section)
└── World-building documents (separate section)
```

**Upload Workflow:**
1. Drag folder onto upload zone
2. Parse path: StoryName/Season01/Ch01/
3. Read page files (001.jpg, 002.jpg...), natural sort
4. Convert PNG/JPEG → WebP
5. Create chapter, order by filename
6. Existing chapters can receive additional parts

---

## 13. EXCLUSIONS (WHAT IS NOT INCLUDED)

- Native iOS/Android apps
- WhatsApp notifications
- Dyslexia-friendly font
- Offline download/sync
- AI-generated content or recommendation engines
- Merchandise store or e-commerce (not designed around it)
- Custom video/audio player
- Translation services or subtitle generation
- Overlay subtitles on pages
- Light mode toggle for reader
- Phone/video call support
- Manual user approval queue (auto-approval after T&C)

---

## 14. ASSUMPTIONS & DEPENDENCIES

1. Client provides logo file
2. Client creates GitHub repo and invites us within 48h of kickoff
3. Client provides DNS access/coordination
4. Client provides sample chapter after contract signature
5. Client appoints moderator(s) before/during Phase 2
6. Stripe setup is client responsibility
7. Content upload is client responsibility
8. Third-party services remain available

---

## 15. COMMUNICATION RULES

- Email only (hello@meemyaserstudio.ae)
- NO phone or video calls
- Response time: 1 business day standard, 2 days for complex technical questions
- ProtonMail account: kovadevV@proton.me
- GitHub: kovadev17

---

## 16. EVERY FEATURE MAPPED TO SOURCE

| Feature | Source |
|---|---|
| Cover grid homepage | Q1 Round 1 |
| Chapter title only | Q3 Round 1 |
| Next button (not auto-advance) | Q5 Round 1 |
| Auto-preload | Q6 Round 1 |
| Double-page spread pan/zoom | Q7 Round 1 |
| No overlay subtitles | Q1 Round 2 |
| Natural transitions | Q9 Round 1 |
| Draft loading | Q10 Round 1 |
| Custom keyboard shortcuts | Q11 Round 1 |
| Right arrow = next | Q12 Round 1 |
| Swipe = next | Q13 Round 1 |
| Fullscreen simple | Q14 Round 1 |
| Blurred background | Q15 Round 1 |
| Sidebar chapter list | Q16 Round 1 |
| Sidebar + floating nav | Q17 Round 1 |
| Pinch-to-zoom mobile | Q2 Round 2 |
| Desktop zoom buttons | Q2 Round 2 |
| Both notification types | Q19 Round 1 |
| Rich notifications | Q20 Round 1 |
| User notification controls | Q21 Round 1 |
| Email only, no WhatsApp | Q22 Round 1 |
| Premium tone | Q23 Round 1 |
| High contrast toggle | Q24 Round 1 |
| No dyslexia font | Q25 Round 1 |
| Full RTL | Q26 Round 1 |
| Irregular publishing | Q27 Round 1 |
| Low offline priority | Q28 Round 1 |
| Three payment schedule | Q23 Round 2 |
| PayPal only | Q24 Round 2 |
| Mobile-first | Q25 Round 2 |
| Maybe merchandise later | Q26 Round 2 |
| Progressive chapter parts | Q27 Round 2 |
| Season folder structure | Q8 Round 2 |
| Zero-padded filenames | Q9 Round 2 |
| Auto WebP conversion | Q10 Round 2 |
| Drag folder upload | Q11 Round 2 |
| Separate character section | Q12 Round 2 |
| Sample after signature | Q13 Round 2 |
| Images + covers + metadata | Q14 Round 2 |
| Logo only brand assets | Q15 Round 2 |
| Premium landing feel | Q16 Round 2 |
| Theater mode tap-to-hide | Q17 Round 2 |
| Reader dark only, site light | Q18 Round 2 |
| DNS guidance needed | Q19 Round 2 |
| She creates repo | Q20 Round 2 |
| Stripe later | Q21 Round 2 |
| Existing sites to integrate | Q22 Round 2 |
| No pre-approval comments | Q6 Round 2 |
| Detailed audit log | Q7 Round 2 |
| Moderator most actions | Q4 Round 2 |
| Bans need owner sign-off | Q4 Round 2 |
| No right-click/download | Email Thread 2 |
| PWA without offline | Email Thread 2 |
| Reading Club naming | Email Thread 3 |
| Auto-approval after T&C | Session History |
| 300+ characters | Session History |
| Gold color scheme | Session History |

---

## 17. EVERYTHING MEEM HAS EXPLICITLY SAID NO TO

- No overlay subtitles
- No pre-approval for comments
- No dyslexia font
- No WhatsApp
- No offline reading
- No right-click/download
- No manual user approval queue
- No light mode in reader
- No visible theater mode toggle button
- No merchandise store architecture
- No native apps
- No phone/video calls
- No "Private" Reading Club (changed to "Reading Club")
- No manga/comics terminology in UI
- No star ratings (removed from demos)

---

## 18. EVERYTHING MEEM HAS EXPLICITLY SAID YES TO

- Yes to spatial pinned comments
- Yes to pinch-to-zoom on mobile
- Yes to zoom buttons on desktop (minimal)
- Yes to auto-preload
- Yes to fullscreen
- Yes to high contrast toggle
- Yes to RTL
- Yes to custom keyboard shortcuts
- Yes to drag-and-drop folder upload
- Yes to WebP auto-conversion
- Yes to season support
- Yes to progressive chapter parts
- Yes to detailed audit log
- Yes to email notifications
- Yes to in-app notifications
- Yes to forum
- Yes to character profiles
- Yes to world-building docs
- Yes to moderator system
- Yes to reporting/delete/ban tools
- Yes to PWA (add to home screen)
- Yes to gold color scheme
- Yes to premium editorial aesthetic
- Yes to mobile-first
- Yes to three payment installments
- Yes to PayPal
- Yes to Stripe-ready architecture

---

*END OF COMPLETE CONTEXT*
