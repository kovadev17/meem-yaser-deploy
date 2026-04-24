# Production Scope Document
## Rūsuma Reading Platform for Restless Worlds™

**Document Version:** 2.0  
**Date:** 2026-04-24  
**Prepared by:** VeloxStudio  
**Client:** Meem Yaser Studio  
**Platform Name:** Rūsuma Reading Platform (branded as "Reading Club")  
**Target Domain:** restlessworlds.com/reading-club

---

## 1. Project Overview

This document defines the complete production scope for the Rūsuma Reading Platform, a premium web-based reading experience for Restless Worlds™. The platform shall deliver an immersive, uncluttered reading environment where the story remains the sole focus, supported by a robust content management system, community features, and moderation tools.

The design philosophy is **clean, minimal, and elegant — like Dropbox**. Every screen shall feel intentional, with zero visual noise. The reader experience is sacred — no feature shall compete with the page for attention. As Meem stated: *"I prefer a calm, uncluttered experience where the focus is always on the story."*

**Direction chosen:** Demo 5 (the horizontal locked-frame reader) was identified by Meem as *"the best reader so far"* — it fills the phone screen well and page swiping feels smooth. This direction forms the foundation of the production build.

The platform shall be built in two phases, totaling **$3,600**, with core development completing in approximately **3 business days per phase**. Total per-phase timeline is approximately 1 week, including client asset delivery, feedback, and acceptance.

---

## 2. Client Information

| Field | Details |
|---|---|
| **Client** | Meem Yaser Studio |
| **Contact** | Meem Yaser |
| **Email** | hello@meemyaserstudio.ae |
| **Invoice Email** | finance@meemyaserstudio.ae |
| **Location** | UAE |
| **Brand** | Restless Worlds™ (registered trademark) |
| **Content/Category Term** | Rūsuma (روسوما) |
| **Platform Name** | Rūsuma Reading Platform (branded as "Reading Club") |
| **Target Domain** | restlessworlds.com/reading-club |
| **Primary Role** | Creator — writes and draws original manga |
| **Moderation** | Will appoint dedicated moderator(s); will not moderate personally |

---

## 3. Deliverables

### Phase 1 — Core Reading Experience ($2,000)

**Timeline:** 1 week from kickoff (core development: ~3 business days; remainder reserved for client asset delivery, feedback, and acceptance)

**Work begins:** Immediately upon Payment 1 receipt and signed agreement return

1. **Landing & Library**
   - Light-mode landing page (#FAFAF8) with premium editorial aesthetic
   - Cover grid homepage presenting all series visually (story-focused, not "trending")
   - Random character strip on homepage for dynamic, fresh feel
   - Community stats section visible to users (engagement metrics)
   - Story detail pages displaying: cover art, title, synopsis, tags, chapter list
   - Chapter list: **Webtoon-style thumbnails** (small square character face or key panel thumbnails) with chapter title and release date — *not* simple text-only list
   - **No star ratings** anywhere on the platform (explicitly excluded per client request)
   - Membership prompt placed later in user flow (not upfront or intimidating)
   - PWA installable: add to home screen, fullscreen app-like experience (no offline storage)
   - Full bilingual support: English and Arabic with complete RTL layout
   - Mobile-first responsive design

2. **Horizontal Image Reader**
   - Dark-mode reader (#0A0A0A) — dark mode only, no toggle
   - Blurred page background for visual continuity
   - Natural page transition animations
   - Draft loading: low-res preview first, then sharpen to full quality
   - Auto-preload next chapter images for seamless reading
   - Double-page spread handling with horizontal pan/zoom, image kept intact
   - Fullscreen mode (simple toggle)
   - Theater mode: no visible toggle button; all UI hides/shows on screen tap (Dropbox-style)
   - Chapter list access via slide-out sidebar + floating/dockable button
   - End-of-chapter explicit "Next" button (no auto-advance)
   - High contrast mode toggle (manual)
   - Content protection: disable right-click context menu and prevent drag-and-save of chapter images
   - **No overlay subtitles** — each language has its own dedicated version of the pages, keeping artwork clean

3. **Navigation & Controls**
   - Right arrow key advances page
   - Swipe direction adapts to reading direction (LTR: left swipe = next; RTL: right swipe = next)
   - Custom keyboard shortcuts (user-configurable)
   - Mobile: pinch-to-zoom with no UI buttons
   - Desktop: zoom buttons (+ / − / reset) — minimal design, auto-hide
   - Zoom shall never interfere with page swiping
   - All interactive elements minimum 44px touch target

4. **Content Upload System**
   - Drag-and-drop folder upload — Dropbox-style, no zipping required
   - Folder name auto-detected as chapter name
   - Page auto-sort by filename using natural sort
   - Support for zero-padded filenames (001.jpg, 002.jpg)
   - Season support: StoryName/Season01/Ch01/ folder structure
   - PNG and JPEG input formats; automatic conversion to WebP on upload
   - Chapter part support: ability to append pages to an existing chapter progressively without breaking reading order

5. **Authentication & Roles**
   - Guest (locked content), Member (premium access), Admin (full access)
   - Login gate with role-based routing
   - Admin panel foundation

6. **Comment System Foundation**
   - Per-page comment threads in a clean side panel, accessible via icon next to the chapter list — no visible pins or overlays on the artwork
   - Comments visible immediately (no pre-approval)
   - Reporting mechanism

### Phase 2 — Community & Polish ($1,600)

**Timeline:** 1 week from Phase 1 acceptance + Payment 2 receipt (core development: ~3 business days; remainder reserved for client asset delivery, feedback, and acceptance)

1. **Forum**
   - Thread list with pin/hot badges
   - Thread detail with replies
   - Same moderation tooling as comments

2. **Character Profiles & World-Building**
   - Separate upload section (not mixed with chapters)
   - Character grid with detail slide-in panels
   - Support for **300+ characters** across stories with organized data structure
   - "Like" feature on character bios for popularity tracking and future merchandising decisions
   - World-building document hosting

3. **Notification System**
   - Rich in-app notifications
   - Email notifications: new chapter releases (required), announcements (optional, user-controlled)
   - No email notifications for replies or social interactions
   - No WhatsApp integration
   - Premium tone throughout
   - Per-user notification preferences (enable/disable each type)

4. **Moderation Tools**
   - Comment deletion by moderators
   - User banning (requires owner sign-off for permanent bans)
   - Content reporting by users
   - Detailed audit log: action, moderator name, timestamp, reason
   - Permission tier: moderators handle routine actions; escalations queue to owner

5. **Membership & Access Control**
   - Subscription gating architecture (Stripe-ready)
   - Free vs premium chapter badges
   - User role system (Guest / Member / Admin)
   - Automatic membership approval after Terms & Conditions acceptance — no manual approval queue

6. **Integration Points**
   - Social media account links
   - Existing website continuity
   - Domain DNS configuration guidance

---

## 4. Technical Requirements

### Design System
- **Landing:** Light warm off-white (#FAFAF8), editorial feel
- **Reader/Admin:** Always dark (#0A0A0A)
- **Accent:** Gold (#D4AF37 / #C9A227) — aligns with Restless Worlds™ brand colors (white, black, grey, gold)
- **Typography:** Premium serif display font + clean geometric sans-serif body
- **Aesthetic:** Apple + Notion + Webtoon + Discord — premium, minimal, zero clutter
- **Mobile-first:** All design decisions prioritize mobile experience

### Architecture
- Web-based responsive SPA; no native apps
- Modern browser APIs for folder drag-and-drop upload
- Image processing pipeline for WebP conversion
- RTL-aware component system (flipped navigation, mirrored layouts, Arabic typography)
- Comment system uses page_id binding with percentage-based anchors (resolution-independent)
- Reading state synced to backend every 10 seconds: page_id, zoom level, pan coordinates

### Performance
- Image lazy loading and preloading
- WebP delivery with fallback
- Optimized for irregular publishing (no fixed schedule)
- Offline reading: explicitly excluded; no chapter caching on device
- PWA installable (add to home screen, fullscreen app-like experience) without offline storage

### Security
- Role-based access control
- Moderator permission tiers
- Audit logging for all moderation actions
- Content protection: disable right-click context menu, prevent drag-and-save of chapter images
- Secure CDN delivery with signed URLs; no direct file access

---

## 5. Content Model

### Hierarchy
```
Story
├── Season (optional)
│   ├── Chapter
│   │   ├── Part 1 (e.g., first 20 pages)
│   │   ├── Part 2 (additional pages appended)
│   │   └── ... (progressive updates supported)
│   └── ...
├── Cover art
├── Title / Synopsis / Tags
├── Character profiles
└── World-building documents
```

### Upload Workflow
1. Creator drags folder onto upload zone
2. System parses folder path: StoryName/Season01/Ch01/
3. System reads page files (001.jpg, 002.jpg...) and sorts naturally
4. PNG/JPEG converted to WebP automatically
5. Chapter created; pages ordered by filename
6. Existing chapters can be updated with additional parts without reordering

### Asset Requirements Per Story
- Chapter page images (PNG/JPEG)
- Cover art
- Title, synopsis, tags metadata
- Logo (provided by client)
- All other brand elements designed by VeloxStudio

---

## 6. Reader Specifications

| Feature | Specification | Source |
|---|---|---|
| Mode | Dark only | Round 2 Q18 |
| Background | Blurred current page | Round 1 Q15 |
| Loading | Draft (low-res → sharp) | Round 1 Q10 |
| Preload | Auto next chapter | Round 1 Q6 |
| Spreads | Pan/zoom intact | Round 1 Q7 |
| Subtitles | None; separate language versions | Round 2 Q1 |
| Zoom Mobile | Pinch only, no buttons | Round 2 Q2 |
| Zoom Desktop | Minimal buttons, auto-hide | Round 2 Q2 |
| Zoom Behavior | Never blocks swipe | Round 2 Q2 |
| Transitions | Natural | Round 1 Q9 |
| Keyboard | Right arrow = next | Round 1 Q12 |
| Swipe | Adapts to reading direction (LTR: left = next; RTL: right = next) | Round 1 Q13 + RTL support |
| Chapter List | Sidebar + floating button | Round 1 Q16–Q17 |
| Chapter Thumbnails | Webtoon-style square thumbnails with title and date | Email feedback (Apr 21) |
| End of Chapter | Explicit Next button | Round 1 Q5 |
| Theater Mode | Tap to toggle chrome (no visible button) | Round 2 Q17 |
| Fullscreen | Simple toggle | Round 1 Q14 |
| High Contrast | Manual toggle | Round 1 Q24 |
| Dyslexia Font | Not included | Round 1 Q25 |
| RTL | Full support | Round 1 Q26 |
| Star Ratings | Excluded globally | Email feedback (Apr 21) |
| Content Protection | No right-click, no drag-save | Email feedback (Apr 22) |

---

## 7. Community & Moderation

### Comments
- Per-page comment threads in a clean side panel — no pins or overlays on artwork
- Visible immediately upon posting — no pre-approval queue
- Users can report comments
- Moderators can delete comments
- Threaded replies in sidebar
- Moderation tools: reporting, delete, ban users when needed

### Forum
- Separate space from page comments
- Thread list with visual hierarchy
- Same moderation tooling as comments
- Accessible only after sign-up

### Moderator Permissions
- Delete posts and comments
- Hide/flag content
- Issue temporary restrictions
- **Permanent bans require owner sign-off**
- Pin/unpin threads
- Handle routine moderation independently (deleting reported content, temporary restrictions)
- **Meem Yaser will not moderate personally; dedicated moderator(s) will be appointed**

### Audit Log (Owner-Visible)
- Action type (delete, ban, pin, approve, etc.)
- Moderator name
- Timestamp
- Reason/note field

---

## 8. Notifications

| Channel | Types | Tone | Control |
|---|---|---|---|
| In-app | All events | Premium | Per-type toggle |
| Email | New chapters (required), announcements (optional) | Premium | User enables/disables each |
| WhatsApp | None | — | — |
| Reply emails | None | — | Explicitly excluded |

---

## 9. Infrastructure & Deployment

| Component | Detail |
|---|---|
| **Domain** | restlessworlds.com (client owns; VeloxStudio provides DNS guidance) |
| **Repository** | Client creates GitHub repo, invites VeloxStudio as collaborator |
| **Frontend Hosting** | CDN/GitHub Pages (static deployment) |
| **Backend** | Serverless/cloud (VeloxStudio IP — architecture not disclosed) |
| **Payment** | Stripe-ready architecture; client sets up Stripe account when launching subscriptions |
| **Integrations** | Existing websites and social media accounts |
| **Sample Content** | Client provides sample chapter after scope signature (IP protection) |

---

## 10. Payment Terms

| Milestone | Amount | Timing |
|---|---|---|
| Project kickoff | $1,500 | Before work begins |
| Phase 1 delivery | $1,050 | Upon Phase 1 acceptance |
| Phase 2 delivery | $1,050 | Upon final acceptance |
| **Total** | **$3,600** | |

- **Method:** PayPal invoice sent to finance@meemyaserstudio.ae
- **Schedule chosen:** Three payments (client preference, Round 2 Q23)
- **Standard rate:** $5,000–6,000; current rate is discounted relationship pricing

---

## 11. Warranty & Maintenance

### Bug-Fix Warranty
- 30 days free bug fixes after each phase delivery
- Covers defects in delivered functionality only
- Does not cover new features, scope changes, or third-party service changes

### Optional Maintenance (Post-Warranty)
| Tier | Price | Includes |
|---|---|---|
| Basic | $80/month | Hosting, security patches, critical fixes |
| Proactive | $150/month | + Performance monitoring, content updates, feature tweaks |

- Month-to-month, cancellable anytime

---

## 12. Assumptions & Dependencies

1. Client will provide logo file and brand color preferences if specific
2. Client will create GitHub repository and send invitation within 48 hours of kickoff
3. Client will provide DNS access or coordination for domain setup
4. Client will provide sample chapter folder structure after contract signature
5. Client will appoint moderator(s) before or during Phase 2
6. Stripe account setup is client responsibility; platform will be Stripe-ready
7. Content (images, covers, metadata) upload is client responsibility
8. All third-party services (domain registrar, GitHub, PayPal) remain available

**Timeline Impact:** Each phase's core development requires approximately 3 business days. The stated 1-week timeline per phase assumes client dependencies (assets, access, feedback) are delivered within 48 hours of request. If client deliverables are delayed beyond 3 business days, the timeline extends by the delay duration plus 2 business days.

---

## 13. Exclusions (Not In Scope)

The following are explicitly excluded from this scope:

- Native iOS or Android applications
- WhatsApp notifications or integrations
- Dyslexia-friendly font option
- Offline download/sync functionality (explicitly excluded per client requirement)
- PWA offline storage or chapter caching (app-like install is included, but no offline reading)
- AI-generated content or recommendation engines
- Merchandise store or e-commerce (architecture is not designed around it)
- Custom video/audio player
- Translation services or subtitle generation
- Overlay subtitles on pages
- Light mode toggle for reader
- Phone or video call support
- Star ratings or comparisons between stories
- Coordinate pins or annotations overlaid on page artwork

---

## 14. Sign-Off

This document becomes binding once confirmed by both parties. Any changes require a written change order approved by both parties.

**To confirm your acceptance of this scope, reply to this email with:**

> *"I agree to the scope and terms above."*

Your reply serves as digital acknowledgment. No physical signature required.

---

**Confirmed by VeloxStudio:**

Kova — VeloxStudio

Date: 2026-04-24
