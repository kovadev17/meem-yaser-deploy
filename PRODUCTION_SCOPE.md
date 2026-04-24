# Production Scope Document
## Rūsuma Reading Platform for Restless Worlds™

**Document Version:** 1.0  
**Date:** 2026-04-24  
**Prepared by:** VeloxStudio  
**Client:** Meem Yaser Studio  
**Platform Name:** Rūsuma Reading Platform (branded as "Reading Club")  
**Target Domain:** restlessworlds.com/reading-club

---

## 1. Project Overview

This document defines the complete production scope for the Rūsuma Reading Platform, a premium web-based manga and comic reading experience for Restless Worlds™. The platform shall deliver an immersive, uncluttered reading environment where the story remains the sole focus, supported by a robust content management system, community features, and moderation tools.

The design philosophy is premium editorial: calm, minimal, and luxurious. Every screen shall feel intentional, with zero visual noise. The reader experience is sacred — no feature shall compete with the page for attention.

The platform shall be built in two phases, totaling $3,600, with delivery expected within approximately two weeks of project kickoff (1 week per phase, pending timely delivery of client assets and access).

---

## 2. Client Information

| Field | Details |
|---|---|
| **Client** | Meem Yaser Studio |
| **Contact** | Meem Yaser |
| **Email** | hello@meemyaserstudio.ae |
| **Location** | UAE |
| **Brand** | Restless Worlds™ |
| **Platform Name** | Rūsuma Reading Platform (branded as "Reading Club") |
| **Target Domain** | restlessworlds.com/reading-club |
| **Primary Role** | Creator — writes and draws manga |
| **Moderation** | Will appoint dedicated moderator(s); will not moderate personally |

---

## 3. Deliverables

### Phase 1 — Core Reading Experience ($2,000)

**Timeline:** 1 week from kickoff (core development: ~3 business days; remainder reserved for client asset delivery, feedback, and acceptance)

**Work begins:** Within 2 business days of Payment 1 receipt and signed agreement return

1. **Landing & Library**
   - Light-mode landing page (#FAFAF8) with premium editorial aesthetic
   - Cover grid homepage presenting all series visually (not "trending" — story-focused)
   - Random character strip on homepage for dynamic, fresh feel
   - Stats feature visible to users (community engagement metrics)
   - Story detail pages displaying: cover art, title, synopsis, tags, chapter list
   - Chapter list: simple numbered list with chapter titles only
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
   - Spatial comments: users click/tap page coordinates → drop numbered pin → threaded sidebar discussion
   - Pins scale responsively with image dimensions
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
   - Support for 300+ characters across stories with organized data structure
   - "Like" feature on character bios for popularity tracking
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
- **Accent:** Gold (#D4AF37 / #C9A227)
- **Typography:** Premium serif display font + clean geometric sans-serif body
- **Aesthetic:** Apple + Notion + Webtoon + Discord — premium, minimal, zero clutter
- **Mobile-first:** All design decisions prioritize mobile experience

### Architecture
- Web-based responsive SPA; no native apps
- Modern browser APIs for folder drag-and-drop upload
- Image processing pipeline for WebP conversion
- Responsive coordinate mapping for spatial comments
- RTL-aware component system (flipped navigation, mirrored layouts, Arabic typography)

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
| Mode | Dark only | Q18 Round 2 |
| Background | Blurred current page | Q15 Round 1 |
| Loading | Draft (low-res → sharp) | Q10 Round 1 |
| Preload | Auto next chapter | Q6 Round 1 |
| Spreads | Pan/zoom intact | Q7 Round 1 |
| Subtitles | None; separate language versions | Q1 Round 2 |
| Zoom Mobile | Pinch only, no buttons | Q2 Round 2 |
| Zoom Desktop | Minimal buttons, auto-hide | Q2 Round 2 |
| Zoom Behavior | Never blocks swipe | Q2 Round 2 |
| Transitions | Natural | Q9 Round 1 |
| Keyboard | Right arrow = next | Q12 Round 1 |
| Swipe | Left = next (LTR), Right = next (RTL) — adapts to reading direction | Q13 Round 1 + RTL support |
| Chapter List | Sidebar + floating | Q16-Q17 Round 1 |
| End of Chapter | Explicit Next button | Q5 Round 1 |
| Theater Mode | Tap to toggle chrome | Q17 Round 2 |
| Fullscreen | Simple toggle | Q14 Round 1 |
| High Contrast | Manual toggle | Q24 Round 1 |
| Dyslexia Font | Not included | Q25 Round 1 |
| RTL | Full support | Q26 Round 1 |

---

## 7. Community & Moderation

### Comments
- Spatial pinned comments on page coordinates
- Visible immediately upon posting — no pre-approval queue
- Users can report comments
- Moderators can delete comments
- Threaded replies in sidebar

### Forum
- Separate space from page comments
- Thread list with visual hierarchy
- Same moderation tooling as comments

### Moderator Permissions
- Delete posts and comments
- Hide/flag content
- Issue temporary restrictions
- **Permanent bans require owner sign-off**
- Pin/unpin threads
- Handle routine moderation independently (deleting reported content, temporary restrictions)

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

- **Method:** PayPal invoice
- **Schedule chosen:** Three payments (client preference)
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

---

## 14. Sign-Off

This document, once signed, becomes the binding scope of work for the Rūsuma Reading Platform. Any changes require a written change order approved by both parties.

**Client:**

Name: _________________________

Signature: _________________________

Date: _________________________

---

**VeloxStudio:**

Name: Kova

Signature: _________________________

Date: _________________________

---

*This scope document is confidential and proprietary to VeloxStudio and Meem Yaser Studio.*
