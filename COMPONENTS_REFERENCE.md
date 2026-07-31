# Components Reference Guide

Complete list of all components and their purposes.

## 🎨 Section Components

### `components/sections/HeroSection.tsx`
**Purpose:** Main landing page with title, confetti, and relationship timer
**Key Props:** None (self-contained)
**Customization:** 
- Hero title: "Happy Girlfriend's Day ❤️"
- Subheading: "Every moment with you is my favorite memory."
- Confetti animation triggers on load
- Confetti duration: 3 seconds

**What to Edit:**
- `<h1>` tag - Main heading
- `<p>` - Subheading
- Confetti timing

---

### `components/sections/PhotoGallery.tsx`
**Purpose:** Masonry gallery with lightbox functionality
**Key Features:**
- 6-image masonry layout
- Hover zoom animation
- Click to open fullscreen lightbox
- Responsive grid

**Customization:**
- Edit `GALLERY_IMAGES` array with your photos
- Format: `{ id, src, alt }`
- Add/remove images as needed
- Adjust grid columns in Tailwind classes

**Storage:** `public/assets/gallery/`

---

### `components/sections/VideoMemories.tsx`
**Purpose:** Video cards with elegant play buttons
**Key Features:**
- 3 video cards
- Play/pause controls
- Gradient overlay with title
- Responsive layout

**Customization:**
- Edit `VIDEOS` array
- Update video titles
- Change video paths
- MP4 format required

**Storage:** `public/assets/videos/`

---

### `components/sections/Timeline.tsx`
**Purpose:** Vertical timeline with milestone markers
**Key Features:**
- 6 milestones by default
- Custom icons/emojis
- Glassmorphic cards
- Alternating layout on desktop

**Customization:**
- Edit `MILESTONES` array
- Update dates, titles, descriptions
- Change icons (emojis)
- Add/remove milestones
- Optional images per milestone

**Events Included:**
- The Day We Met
- First Date
- First Trip
- Birthday Together
- Future Adventures
- Forever Together

---

### `components/sections/LoveLetter.tsx`
**Purpose:** Beautiful love letter display
**Key Features:**
- Glassmorphic card design
- Decorative heart emojis
- Animated entrance
- Heartfelt message display

**Customization:**
- Edit `LOVE_LETTER` constant
- Replace with your message
- Use \n for line breaks
- Keep the backticks
- 3-5 paragraphs recommended

---

### `components/sections/RomanticQuotes.tsx`
**Purpose:** Auto-rotating romantic quote carousel
**Key Features:**
- 10 quotes by default
- 4-second rotation interval
- Manual navigation dots
- Smooth transitions

**Customization:**
- Edit `QUOTES` array
- Add/remove quotes
- Adjust rotation timing (line ~30)
- Change quotes to personal ones

**Current Quotes:**
- "You are my today and all of my tomorrows."
- "When I am with you, I am home."
- And 8 more...

---

### `components/sections/ReasonsILoveYou.tsx`
**Purpose:** Interactive flip cards revealing reasons
**Key Features:**
- 8 cards by default (2x4 grid on desktop)
- Click/hover to flip
- Animated reveal
- Front shows prompt, back shows reason

**Customization:**
- Edit `REASONS` array
- Front text: "Click to reveal"
- Back text: Your reasons
- Can adjust number of reasons
- Grid auto-adjusts

**Current Reasons:**
- Your beautiful smile
- Your incredible kindness
- Your infectious laugh
- And 5 more...

---

### `components/sections/PolaroidMemories.tsx`
**Purpose:** Scattered polaroid-style memory display
**Key Features:**
- Randomly rotated images
- Handwritten-style captions
- Hover zoom effect
- Absolute positioning for scattered look

**Customization:**
- Edit `POLAROIDS` array
- Update image paths
- Change captions
- Adjust rotation angles (rotation: -6 to 6 recommended)
- Add/remove polaroids

**Array Format:**
```typescript
{
  id: 1,
  image: 'path/to/image.jpg',
  caption: 'Your caption',
  rotation: -6,  // degrees
}
```

---

### `components/sections/FutureDreams.tsx`
**Purpose:** Display shared future goals and dreams
**Key Features:**
- 6 dream cards
- Icon + title + description
- Glassmorphic design
- Hover effects

**Customization:**
- Edit `DREAMS` array
- Change icons (emojis)
- Update titles and descriptions
- Add/remove dreams
- Adjust layout (currently 3 columns)

**Current Dreams:**
- Travel together
- Build our home
- Have pets
- Get married
- Build dreams
- Grow old together

---

### `components/sections/FinalMessage.tsx`
**Purpose:** Cinematic closing message
**Key Features:**
- Large centered text
- Animated hearts
- Beats and floats
- Gradient backgrounds

**Customization:**
- Edit main message text
- Change "Happy Girlfriend's Day ❤️" closing
- Adjust animation timings
- Change emoji count/style

**Current Message:**
"I loved you yesterday. I love you today. I'll love you forever."

---

## ✨ Animation Components

### `components/animations/FloatingElements.tsx`
**Purpose:** Cursor-following hearts and sparkles
**Key Features:**
- Hearts follow cursor
- Continuous sparkle background
- Auto-cleanup after animation
- Configurable sizes

**Behavior:**
- Creates heart when you move mouse (1% chance)
- Hearts float upward and fade
- Sparkles appear randomly
- Both fade after duration

**Customization:**
- Adjust spawn probability (line ~20: 0.98)
- Change heart size range (line ~22-23)
- Modify animation duration
- Change colors (use CSS classes)

---

### `components/animations/ScrollProgress.tsx`
**Purpose:** Top progress bar following scroll
**Key Features:**
- Thin gradient bar at top
- Updates on scroll
- Smooth transitions
- Z-index: 50 (always visible)

**Customization:**
- Change gradient colors
- Adjust bar height (h-1)
- Modify transition timing

---

### `components/animations/BackToTop.tsx`
**Purpose:** Floating heart button to jump to top
**Key Features:**
- Only appears after scrolling 300px
- Heart icon
- Pulse glow animation
- Bottom-right position
- Smooth scroll to top

**Customization:**
- Change scroll trigger distance (line ~10: 300)
- Change position (bottom-8 right-8)
- Adjust icon size
- Change colors

---

### `components/animations/LoadingScreen.tsx`
**Purpose:** Initial loading screen with beating heart
**Key Features:**
- 2-second display duration
- Beating heart animation
- Centered layout
- Fades on page load

**Customization:**
- Change display duration (line ~9: 2000ms)
- Modify text
- Change heart size
- Adjust animations

---

## 🎯 UI Components

### `components/ui/RelationshipTimer.tsx`
**Purpose:** Live counting timer showing relationship duration
**Key Features:**
- Updates every second
- Shows years, months, days, hours, minutes, seconds
- Glassmorphic cards for each unit
- Real-time calculation

**Critical Edit:**
```typescript
// Line ~10 - MUST CHANGE THIS!
const RELATIONSHIP_START = new Date('2022-01-15')
```

**Customization:**
- Change date format (YYYY-MM-DD)
- Adjust display text
- Modify styling
- Change card appearance

---

## 🏗️ Component Structure

### File Organization
```
components/
├── animations/          # Page-wide effects
│   ├── FloatingElements.tsx
│   ├── ScrollProgress.tsx
│   ├── BackToTop.tsx
│   └── LoadingScreen.tsx
│
├── sections/           # Main content sections
│   ├── HeroSection.tsx
│   ├── PhotoGallery.tsx
│   ├── VideoMemories.tsx
│   ├── Timeline.tsx
│   ├── LoveLetter.tsx
│   ├── RomanticQuotes.tsx
│   ├── ReasonsILoveYou.tsx
│   ├── PolaroidMemories.tsx
│   ├── FutureDreams.tsx
│   └── FinalMessage.tsx
│
└── ui/                 # Reusable UI components
    └── RelationshipTimer.tsx
```

---

## 🔄 Data Flow

### How Components Get Data

1. **Direct Constants** (Most sections)
   - Data defined in component file
   - Arrays like `GALLERY_IMAGES`, `REASONS`, etc.
   - Easy to customize in place

2. **Passed Props** (Some components)
   - Receive data from parent
   - Allows reusability
   - Currently unused in this project

3. **Time-Based** (LoadingScreen, RelationshipTimer)
   - Calculate on render
   - Update via hooks
   - Real-time data

---

## 🎨 Animation Patterns

### Used Throughout Project

```typescript
// Fade in on scroll
initial={{ opacity: 0, y: 20 }}
whileInView={{ opacity: 1, y: 0 }}
transition={{ duration: 0.6 }}

// Hover effects
whileHover={{ scale: 1.05, y: -4 }}

// Continuous animation
animate={{ scale: [1, 1.1, 1] }}
transition={{ repeat: Infinity, duration: 1.5 }}
```

---

## 📱 Responsive Classes

All components use Tailwind responsive prefixes:
- `md:` - Tablet and up (768px+)
- `lg:` - Desktop and up (1024px+)
- Default - Mobile first

Example:
```tsx
<div className="grid grid-cols-1 md:grid-cols-3 gap-4">
```

---

## 🎬 CSS Animations

### In `app/globals.css`

- `@keyframes float` - Gentle floating motion
- `@keyframes floatHeart` - Rising and fading
- `@keyframes sparkle` - Twinkling effect
- `@keyframes beatHeart` - Heart pulse
- `@keyframes fadeInUp` - Fade in with lift
- `@keyframes pulse-glow` - Glowing pulse

All use GPU-accelerated transforms.

---

## 🔗 Dependencies

Each component needs:
- `'use client'` - Client-side rendering
- `import { motion } from 'framer-motion'` - Animations
- `import Image from 'next/image'` - Image optimization
- `import { ... } from 'lucide-react'` - Icons

---

## 💡 Best Practices

1. **Edit component data** in the constant arrays
2. **Don't change props** structure without knowing effects
3. **Keep HTML structure** intact
4. **Update content only**, not styling
5. **Test changes** with `pnpm dev`

---

## 🆘 Component-Specific Help

### If PhotoGallery images don't show:
- Check path starts with `/assets/`
- Ensure images in `public/assets/gallery/`
- Verify array is updated

### If timeline dates look wrong:
- Use `MMM DD, YYYY` format
- All dates must be strings
- Check quotes

### If flip cards don't work:
- Ensure CSS transform: preserve-3d
- Check `backfaceVisibility`
- Verify transform origin

### If animations are jerky:
- Check browser performance
- Disable other extensions
- Clear cache

---

## 📊 Component Stats

| Component | Lines | Update Level | Complexity |
|-----------|-------|--------------|-----------|
| HeroSection | 99 | High | Medium |
| PhotoGallery | 97 | High | High |
| Timeline | 133 | High | High |
| ReasonsILoveYou | 95 | High | Medium |
| RomanticQuotes | 85 | Medium | Low |
| FloatingElements | 120 | Low | High |
| RelationshipTimer | 96 | High | Medium |

---

**For specific customization questions, refer to [CUSTOMIZATION_GUIDE.md](./CUSTOMIZATION_GUIDE.md)**

**For editing help, see [QUICK_EDITS.md](./QUICK_EDITS.md)**
