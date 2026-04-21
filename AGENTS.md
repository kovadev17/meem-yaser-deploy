# Meem Yaser Studio — Manga Platform Demo

## What This Is
A single-file HTML client demo for a manga reading platform. The client is Meem Yaser Studio (UAE-based manga studio). This demo is meant to close a development deal — it must feel like a real product.

## Architecture
- **Single HTML file** — all CSS and JS inline, no build step
- **Tailwind CSS** via CDN (`https://cdn.tailwindcss.com`)
- **Google Fonts** — Inter (EN), Cairo (AR), JetBrains Mono (monospace)
- **Font Awesome 6.4** via CDN for icons
- **No frameworks** — vanilla JS only, no React/Vue/Angular
- **No external images** — all visual elements are inline SVGs

## Design System
- Landing pages: light warm off-white `#FAFAF8` background
- Reader + Admin: always dark `#0A0A0A`
- Accent color: gold `#D4AF37`
- Cards: white `#FFFFFF` with subtle shadows
- NO WebGL, NO particle effects, NO custom cursors
- Feel: Apple + Notion + Webtoon + Discord — premium, clean, minimal

## Key Features
1. **Login Gate** — 3 roles: Guest (locked), Member (premium), Admin (full)
2. **Hub/Homepage** — Hero banner, Continue Reading, Trending, New Chapters, Characters, Forum
3. **Manga Detail** — Cover, tags, rating, chapter list with Free/Premium/Locked badges, character cards
4. **Horizontal Reader** — SVG manga pages, arrow/swipe navigation, fullscreen, idle auto-hide chrome
5. **Spatial Comments** — Dropbox-style pin system: click page → drop numbered pin → threaded comment sidebar
6. **Characters Page** — Grid + detail slide-in panel
7. **Forum** — Thread list with pins/hot badges, detail panel
8. **Admin Panel** — Stats, user approvals, upload zone, quick actions
9. **Bilingual** — EN/AR toggle with full RTL support (dir="rtl", Cairo font, flipped arrows/sidebar)
10. **PWA Toast** — Install prompt after 3s on hub

## State Management
Global `state` object holds: lang, role, view, mangaId, readerPage, sidebarOpen, draftPin, activePinId, isPinching, idleTimer, pwaShown.

## View Routing
Sections with class `view` — `navigate(viewId)` hides all, shows target with fade animation. `renderDynamic()` re-renders content based on current view.

## Mock Data
`db` object contains: manga (4 titles), chars (6), threads (5), pins (6 across 5 pages), approvals (3).

## RTL Behavior
- `html[dir="rtl"]` switches when lang changes
- `.rtl-flip` class mirrors icons
- Pin positions mirror: `100 - x` in Arabic
- Reader swipe direction flips
- Sidebar slides from left in Arabic

## Mobile Considerations
- `touch-none` on reader container to prevent scroll
- Pinch-zoom detection (`isPinching` flag) disables swipe during zoom
- `min-w-[44px] min-h-[44px]` on all interactive elements
- Hamburger nav for mobile
- Sidebar becomes full-width overlay on small screens
- `100dvh` for proper mobile viewport height

## Critical Rules
- DO NOT add external image URLs (everything must be SVG or CSS)
- DO NOT break RTL — test both EN and AR
- DO NOT break pinch-zoom detection in reader
- DO NOT add WebGL/Three.js/GSAP
- DO NOT change the color system (keep light landing, dark reader)
- DO NOT remove the spatial comment system — it's the #1 selling feature
- All interactive elements must be at least 44px touch target
- Page transitions must stay smooth (0.7s fade)
