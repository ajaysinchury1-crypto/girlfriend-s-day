# Quick Edits - Find & Replace Guide

Copy these paths and find the exact lines to edit. Search in your code editor with Ctrl+F (Cmd+F on Mac).

## Most Important Edits (Do These First!)

### 1. Your Relationship Start Date
**File:** `components/ui/RelationshipTimer.tsx`
**Find:** `const RELATIONSHIP_START = new Date('2022-01-15')`
**Replace with:** Your actual date in YYYY-MM-DD format
**Example:** `const RELATIONSHIP_START = new Date('2020-06-15')`

### 2. Your Love Letter
**File:** `components/sections/LoveLetter.tsx`
**Find:** `const LOVE_LETTER = \`...`
**Replace with:** Your own heartfelt message (keep the backticks and use \n for new lines)

### 3. Reasons You Love Them
**File:** `components/sections/ReasonsILoveYou.tsx`
**Find:** `const REASONS = [`
**Replace each item:**
```typescript
'Your beautiful smile',
'Your incredible kindness',
'Your infectious laugh',
// ... replace with your own
```

## Gallery Images

### Add Your Photos
**File:** `components/sections/PhotoGallery.tsx`
**Find:** `const GALLERY_IMAGES = [`
**Instructions:**
1. Add your image files to `public/assets/gallery/`
2. Update the array with your image paths
3. Example:
```typescript
const GALLERY_IMAGES = [
  { id: 1, src: '/assets/gallery/photo1.jpg', alt: 'Our first date' },
  { id: 2, src: '/assets/gallery/photo2.jpg', alt: 'Beach vacation' },
  // ... add more
]
```

## Timeline Milestones

### Update Your Timeline
**File:** `components/sections/Timeline.tsx`
**Find:** `const MILESTONES = [`
**Edit each milestone:**
```typescript
{
  id: 1,
  date: 'YOUR_DATE',        // Change to actual date
  title: 'YOUR_TITLE',      // Change to your milestone
  description: 'YOUR TEXT', // Change your description
  icon: '❤️',              // Keep or change emoji
},
```

## Romantic Quotes

### Customize Quotes
**File:** `components/sections/RomanticQuotes.tsx`
**Find:** `const QUOTES = [`
**Example to replace:**
```typescript
const QUOTES = [
  'Your custom romantic quote here',
  'Another meaningful quote',
  // ... add more quotes
]
```

## Future Dreams

### Update Shared Dreams
**File:** `components/sections/FutureDreams.tsx`
**Find:** `const DREAMS = [`
**Edit each dream:**
```typescript
{
  icon: '🌍',              // Change emoji
  title: 'Your Dream',     // Change title
  description: 'Description of your shared dream',
},
```

## Videos

### Add Your Videos
**File:** `components/sections/VideoMemories.tsx`
**Find:** `const VIDEOS = [`
**Instructions:**
1. Add MP4 videos to `public/assets/videos/`
2. Update the array:
```typescript
const VIDEOS = [
  { id: 1, title: 'Our First Video', src: '/assets/videos/video1.mp4' },
  // ... add more
]
```

## Polaroid Memories

### Customize Polaroids
**File:** `components/sections/PolaroidMemories.tsx`
**Find:** `const POLAROIDS = [`
**Edit polaroid entries:**
```typescript
{
  id: 1,
  image: '/assets/gallery/photo.jpg',
  caption: 'Your caption here',
  rotation: -6,  // Rotation angle
},
```

## Colors & Design

### Change Color Palette
**File:** `app/globals.css`
**Find:** `:root {` section
**Change these colors:**
```css
--primary: #e8b4c8;      /* Blush Pink - change this */
--secondary: #d4a5a5;    /* Rose - change this */
--accent: #f4d7dd;       /* Light Pink - change this */
--background: #faf7f5;   /* Soft White - change this */
--foreground: #3e3e42;   /* Dark Gray - change this */
```

**How to use new colors:**
- Get hex color from: [colorcodes.io](https://www.colorcodes.io/)
- Replace the hex value
- Changes apply globally!

## Page Titles & Metadata

### Update Page Title
**File:** `app/layout.tsx`
**Find:** `title: 'Happy Girlfriend\'s Day ❤️'`
**Replace with:** Your own title

### Update Page Description
**File:** `app/layout.tsx`
**Find:** `description: 'A premium, interactive romantic website...'`
**Replace with:** Your own description

## Section Headings

### Hero Section Heading
**File:** `components/sections/HeroSection.tsx`
**Find:** `<h1>Happy Girlfriend&apos;s Day ❤️</h1>`
**Note:** This shows as "Happy Girlfriend's Day" on the page

### Hero Section Subheading
**File:** `components/sections/HeroSection.tsx`
**Find:** `<p>Every moment with you is my favorite memory.</p>`
**Change the text inside the tags**

## Quick Search Terms

Use these to quickly find what you need:

| What You Want | Search For |
|---|---|
| Edit relationship date | `RELATIONSHIP_START` |
| Edit love letter | `LOVE_LETTER` |
| Edit reasons | `REASONS_I_LOVE_YOU` or `REASONS = [` |
| Edit timeline | `MILESTONES = [` |
| Edit quotes | `QUOTES = [` |
| Edit dreams | `DREAMS = [` |
| Edit gallery | `GALLERY_IMAGES` |
| Edit videos | `VIDEOS = [` |
| Edit colors | `:root {` in globals.css |
| Edit fonts | `Playfair_Display` or `Lora` |
| Edit hero title | `Happy Girlfriend` |

## Common Replacements

### Date Format
Always use: `YYYY-MM-DD`
- ✅ Correct: `2022-06-15`
- ❌ Wrong: `06/15/2022`
- ❌ Wrong: `June 15, 2022`

### Emoji
- ❤️ Heart
- 💖 Sparkling Heart
- 💕 Two Hearts
- 💝 Heart with Ribbon
- 🌹 Rose
- 💐 Bouquet
- 🎀 Ribbon
- ✨ Sparkles
- 🌹 Flower
- 🎉 Party

### Colors
**Pink Palette:**
- `#e8b4c8` - Blush Pink (Primary)
- `#f4d7dd` - Light Pink (Accent)
- `#d4a5a5` - Rose (Secondary)

**Other Colors:**
- `#ffffff` - White
- `#faf7f5` - Off-white
- `#3e3e42` - Dark Gray

## Before You Deploy

✅ **Checklist:**
- [ ] Updated relationship date
- [ ] Changed love letter
- [ ] Added your reasons
- [ ] Updated timeline
- [ ] Changed color palette (if desired)
- [ ] Added your photos
- [ ] Updated quotes
- [ ] Tested on mobile
- [ ] No errors in console
- [ ] Ready to share!

## Common Issues When Editing

### Image doesn't show
- ❌ `src: 'assets/gallery/photo.jpg'` (missing leading /)
- ✅ `src: '/assets/gallery/photo.jpg'` (correct)

### Text looks wrong
- Make sure you're inside the quotes
- Don't delete the quotes themselves
- Don't accidentally delete commas

### Animation doesn't work
- Check all elements render correctly
- Try refreshing the page
- Clear browser cache

### Date doesn't update timer
- Use format: `YYYY-MM-DD`
- No quotes around numbers
- Correct: `new Date('2022-06-15')`

## Need Help?

- See `CUSTOMIZATION_GUIDE.md` for detailed instructions
- See `README.md` for full documentation
- Use Ctrl+F to search file contents
- Check console for error messages

## Testing Your Edits

```bash
# Start development server
pnpm dev

# Your changes appear instantly! (hot reload)
# Just save the file and refresh the browser if needed
```

## Most Edited Files (In Order)

1. `components/ui/RelationshipTimer.tsx` - Date
2. `components/sections/LoveLetter.tsx` - Love message
3. `components/sections/ReasonsILoveYou.tsx` - Reasons
4. `components/sections/Timeline.tsx` - Milestones
5. `components/sections/RomanticQuotes.tsx` - Quotes
6. `components/sections/PhotoGallery.tsx` - Images
7. `components/sections/FutureDreams.tsx` - Dreams
8. `components/sections/PolaroidMemories.tsx` - Polaroids
9. `app/globals.css` - Colors
10. `app/layout.tsx` - Title/metadata

---

**Pro Tip:** Use Find & Replace (Ctrl+H / Cmd+H) to make bulk changes across multiple strings at once!

Happy editing! 💕
