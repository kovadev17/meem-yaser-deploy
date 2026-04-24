# MEGA PROMPT: Generate the Production Scope Document for Meem Yaser Studio

## YOUR ROLE
You are a senior technical product writer drafting a formal **Production Scope Document** for a client. This document will be attached to a contract and used as the single source of truth for development. It must be precise, complete, and leave zero ambiguity.

---

## CLIENT IDENTITY

**Client Name:** Meem Yaser Studio  
**Client Email:** hello@meemyaserstudio.ae  
**Client Location:** Dubai, UAE  
**Client Instagram:** @meemyaserstudio  
**Client Website:** meemyaserstudio.ae  
**Client Role:** Creator/Owner — she writes and draws manga. She will NOT personally moderate.  
**Studio:** VeloxStudio (us), represented by Kova  
**Project Brand Name:** Restless Worlds™ (registered trademark)  
**Content Category Name:** Rūsuma (روسوما) — coined by Meem to fill Arabic gap for comics/manga  
**Platform Name:** Reading Club (NOT "Private Reading Club")  
**Target Domain:** restlessworlds.com/reading-club  

---

## CRITICAL BRAND RULES

1. **Restless Worlds™** = the registered trademark and brand. The universe. The studio identity.
2. **Rūsuma / روسوما** = content category label. NOT the brand. Used in UI where "Stories" or "Manga" would go.
3. **NEVER** call it "manga" or "comics" in the UI. SEO/meta tags can use those terms for discoverability.
4. **"Reading Club"** (not "Private Reading Club") — changed to be more open and welcoming.
5. **Colors:** White, black, grey, **gold** (#D4AF37 / #C9A227 / #E8C84A). Landing light (#FAFAF8), reader dark (#0A0A0A).

---

## PROJECT OVERVIEW

Build a premium web-based manga/comic reading platform for Meem Yaser Studio. The platform is a reading experience where users browse a library of stories, read chapters in a horizontal image-based reader, leave spatial comments pinned to specific coordinates on pages, participate in a forum, view character profiles and world-building lore, and manage memberships.

**CRITICAL DESIGN PRINCIPLE (direct quote from Meem):**
> "I care a lot about how the reader feels while using the platform — it should be comfortable, immersive, and easy to navigate. I prefer a calm, uncluttered experience where the focus is always on the story."

**Emotional mandate:** Premium / luxury (clean, editorial, high-end). Calm. Uncluttered. Focus always on the story. Apple + Notion + Webtoon + Discord aesthetic. NO clutter. NO distraction. Every screen must feel intentional. The reader experience is sacred — no feature competes with the page.

---

## COMPLETE QUESTIONNAIRE ANSWERS — ROUND 1 (Original 30-question questionnaire)

**NOTE:** Meem answered an older cached 30-question version. Q8 decoded as "es" (corrupted). Q18 was skipped. These were clarified in Round 2.

### Library & Navigation
- **Q1: How should series be presented on the homepage?** → Cover grid (visual cover thumbnails)
- **Q2: How should chapters be organized within a series?** → "Simple numbered list for now, with the ability to group chapters into volumes or arcs later if needed."
- **Q3: How should chapters be listed within a series?** → Chapter title only (not "Chapter 1: Title")
- **Q4: How should reading progress be tracked?** → Notification-based (notify user of progress, not persistent progress bar)
- **Q5: What should happen at the end of a chapter?** → Next button (explicit button to next chapter, not auto-advance)
- **Q6: Should chapter images be preloaded?** → Yes, auto-preload (preload next chapter images automatically)
- **Q7: How should double-page spreads be handled?** → "Allow horizontal pan/zoom for spreads while keeping the full image intact."

### Reader Experience
- **Q8: Should subtitles be shown for translated content?** → **CORRUPTED** — decoded as "es". Clarified in Round 2: NO overlay subtitles. Each language gets its own dedicated page version.
- **Q9: Should there be a page turn animation?** → Natural (smooth, not slide or instant)
- **Q10: What loading style do you prefer for pages?** → Draft (show rough/low-res first, then sharpen)
- **Q11: Should custom keyboard shortcuts be supported?** → Yes, custom (user-defined shortcuts)
- **Q12: What happens when the user presses the right arrow key?** → Action (next page)
- **Q13: What happens when the user swipes left?** → Next page
- **Q14: Should there be fullscreen mode?** → Yes, simple (toggle, no extra effects)
- **Q15: What background do you prefer for the reader?** → Blur (blurred version of current page as background)
- **Q16: How should chapter list be accessed?** → Sidebar (slide-out panel)
- **Q17: Where should chapter list navigation live?** → Both (sidebar + floating/dockable)

### Accessibility
- **Q18: Should reader zoom be supported?** → **SKIPPED in Round 1**. Clarified in Round 2: Yes, pinch-to-zoom on mobile/iPad (no buttons), zoom buttons on desktop (minimal/auto-hide), must not interfere with page swiping.
- **Q19: What types of notifications should users receive?** → Both (in-app + email)
- **Q20: Should the notification system be simple or rich?** → Rich
- **Q21: Preferred notification system design?** → "All of the above, but with user-level controls to enable/disable each notification type"
- **Q22: Email vs WhatsApp vs both?** → Email notifications ONLY (no WhatsApp). Required: new chapter releases. Optional: announcements. NO email notifications for replies or other user interactions.
- **Q23: What tone should notifications have?** → Premium
- **Q24: Should high contrast mode be available?** → Yes, manual toggle
- **Q25: Should dyslexia-friendly font be available?** → No
- **Q26: Should RTL layout be supported?** → Yes (full Arabic RTL support required)

### Content & Updates
- **Q27: Preferred update frequency?** → Irregular (no fixed schedule, publish when ready)
- **Q28: How important is offline reading?** → Low priority
- **Q29: Upload experience priority?** → Three payments (this was a payment-schedule question that leaked into wrong section — payment clarified in Round 2)
- **Q30: What matters most?** → "I care a lot about how the reader feels while using the platform — it should be comfortable, immersive, and easy to navigate. I prefer a calm, uncluttered experience where the focus is always on the story."

---

## COMPLETE QUESTIONNAIRE ANSWERS — ROUND 2 (Follow-up, 27 questions)

### Clarifications
- **Q1: Subtitles for translated content?** → Other: "I prefer no overlay subtitles. Each language should have its own dedicated version of the pages, keeping the artwork clean and the reading experience intact."
- **Q2: Zoom support?** → Other: "Pinch-to-zoom on mobile and iPad with a clean UI (no buttons). On desktop, zoom buttons are fine as long as they stay minimal or auto-hide. Zoom should not interfere with page swiping."

### Moderation & Team
- **Q3: How many moderators?** → Not yet — but she'll appoint one later
- **Q4: What can moderators do without approval?** → Most actions — but bans and permanent removals require her sign-off
- **Q5: Who handles comment approval queue?** → Other (no text provided) — BUT Q6 clarifies there IS NO approval queue
- **Q6: Same moderation rules for forum + comments?** → Other: "I prefer comments to be visible immediately (no pre-approval). Please include moderation tools like reporting, the ability to delete comments, and ban users when needed."
- **Q7: Audit log for owner?** → Yes — detailed log: who did what, when, with reason

### Content Upload Workflow
- **Q8: Folder structure?** → Other: "Stories may include seasons, so the structure should support: StoryName/Season01/Ch01/"
- **Q9: Page file naming?** → Zero-padded: 001.jpg, 002.jpg (for large chapters)
- **Q10: File formats?** → Other: "I use a mix of PNG and JPEG. It would be ideal if the platform automatically converts and optimizes them to WebP during upload."
- **Q11: Upload method?** → Drag-and-drop a folder — system reads folder name, auto-sorts pages
- **Q12: Character profiles/world-building upload?** → Separate section
- **Q13: Sample chapter for testing?** → Yes — after we sign the scope (IP protection)

### Assets & Brand
- **Q14: Visual assets per story?** → Images + covers + title/synopsis/tags metadata
- **Q15: Existing brand assets?** → Logo only — we design the rest to match
- **Q16: Landing page feel?** → Premium / luxury (clean, editorial, high-end)
- **Q17: Theater mode?** → Other: "No visible toggle button. The UI should hide/show with a simple tap on the screen (like Dropbox). Clean, minimal, and immersive"
- **Q18: Light/dark mode?** → Other: "The reader should be dark mode only, while the main website stays light mode. No toggle or switching needed."

### Infrastructure
- **Q19: Domain ownership?** → Yes — but she needs guidance on DNS setup
- **Q20: Repo handling?** → She creates the GitHub repo and invites us
- **Q21: Payment processor?** → Other: "I'll set up Stripe when I'm ready to launch subscriptions"
- **Q22: Existing digital infrastructure?** → Other: "I have existing websites and social media accounts that should be integrated"

### Payment & Terms
- **Q23: Payment schedule?** → Three payments ($1,500 start / $1,050 mid / $1,050 delivery)
- **Q24: Payment method?** → PayPal invoice
- **Q25: Platform priority?** → Mobile-first
- **Q26: Merchandise later?** → Maybe — but don't design around it
- **Q27: Anything else?** → "I don't always upload full chapters at once. Sometimes I split a chapter into parts (e.g. 40 pages → upload 20 pages as Part 1, then continue later). So the system should support updating an existing chapter or adding parts progressively without breaking the reading order."

---

## ADDITIONAL REQUIREMENTS FROM EMAILS & DEMO FEEDBACK (NOT IN QUESTIONNAIRE)

### From Email Threads
- **PWA behavior**: Add to home screen, fullscreen app-like experience
- **NO offline reading or caching chapters on device**
- **NO right-click, download, or save page images** — reading stays fully within the site
- **Dropbox-like folder upload**: Drag JPEG/PNG folders directly, NO zipping required
- **Arabic font issue** needs fixing before production
- Meem confirmed: "I'm ready to move forward with Phase 1"
- Meem requested: formal scope document and pricing before kickoff
- Phase 2 confirmed to include: notifications, moderation system, roles, subscriptions

### From Demo Feedback Sessions
- **Combined approach**: Restless Worlds Reader (core reading) + Meem Yaser Platform (system shell)
- **300+ characters** across stories must be supported
- **Character "likes"** on bios for popularity tracking (future merchandising data)
- **Random character strip** on homepage for dynamic feel
- **Stats feature** appreciated and to be included
- **Membership prompt placed later** in flow (not upfront/intimidating)
- **Chapters list next to comments icon**
- **FAQs in side menu** (not on homepage)
- **Auto-approval after T&C acceptance** (no manual approval queue)
- Removed star ratings (no inter-story comparisons)
- Mobile reader must be flawless — "the reading experience is what will make or break the brand"

---

## SYNTHESIZED REQUIREMENTS

### A. Platform Architecture
- **Web-based, responsive** — no native apps
- **Mobile-first** design priority
- **Bilingual**: English + Arabic with full RTL support
- **Domain**: restlessworlds.com/reading-club (she owns it, needs DNS help)
- **Repo**: She creates GitHub repo, invites us as collaborator
- **PWA**: Add to home screen, fullscreen, BUT no offline storage
- **Content protection**: Disable right-click, prevent download/save of images

### B. Content Model (CRITICAL)
- **Stories may have SEASONS**: StoryName/Season01/Ch01/
- **Chapters may be split into PARTS**: A chapter can be uploaded in pieces (e.g., 20 pages as Part 1, then continued later). System must support updating existing chapters / adding parts progressively WITHOUT breaking reading order.
- **Page naming**: Zero-padded (001.jpg, 002.jpg)
- **File formats**: PNG + JPEG mix. Auto-convert to WebP on upload.
- **Folder upload**: Drag-and-drop folder. System reads folder name as chapter name. Auto-sorts pages by filename.
- **Assets per story**: Chapter images + cover art + title/synopsis/tags metadata
- **Brand assets**: Logo only provided. We design everything else.
- **300+ characters** supported with organized data structure

### C. Reader (The Core Product)
- **Horizontal image-based reader** (manga pages as images)
- **Dark mode ONLY** for reader. Light mode for main website. No toggle in reader.
- **Background**: Blurred version of current page
- **Loading**: Draft mode (show low-res first, sharpen)
- **Preload**: Auto-preload next chapter images
- **Double-page spreads**: Horizontal pan/zoom, keep full image intact
- **No overlay subtitles**: Each language gets its own page version
- **Zoom**:
  - Mobile/iPad: Pinch-to-zoom, NO buttons, clean UI
  - Desktop: Zoom buttons allowed but must be minimal / auto-hide
  - Zoom must NOT interfere with page swiping
- **Page transitions**: Natural/smooth
- **Navigation**:
  - Keyboard: Right arrow = next page
  - Swipe: Adapts to reading direction (LTR: left swipe = next; RTL: right swipe = next)
  - Custom keyboard shortcuts (user-configurable)
- **Theater mode**: NO visible toggle button. UI hides/shows with simple tap on screen (like Dropbox). Clean, minimal, immersive.
- **Fullscreen**: Simple toggle
- **End of chapter**: Next button (explicit, not auto-advance)
- **High contrast mode**: Manual toggle available
- **Dyslexia font**: NOT needed
- **RTL**: Full Arabic support
- **All touch targets**: Minimum 44px

### D. Comments & Community (SPATIAL COMMENTS — #1 selling feature)
- **Spatial/pinned comments**: Users click/tap page coordinates → drop numbered pin → threaded comment in sidebar. Like Dropbox comments.
- **NO pre-approval for comments**: Visible immediately
- **Moderation tools**: Reporting, delete comments, ban users
- **Forum**: Separate from page comments. Same moderation tooling.
- **Audit log**: Detailed — who did what, when, with reason

### E. Library & Discovery
- **Homepage**: Cover grid presentation (not "trending this week")
- **Chapter list**: Simple numbered list, chapter title only
- **Progress tracking**: Notification-based (not persistent progress bar)
- **Character profiles**: Separate section, own upload area
- **World-building docs**: Separate section
- **Random character strip** on homepage
- **Character "likes"** for popularity tracking

### F. Notifications
- **Rich notification system** with user-level controls
- **In-app + email** (both)
- **Email content**: New chapter releases (required), announcements (optional)
- **NO email for**: Replies, user interactions
- **NO WhatsApp**
- **Tone**: Premium

### G. Admin / Content Management
- **Upload method**: Drag-and-drop folder (like Dropbox, NO zipping)
- **Auto-detect**: Story, season, chapter from folder structure
- **Auto-convert**: PNG/JPEG → WebP on upload
- **Character/world-building**: Separate upload section (not same as chapters)
- **Moderator roles**:
  - She appoints moderator(s) later
  - Most actions autonomous
  - Bans/permanent removals require her sign-off
  - Detailed audit log
- **Sample chapter**: Provided after scope signed (IP protection)

### H. Design System
- **Landing pages**: Light warm off-white (#FAFAF8), editorial feel
- **Reader + Admin**: Always dark (#0A0A0A)
- **Accent**: Gold (#D4AF37 / #C9A227)
- **Typography**: Cormorant (display) + Space Grotesk (body)
- **Feel**: Premium, editorial, luxury, clean, minimal
- **NO clutter, NO distraction**

### I. Membership & Billing (FUTURE — not Phase 1)
- **Payment processor**: Stripe (she'll set up when ready)
- **Subscription gating**: Architecture must support it but may not be active at launch
- **Access model**: Visitors browse freely, free chapters defined by Meem, locked chapters require sign-up, auto-approval after T&C

### J. Integrations
- **Existing websites and social media** — to be integrated
- **Domain**: restlessworlds.com — she owns it

---

## PHASE BREAKDOWN & PRICING

### PHASE 1 — Core Reading Experience ($2,000)
- Scope: Landing/library, horizontal reader, content upload system, auth/roles, comment foundation
- Delivery: Working platform with core reading experience
- Timeline: ~2 weeks after Payment 1

### PHASE 2 — Community & Polish ($1,600)
- Scope: Forum, character profiles, world-building, notification system, moderation tools, membership/payment integration prep
- Delivery: Full platform feature-complete
- Timeline: ~2 weeks after Phase 1 delivery + Payment 2

### TOTAL: $3,600 (discounted from standard $5,000–$6,000)

### PAYMENT SCHEDULE (client chose)
- **Payment 1**: $1,500 upfront — before work begins
- **Payment 2**: $1,050 at Phase 1 delivery
- **Payment 3**: $1,050 at Phase 2 delivery (final)
- **Method**: PayPal invoice

### BUG-FIX WARRANTY
- 30 days free bug fixes after each phase delivery
- Does not cover new features or scope changes

### MAINTENANCE (optional, post-delivery)
- **Basic**: $80/month — hosting, security patches, critical fixes
- **Proactive**: $150/month — + performance monitoring, content updates, feature tweaks
- Month-to-month, cancel anytime

---

## TECHNICAL CONSTRAINTS & NOTES

1. **Single-file HTML demo exists** — it was a FREE exploration, NOT production code. Do not reference it as a deliverable. Production is built from scratch by the full studio.
2. **Backend architecture is VeloxStudio IP** — do NOT share full backend specs with client. Only describe features and user-facing behavior.
3. **No phone/video calls** — email/chat only
4. **Content split into parts** is a NON-TRIVIAL requirement — the data model must support chapter parts that can be added progressively without breaking reading order.
5. **Season support** means the content hierarchy is: Story → Season → Chapter → Part (optional)
6. **Auto WebP conversion** requires image processing pipeline
7. **Drag-and-drop folder upload** requires modern browser APIs (File System Access API or recursive File API)
8. **Spatial comments** require coordinate mapping relative to image dimensions with responsive scaling
9. **RTL support** must flip navigation directions, sidebar position, and pin coordinates
10. **"No pre-approval" for comments** means real-time moderation (report/delete/ban) not queue-based approval
11. **PWA without offline** — app-like experience but no service worker caching of chapters
12. **Content protection** — disable right-click context menu, prevent drag-and-save of images
13. **300+ characters** requires efficient data structure and pagination

---

## EVERYTHING MEEM HAS EXPLICITLY SAID NO TO

- No overlay subtitles
- No pre-approval for comments
- No dyslexia font
- No WhatsApp notifications
- No offline reading or caching
- No right-click/download/save image
- No manual user approval queue (auto-approval after T&C)
- No light mode toggle in reader
- No visible theater mode toggle button
- No merchandise store architecture (don't design around it)
- No native iOS/Android apps
- No phone/video call support
- No "Private" Reading Club
- No manga/comics terminology in UI
- No star ratings (removed from demos)
- No zipping for uploads (folder drag-and-drop only)

---

## EVERYTHING MEEM HAS EXPLICITLY SAID YES TO

- Yes to spatial pinned comments (like Dropbox)
- Yes to pinch-to-zoom on mobile (no buttons)
- Yes to zoom buttons on desktop (minimal, auto-hide)
- Yes to auto-preload next chapter
- Yes to fullscreen mode
- Yes to high contrast toggle
- Yes to full RTL support
- Yes to custom keyboard shortcuts
- Yes to drag-and-drop folder upload
- Yes to auto WebP conversion
- Yes to season support (StoryName/Season01/Ch01/)
- Yes to progressive chapter parts
- Yes to detailed audit log
- Yes to email notifications
- Yes to in-app notifications
- Yes to forum
- Yes to character profiles (separate section)
- Yes to world-building docs (separate section)
- Yes to moderator system
- Yes to reporting/delete/ban tools
- Yes to PWA (add to home screen, fullscreen)
- Yes to gold color scheme
- Yes to premium editorial aesthetic
- Yes to mobile-first
- Yes to three payment installments
- Yes to PayPal
- Yes to Stripe-ready architecture
- Yes to 300+ character support
- Yes to character "likes"
- Yes to random character strip on homepage
- Yes to stats feature
- Yes to cover grid homepage

---

## WHAT TO PRODUCE

Generate a formal **Production Scope Document** in Markdown with these sections:

1. **Project Overview** (2-3 paragraphs)
2. **Client Information**
3. **Deliverables** (Phase 1 and Phase 2, detailed bullet lists)
4. **Technical Requirements** (design system, architecture, performance, security)
5. **Content Model** (story/season/chapter/part hierarchy, upload workflow, asset requirements)
6. **Reader Specifications** (all reader behavior, navigation, zoom, theater mode, etc.)
7. **Community & Moderation** (comments, forum, roles, audit log)
8. **Notifications** (types, channels, tone)
9. **Infrastructure & Deployment** (domain, repo, hosting, DNS)
10. **Payment Terms** (schedule, method, total)
11. **Warranty & Maintenance** (30-day bug fix, optional maintenance tiers)
12. **Assumptions & Dependencies** (what we assume client will provide, what depends on third parties)
13. **Exclusions** (what is NOT included in scope)
14. **Sign-off** (client signature block, date)

The tone must be **professional, precise, and confident**. No hedging. No "we might." Use "will" and "shall." Every feature must trace back to a specific questionnaire answer or email feedback.

**DO NOT mention AI, automation, agents, or non-human labor.** The document must read as written by a human studio lead.

**DO NOT share backend architecture details** — only user-facing features and requirements.
