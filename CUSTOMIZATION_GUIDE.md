# Happy Girlfriend's Day Website - Customization Guide

This romantic website is fully customizable! Here's where to edit all the content to make it uniquely yours.

## Quick Start

1. **Relationship Start Date** - Edit the date in `components/ui/RelationshipTimer.tsx`
   - Find: `const RELATIONSHIP_START = new Date('2022-01-15')`
   - Change to your actual relationship start date

2. **Love Letter** - Edit your message in `components/sections/LoveLetter.tsx`
   - Find the `LOVE_LETTER` constant and replace with your own heartfelt message

3. **Reasons I Love You** - Edit in `components/sections/ReasonsILoveYou.tsx`
   - Replace the `REASONS` array with reasons meaningful to your relationship

4. **Timeline Milestones** - Edit in `components/sections/Timeline.tsx`
   - Update dates, titles, descriptions, and icons for your special moments

## Media Assets

### Gallery Images
- **Location**: `public/assets/gallery/`
- **Current**: Using placeholder images
- **To Replace**: 
  1. Add your images to `public/assets/gallery/`
  2. Update the `GALLERY_IMAGES` array in `components/sections/PhotoGallery.tsx`
  3. Format: `{ id: number, src: 'path/to/image', alt: 'description' }`

### Videos
- **Location**: `public/assets/videos/`
- **Current**: Placeholder paths
- **To Add**:
  1. Add your MP4 videos to `public/assets/videos/`
  2. Update the `VIDEOS` array in `components/sections/VideoMemories.tsx`

### Polaroid Memories
- **Location**: Uses gallery images
- **To Customize**:
  1. Edit the `POLAROIDS` array in `components/sections/PolaroidMemories.tsx`
  2. Add your images and custom captions

## Customization Details

### Hero Section (`components/sections/HeroSection.tsx`)
- **Heading**: "Happy Girlfriend's Day ❤️"
- **Subheading**: "Every moment with you is my favorite memory."
- ✅ Automatically shows confetti on page load
- ✅ Contains relationship timer

### Photo Gallery (`components/sections/PhotoGallery.tsx`)
- Currently shows 6 placeholder images
- Hover to zoom and click to open fullscreen lightbox
- Edit the `GALLERY_IMAGES` array to add your photos

### Video Memories (`components/sections/VideoMemories.tsx`)
- Edit video titles and paths in the `VIDEOS` array
- Supports MP4 format
- Click to play with controls

### Timeline (`components/sections/Timeline.tsx`)
- Edit the `MILESTONES` array
- Add/remove milestones, change dates, titles, descriptions
- Each milestone can have an optional image

### Love Letter (`components/sections/LoveLetter.tsx`)
- Edit the `LOVE_LETTER` constant
- Use \n for line breaks
- Customize with your own romantic message

### Romantic Quotes (`components/sections/RomanticQuotes.tsx`)
- Edit the `QUOTES` array
- Auto-rotates every 4 seconds
- Click the dots to jump to specific quotes

### Reasons I Love You (`components/sections/ReasonsILoveYou.tsx`)
- Edit the `REASONS` array
- Cards flip on click/hover
- Currently 8 reasons (adjustable)

### Polaroid Memories (`components/sections/PolaroidMemories.tsx`)
- Edit the `POLAROIDS` array
- Customize rotation, captions, and images
- Hover to zoom

### Future Dreams (`components/sections/FutureDreams.tsx`)
- Edit the `DREAMS` array
- Change icons, titles, descriptions

## Styling Customization

### Colors
Edit the color palette in `app/globals.css`:
- **Primary**: `#e8b4c8` (Blush Pink)
- **Secondary**: `#d4a5a5` (Rose)
- **Accent**: `#f4d7dd` (Light Pink)
- **Background**: `#faf7f5` (Soft White)
- **Foreground**: `#3e3e42` (Dark Gray)

### Fonts
- **Heading Font**: Playfair Display (elegant serif)
- **Body Font**: Lora (modern serif)
- Set in `app/layout.tsx`

## Animation Settings

### Animations Available
- **Float**: Elements float up and down (`animate-float`)
- **Floating Hearts**: Follow cursor and rise (`animate-float-heart`)
- **Sparkle**: Twinkling effect (`animate-sparkle`)
- **Beat Heart**: Heartbeat animation (`animate-beat-heart`)
- **Pulse Glow**: Glowing pulse (`animate-pulse-glow`)

All animations are defined in `app/globals.css` under `@layer utilities`

## Advanced Customization

### Add More Sections
1. Create a new component in `components/sections/`
2. Add it to `app/page.tsx`
3. Follow the same pattern with `motion` from Framer Motion

### Change Audio
The design mentions optional background music. To add:
1. Add `<audio>` element to `HeroSection.tsx`
2. Place audio file in `public/assets/music/`

### Modify Animations
Edit keyframes in `app/globals.css`:
- `@keyframes float`
- `@keyframes floatHeart`
- `@keyframes sparkle`
- `@keyframes fallPetal`

## Mobile Responsiveness
- ✅ Fully responsive on mobile, tablet, and desktop
- Breakpoints: `md:` (768px) and above
- All components use responsive grid layouts

## Deployment

### Deploy to Vercel
1. Push to GitHub
2. Connect to Vercel
3. Deploy with one click
4. All environment variables are local only

## Tips & Tricks

1. **Test on Different Devices**: Use Chrome DevTools to test responsive design
2. **Optimize Images**: Use compressed, optimized images for faster loading
3. **Video Format**: MP4 works best for browser compatibility
4. **Preview Changes**: Use `pnpm dev` to see changes in real-time
5. **Smooth Scrolling**: All sections use scroll-triggered animations

## Troubleshooting

### Images not showing
- Check file paths in component arrays
- Ensure images are in `public/` directory
- Verify file extensions are correct

### Animations not working
- Check that Framer Motion is installed: `pnpm list framer-motion`
- Verify CSS animations are loaded in `app/globals.css`
- Clear cache: `rm -rf .next && pnpm dev`

### Videos not playing
- Use MP4 format for best compatibility
- Check file is in `public/assets/videos/`
- Test video plays in browser directly

## Support

For questions about:
- **Next.js**: [nextjs.org](https://nextjs.org)
- **Tailwind CSS**: [tailwindcss.com](https://tailwindcss.com)
- **Framer Motion**: [framer.com/motion](https://www.framer.com/motion/)
- **React**: [react.dev](https://react.dev)

Enjoy creating your special romantic website! 💕
